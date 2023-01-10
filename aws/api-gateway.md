# Amazon Web Services: API Gateway

## Make Changes to an API

After making any changes to an API Gateway, you must redeploy the gateway for changes to take effect by following the [same steps as deploying](https://docs.aws.amazon.com/apigateway/latest/developerguide/how-to-deploy-api-with-console.html#how-to-deploy-api-console).

## Restrict Access

Configure allowed/denied entities using [Resource Policies](https://aws.amazon.com/premiumsupport/knowledge-center/api-gateway-resource-policy-access/). See [sample resource policies here](https://docs.aws.amazon.com/apigateway/latest/developerguide/apigateway-resource-policies-examples.html).

You may need to switch the authorization to IAM.

Examples:
