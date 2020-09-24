# API-NodeJS-Opens
Este repositório contém uma API em NodeJS para apresentação a empresa Opens.

<hr>

### 1. Após baixar o repositório é necessário rodar o comando abaixo para instalar os pacotes:
<pre> $ npm install</pre>

### 2. Para rodar a API utilize os comandos abaixo:
<pre> $ npm run dev --> Roda a API em modo desenvolvimento - $ nodemon bin/server.js</pre>
<pre> $ npm run start --> Roda a API em modo de produção - $ node bin/server.js</pre>

### 3. Logo abaixo estão as URL's das rotas da API:
<pre>
Lista todos os usuários, somente acessível com usuário pertencente a role admin.
Metódo: GET
URL: '/user'
</pre>

<pre>
Lista o usuário logado.
Metódo: GET
URL: '/user/sign'
</pre>

<pre>
Lista o usuário por id, somente acessível com usuário pertencente a role admin, em :id deve ser substituído pelo id do usuário.
Metódo: GET
URL: '/user/:id'
</pre>

<pre>
Insere um novo usuário, somente acessível com usuário pertencente a role admin.
Metódo: POST
URL: '/user'
<strong>Os parametros devem ser passados via body, segue abaixo o modelo json:</strong>
{
	"name":"nome_usuário",
	"login":"login_usuário",
	"email":"email_usuário@gmail.com",
	"password":"senha",
	"role":"função_admin_user"
}
</pre>

<pre>
Altera os dados do usuário logado.
Metódo: PUT
URL: '/user/sign'
Os parametros devem ser passados via body, segue abaixo o modelo json:
{
	"name":"carina vl",
	"email":"carina.vl@gmail.com",
	"password":"123456",
	"role":"user"
}
<strong>OBS.: Não é possível alterar o login já cadastrado.</strong>
</pre>

<pre>
Altera os dados do usuário informado na URL, somente acessível com usuário pertencente a role admin, em :id deve ser substituído pelo id do usuário.
Metódo: PUT
URL: '/user/:id'
Os parametros devem ser passados via body, segue abaixo o modelo json:
{
	"name":"carina vl",
	"email":"carina.vl@gmail.com",
	"password":"123456",
	"role":"user"
}
<strong>OBS.: Não é possível alterar o login já cadastrado.</strong>
</pre>

<pre>
Deleta o usuário informado na URL, somente acessível com usuário pertencente a role admin, em :id deve ser substituído pelo id do usuário.
Metódo: DELETE
URL: '/user/:id'
</pre>

