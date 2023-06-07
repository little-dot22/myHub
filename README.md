# myHub

docker run --rm -v "${PWD}:/local" openapitools/openapi-generator-cli generate -i /local/api/openapi.yaml -g grpc-go -o /local/idl