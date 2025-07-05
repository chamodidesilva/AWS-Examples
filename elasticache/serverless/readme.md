## Create serverless cache

```sh
aws elasticache create-serverless-cache --serverless-cache-name my-cache-test-66554 --engine redis
```

## Install redis client

```sh
sudo apt install redis-tools -y
```

## Try to connect to the elasticache redis server endpoint

```sh
redis-cli my-cache-test-66554-iaex1a.serverless.aps1.cache.amazonaws.com:6379
```

Cannot do so since I'm not in the same VPC as the redis server



