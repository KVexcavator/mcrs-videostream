Env set:
export PORT=3000

Dev mode:
npm install
mpm run start:dev

Prod mode:
npm install --only=production
npm start

Docker:
docker --version
docker --help
https://hub.docker.com/layers/node/library/node/16.13.2-alpine/images/sha256-f21f35732964a96306a84a8c4b5a829f6d3a0c5163237ff4b6b8b34f8d70064b?context=explore
docker build -t video-streaming --file Dockerfile .
docker image list список доступных
docker run -d -p 3000:3000 video-streaming
(-d detached mode без отображения в терминале)
docker container list список запущенных
docker logs <container-id>
docker stop <container-id>
