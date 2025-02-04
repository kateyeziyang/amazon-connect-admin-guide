# Flow block: Invoke AWS Lambda function<a name="invoke-lambda-function-block"></a>

## Description<a name="invoke-lambda-function-block-description"></a>
+ Calls AWS Lambda, and optionally returns key\-value pairs\.
+ The returned key\-value pairs can be used to set contact attributes\.
+ For an example, see [Tutorial: Create a Lambda function and invoke in a flow](connect-lambda-functions.md#tutorial-invokelambda)\.

## Supported channels<a name="invoke-lambda-channels"></a>

The following table lists how this block routes a contact who is using the specified channel\. 


| Channel | Supported? | 
| --- | --- | 
| Voice | Yes | 
| Chat | Yes | 
| Task | Yes | 

## Flow types<a name="invoke-lambda-function-block-types"></a>

You can use this block in the following [contact flow types](create-contact-flow.md#contact-flow-types):
+ Inbound flow
+ Customer Queue flow
+ Customer Hold flow
+ Customer Whisper flow
+ Agent Hold flow
+ Agent Whisper flow
+ Transfer to Agent flow 
+ Transfer to Queue flow

## Properties<a name="invoke-lambda-function-block-properties"></a>

![\[Image NOT FOUND\]](http://docs.aws.amazon.com/connect/latest/adminguide/images/invoke-lambda-properties.png)

Note the following properties: 
+ **Timeout**: Enter how long to wait for Lambda to time out\. 

  If your Lambda invocation gets throttled, the request is retried\. It is also retried if a general service failure \(500 error\) happens\. 

  When a synchronous invocation returns an error, Amazon Connect retries up to three times, for a maximum of 8 seconds\. At that point, the contact is routed down the **Error** branch\.

## Configuration tips<a name="invoke-lambda-function-block-tips"></a>
+ To use an AWS Lambda function in a flow, first add the function to your instance\. For more information, see [Add a Lambda function to your Amazon Connect instance](connect-lambda-functions.md#add-lambda-function), 
+ After you add the function to your instance, you can select the function from the **Select a function** drop\-down list in the block to use it in the flow\.

## Configured block<a name="invoke-lambda-function-block-configured"></a>

When this block is configured, it looks similar to the following image:

![\[Image NOT FOUND\]](http://docs.aws.amazon.com/connect/latest/adminguide/images/invoke-lambda-configured.png)

## Sample flows<a name="invoke-lambda-function-block-samples"></a>

[Sample Lambda integration](sample-lambda-integration.md)

## Scenarios<a name="invoke-lambda-function-block-scenarios"></a>

See these topics for scenarios that use this block:
+ [Invoke AWS Lambda functions](connect-lambda-functions.md)