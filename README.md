General Instructions

[CLONING PROJECT]

git clone https://github.com/rrojasf/microservices_master.git taskmanager_microservices_project

[INITIALIZE SUBMODULES]

**alternate 1**

cd taskmanager_microservices_project

git submodule init

git submodule update

**alternate 2 (CLONING RECURSIVE)**

git clone --recursive https://github.com/rrojasf/microservices_master.git taskmanager_microservices_project

[USE ENV SETTINGS FOR LOCAL CONFIGURATION]
(skip for use deployed apis/replace endpoints)

cd taskmanager_microservices_project

mv user-api/env/.env-local user-api/env/.env
mv task-api/env/.env-local task-api/env/.env

go to user-api/app folder and execute npm install
go to task-api/app folder and execute npm install

(By default React App is configured to go to live servers, if you want to try connection to local apis you must replace config.js by renaming config.local.js to config.js)

rename config.local.js  to config.js into tasks-manager-api directory (reactjs app) (for using local apis)

docker-compose build
docker-compose up

*[SERVERS]*

[REACTJS GUI APP]: (https://taskmanager-ms-app.herokuapp.com/)
[USERS API]: (https://taskmgr-ms-user-api.herokuapp.com/api/users)
[TASKS API]: (https://taskmgr-ms-task-api.herokuapp.com/api/tasks)

-Local Servers at 
[local-users-api] (http://localhost:81/api/users)
[local-tasks-api] (http://localhost:82/api/tasks)

[DATABASE]

By default apis are working with a DBaas solution for easy use of data 

MongoDB Atlas Instance
