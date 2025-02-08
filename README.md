#### **Step 1: Create a New Node.js Project**

    mkdir level2-first-project
    cd level2-first-project
    npm init -y
This creates a new project with a `package.json` file.
#### **Step 2: Install Dependencies**
    npm install express
    npm install mongoose --save
    npm install typescript --save-dev
    npm i cors
    npm i dotenv
**express** → Web framework for Node.js
**mongoose** → ODM (Object Data Modeling) for MongoDB
**dotenv** → Loads environment variables from `.env`
**cors** → Middleware to allow cross-origin requests

For TypeScript and development tools, install:

    npm install --save-dev typescript ts-node @types/node @types/express @types/cors @types/mongoose nodemon

#### **Step 3: Initialize TypeScript**
    npx tsc --init
This generates a `tsconfig.json` file. Update it:

```javascript
{
      "compilerOptions": {
        "target": "ES6",
        "module": "CommonJS",
        "outDir": "./dist",
        "rootDir": "./src",
        "strict": true,
        "esModuleInterop": true
      }
    }
```

 #### **Step 3: Create the Folder Structure**

mkdir src src/config src/models src/routes
touch src/server.ts src/config/db.ts .env


 #### **Step 3: Setup Express Server**
**app.ts**
 ```javascript
const express = require('express')
export const app = express()

app.get('/', (req, res) => {
  res.send('Hello World!')
})
```

**server.ts**
```javascript
const  app  =  require('./app');
const  port  =  3000;
app.listen(port, () => {
  console.log(`Example app listening on port ${port}`)
})
```

 #### **Step 4: Run Server**
```javascriptå
"scripts": {
"build": "tsc",
"test": "echo \"Error: no test specified\" && exit 1"
},
```








