General Instructions

[CLONING PROJECT]

git clone https://github.com/rrojasf/microservices_master.git taskmanager_microservices_project

[INITIALIZE SUBMODULES]
alternate 1

git submodule init

git submodule update

alternate 2 (CLONING RECURSIVE)

git clone --recursive https://github.com/rrojasf/microservices_master.git taskmanager_microservices_project

[USE ENV SETTINGS FOR LOCAL CONFIGURATION]
(skip for use deployed apis)

mv user-api/env/.env-local user-api/env/.env
mv task-api/env/.env-local task-api/env/.env

rename config-local.js  to config.js into tasks-manager-api directory (reactjs app) (for using local apis)

by default system connects to public servers

docker-compose build


[SERVERS]

https://taskmanager-ms-app.herokuapp.com/
https://taskmgr-ms-user-api.herokuapp.com/api/users
https://taskmgr-ms-task-api.herokuapp.com/api/tasks

