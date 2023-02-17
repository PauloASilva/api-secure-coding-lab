FROM node:19.6.0-alpine3.17

WORKDIR /app

RUN npm i -g @open-rpc/mock-server@1.7.5
RUN wget https://raw.githubusercontent.com/open-rpc/examples/master/service-descriptions/petstore-openrpc.json \
    -O openrpc.json

ENTRYPOINT ["open-rpc-mock-server", "-d", "openrpc.json"]
