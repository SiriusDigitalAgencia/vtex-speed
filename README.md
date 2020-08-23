# vtex-speed
atualização do vtex/speed adaptado para o nosso modo de trabalho e assim poder usar o git do projeto no mesmo ambiente do vtex-speed.
O objetivo é armazenar no git uma versão do projeto usando o mesmo ambiente do vtex-speed, mas sem armazenar no projeto os arquivos do vtex-speed que não são necessários para o projeto. 

## Passos para instalação :
1 - baixar o git do vtex-speed em https://github.com/vtex/speed.git
<br/><code>git clone https://github.com/vtex/speed.git</code>

2 - entrar na pasta speed gerada pelo clone.

3 - apagar a pasta .git e os arquivos .gitignore, Gruntfile.coffee, README.md, package.json e limpar a pasta src

4 - Criar ambiente git zerado
<br/><code>git init .</code>

5 - Se for um projeto vazio no GitHub, executar os comandos abaixo. Se for um projeto existente, pular para o passo 6.
<br/>- executar o comando de remote para baixar o repositório da nossa versão vtex-speed 
<br/><code>git remote add origin https://github.com/ohmai-digital/vtex-speed.git</code>
<br />- executar o comando de baixar o conteúdo do repositório.
<br/><code>git pull origin master</code>
<br />- alterar o arquivo package.json na linha 3 ("accountName": "nome-da-conta") para indicar o accountname que estará trabalhando.
<br/>- remover o relacionamento com o repositório vtex-speed
<br/><code>git remote remove origin</code>
<br/>- Apagar o arquivo README.md

6 - Executar os comandos de remote para baixar a versão do projeto ativo que deseja trabalhar (repositório da lojavirtual).
<br/><code>git remote add origin url-remota-repositorio</code>

7 - Atualize o repositorio local com os dados do repositório da loja. Mesmo que esteja vazio online.
<br/><code>git pull origin master --allow-unrelated-histories</code>

8 - Instalar os packages atualizados do VTEX Speed
<br/><code>npm install</code>

9 - Renomear a pasta para o nome do projeto.
- volte um nível na pasta aberta e execute o comando abaixo.
<br/><code>rename speed nome-repositorio</code>

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

