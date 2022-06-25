# React Skeleton Web for KsMf 
Template to create Web application based on ReactJs easily.

# React Web App Skeleton
Template to create web application based on [React](https://create-react-app.dev/docs/getting-started), [Material UI](https://mui.com/)
 and [KsMf](https://github.com/ameksike/ksmf/wiki) in an easy way. This project implements an example where three main entities are managed: Users, Tags and Comments.

## Run production mode
- npm run client:build
- npm start 

## Run develop mode 
- npm run client:start
- npm run dev

## Test
Run all test:
- npm run 

Run the tests separately:
- npm run client:test
- npm run server:test

## Integration 
This project depends on an external REST API service which provides all the data, therefore it works as an example of system integration. 
```
+----------------+                       +-------------+
| Web App        |<--------------------->|  REST API   |
| React / KsMf   |          HTTPS        |  KsMf       |
+----------------+                       +-------------+
```
To connect this application with the external service follow the steps below:
- git clone https://github.com/ameksike/ksmf-skeleton-rest.git
- cd ksmf-skeleton-rest
- npm install
- edit ./cfg/config.json and define database access options
- npx sequelize-cli db:migrate
- npx sequelize-cli db:seed:all
- npm start
- back to this project 'ksmf-skeleton-web-angular'
- edit ```server\src\app\service\MyAPI.js``` constructor or create ```.env``` with **MyAPI_URL** and set **http://localhost:3005** or the specific configuration for the external REST API in case the default options have been changed.

For more information see the following link: [ksmf-skeleton-rest](https://github.com/ameksike/ksmf-skeleton-rest).

![Screenshot](readme/front.jpg)

## Project skeleton 
```
- client 
|	+ build
|	+ public
|	+ src
|	- package.json
|	- README.md
- server	
|	+ bin/
|	|    - server.js
|	+ cfg/
|	|    - config.json
|	|    - core.json
|	+ src/
|	|    + app/
|	|    |    - index.js
|	|    + commnet/
| 	|    |    + controller/
|	|    |    |    - DefaultController.js
|	|    + user/
| 	|    |    + controller/
|	|    |    |    - DefaultController.js
- package.json
- .env
- .gitignore
- README.md
```

## Backend dev steps
- npm install ksmf
- npm install axios
- npm install jest --save-dev
- npm install supertest --save-dev
- npm install nodemon --save-dev

## Frontend dev steps
- npm install -g create-react-app
- npm init react-app client
- cd client
- npm install react-router-dom
- npm install @mui/material @emotion/react @emotion/styled 
- npm install @mui/icons-material
- npm install emotion-theming
- npm install react-i18next i18next --save
- npm install i18next-browser-languagedetector
- npm install react-redux
- npm install @reduxjs/toolkit
- npm install react-cookies
- npm install sass --save-dev
