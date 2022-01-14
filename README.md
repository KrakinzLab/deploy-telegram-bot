 
 ​#​ ​Steps to host your Telegram bot 
 ​##​ ​Heroku: 
  
 ​-​ [ ] Create a Telegram bot with Telegraf API. 
 ​-​ [ ] Create account on [​Heroku​](http://heroku.com/). 
 ​-​ [ ] Install [​Heroku CLI​](https://devcenter.heroku.com/articles/getting-started-with-nodejs#set-up). 
 ​-​ [ ] Install and [​setup git​](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git). 
 ​-​ [ ] Add ​**micro-bot**​ to the project 
 ​    ```bash 
 ​    npm install micro-bot --save 
 ​    ``` 
 ​-​ [ ] Remove Telegraf dependency from ​**package.json**​. 
 ​-​ [ ] set the start command in ​**package.json**​: 
 ​    ```javascript 
 ​    ​... 
 ​    ​"​main​"​:​ ​"​index.js​"​, 
 ​    ​"​scripts​"​:​ { 
 ​    ​"​start​"​:​ ​"​micro-bot​" 
 ​    } 
 ​    ​... 
 ​    ``` 
 ​-​ [ ] Make changes in the code. 
 ​    ​-​ [ ] Change the telegraf import to: 
 ​        ```javascript 
 ​        ​const​ { ​Composer​ } ​=​ ​require​(​'​micro-bot​'​) 
 ​        ``` 
 ​    ​-​ [ ] Create bot from ​**Composer:** 
 ​        ```javascript 
 ​        ​const​ ​bot​ ​=​ ​new​ ​Composer​() 
 ​        ``` 
 ​    ​-​ [ ] Finally remove bot.launch() line instead use: 
 ​        ```javascript 
 ​        ​module​.​exports​ ​=​ bot 
 ​        ``` 
 ​-​ [ ] Init a new git repo: 
 ​    ```bash 
 ​    git init 
 ​    ``` 
 ​-​ [ ] make ​**.gitignore**​ file with following content: 
 ​    ``` 
 ​    node_modules 
 ​    ``` 
 ​-​ [ ] Login to Heroku: 
 ​    ```bash 
 ​    heroku login 
 ​    ``` 
 ​-​ [ ] Create a Heroku app: 
 ​    ```bash 
 ​    heroku create 
 ​    ``` 
 ​-​ [ ] Update Heroku config 
 ​    ```bash 
 ​    heroku config:set --app YourAppId BOT_TOKEN=​'​YOUR BOT TOKEN​' 
 ​    heroku config:set --app YourAppId BOT_DOMAIN=​'​https://YourAppId.herokuapp.com​' 
 ​    ``` 
 ​-​ [ ] Create a ​**Procfile**​ in the root of the bot with the following content: 
 ​    ``` 
 ​    web: micro-bot -p $PORT 
 ​    ``` 
 ​-​ [ ] Finally use git to deploy: 
 ​    ```bash 
 ​    git add ​. 
 ​    git commit -m ​'​commit message​' 
 ​    git push heroku master 
 ​    ``` 
  
 ​##​ ​How to make changes and redeploy the code: 
 ​-​ [ ] Just save all changes. 
 ​-​ [ ] Run following commands: 
 ​    ```bash 
 ​    git add ​. 
 ​    git commit -m ​'​commit message​' 
 ​    git push heroku master 
 ​    ```
<div align="center">
<h1> 🤡 Developer 😎 </h1> 
<br>

[![-Alison-](https://github.com/red-alison.png?size=250)](https://github.com/red-alison) </div>
