# Respostas das Perguntas de Reflexão

## 1. Por que a Secret aparece como ** ?

Porque o GitHub protege automaticamente valores sensíveis cadastrados como Secrets. Mesmo que o workflow tente imprimir o valor, o GitHub mascara o conteúdo nos logs para evitar vazamento de credenciais.

## 2. O Job deploy_app consegue acessar BUILD_VERSION?

Não.

A variável BUILD_VERSION foi criada dentro do escopo do job build_app. Como cada job roda em uma máquina virtual separada, variáveis locais de um job não são compartilhadas automaticamente com outros jobs.