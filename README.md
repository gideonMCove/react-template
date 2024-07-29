# Steps for making a MERN application in VS Code

## React project
1. npm create vite@latest
1. name project (and package)
1. choose framework: React
1. choose variant: JavaScript
1. (this creates public folder, src > assets, App.css, index.css, App.jsx, main.jsx, index.html etc)
1. cd into the project folder
1. npm install //adds node modules
1. add two rules into .eslintrc.cjs file //optional
1.  'react/prop-types': 'off', // prevents warnings if you’re not declaring types for your props 
1.  'react/no-unescaped-entities': 'off' // prevents warnings if you’re using contractions within JSX.
1. mkdir src > components folder
1. create component files like Header.jsx, Main.jsx, Home.jsx, Footer.jsx, Nav.jsx

## router-react
1. npm install react-router-dom
1. In main.jsx, add import { BrowserRouter } from 'react-router-dom'
1. In main.jsx, add  <React.StrictMode> and <BrowserRouter> before and after <App/>
1. In App.jsx, add import {Route, Routes} from 'react-router-dom'
1. In App.jsx (or Main.jsx), add <Routes> //routes go here// <Routes/>
1. In App.jsx (or Main.jsx), add <Route path="/" element={<Home/>}/>
1. In App.jsx (or Main.jsx), add <Route path="/componentA" element={<ComponentA/>}/> 
1. In App.jsx (or Main.jsx), add <Route path="/componentA/:id" element={<ComponentADetails/>}/> 
1. In Nav.jsx, add <Link to="/"> <h 2> Home </h 2> </Link>
1. In Nav.jsx, add <Link to="/componentA"> <h 2> Component A</h 2> </Link>

## Hooks and State and Effect
1. In App.jsx, add import { useState, useEffect } from 'react'
1. const [array, setArray] = useState([])

## React Axios API 
1. npm install axios
1. App.jsx -> import { useState, useEffect } from 'react'
1. App.jsx -> import axios from 'axios'
1. touch .env (optional)
1. add API key: REACT_APP_TMDB_KEY=<Your secret token> (optional)
1. include .env in gitIgnore (optional)
1. include /node_modules and .DS_store in gitIgnore (optional)

## Mongoose and Express
1. npm init -y //creates package.json
1. npm install express //for controllers
1. npm install nodemon --save-dev
1. npm install cors //for middleware
1. npm install mongoose //creates and package-lock.json
1. npm install body-parser //used to create and update json in thunder client
1. npm install morgan //shows commands that are in command line
Those steps will add these items:
* file "package.json" **Note: Make sure it references the correct JS file of server.js**
* file "package-lock.json"
1. manually add to package.json scripts:  
* "start":"node server.js",
*  "dev":"nodemon server.js"
1. mkdir db models seed controllers
1. touch db/index.js 
1. touch models/{modelA,modelB,index}.js 
1. touch server.js
1. touch controllers/{dogControllers,catController}/.js
1. touch seed/initialData.js //create seed file
1. node seed/initialData.js //to actually run the seed file
1. add lines to server.js
* const bodyParser = require('body-parser')
* const logger = require('morgan');
* app.use(bodyParser.json()) 
* app.use(logger('dev'))

* ## Deploy React
* 1. ## To Deploy a React project on Surge:
1. be in the folder that has index.html as a listed file
1. npm run build //this will add folder 'dist' 
1. surge ./dist
1. choose domain name < NAME >.surge.sh
