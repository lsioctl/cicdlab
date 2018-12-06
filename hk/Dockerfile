# multi-stage for docker heroku deployments
FROM docker:stable 
FROM node:10-alpine 
RUN apk add --no-cache curl
RUN apk add --no-cache bash 
RUN curl https://cli-assets.heroku.com/install.sh | sh
# copy dockers binaries
COPY --from=0 /usr/local/bin/ /usr/local/bin
