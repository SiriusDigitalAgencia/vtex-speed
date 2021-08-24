# vtex-speed

atualização do vtex/speed adaptado para o nosso modo de trabalho e assim poder usar o git do projeto no mesmo ambiente do vtex-speed.
A vantagem de ter o vtex/speed junto do projeto implantado é de apenas baixar o git e sair rodando.

## Passos para instalação :

1 - Realizar o clone do nosso VTEX/Speed.
<br/><code>git clone https://github.com/SiriusDigitalAgencia/vtex-speed.git</code>

2 - entrar na pasta vtex-speed gerada pelo clone.

3 - apagar a pasta .git e o arquivo README.md e renomear o arquivo README-projeto.md para README.md.

4 - alterar o arquivo package.json na linha 3 ("accountName": "nome-da-conta") para indicar o accountname que estará trabalhando.

5 - Criar ambiente git zerado
<br/><code>git init .</code>

6 - Conectar o GIT local ao GIT Hub.
<br/><code>git remote add origin url-remota-repositorio-projeto</code>

7 - Atualize o repositorio local com os dados do repositório da loja. Mesmo que esteja vazio online.
<br/><code>git pull origin master --allow-unrelated-histories</code>

8 - Instalar os packages atualizados do VTEX Speed
<br/><code>npm install</code>

## Passos para executar o vtex-speed e acessar o site da loja em ambiente de desenvolvimento

1 - npm start ou yarn start

2 - Abra o navegador e acesse a url do site abaixo, alterando o {{acountname}} pelo nome da conta incluido no arquivo package.json
<br/>https://{{accountname}}.vtexlocal.com.br

3 - Autorize o navegador a acessar o ambiente seguro mesmo sem ser reconhecido.

4 - Faça login com a conta que possui no admin da loja

### Pronto. Todos os passos estão prontos para começar a trabalhar

## Passos para commit

<code>git add \*</code>
<br/><code>git commit -m "descrição do commit"</code>
<br/><code>git push origin master</code>

## Passos para baixar a última versão do repositório

git pull origin master
