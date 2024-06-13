# Academy Pay
<p align="center">
  <img alt="GitHub language count" src="https://img.shields.io/github/languages/count/Kauanedev/academy-pay?color=%2304D361">
  
  <a>
    <img alt="GitHub last commit" src="https://img.shields.io/github/last-commit/Kauanedev/academy-pay">
  </a>
</p>

<p align="center">
	<img alt="Javascript" src="https://img.shields.io/badge/Javascript-0d1b2a?style=for-the-badge&logo=javascript">
	<img alt="Postgresql" src="https://img.shields.io/badge/PostgreSQL-316192?style=for-the-badge&logo=postgresql&logoColor=white">
	<img alt="ExpressJs" src="https://img.shields.io/badge/express-ffd000?style=for-the-badge&logo=express">
	<img src = "https://img.shields.io/badge/Knex.js-D26B38.svg?style=for-the-badge&logo=knexdotjs&logoColor=white"/>  
	<img src = "https://img.shields.io/badge/.ENV-ECD53F.svg?style=for-the-badge&logo=dotenv&logoColor=black"/>  
	<img src = "https://img.shields.io/badge/json%20web%20tokens-323330?style=for-the-badge&logo=json-web-tokens&logoColor=pink"/>
	<img src = "https://img.shields.io/badge/Axios-5A29E4.svg?style=for-the-badge&logo=Axios&logoColor=white"/>  
	<img alt="React" src="https://img.shields.io/badge/React-005CFE?style=for-the-badge&logo=react">
    	<img src = "https://img.shields.io/badge/React%20Router-CA4245.svg?style=for-the-badge&logo=React-Router&logoColor=white"/>  
	<img src = "https://img.shields.io/badge/CSS3-1572B6.svg?style=for-the-badge&logo=CSS3&logoColor=white"/>  
	<img src = "https://img.shields.io/badge/HTML5-E34F26.svg?style=for-the-badge&logo=HTML5&logoColor=white"/>  
	<img src = "https://img.shields.io/badge/Chakra%20UI-319795.svg?style=for-the-badge&logo=Chakra-UI&logoColor=white"/>  
</p>

<h1 align="center">
    <img alt="LOGIN PAGE" title="#LOGIN PAGE" src="assets\login-page.png" />
</h1>


<h4 align="center"> 
💸 Academy Pay 💸
</h4>

<p align="center">
<a href="#about">About</a> •
<a href="#functionalities">Functionalities</a> •
<a href="#run">Run the project</a> •
<a href="#endpoints">API Endpoints</a> •
<a href="tecnologies">Tecnolgies<a/> •
<a href="#colab">Collaborators</a> •
<a href="#deploy">Deployed version</a> •
<a href="#license">License</a>
</p>

## 💻 About the project
<p id="about">
Academy Pay is a solution designed to meet the financial management needs of commercial establishments. It provides a safe and efficient platform for registering customers and organizing the accounts associated with each of them. Owners find this tool an effective resource for transparent management and detailed monitoring of customer transactions.
</p>



<p id="functionalities">

 ## ⚙️ Functionalities
</p>


- Register user
- Register client
- Register client charges
- Validation system for dates and due dates 
- Update user and client records
- General financial tracking

### Web
  
  <h1 align="center">
   <img alt="Register Client" src="assets\register-client.png" />
</h1>
  <h1 align="center">
   <img alt="Register Chrges" src="assets\register-billing.png" />
</h1>
<h1 align="center">
    <img alt="Billing Page" src="assets\billing-page.png" />
</h1>

<h1 align="center">
    <img alt="Home Page" src="assets\home-page.png" />
</h1>


<p id="run">
  
## 🏃‍♀️ Run the project
</p>

### 🎲 Run Backend
💡 try the deployed version: https://backend-devastados.vercel.app/
```bash

 
# Clone this repository:
$ git clone git@github.com:Kauanedev/academy-pay.git

# Access the project folder:
$ cd academy-pay 

# Go to server folder:
$ cd server

# Install dependencies:
$ npm install

# Run the app in the development mode
$ npm run dev

# Server will start on port:3000

```

### 🧭 Run Frontend
💡 try the deployed version: https://desafio-final-front-dds-t12-omega.vercel.app/
```bash

# Clone this repository:
$ git clone git@github.com:Kauanedev/academy-pay.git

# Access the project folder:
$ cd academy-pay

# Go to frontend folder:
$ cd frontend

# Install dependencies:
$ npm install

# Run the app in the development mode:
$ npm run start

# Server will start on port:3000 - Open ~ http://localhost:3000 ~ to view it in your browser.

```

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
  "email":"teste@gmail.com",
  "password": "password"
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

#### **Utilities** 

-   Figma:  **[Figma](https://www.figma.com/)**  →  **[Prototype](https://www.figma.com/file/EsX2ltIJ6gSGFzXXCU1pQH/M05-SPRINT-03?type=design&node-id=410-47347&mode=design&t=M4n4IHXTH8lNe2cO-0)**
-   API:  **[API](https://backend-devastados.vercel.app/)**
-   Source-Code Editor:  **[Visual Studio Code](https://code.visualstudio.com/)** 
-   API Client:  **[Insomnia](https://insomnia.rest/)**
-   Icons:  **[Chakra Ui Icons](https://chakra-ui.com/docs/components/icon)**
-   Fonts:  **[Nunito](https://fonts.google.com/specimen/Nunito)**,  **[Montserrat](https://fonts.google.com/specimen/Montserrat?query=montse)**
---


<p id="colab">
 
  ## 🤝 Collaborators
</p>
This is the dream team that made it all happen: 💜 

<table>
  <tr>
    <td align="center">
      <a href="https://www.linkedin.com/in/kauane-santos-dev/">
        <img src="https://github.com/Kauanedev.png" width="100px;"; alt="perfil kau"/><br/>
        <sub> Kauane Santos <sub/>
        <a/>
    </td>
    <td align="center">
      <a href="https://github.com/SchneiderMurilo">
        <img src="https://avatars.githubusercontent.com/u/129790001?v=4" width="100px;" ; alt="perfil Murilo"/><br/>
        <sub> Murilo Schneider 👨‍💻 <sub/>
        <a/>
    </td>
    <td align="center">
      <a href="https://github.com/LuizDevExe">
        <img src="https://avatars.githubusercontent.com/u/109562299?v=4" width="100px;"; alt="perfil Murilo"/><br/>
        <sub> Luiz Pedro 👨‍💻 <sub/>
        <a/>
    </td>
      <td align="center">
      <a href="https://github.com/JefersonVM">
        <img src="https://avatars.githubusercontent.com/u/62728162?v=4" width="100px;"; alt="perfil Murilo"/><br/>
        <sub> Jeferson Vieira  👨‍💻 <sub/>
        <a/>
    </td>
      </td>
      <td align="center">
      <a href="https://github.com/gabrielnfarias" >
        <img src="https://avatars.githubusercontent.com/u/105251567?v=4" width="100px;" style="border-radius: 50%"; alt="perfil Murilo"/><br/>
        <sub> Gabriel Navarro  👨‍💻 <sub/>
        <a/>
    </td>
  </tr>
</table>


<p id="deploy">

## 🚀 Deployed Application
<p/>

  Visit our project and try it for yourself:
</p>

🖥️[Frontend](https://desafio-final-front-dds-t12-omega.vercel.app/sign-in)
🎲[Backend](https://backend-devastados.vercel.app/)	

<p id="license">
	
## 📝 Licese
</p>

This project is under license [MIT](./LICENSE).

Made with 💓 by Kauane Santos 👋 [Contact me!](https://www.linkedin.com/in/kauane-santos-dev/)
