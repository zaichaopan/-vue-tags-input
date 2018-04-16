# Usage

## step1

init the project

```bash
docker-compose run --rm web vue init webpack .
```

## step 2

change host in config/index.js from __localhost__ to __0.0.0.0__

## step 3

```bash
docker-compose up -d
```

### using shell

```bash
. ./dev.sh
```

using the command in dev script to exec command in the container.

```bash
# install packages
 web-npm install
```
