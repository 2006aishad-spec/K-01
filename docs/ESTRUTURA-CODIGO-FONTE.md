# Estrutura do código-fonte recebido

Foi recebido um arquivo `code.zip` que contém um projeto de aplicação, e não apenas o APK compilado.

## Validação do arquivo

- Arquivo ZIP válido.
- 108 entradas no arquivo, incluindo ficheiros de projeto e cache.
- Aproximadamente 830 KB de conteúdo descomprimido.
- O arquivo contém `package.json`, `pnpm-lock.yaml`, configurações Expo/TypeScript, ecrãs, componentes, armazenamento, servidor, esquema de base de dados e testes.

## Estrutura identificada

### Aplicação
- `app/(tabs)/index.tsx` — início
- `app/(tabs)/schedule.tsx` — horário
- `app/(tabs)/grades.tsx` — notas
- `app/(tabs)/calendar.tsx` — calendário
- `app/(tabs)/study.tsx` — estudos
- `app/(tabs)/report.tsx` — boletim
- `app/settings.tsx` — definições
- `app/oauth/callback.tsx` — retorno de autenticação
- `app/dev/theme-lab.tsx` — laboratório de tema/desenvolvimento

### Componentes e lógica partilhada
- `components/`
- `constants/`
- `hooks/`
- `lib/k01-store.tsx`
- `lib/trpc.ts`
- `shared/`

### Servidor e base de dados
- `server/`
- `drizzle/schema.ts`
- `drizzle/0000_elite_eternals.sql`
- `drizzle/relations.ts`

### Testes e configuração
- `tests/auth.logout.test.ts`
- `tests/cors.test.ts`
- `app.config.ts`
- `package.json`
- `pnpm-lock.yaml`
- `tsconfig.json`
- configurações de Expo, Metro, Tailwind, ESLint e Babel

## Dependências e tecnologia declaradas

O `package.json` declara Expo SDK 57, React Native 0.86.3, React 19.2.3, Expo Router, AsyncStorage, tRPC, Drizzle ORM, MySQL e Vitest.

Estas versões são o que o manifesto declara; a instalação e compilação ainda não foram executadas nesta auditoria.

## Limpeza antes de integrar

O ZIP contém uma pasta `.expo/` com caches e ficheiros gerados. Esses conteúdos não devem ser tratados como código-fonte essencial e normalmente devem ser excluídos do Git.

Antes de publicar o código, rever ficheiros de ambiente, configurações de autenticação, URLs de serviços e qualquer segredo. Não publicar tokens, palavras-passe, chaves ou dados reais de alunos.

## Estado da integração

Este documento regista a inspeção do arquivo recebido. Não significa que todos os ficheiros do ZIP já tenham sido extraídos e enviados ao GitHub. A sincronização completa do código-fonte requer a transferência dos ficheiros de projeto para o repositório e validação posterior da compilação.
