# API de Pet Shop

Esse é o repositório com a base de JSON-Server + JSON-Server-Auth já configurada, feita para ser usada no desenvolvimento das API's nos Capstones do Q2.

## Endpoints

Assim como a documentação do JSON-Server-Auth traz (https://www.npmjs.com/package/json-server-auth), existem 3 endpoints que podem ser utilizados para cadastro e 2 endpoints que podem ser usados para login.

### Cadastro de novo usuário

POST /register <br/>
POST /signup <br/>
POST /users

Qualquer um desses 3 endpoints irá cadastrar o usuário na lista de "Users", sendo que os campos obrigatórios são os de email e password.
Você pode ficar a vontade para adicionar qualquer outra propriedade no corpo do cadastro dos usuários.

### Login de usuário

POST /login <br/>
POST /signin

Qualquer um desses 2 endpoints pode ser usado para realizar login com um dos usuários cadastrados na lista de "Users"

## Cadastrando novo pet

### Endpoint:

POST /animals <br/>

### Corpo da requisição:

<br/>
{ <br/>
"userId": (id do usuário que esta cadastrando o animal),<br/>
"name": "Nome do animal",<br/>
"animalType": "Espécie do Animal",<br/>
"cor": "Cor do animal",<br/>
"raça": "Raça do animal",<br/>
"idade": "idade do animal"<br/>
}

## Adicionando novo atendimento

### Endpoint:

<br/>
POST /schedule 
<br/>

### Corpo da requisição:

<br/>
{ <br/>
"userId": (id do usuário que esta cadastrando novo atendimento),<br/>
"animalName": "Nome do animal",<br/>
"treatmentType": "Espécie do Animal",<br/>
"scheduleDate": "Cor do animal"<br/>
}

## Listando animais, atendimentos e usuários

### Endpoints:

<br/>
<p>GET /users/id</p>
<p>GET /animals/userId</p>
<p>GET /schedule/userId</p>

### Listar o usurario com atendimentos ou animais cadastrados:

<br/>
<p>GET /users/id?\_embed=animals</p>
<p>GET /users/id?\_embed=schedule</p>
