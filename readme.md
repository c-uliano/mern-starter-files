## General setup
- rename project folder
- set up github repo for main project folder

## Client setup
- `cd PROJECT-FOLDER-NAME`
- `npx create-react-app client`
    - update to this, use vite to create react apps now, `create-react-app` is outdated
- `cd client`
- `npm i axios react-router-dom`
    - install whatever else the project needs
- index.js, wrap <br/>
&lt;BrowserRouter&gt;<br/>
&lt;App/&gt;<br/>
&lt;BrowserRouter/&gt;<br/> & 
import { BrowserRouter } from 'react-router-dom';
- App.js, create 
&lt;Routes&gt;&lt;Routes/&gt; 
and add in as many
&lt;Route/&gt; as necessary & 
import { Link, Route, Routes } from 'react-router-dom';
- in /src create /components folder, add components here
- `npm start` to start the frontend server
- `ctrl c` to stop

## Server setup
- create `.gitignore`, add `/node_modules`
- `npm i express mongoose cors`
    - install whatever else the project needs
    - I have `nodemon` installed globally, otherwise also install it as part of your project
- create database, probably in compass
- go through and rename everything labeled RENAME
- update database name in mongoose.config.js
- run `brew services start mongodb-community@5.0` to be able to connect to database
    - I have this always running
    - `brew services stop mongodb-community@5.0` to stop the service, if necessary
- `cd server`
- `nodemon server.js` to start the backend server
- `ctrl c` to stop
