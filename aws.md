# AWS

Useful links and documents

#### AWS Articles

[Amazon Web Services In Plain English](https://expeditedsecurity.com/aws-in-plain-english/)

[Demystifying your AWS Certification exam score](https://aws.amazon.com/blogs/training-and-certification/demystifying-your-aws-certification-exam-score/)

#### IAM

[How can I grant my Amazon EC2 instance access to an Amazon S3 bucket in another AWS account?](https://aws.amazon.com/de/premiumsupport/knowledge-center/s3-instance-access-bucket/)

#### SQS

[Amazon SQS dead-letter queues](https://docs.aws.amazon.com/AWSSimpleQueueService/latest/SQSDeveloperGuide/sqs-dead-letter-queues.html/)


[Amazon SQS dead-letter queues](https://stackoverflow.com/questions/23260024/how-to-prevent-duplicate-sqs-messages)

#### S3 Events

[Configuring Amazon S3 event notifications](https://docs.aws.amazon.com/AmazonS3/latest/dev/NotificationHowTo.html/)

#### Athena

Athena Views in Terraform - https://stackoverflow.com/questions/56289272/create-aws-athena-view-programmatically/58370023#58370023

#### CloudWatch

CW Insights

```sh
fields  @message
| filter @message like /tigeroscar/
| limit 10
```