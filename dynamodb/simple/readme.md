https://docs.aws.amazon.com/serverless-application-model/latest/developerguide/sam-resource-simpletable.html#sam-resource-simpletable--examples

## Build template

```sh
sam build
```

## Deploy Table

```sh
sam deploy \
--template-file template.yaml \
--stack-name "my-simple-table" \
--resolve-s3 \
--region ap-south-1 \
--no-confirm-changeset \
--no-fail-on-empty-changeset
```

## Insert items

```sh
aws dynamodb put-item \
--table-name my-simple-table-MyDynamoDBTable-J18X5G98JVAL \
--item file://item.json \
--return-consumed-capacity TOTAL \
--return-item-collection-metrics SIZE
```