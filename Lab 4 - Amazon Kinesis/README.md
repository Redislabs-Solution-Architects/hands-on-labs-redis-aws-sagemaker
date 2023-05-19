# Amazon Kinesis

In this lab, you are going to :
* Configure Amazon Kinesis Data stream, to capture the real-time financial transactions from end-users.
* Configure Amazon Kinesis data stream to trigger AWS lambda function, to invoke fraud detection.



## Configure Amazon Kinesis Data Stream

1. Start by searching for `Kinesis` in your AWS Web console

![](images/01-kinesis.png)

2. Click on `Create data stream`

![](images/02-kinesis.png)

3. Create data stream by giving it a name : `demo-stream`.
Choose capcity mode as `On-Demand`.

![](images/03-kinesis.png)

4. Go ahead and create the datastream.

![](images/04-kinesis.png)

5. After you successfully created the data stream, you will see a successful message.

![](images/05-kinesis.png)

## Configure Lambda Trigger

1. Navigate back yourself to the `Lambda` ==> `Functions` ==>  `aws-redis-fraud-detection-processor`. Click on the `Add trigger`

![](images/01-trigger.png)

2. Search for `Kinesis`

![](images/02-trigger.png)

3. Search for your data stream and select `demo-stream`

![](images/03-trigger.png)

4. Setup the batch size as 1 instead of 100, just to simulate kinesis reading one transaction at a time.

![](images/04-trigger.png)

5. Sometimes, if you do not have enough previleges, you may encounter an error like this.
```
An error occurred when creating the trigger: Cannot access stream arn:aws:kinesis:us-west-2:016366241477:stream/demo-stream. Please ensure the role can perform the GetRecords, GetShardIterator, DescribeStream, ListShards, and ListStreams Actions on your stream in IAM.
```

![](images/05-trigger.png)

6. To resolve this error, navigate back to your lambda function ( `Lambda` ==> `Functions` ==> `aws-redis-fraud-detection-processor`). Click on the `Configuration` tab.

![](images/06-trigger.png)

7. Click on `Permissions` and click on the `Role name` that will open the `Role` properties page in a seperate window.

![](images/07-trigger.png)

8. Here, go ahead and add permissions.

![](images/08-trigger.png)

9. Search for `Kinesis` and add `AmazonKinesisFullAccess` permission.

![](images/09-trigger.png)

10. Click on `Add permissions`

![](images/10-trigger.png)

11. Similarly, search for `Cloudwatch` and add `CloudWatchFullAccess` permission

![](images/11-trigger.png)

12. After adding these two permissions, your `Permission policies` for your lambda role should have these permissions added.

![](images/12-trigger.png)

13. Now go back to your Lambda function and try adding the trigger again, by clicking on the `Add trigger` button.

![](images/13-trigger.png)

14. Go ahead and configure Kinesis as the trigger with batch size = `1` and `Latest` as the starting position

![](images/14-trigger.png)

15. If everything goes well, your trigger is configured successfully as shown below.

![](images/15-trigger.png)

## Conclusion
In summary, you have done the following things in this lab:
* You have configured `Amazon Kinesis Data stream`, to capture the real-time financial transactions from end-users.
* You have configurde `Amazon Kinesis data stream` to trigger `AWS lambda` function, to invoke fraud detection.

See you in the next lab.  [Go back](..)
