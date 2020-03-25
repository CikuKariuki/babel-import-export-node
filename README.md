1. npm install nodemon --save-dev
2. in scripts: "start":"nodemon src/index.js"
3. npm install @babel/core @babel/node --save-dev
4. add to "start" in "scripts" .... "start" : "nodemon --exec babel-node src/index.js"   It shouldn't change anything
5. npm install @babel/preset-env --save-dev 
6. create .babelrc file in root directory and include the presets for babel...{ "presets": ["@babel/preset-env" ]}
7. create .env file, write my_secret = my secret!!1
8. index.js, import dotenv/config and other import statements that will work if they have been exported.

source of information: https://www.robinwieruch.de/minimal-node-js-babel-setup

----------------------------------------------------------------------------------------------------------
Installing babel
 
1. npm install nodemon --save-dev
{
 ...
 "main": "index.js",
 "scripts": {
2.   "start": "nodemon src/index.js",
   "test": "echo \"Error: no test specified\" && exit 1"
 },
 "keywords": [],
 ...
}
 
in your src/index.js:
3. console.log('Hello ever running Node.js project.');
 
4. npm install @babel/core @babel/node --save-dev
 
{
 ...
 "main": "index.js",
 "scripts": {
5.    "start": "nodemon --exec babel-node src/index.js",
   "test": "echo \"Error: no test specified\" && exit 1"
 },
 "keywords": [],
 ...
}
 
6. npm install @babel/preset-env --save-dev
 
7. in the root: touch .babelrc
 
 
8. in babelrc: {
 "presets": [
   "@babel/preset-env"
 ]
}
 
9. touch .env
 
10. in env: MY_SECRET = mypassword
 
11. npm install dotenv --save
 
 
12. import 'dotenv/config';
console.log('Hello Node.js project.');
console.log(process.env.MY_SECRET);
