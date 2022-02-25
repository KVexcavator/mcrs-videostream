Env set:
export PORT=3000

Dev mode:
npm install
mpm run start:dev

Prod mode:
npm install --only=production
npm start
---------------------------------------------
Docker:
docker --version
docker --help
https://hub.docker.com/layers/node/library/node/16.13.2-alpine/images/sha256-f21f35732964a96306a84a8c4b5a829f6d3a0c5163237ff4b6b8b34f8d70064b?context=explore
docker build -t video-streaming --file Dockerfile .

список доступных:
docker image list
docker run -d -p 3000:3000 video-streaming
(-d detached mode без отображения в терминале)

список запущенных:
docker container list
docker logs <container-id>
docker stop <container-id>

Удаление контейнера:
docker ps  показывает запушенные и остановленные
docker kill <your-container-id>
docker rm <your-container-id>
docker image list
docker rmi <your-image-id> --force

запуск из Azure репозитория:
docker run -d -p 3000:3000 kvexcavatormsrs.azurecr.io/video-streaming:latest
----------------------------------------
Docker Compose
docker-compose help

построить и запустить
docker-compose up --build

список запущенных контейнеров:
docker-compose ps

остановка с переводом в сотоянию остановлено:
docker-compose stop
остановка с очисткой:
docker-compose down
перезапуск:
docker-compose down && docker-compose up --build

---------------------------
для azure-storage
export PORT=3000
export STORAGE_ACCOUNT_NAME=<the name of your storage account>
export STORAGE_ACCESS_KEY=<the access key for your storage account>
npm run start:dev
------------------------------

http://localhost:4000/video?path=SampleVideo_1280x720_10mb.mp4
http://localhost:4001/video
