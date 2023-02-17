Damn Vulnerable GraphQL Application - GraphQL
=============================================

Damn Vulnerable GraphQL Application is an intentionally vulnerable
implementation of Facebook's GraphQL technology, to learn and practice GraphQL
Security. ([GitHub][1])

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
curl http://localhost:5013/graphql \
  -X $'POST' \
  -H $'Content-Type: application/json' \
  --data-binary $'{\"query\":\"\\n  query IntrospectionQuery {\\n    __schema {\\n      queryType { name }\\n      mutationType { name }\\n      subscriptionType { name }\\n      types {\\n        ...FullType\\n      }\\n      directives {\\n        name\\n        description\\n        locations\\n        args {\\n          ...InputValue\\n        }\\n      }\\n    }\\n  }\\n\\n  fragment FullType on __Type {\\n    kind\\n    name\\n    description\\n    fields(includeDeprecated: true) {\\n      name\\n      description\\n      args {\\n        ...InputValue\\n      }\\n      type {\\n        ...TypeRef\\n      }\\n      isDeprecated\\n      deprecationReason\\n    }\\n    inputFields {\\n      ...InputValue\\n    }\\n    interfaces {\\n      ...TypeRef\\n    }\\n    enumValues(includeDeprecated: true) {\\n      name\\n      description\\n      isDeprecated\\n      deprecationReason\\n    }\\n    possibleTypes {\\n      ...TypeRef\\n    }\\n  }\\n\\n  fragment InputValue on __InputValue {\\n    name\\n    description\\n    type { ...TypeRef }\\n    defaultValue\\n  }\\n\\n  fragment TypeRef on __Type {\\n    kind\\n    name\\n    ofType {\\n      kind\\n      name\\n      ofType {\\n        kind\\n        name\\n        ofType {\\n          kind\\n          name\\n          ofType {\\n            kind\\n            name\\n            ofType {\\n              kind\\n              name\\n              ofType {\\n                kind\\n                name\\n                ofType {\\n                  kind\\n                  name\\n                }\\n              }\\n            }\\n          }\\n        }\\n      }\\n    }\\n  }\\n\"}'
```

[1]: https://github.com/dolevf/Damn-Vulnerable-GraphQL-Application
