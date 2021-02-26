# gin-jwt-middleware-rsa
[![Go Report Card](https://goreportcard.com/badge/github.com/bri-b-dev/gin-jwt-middleware-rsa)](https://goreportcard.com/report/github.com/bri-b-dev/gin-jwt-middleware-rsa)

## What is JWT?
JSON Web Token (JWT) more information:
[http://self-issued.info/docs/draft-ietf-oauth-json-web-token.html](http://self-issued.info/docs/draft-ietf-oauth-json-web-token.html)

## How to use this?
#### Install package
```bash
$ go get github.com/bri-b-dev/gin-jwt-middleware-rsa
```

#### In your gin application main.go, import the package
```go
import (
    "github.com/bri-b-dev/gin-jwt-middleware-rsa"
)
```

#### Use the middleware
```go
app := gin.Default()

app.Use(auth.JWTAuthMiddleware(encoded, YOUR_SECRET)
```

- encoded is a booleen: if your JWT secret is encoded
- YOUR_SECRET: Your JWT secret, here you can use the env variable
