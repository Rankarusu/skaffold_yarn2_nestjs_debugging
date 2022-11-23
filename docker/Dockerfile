######################################################################
# SOURCE
# See https://hub.docker.com/_/node for information about the docker images
######################################################################
FROM node:lts as sources

WORKDIR /nest
#copy necessary files into the container and install dependencies
COPY . ./

######################################################################
# DEVSERVER
# is used locally to hot reload changed files
######################################################################
FROM sources as devserver
EXPOSE 3000
ENTRYPOINT [ "yarn", "start:debug" ]

