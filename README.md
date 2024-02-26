# Academy Pay (Backend)
<p align="center">
  <img alt="GitHub language count" src="https://img.shields.io/github/languages/count/Kauanedev/academy-pay-back?color=%2304D361">
  
  <a href="https://github.com/Kauanedev/din-din-project/commits/main">
    <img alt="GitHub last commit" src="https://img.shields.io/github/last-commit/Kauanedev/academy-pay-back">
  </a>
</p>

<p align="center">
  <img alt="Postgresql" src="https://img.shields.io/badge/PostgreSQL-316192?style=for-the-badge&logo=postgresql&logoColor=white">
    <img alt="Javascript" src="https://img.shields.io/badge/Javascript-0d1b2a?style=for-the-badge&logo=javascript">
    <img alt="ExpressJs" src="https://img.shields.io/badge/express-ffd000?style=for-the-badge&logo=express">
</p>
<h4 align="center"> 
💸 Academy Pay 💸
</h4>

<p align="center">
 <a href="#about">About</a> •
  <a href="#run">Run the project</a> •
  <a href="tecnologies">Tecnolgies<a/> •
 <a href="#endpoints">API Endpoints</a> •
 <a href="#colab">Collaborators</a> •
</p>

## 💻 About the project
<p id="about">
🤑Academy Pay is a solution designed to meet the financial management needs of commercial establishments. It provides a safe and efficient platform for registering customers and organizing the accounts associated with each of them. Owners find this tool an effective resource for transparent management and detailed monitoring of customer transactions.
</p>


<p id="run">
  
## 🏃‍♀️ Run the project
</p>

#### 🎲 Run Backend

```bash

 
# Clone this repository:
$ git clone git@github.com:Kauanedev/academy-pay-back.git


# Go to server folder
$ cd server

# Install dependencies
$ npm install

# Run the app in the development mode.
$ npm run dev

# Server will start on port:3000 - Open ~ http://localhost:3000 ~ to view it in your browser.

```


<p id="tecnologies">
  
  ## 🛠 Tecnologies 
</p>

#### **Website**  ([React](https://reactjs.org/))

-   **[Chakra UI](https://chakra-ui.com/)**
-   **[Axios](https://axios-http.com/ptbr/docs/intro)**
-   **[Framer Motion](https://www.framer.com/motion/)**
-   **[Crypto JS](https://github.com/brix/crypto-js)**
-   **[React Router Dom](https://reactrouter.com/en/main)**

#### **Server**  ([NodeJS](https://nodejs.org/en/))

-   **[Axios](https://axios-http.com/ptbr/docs/intro)**
-   **[Bcript](https://github.com/kelektiv/node.bcrypt.js#readme)**
-   **[CORS](https://expressjs.com/en/resources/middleware/cors.html)**
-   **[dotENV](https://github.com/motdotla/dotenv)**
-   **[Express](https://expressjs.com/)**
-   **[KnexJS](http://knexjs.org/)**
-   **[Joi](https://joi.dev/)**
-   **[JSON webToken](https://jwt.io/)**
-   **[Knex](https://knexjs.org/)**

#### **Utilities** 

-   Figma:  **[Figma](https://www.figma.com/)**  →  **[Protótipo](https://www.figma.com/file/EsX2ltIJ6gSGFzXXCU1pQH/M05-SPRINT-03?type=design&node-id=410-47347&mode=design&t=M4n4IHXTH8lNe2cO-0)**
-   API:  **[API](https://backend-devastados.vercel.app/)**
-   Source-Code Editor:  **[Visual Studio Code](https://code.visualstudio.com/)** 
-   Commit Conventional:  **[Commitlint](https://github.com/conventional-changelog/commitlint)**
-   API Client:  **[Insomnia](https://insomnia.rest/)**
-   Icons:  **[Chakra Ui Icons](https://chakra-ui.com/docs/components/icon)**
-   Fonts:  **[Nunito](https://fonts.google.com/specimen/Nunito)**,  **[Montserrat](https://fonts.google.com/specimen/Montserrat?query=montse)**
---

<p id="endpoints">
  
## 📍API Endpoints
</p>    

| route               | description                                          
|----------------------|-----------------------------------------------------
| <kbd>POST /registerUser</kbd>     | See [request details](#post-register-user)
| <kbd>POST /login</kbd>     |  See [request details](#post-login)
| <kbd></kbd>     | 
| <kbd>PUT /editUser/:idUser</kbd>     |See [request details](#put-edit-user)
| <kbd>GET /getUser/:idUser</kbd>     | Returns specific user
| <kbd>POST /registerClient/:idUser</kbd>     | See [request details](#post-register-client)
| <kbd>GET /listClients/:idUser</kbd>     | Returns Clients
| <kbd>GET /getClient/:idUser</kbd>     | Returns specific client
| <kbd>PUT /editClient/:idUser</kbd>     | See [request details](#put-edit-client)
| <kbd></kbd>     | 
| <kbd>POST /registerBilling/:idUser/:idClient</kbd>     | See [request details](#post-register-billing) 
| <kbd>PUT /editBilling/:idBill</kbd>     | See [request details](#put-edit-billing) 
| <kbd>GET /listBills/:idUser</kbd>     | Returns bills from specific user
| <kbd>GET /getBill/:idBill</kbd>     | Returns specific bill 
| <kbd>GET /listClientBills/:idUser/:idClient</kbd>     | Returns bills from specific client
| <kbd>DELETE /deleteBill/:idBill</kbd>     | Deletes specif bill
| <kbd></kbd>     | 
| <kbd>GET /homepage/:idUser</kbd>     | Returns all charges from clients of specific user 

<h3 id="post-register-user">POST /registerUser</h3>

**REQUEST**  
```json
{
  "name":"User Name",
  "email":"test@gmail.com",
  "password": "password"
}
```

<h3 id="post-register-user">POST /login</h3>

**REQUEST**  
```json
{
  "email":"teste02@gmail.com",
  "password": "senha"
}
```

**RESPONSE**
```json
{
	"user": {
		"id": 25,
		"name": "User Name",
		"cpf": null,
		"email": "test@gmail.com",
		"phone": null
	},
	"token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpZCI6MjUsImlhdCI6MTcwODk4MDA5MywiZXhwIjoxNzA5MDA4ODkzfQ.bD47unSSmt8XhtzpmCc9YykGRjB7MvMFh6g4Jvz0OLg"
}
```

<h3 id="put-edit-user">PUT /editUser/:idUser</h3>

**REQUEST**  
```json
{
  "name":"User Name",
  "email":"test@gmail.com",
  "password": "password",
	"cpf":"",
	"phone":""
}
```

**RESPONSE**
```json
{
	"message": "Dados alterados com sucesso!",
	"changePassword": true,
	"data": [
		{
			"name": "User Name",
			"email": "test@gmail.com",
			"cpf": "",
			"phone": ""
		}
	]
}
```
<h3 id="post-register-client">POST /registerClient/:idUser</h3>

**REQUEST**  
```json
{
  "name":"client",
  "email":"client@gmail.com",
  "phone": "14122248547",
  "cpf": "462.020.777-27",
	"state":"RJ"
}
```
<h3 id="put-edit-client">PUT /editClient/:idUser</h3>

**REQUEST**  
```json
{
	"id":"265962",
	"name": "client",
	"email": "client59.2@gmail.com",
	"cpf": "52652352313",
	"phone": "59531248129",
	"zip_code": null,
	"address": null,
	"complementary_address": null,
	"neighborhood": null,
	"city": "Rio de Janeiro",
  "state": "RJ"
}
```

<h3 id="post-register-billing">POST /registerBilling/:idUser/:idClient</h3>

**REQUEST**  
```json
{
  "status":"PENDENTE",
  "value":53000,
  "due_date":"2023-12-02"
}

```
<h3 id="put-edit-billing">PUT /editBilling/:idBill</h3>

**REQUEST**  
```json
{
	"name":"client",
	"value":"15590",
	"due_date":"2023-11-24",
	"status":"PAGO",
	"payment_date":"2023-11-26"
}
```

<p id="colab">
 
  ## 🤝 Collaborators
</p>
This is the team that made it all happen: 💜 

<table>
  <tr>
<td align="center"><a href="https://github.com/Kauanedev"><img style="border-radius: 50%;" src="https://media.licdn.com/dms/image/D4E03AQE8gv40ZhO8ww/profile-displayphoto-shrink_200_200/0/1680386723608?e=1714003200&v=beta&t=sNOFcWeNpaJMxV7lMfxfHDaWzAVxz0GfprxS_I0i6DI" width="100px;" alt=""/><br /><sub><b>Kauane Santos</b></sub></a><br /><a href="https://github.com/Kauanedev" >💫</a></td>

<td align="center"><a href="https://github.com/SchneiderMurilo"><img style="border-radius: 50%;" src="https://avatars.githubusercontent.com/u/129790001?v=4" width="100px;" alt=""/><br /><sub><b>Murilo Schneider</b></sub></a><br /><a href="https://github.com/SchneiderMurilo" >👨‍💻</a></td>
    
<td align="center"><a href="https://github.com/LuizDevExe"><img style="border-radius: 50%;" src="https://media.licdn.com/dms/image/D4D03AQErTbo1oWSLaA/profile-displayphoto-shrink_800_800/0/1702061663832?e=1714003200&v=beta&t=yevdEw4MHro-1zXXbV9itcVyunO3Zni0_tCTS4LN848" width="100px;" alt=""/><br/><sub><b>Luiz Pedro</b></sub></a><br/> <a href="https://github.com/LuizDevExe">👨‍💻</a></td>

    
<td align="center"><a href="https://github.com/JefersonVM"><img style="border-radius: 50%;" src="https://avatars.githubusercontent.com/u/62728162?v=4" width="100px;" alt=""/><br /><sub><b>Jeferson Vieira</b></sub></a><br /><a href="https://github.com/JefersonVM" >👨‍💻</a></td>

<td align="center"><a href="https://github.com/gabrielnfarias"><img style="border-radius: 50%;" src="https://avatars.githubusercontent.com/u/105251567?v=4" width="100px;" alt=""/><br /><sub><b>Gabriel Navarro Farias</b></sub></a><br /><a href="https://github.com/gabrielnfarias" >👨‍💻</a></td>

  </tr>
</table>


Feito com 💓 por Kauane Santos 👋 [Entre em contato!](https://www.linkedin.com/in/kauane-santos-dev/)