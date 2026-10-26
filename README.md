# K 01 — Aplicativo Escolar

Aplicação Android de apoio ao estudo e à organização escolar, preparada para o contexto do 11.º ano do Centro Escolar Attadamun, na Guiné-Bissau.

> **Estado do projeto:** o APK analisado está identificado como versão 1.0.0. Foi também recebido um ZIP com o projeto-fonte. A estrutura desse ZIP foi inspecionada e está documentada em [docs/ESTRUTURA-CODIGO-FONTE.md](docs/ESTRUTURA-CODIGO-FONTE.md), mas os ficheiros do ZIP ainda não foram todos transferidos para o repositório. Consulte também a [auditoria técnica](docs/AUDITORIA-TECNICA.md).

## Ecrãs identificados

- Início
- Horário
- Notas
- Calendário
- Estudos
- Boletim

O projeto-fonte recebido contém referências a estes ecrãs, configurações Expo/React Native, componentes, armazenamento, servidor, esquema de base de dados e testes. A presença dos ficheiros não significa que todas as funções tenham sido testadas.

## Informações técnicas declaradas

- Versão do APK analisado: `1.0.0`
- Plataforma: Android
- Tecnologia: React Native + Expo
- Motor JavaScript: Hermes
- Expo SDK declarado no projeto-fonte: 57
- Android mínimo declarado no APK: API 24
- Android de destino declarado no APK: API 36
- Tamanho aproximado do APK: 65 MB

## Descarregar a aplicação

O APK ainda não está anexado a uma [Release](../../releases). Não há, neste momento, um link direto de download do APK neste repositório.

## Código-fonte e sincronização

O arquivo `code.zip` recebido contém 108 entradas, incluindo código da aplicação e do servidor, configurações, migrações de base de dados e testes. O arquivo ZIP é válido.

**Atenção:** a inspeção do ZIP não significa que o seu conteúdo já tenha sido carregado integralmente para este repositório. A integração atual permite gerir ficheiros de texto, mas não forneceu uma operação direta para extrair e transferir automaticamente o ZIP completo como um conjunto de ficheiros. A sincronização automática com o construtor original e a compilação de novas versões também não estão configuradas.

## Validação pendente

- Testar a persistência de horários, notas, eventos e apontamentos.
- Confirmar as fórmulas das médias e os campos do boletim.
- Testar o funcionamento offline.
- Rever autenticação, permissões e comunicação com serviços externos.
- Instalar e compilar o projeto-fonte num ambiente apropriado.

## Privacidade e segurança

Não publiques palavras-passe, tokens, chaves de API, dados reais de alunos, notas pessoais ou boletins identificáveis. Consulta [SECURITY.md](SECURITY.md) e a [auditoria técnica](docs/AUDITORIA-TECNICA.md).

## Relatar um problema

Indica a versão da aplicação, o dispositivo, os passos para reproduzir e o resultado observado. Remove sempre dados pessoais das capturas de ecrã.
