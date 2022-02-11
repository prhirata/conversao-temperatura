# Construção Dockerfile

1) Criei o arquivo `.dockerignore` e inclui a pasta `node_modules`.

2) Verifiquei qual versão do node a aplicação usa para descobrir qual imagem do node usar. Para isso rodei o comando `npm version`.

3) Criei o diretório da aplicação e setei como diretório corrente.

4) Copiei os arquivos package.json e package-lock.json para o diretório criado no passo 2.

5) Rodei o comando `npm install` para baixar as dependências.

6) Copiei os arquivos da pasta `src/` para a pasta da imagem criada no passo 2.

7) Expus a porta 8080 para acessar a aplicação.

8) Executei CMD para executar a aplicação.

# Teste Dockerfile

1) Para validar o Dockerfile, execute o comando abaixo de dentro da pasta onde está o arquivo Dockerfile (neste caso pasta `src/`) para construir a imagem:

`docker build -t paulohirata/conversao-temperatura:desafio .`

2) Execute o comando abaixo para criar o container a partir da imagem acima:

`docker container run -d -p 8080:8080 --name conversao-temperatura paulohirata/conversao-temperatura:desafio`

3) Abra o browser, e acesse o endereço `http://localhost:8080/`.
