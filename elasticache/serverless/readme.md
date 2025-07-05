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

## Create an Ec2 instance in the same VPC to access redis cache

from cfn template,

```sh
aws cloudformation deploy \
--template-file template.yaml \
--no-execute-changeset \
--region ap-south-1 \
--stack-name redis-client-ec2 \
--capabilities CAPABILITY_NAMED_IAM

aws cloudformation execute-change-set \
--change-set-name arn:aws:cloudformation:ap-south-1:647264525674:changeSet/awscli-cloudformation-package-deploy-1751743307/033066fa-251f-4108-967f-c9b4c78ab793 \
--stack-name redis-client-ec2
```

Or run deploy command without the '--no-execute-changeset' if reviewing the change set is not needed

## Connect to the elasticache redis cache server from EC2

from SSM session manager,

```sh
redis-cli -h <endpoint-host> --tls
```

once connected to redis, you can set key/value pairs as,

```sh
set <key> <value>
```

and to view the data,

```sh
get <key>
```

**It's required to use --tls since the cache has encryption in transit enabled**

**To use TLS, the redis client version that you install should support tls (The one from redis official page works: https://redis.io/docs/latest/operate/oss_and_stack/install/archive/install-redis/install-redis-on-linux/)**

