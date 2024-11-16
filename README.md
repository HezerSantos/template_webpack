npm init -y

npm install --save-dev webpack webpack-cli

npx webpack //this creates the file in dist

npm install --save-dev html-webpack-plugin

npm install --save-dev style-loader css-loader

npm install --save-dev html-loader

npm install --save-dev webpack-dev-server

npx webpack serve ctrl + c to kill

git branch gh-pages

git checkout gh-pages && git merge main --no-edit

npx webpack

git add dist -f && git commit -m "Deployment commit"

git subtree push --prefix dist origin gh-pages

git checkout main

lint

npm install --save-dev eslint @eslint/js

touch eslint.config.js

import js from "@eslint/js";

export default [
    js.configs.recommended,
   {
       rules: {
           "no-unused-vars": "warn",
           "no-undef": "warn"
       }
   }
];

npx eslint project-dir/ file1.js

prettier

npm install --save-dev --save-exact prettier

node --eval "fs.writeFileSync('.prettierrc','{}\n')"

node --eval "fs.writeFileSync('.prettierignore','# Ignore artifacts:\nbuild\ncoverage\n')"

npx prettier . --write //runs prettier

npx prettier . --check //checks prettier

npm install --save-dev eslint-config-prettier


import eslintConfigPrettier from "eslint-config-prettier";

export default [
  someConfig,
  eslintConfigPrettier,
];

"scripts": {
  "setup": "npm init -y && npm install --save-dev webpack webpack-cli && npx webpack && npm install --save-dev html-webpack-plugin && npm install --save-dev style-loader css-loader && npm install --save-dev html-loader && npm install --save-dev webpack-dev-server && npm install --save-dev --save-exact prettier && node --eval \"require('fs').writeFileSync('.prettierrc', '{}\\n')\" && node --eval \"require('fs').writeFileSync('.prettierignore', '# Ignore artifacts:\\nbuild\\ncoverage\\n')\""
}

