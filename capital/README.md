c{api}tal - REST
================

A built-to-be-vulnerable API application based on the OWASP top 10 API
vulnerabilities. Use c{api}tal to learn, train and exploit API Security
vulnerabilities within your own API Security CTF. ([GitHub][1])

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
curl http://localhost:8000/openapi.json
```

[1]: https://github.com/Checkmarx/capital
