# Deploy Command

## lambda-golang-cf-template.json

```
# Upload lambda execution file to S3 bucket
aws cloudformation package \
    --use-json \ 
    --template-file lambda-golang-cf-template.json \
    --s3-bucket cf-template-bucket-xxxxx \
    --output-template-file outputed-template.json \
    --profile xxxxxx

# Deploy lambda function
aws cloudformation deploy \
    --template-file outputed-template.json \
    --stack-name lambda-xxxxx-stack \
    --capabilities CAPABILITY_NAMED_IAM \
    --parameter-overrides LambdaFunctionName=lambda-golang-api \
    --profile xxxxxx
```