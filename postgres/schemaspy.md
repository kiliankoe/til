# Visualizing a DB schema with Schemaspy

Not really specific to Postgres, but sorting here nonetheless.

Running Schemaspy from within a docker container:

```shell
docker run -v `pwd`/diagram:/output schemaspy/schemaspy:latest -t pgsql --port 5432 -u <user> -p <pw> -db <db_name> -host docker.for.mac.localhost
```
