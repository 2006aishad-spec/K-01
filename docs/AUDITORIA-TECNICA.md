# Auditoria técnica estática — K 01 1.0.0

## Âmbito

Esta nota documenta os resultados de uma análise estática do APK fornecido. Não substitui a revisão do código-fonte, testes de execução num dispositivo Android, análise de tráfego de rede ou uma auditoria de segurança profissional.

## Dados identificados

- Nome apresentado: K 01 — Aplicativo Escolar
- Versão declarada: 1.0.0
- Tecnologia identificada: React Native + Expo
- Motor JavaScript: Hermes
- SDK Expo declarado no pacote: 57
- Android mínimo declarado: API 24
- Android de destino declarado: API 36
- Arquiteturas: ARM de 32 e 64 bits
- Tamanho aproximado do APK: 65 MB
- Endereço de servidor encontrado na configuração: `k01app-5vjwix6b.manus.space`
- Também existem referências a serviços de autenticação Manus.

## Ecrãs referenciados

Foram encontradas referências a:
- Início (`index.tsx`)
- Horário (`schedule.tsx`)
- Notas (`grades.tsx`)
- Calendário (`calendar.tsx`)
- Estudos (`study.tsx`)
- Boletim (`report.tsx`)
- Retorno de autenticação (`oauth/callback.tsx`)
- Ferramenta de desenvolvimento/tema (`dev/theme-lab.tsx`)

Estas referências confirmam a presença de recursos correspondentes no pacote, não o funcionamento correto de cada ecrã.

## Permissões e áreas a rever

O manifesto contém permissões e componentes associados a rede, notificações, microfone/áudio, serviços de áudio/vídeo em segundo plano, biometria, armazenamento e sobreposições do sistema. Algumas podem ser acrescentadas por dependências. A presença no manifesto não prova que todas sejam usadas em execução.

Recomendações:
1. Justificar cada permissão e remover as desnecessárias.
2. Rever especialmente `SYSTEM_ALERT_WINDOW` (sobreposições).
3. Verificar regras de cópia de segurança Android, pois `allowBackup=true` foi identificado.
4. Confirmar que tokens e dados escolares não são incluídos em backups desprotegidos.
5. Testar a autenticação e garantir que cada utilizador só acede aos próprios dados.
6. Documentar quais dados são enviados ao servidor externo, a finalidade, retenção e processo de eliminação.
7. Não inserir dados reais de alunos em pedidos a serviços de IA sem uma base legal, consentimento adequado e medidas de proteção.

## Testes funcionais recomendados

### Notas
- Aceitar apenas notas entre 0 e 20, com decimais.
- Não converter campos em falta para zero.
- Calcular M.F = (C.O + T.P + T.I) / 3 apenas quando os três valores estão preenchidos.
- Calcular a média geral apenas com disciplinas que tenham M.F válida.
- Não inventar fórmulas oficiais para Média, M.A, P-G ou EXT / 2.ª ÉPO.

### Persistência e modo offline
- Criar e editar horários, notas, eventos e apontamentos.
- Fechar e reabrir a app e confirmar a persistência.
- Ativar modo de avião e testar todas as funções que deveriam funcionar offline.
- Testar exportação, recuperação e cópias de segurança, se existirem.

### Boletim
- Verificar dados do aluno, disciplinas, médias, paginação e impressão.
- Não tratar uma reprodução digital como documento oficialmente autenticado sem validação da escola.

### Segurança
- Testar controlo de acesso, gestão de sessões e logout.
- Verificar se dados de um aluno podem ser consultados por outra conta.
- Inspecionar tráfego de rede e armazenamento local em ambiente de teste.
- Não executar testes intrusivos contra serviços de terceiros sem autorização.

## Limitações desta análise

Não foi possível, nesta análise estática, confirmar:
- funcionamento de todos os ecrãs;
- exatidão real dos cálculos;
- armazenamento local versus remoto de cada categoria de dados;
- comportamento integral offline;
- conteúdo efetivo das comunicações de rede;
- segurança da autenticação;
- operação atual do servidor;
- assinatura e cadeia de confiança do APK;
- comportamento da aplicação em execução.

## Conclusão

O APK contém uma estrutura Android baseada em React Native/Expo e referências aos principais ecrãs escolares. Antes de utilização com dados reais, devem ser testadas as regras de notas, a persistência, a autenticação, o modo offline e as permissões. A análise não encontrou evidência suficiente para concluir que existe malware ou uso indevido de dados; também não certifica a segurança da aplicação.
