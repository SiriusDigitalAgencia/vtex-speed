# vtex-speed
atualização do vtex/speed adaptado para o nosso modo de trabalho e assim poder usar o git do projeto no mesmo ambiente do vtex-speed.

## Passos para instalação :
1 - baixar o git do vtex-speed em https://github.com/vtex/speed.git
<br/><code>git clone https://github.com/vtex/speed.git</code>

2 - entrar na pasta speed gerada pelo clone.

3 - apagar a pasta .git e os arquivos .gitignore, Gruntfile.coffee, README.md, package.json

4 - Se for um novo projeto, executar os comandos do 4a. Se for um projeto existente, executar os comandos do 4b.

4a) 
<br/>- executar o comando de remote para baixar a nossa versão vtex-speed 
<br/><code>git remote add origin https://github.com/ohmaidigital/vtex-speed.git</code>

- alterar o arquivo package.json na linha 3 ("accountName": "nome-da-conta") para indicar o accountname que estará trabalhando.

4b) 
<br/>- executar o comando de remote para baixar a versão do projeto ativo
<br/><code>git init .</code>
<br/><code>git remote add origin url-remota-repositorio</code>

5 - executar o comando de baixar o conteúdo do repositório.
<br/><code>git pull origin master</code>

6 - Instalar os packages atualizados do VTEX Speed
<br/><code>npm install</code>

## Passos para executar o vtex-speed e acessar o site da loja em ambiente de desenvolvimento
1 - npm start

2 - Abra o navegador e acesse a url do site abaixo, alterando o {{acountname}} pelo nome da conta incluido no arquivo package.json
<br/>http://{{accountname}}.vtexlocal.com.br 

3 - Faça login com a conta que possui no admin da loja

### Pronto. Todos os passos estão prontos para começar a trabalhar.

## Passos para commit
<code>git add *</code>
<br/><code>git commit -m "descrição do commit"</code>
<br/><code>git push origin master</code>

## Passos para baixar a última versão do repositório
git pull origin master

