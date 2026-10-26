# Como publicar o ZIP do código-fonte

## Estado atual

O arquivo de origem recebido foi validado e preparado numa versão limpa, sem a pasta de cache `.expo/`. O arquivo contém o projeto-fonte, mas **ainda não está anexado ao GitHub**. O conector disponível nesta sessão consegue criar e editar ficheiros de texto, mas não consegue transferir o arquivo binário local diretamente para uma Release.

## Publicar o ZIP a partir do telemóvel

1. Descarrega o arquivo `k01-codigo-fonte-limpo.zip` preparado nesta conversa.
2. Abre https://github.com/2006aishad-spec/K-01 no navegador e entra na tua conta.
3. Abre **Releases** e escolhe **Draft a new release** (ou **Create a new release**).
4. Usa uma etiqueta como `source-v1.0.0` e um título como **K 01 — Código-fonte 1.0.0**.
5. Na área de anexos da versão, seleciona o arquivo ZIP descarregado.
6. Antes de publicar, confirma que o ZIP é o código-fonte correto e que não contém palavras-passe, tokens, chaves privadas ou dados pessoais de alunos.
7. Publica a Release. Depois, verifica que o arquivo aparece como anexo descarregável.

## Importante

Anexar o ZIP a uma Release torna o código-fonte descarregável, mas **não extrai os ficheiros para as pastas do repositório** e não cria sincronização automática. Para ter cada ficheiro visível no GitHub e compilar o projeto a partir do repositório, é necessário extrair e enviar as pastas e os ficheiros usando Git ou um fluxo de importação local.

Não publiques APKs ou código que contenham segredos, nem dados reais de estudantes.
