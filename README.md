# Golang Project


```bash
git config --list
```

## Set the username

Use the user name you're using for the host: `USER_NAME=k33g` (to keep your git credentials)

```yaml
services:

  devcontainer:
    build:
      context: .
      dockerfile: golang.Dockerfile
      args:
        - GO_VERSION=1.23.1
        - TINYGO_VERSION=0.33.0
        - USER_NAME=k33g
    volumes:
      - ../..:/workspaces:cached      
    environment:
      - MESSAGE="Hello World!"
    command: sleep infinity
```
