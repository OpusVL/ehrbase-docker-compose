# Open Electronic Health Record Platform

https://ehrbase.org/

Java Spring based product with Tomcat JSP and PostgreSQL database.

This docker-compose combines both the `ehrdb` and `ehrbase` products into a single container set.

The `ehrbase` is a compiled version using the `:next` tag. `ehrdb` uses the `:latest` tag.

`ehrbase` is exposed on port 8080 and postgres is not exposed.

The postgres data will be placed in `./postgres` by default.

## Environment Variables

There is a [`.env.sample`](.env.sample) file containing the variables used which are pretty self explanatory. Copy or rename this file to `.env` and set the values as required.

```properties
POSTGRES_USER=postgres
POSTGRES_PASSWORD=postgres
EHRBASE_USER=ehrbase
EHRBASE_PASSWORD=ehrbase
EHRBASE_DB=ehrbase

DB_URL=jdbc:postgresql://ehrdb:5432/ehrbase
DB_USER=ehrbase
DB_PASS=ehrbase
SYSTEM_NAME=local.ehrbase.org
```

## Usage

```shll
$ docker-compose up -d
```

## API Documentation

http://localhost:8080/ehrbase/swagger-ui.html