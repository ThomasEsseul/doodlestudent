FROM node:lts as build

WORKDIR /usr/src/app

# ADD server-confs/roneul/roneul.conf /server-confs/roneul.conf
ADD . .

RUN npm install
RUN npm run build --prod

FROM bunkerity/bunkerized-nginx:latest as prod
COPY --from=build /usr/src/app/dist/tlcfront /www/