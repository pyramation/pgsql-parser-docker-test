# pgsql-parser docker test

docker test for [pgsql-parser](https://github.com/pyramation/pgsql-parser)

# 1 build the docker image

run `docker-compose build`

# 2 start the server

```sh
docker run -d \
  -it \
  --name build_pgsql_parser \
  pyramation/pgsql_parser
```

# 3 jump inside

`ssh` into the box

```sh
docker exec -it build_pgsql_parser /bin/bash
```
# 4 create npm repo and add pgsql-parser

see, it works!

```
mkdir myproj
cd myproj/
npm init
yarn 
yarn add pgsql-parser
node
> require('pgsql-parser')
{
  Deparser: [Getter],
  deparse: [Getter],
  enums: [Getter],
  parseFunction: [Getter],
  parse: [Function: parse]
}
> 
```