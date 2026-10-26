# Publicar o APK para download no GitHub

O repositório é público, mas o APK de 65 MB ainda não foi anexado a uma Release. Os ficheiros de documentação não substituem o ficheiro instalável.

## Publicação manual

1. Abre [Releases](../../releases).
2. Seleciona **Draft a new release** (ou **Create a new release**).
3. Cria uma etiqueta de versão, por exemplo `v1.0.0`, apenas se corresponder ao APK que estás a publicar.
4. Título sugerido: `K 01 1.0.0 — APK Android`.
5. Escreve as limitações conhecidas e o que foi realmente testado.
6. Anexa o ficheiro `k-01--aplicativo-escolar-1.0.0.apk`.
7. Publica a Release e abre o link numa janela privada para confirmar que o download funciona sem iniciar sessão.

## Antes de publicar

- Confirma que tens autorização para distribuir a versão.
- Verifica a assinatura do APK e guarda a impressão digital do certificado.
- Testa a instalação num dispositivo Android de teste.
- Não publiques chaves privadas, ficheiros de configuração com segredos, bases de dados reais nem dados de alunos.
- Não afirmes que a aplicação é segura ou oficialmente aprovada sem testes correspondentes.
- Considera publicar uma soma SHA-256 para que os utilizadores possam verificar o ficheiro descarregado.

## Sincronização do projeto

Publicar um APK numa Release não sincroniza automaticamente o projeto-fonte com a ferramenta que o criou. Para sincronização contínua, o código-fonte completo deve estar num repositório Git e o ambiente de desenvolvimento deve estar ligado a este repositório. Depois disso, alterações devem ser commitadas e enviadas para o GitHub; a compilação automática exige uma pipeline configurada separadamente.
