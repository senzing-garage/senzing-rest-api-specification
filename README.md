# senzing-rest-api-specification

## Overview

The Senzing REST API specification is an OpenAPI 3.0 Specification of the RESTful API supported by the
[Senzing API server](https://github.com/Senzing/senzing-api-server).

## View

Viewing the Senzing REST API OpenAPI specification:

- In [Swagger UI](https://petstore.swagger.io/?url=https://raw.githubusercontent.com/Senzing/senzing-rest-api-specification/master/senzing-rest-api.yaml)
- In [Swagger validator](http://validator.swagger.io/?url=https://raw.githubusercontent.com/Senzing/senzing-rest-api-specification/master/senzing-rest-api.yaml)
- In [Swagger editor](http://editor.swagger.io/?url=https://raw.githubusercontent.com/Senzing/senzing-rest-api-specification/master/senzing-rest-api.yaml)
- In [GitHub](senzing-rest-api.yaml)
- Using Docker

    ```console
    docker run \
      --env URL=https://raw.githubusercontent.com/Senzing/senzing-rest-api-specification/master/senzing-rest-api.yaml \
      --name senzing-swagger-ui \
      --publish 9180:8080 \
      --rm \
      swaggerapi/swagger-ui
    ```

   then open browser to [localhost:9180](http://localhost:9180)

## Submitting comments

Please create an [issue](https://github.com/Senzing/senzing-rest-api-specification/issues) for any requests for clarification or change.
