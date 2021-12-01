# Deploy Command

## s3-private-bucket-cf-template.json

```
aws cloudformation deploy \
    --template-file s3-private-bucket-cf-template.json \
    --stack-name s3bucket-xxxxx-stack \
    --parameter-overrides BucketName=cf-template-bucket-xxxxx \
    --profile xxxxxx
```