# senzing-rest-api-specification

If you are beginning your journey with [Senzing],
please start with [Senzing Quick Start guides].

You are in the [Senzing Garage] where projects are "tinkered" on.
Although this GitHub repository may help you understand an approach to using Senzing,
it's not considered to be "production ready" and is not considered to be part of the Senzing product.
Heck, it may not even be appropriate for your application of Senzing!

## Overview

The Senzing REST API specification is an OpenAPI 3.0 Specification of the
RESTful API supported by the [Senzing API server].

## View (Latest version)

Viewing the Senzing REST API OpenAPI specification:

1. In [Swagger UI]
1. In [Swagger validator]
1. In [Swagger editor]
1. Using Docker.
   Example:

   ```console
   sudo docker run \
     --env URL=https://raw.githubusercontent.com/senzing-garage/senzing-rest-api-specification/main/senzing-rest-api.yaml \
     --name senzing-swagger-ui \
     --publish 9180:8080 \
     --rm \
     swaggerapi/swagger-ui
   ```

   Open browser to [localhost:9180]

1. In [GitHub]

## View (Previous Versions)

View previous versions of the Senzing REST API OpenAPI specification:

- [Version 3.1.0]
- [Version 3.0.0]
- [Version 2.7.0]
- [Version 2.6.0]
- [Version 2.5.0]
- [Version 2.4.0]
- [Version 2.3.0]
- [Version 2.2.0]
- [Version 2.1.1]
- [Version 2.1.0]
- [Version 2.0.0]
- [Version 1.8.2]
- [Version 1.8.1]
- [Version 1.7.5]

## Submitting comments

Please create an [issue] for any requests for clarification or change.

[GitHub]: senzing-rest-api.yaml
[issue]: https://github.com/senzing-garage/senzing-rest-api-specification/issues
[localhost:9180]: http://localhost:9180
[Senzing API server]: https://github.com/senzing-garage/senzing-api-server
[Senzing Garage]: https://github.com/senzing-garage
[Senzing Quick Start guides]: https://docs.senzing.com/quickstart/
[Senzing]: https://senzing.com/
[Swagger editor]: http://editor.swagger.io/?url=https://raw.githubusercontent.com/senzing-garage/senzing-rest-api-specification/main/senzing-rest-api.yaml
[Swagger UI]: https://petstore.swagger.io/?url=https://raw.githubusercontent.com/senzing-garage/senzing-rest-api-specification/main/senzing-rest-api.yaml
[Swagger validator]: http://validator.swagger.io/?url=https://raw.githubusercontent.com/senzing-garage/senzing-rest-api-specification/main/senzing-rest-api.yaml
[Version 1.7.5]: https://petstore.swagger.io/?url=https://raw.githubusercontent.com/senzing-garage/senzing-rest-api-specification/1.7.5/senzing-rest-api.yaml
[Version 1.8.1]: https://petstore.swagger.io/?url=https://raw.githubusercontent.com/senzing-garage/senzing-rest-api-specification/1.8.1/senzing-rest-api.yaml
[Version 1.8.2]: https://petstore.swagger.io/?url=https://raw.githubusercontent.com/senzing-garage/senzing-rest-api-specification/1.8.2/senzing-rest-api.yaml
[Version 2.0.0]: https://petstore.swagger.io/?url=https://raw.githubusercontent.com/senzing-garage/senzing-rest-api-specification/2.0.0/senzing-rest-api.yaml
[Version 2.1.0]: https://petstore.swagger.io/?url=https://raw.githubusercontent.com/senzing-garage/senzing-rest-api-specification/2.1.0/senzing-rest-api.yaml
[Version 2.1.1]: https://petstore.swagger.io/?url=https://raw.githubusercontent.com/senzing-garage/senzing-rest-api-specification/2.1.1/senzing-rest-api.yaml
[Version 2.2.0]: https://petstore.swagger.io/?url=https://raw.githubusercontent.com/senzing-garage/senzing-rest-api-specification/2.2.0/senzing-rest-api.yaml
[Version 2.3.0]: https://petstore.swagger.io/?url=https://raw.githubusercontent.com/senzing-garage/senzing-rest-api-specification/2.3.0/senzing-rest-api.yaml
[Version 2.4.0]: https://petstore.swagger.io/?url=https://raw.githubusercontent.com/senzing-garage/senzing-rest-api-specification/2.4.0/senzing-rest-api.yaml
[Version 2.5.0]: https://petstore.swagger.io/?url=https://raw.githubusercontent.com/senzing-garage/senzing-rest-api-specification/2.5.0/senzing-rest-api.yaml
[Version 2.6.0]: https://petstore.swagger.io/?url=https://raw.githubusercontent.com/senzing-garage/senzing-rest-api-specification/2.6.0/senzing-rest-api.yaml
[Version 2.7.0]: https://petstore.swagger.io/?url=https://raw.githubusercontent.com/senzing-garage/senzing-rest-api-specification/2.7.0/senzing-rest-api.yaml
[Version 3.0.0]: https://petstore.swagger.io/?url=https://raw.githubusercontent.com/senzing-garage/senzing-rest-api-specification/3.0.0/senzing-rest-api.yaml
[Version 3.1.0]: https://petstore.swagger.io/?url=https://raw.githubusercontent.com/senzing-garage/senzing-rest-api-specification/3.1.0/senzing-rest-api.yaml
