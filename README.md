1. npm install nodemon --save-dev
2. in scripts: "start":"nodemon src/index.js"
3. npm install @babel/core @babel/node --save-dev
4. add to "start" in "scripts" .... "start" : "nodemon --exec babel-node src/index.js" 
--It shouldn't change anything
5. npm install @babel/preset-env --save-dev 
6. create .babelrc file in root directory and include the presets for babel...{ "presets": ["@babel/preset-env" ]}
7. 