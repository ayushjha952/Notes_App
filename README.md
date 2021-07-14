# **Notes App** 

>A basic notes app with normal CRUD functionality.

>A login and logout system with Google Authentication.  

## **Environment Variables**

Because we have used MongoDB, we’ll need a MongoDB SRV URI. You can create a database from this [link](https://www.mongodb.com/cloud/atlas). 

Now, create a `.env` file  to store the MongoDB SRV URI and the base URL, to run this project. The base URL will be your local host server location for now. Here’s my .env file code:

```
MONGO_URI=mongodb+srv://nemo:YourPasswordHere@cluster0.mkws3.mongodb.net/myFirstDatabase?retryWrites=true&w=majority
BASE=http://localhost:3000
```

Remember to change the ```<password>``` field in the MongoDB URI with your database password.

Before implementing Google OAuth in our app, we need to first get our API key. To acquire it, go to the Google Developers Console page, and then create a project.

After creating the project click on ```Credentials``` , after this, click on ```Create Credentials```, then click on ```OAuth Client ID```. On the Application Type field, select ```Web Application```. Along with that, use the following settings:

![screenshot](https://miro.medium.com/max/613/1*NHQP35K0fP8XXNKuBWGavw.png)


When you click on Create, you’ll receive your Client ID Key and the Client Secret Key.

In ```.env``` file copy the Client ID Key in ```GOOGLE_CLIENT_ID``` and
Client Secret Key in ```GOOGLE_CLIENT_SECRET```. 

Updated ```.env``` file code:

```
MONGO_URI=mongodb+srv://nemo:YourPasswordHere@cluster0.mkws3.mongodb.net/myFirstDatabase?retryWrites=true&w=majority
BASE=http://localhost:3000
GOOGLE_CLIENT_ID = "paste your Client ID Key here"
GOOGLE_CLIENT_SECRET = "paste your Client Secret Key here"
```

## **Run Locally**

Clone the project

```bash
  git clone https://github.com/ayushjha952/Notes_App.git
```

Go to the project directory

```bash
  cd Url_Shortner
```

Install dependencies

```bash
  npm install
```

Start the server

```bash
  npm run start
```