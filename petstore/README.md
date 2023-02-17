Petstore Playground - JSON-RPC
==============================

OpenRPC Petstore mock server. ([GitHub][1])

## How-to

### Start

```
docker-compose up -d
```

### Stop

```
docker-compose down
```

### Documentation

After starting:

```
curl http://localhost:3333/ \
  -X POST \
  -H $'Content-Type: application/json' \
  --data-binary $'{
    "jsonrpc": "2.0",
    "method": "rpc.discover",
    "id": 0
  }'
```

[1]: https://github.com/open-rpc/mock-server
