# pkleavue2


If you check your project's structure, you will see that there is already an existing directory named test.  
Inside this directory, there are two directories, unit and e2e. For now, we should go to the unit folder.  
Here, you will see another directory called specs. This is where all our unit test specifications will reside.  
Let's start by creating a directory called __vuex__ inside specs. Here is where all our specs for Vuex-related JavaScript files will live.



## 8. Deploying – Time to Go Live!
### Software deployment
[ngrok](https://ngrok.com/download)
```
ngrok http 8080
```

### Setting continuous integration with Travis
.travis.yml  
See last two lines
```
language: node_js 
sudo: required 
dist: trusty 
node_js: 
  - "5.11.0" 
 
before_script: 
  - export CHROME_BIN=/usr/bin/google-chrome 
  - sudo apt-get update 
  - sudo apt-get install -y libappindicator1 fonts-liberation 
  - wget https://dl.google.com/linux/direct/google-chrome-
    stable_current_amd64.deb 
  - sudo dpkg -i google-chrome*.deb 
  - export DISPLAY=:99.0 
  - sh -e /etc/init.d/xvfb start 
```


### Deploying the Pomodoro application
```
heroku logs --app catodoro --tail  
```
it fails. Do not forget to create a npm start script in package.json.


### Deploying the shopping list application
try heroku locally
```
npm run build 
heroku local web  
```
