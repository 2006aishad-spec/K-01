# K 01 — Aplicativo Escolar

Aplicação Android de apoio ao estudo e à organização escolar, preparada para o contexto do 11.º ano do Centro Escolar Attadamun, na Guiné-Bissau.

> **Estado do projeto:** o APK analisado está identificado como versão 1.0.0. A presença de ecrãs no pacote não significa que todas as funcionalidades tenham sido testadas ou certificadas. Consulte [a auditoria técnica](docs/AUDITORIA-TECNICA.md).

## Ecrãs identificados no APK

- Início
- Horário
- Notas
- Calendário
- Estudos
- Boletim

O pacote também contém referências a um fluxo de autenticação. O comportamento real destas funções precisa de ser validado num dispositivo Android.

## Informações da versão analisada

- Versão declarada: `1.0.0`
- Plataforma: Android
- Tecnologia identificada: React Native + Expo
- Motor JavaScript: Hermes
- Android mínimo declarado: API 24 (Android 7.0)
- Android de destino declarado: API 36
- Arquiteturas incluídas: ARM de 32 e 64 bits
- Tamanho do APK analisado: aproximadamente 65 MB

## Descarregar a aplicação

O objetivo é publicar os APKs na secção [Releases](../../releases), para que os utilizadores possam descarregar uma versão identificada. **O APK ainda não está anexado a uma release por esta integração.** Até à publicação, não há aqui um link direto de download da aplicação.

## Instalação Android

Quando o APK estiver publicado na secção Releases:

1. Abra a página [Releases](../../releases).
2. Escolha a versão desejada e descarregue o ficheiro APK.
3. Instale apenas se confiar na origem e compreender que a versão ainda precisa de validação.
4. O Android poderá pedir autorização para instalar aplicações obtidas fora da loja oficial.

## Funcionalidades a validar

- Persistência de horários, notas, eventos e apontamentos após fechar e reabrir a aplicação.
- Funcionamento sem Internet das funções que devem ser offline.
- Cálculos das médias, validação de notas e conteúdo do boletim.
- Autenticação e separação dos dados de cada utilizador.
- Necessidade de cada permissão Android e tratamento dos dados enviados a serviços externos.
- Compatibilidade, desempenho e tamanho da instalação.

## Privacidade e segurança

A análise estática do APK encontrou configurações para comunicação com serviços externos e várias permissões Android. Isso não demonstra, por si só, uso indevido. Consulte [docs/AUDITORIA-TECNICA.md](docs/AUDITORIA-TECNICA.md).

**Não coloque neste repositório** palavras-passe, tokens, chaves de API, dados reais de alunos, notas pessoais ou boletins identificáveis.

## Código-fonte e sincronização

Este repositório deve conter o código-fonte completo e as instruções de compilação quando forem disponibilizados. O APK compilado, por si só, não substitui o projeto-fonte original.

Neste momento, este README documenta a versão analisada; não afirma que o código-fonte completo já foi recuperado nem que a publicação automática de novas versões esteja configurada. As alterações feitas no GitHub através desta integração não sincronizam automaticamente uma pasta local ou o projeto original no construtor da aplicação.

## Relatar um problema

Ao reportar um erro, indique:
- modelo do dispositivo e versão Android;
- versão do K 01;
- passos para reproduzir o problema;
- resultado esperado e resultado observado.

Não anexe dados pessoais, notas reais ou capturas de ecrã com informação privada de alunos.
