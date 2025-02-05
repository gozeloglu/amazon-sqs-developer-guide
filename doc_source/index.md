# Amazon Simple Queue Service Developer Guide

-----
*****Copyright &copy; Amazon Web Services, Inc. and/or its affiliates. All rights reserved.*****

-----
Amazon's trademarks and trade dress may not be used in 
     connection with any product or service that is not Amazon's, 
     in any manner that is likely to cause confusion among customers, 
     or in any manner that disparages or discredits Amazon. All other 
     trademarks not owned by Amazon are the property of their respective
     owners, who may or may not be affiliated with, connected to, or 
     sponsored by Amazon.

-----
## Contents
+ [What is Amazon Simple Queue Service?](welcome.md)
+ [Setting up Amazon SQS](sqs-setting-up.md)
+ [Getting started with Amazon SQS](sqs-getting-started.md)
+ [Configuring Amazon SQS queues (console)](sqs-configuring.md)
   + [Creating an Amazon SQS queue (console)](sqs-configure-create-queue.md)
   + [Editing an Amazon SQS queue (console)](sqs-configure-edit-queue.md)
   + [Configuring queue parameters (console)](sqs-configure-queue-parameters.md)
   + [Configuring access policy (console)](sqs-configure-add-permissions.md)
   + [Configuring server-side encryption (SSE) for a queue using SQS-owned encryption keys (console)](sqs-configure-sqs-sse-queue.md)
   + [Configuring server-side encryption (SSE) for a queue (console)](sqs-configure-sse-existing-queue.md)
   + [Configuring a dead-letter queue (console)](sqs-configure-dead-letter-queue.md)
   + [Configuring a dead-letter queue redrive (console)](sqs-configure-dead-letter-queue-redrive.md)
   + [Configuring cost allocation tags for an Amazon SQS queue (console)](sqs-configure-tag-queue.md)
   + [Subscribing an Amazon SQS queue to an Amazon SNS topic (console)](sqs-configure-subscribe-queue-sns-topic.md)
   + [Configuring a queue to trigger an AWS Lambda function (console)](sqs-configure-lambda-function-trigger.md)
+ [Managing Amazon SQS queues (console)](sqs-using-sqs.md)
   + [Sending messages to a queue (console)](sqs-using-send-messages.md)
   + [Sending a message with attributes (console)](sqs-using-send-message-with-attributes.md)
   + [Receiving and deleting messages (console)](sqs-using-receive-delete-message.md)
   + [Purging messages from an Amazon SQS queue (console)](sqs-using-purge-queue.md)
   + [Deleting an Amazon SQS queue](sqs-using-delete-queue.md)
   + [Confirming that a queue is empty](confirm-queue-is-empty.md)
+ [How Amazon SQS works](sqs-how-it-works.md)
   + [Basic Amazon SQS architecture](sqs-basic-architecture.md)
   + [Amazon SQS Standard queues](standard-queues.md)
   + [Amazon SQS FIFO (First-In-First-Out) queues](FIFO-queues.md)
      + [Message ordering](FIFO-queues-message-order.md)
      + [Key terms](FIFO-key-terms.md)
      + [FIFO delivery logic](FIFO-queues-understanding-logic.md)
      + [Exactly-once processing](FIFO-queues-exactly-once-processing.md)
      + [Moving from a standard queue to a FIFO queue](FIFO-queues-moving.md)
      + [High throughput for FIFO queues](high-throughput-fifo.md)
         + [Partitions and data distribution for high throughput for SQS FIFO queues](partitions-and-data-distribution.md)
      + [Compatibility](FIFO-compatibility.md)
   + [Amazon SQS queue and message identifiers](sqs-queue-message-identifiers.md)
   + [Message metadata](sqs-message-metadata.md)
   + [Resources required to process Amazon SQS messages](sqs-resources-required-process-messages.md)
   + [List queue pagination](list-all-queues-pagination.md)
   + [Amazon SQS cost allocation tags](sqs-queue-tags.md)
   + [Amazon SQS short and long polling](sqs-short-and-long-polling.md)
   + [Amazon SQS dead-letter queues](sqs-dead-letter-queues.md)
   + [Amazon SQS visibility timeout](sqs-visibility-timeout.md)
   + [Amazon SQS delay queues](sqs-delay-queues.md)
   + [Amazon SQS temporary queues](sqs-temporary-queues.md)
   + [Amazon SQS message timers](sqs-message-timers.md)
+ [Best practices for Amazon SQS](sqs-best-practices.md)
   + [Recommendations for Amazon SQS standard and FIFO queues](sqs-standard-fifo-queue-best-practices.md)
      + [Working with Amazon SQS messages](working-with-messages.md)
      + [Reducing Amazon SQS costs](reducing-costs.md)
      + [Moving from an Amazon SQS Standard queue to a FIFO queue](moving-from-high-throughout-queue-to-FIFO-queue.md)
   + [Additional recommendations for Amazon SQS FIFO queues](sqs-additional-fifo-queue-recommendations.md)
      + [Using the Amazon SQS message deduplication ID](using-messagededuplicationid-property.md)
      + [Using the Amazon SQS message group ID](using-messagegroupid-property.md)
      + [Using the Amazon SQS receive request attempt ID](using-receiverequestattemptid-request-parameter.md)
+ [Amazon SQS Java SDK examples](sqs-java-tutorials.md)
   + [Using server-side encryption (SSE)](sqs-java-configure-sse.md)
   + [Configuring tags for a queue](sqs-java-add-update-remove-tag-queue.md)
   + [Sending message attributes](sqs-java-send-message-with-attributes.md)
   + [Managing large Amazon SQS messages using Amazon S3](sqs-s3-messages.md)
+ [Working with JMS and Amazon SQS](sqs-java-message-service-jms-client.md)
   + [Prerequisites](prerequisites.md)
   + [Getting started with the Amazon SQS Java Messaging Library](getting-started.md)
   + [Using the Amazon SQS Java Message Service (JMS) Client with other Amazon SQS clients](sqs-jms-client-with-sqs-clients.md)
   + [Working Java example for using JMS with Amazon SQS Standard queues](sqs-jms-code-examples.md)
   + [Supported JMS 1.1 implementations](supported-implementations.md)
+ [Amazon SQS tutorials](sqs-other-tutorials.md)
   + [Creating an Amazon SQS queue (AWS CloudFormation)](create-queue-cloudformation.md)
   + [Tutorial: Sending a message to an Amazon SQS queue from Amazon Virtual Private Cloud](sqs-sending-messages-from-vpc.md)
+ [Amazon SQS quotas](sqs-quotas.md)
   + [Quotas related to queues](quotas-queues.md)
   + [Quotas related to messages](quotas-messages.md)
   + [Quotas related to policies](quotas-policies.md)
+ [Automating and troubleshooting Amazon SQS queues](sqs-automating-troubleshooting.md)
   + [Automating notifications from AWS services to Amazon SQS using Amazon EventBridge](sqs-automating-using-eventbridge.md)
   + [Troubleshooting Amazon Simple Queue Service queues using AWS X-Ray](sqs-troubleshooting-using-x-ray.md)
+ [Security in Amazon SQS](sqs-security.md)
   + [Data protection](sqs-data-protection.md)
      + [Data encryption](sqs-data-encryption.md)
         + [Encryption at rest](sqs-server-side-encryption.md)
         + [Key management](sqs-key-management.md)
      + [Internetwork traffic privacy](sqs-internetwork-traffic-privacy.md)
   + [Identity and access management in Amazon SQS](sqs-authentication-and-access-control.md)
      + [Overview of managing access in Amazon SQS](sqs-overview-of-managing-access.md)
      + [Using identity-based policies with Amazon SQS](sqs-using-identity-based-policies.md)
         + [AWS managed (predefined) policies for Amazon SQS](sqs-access-policy-aws-managed-policies.md)
         + [Basic examples of IAM policies for Amazon SQS](sqs-basic-examples-of-iam-policies.md)
         + [Basic examples of Amazon SQS policies](sqs-basic-examples-of-sqs-policies.md)
      + [Using custom policies with the Amazon SQS Access Policy Language](sqs-creating-custom-policies.md)
         + [Amazon SQS access control architecture](sqs-creating-custom-policies-architecture.md)
         + [Amazon SQS access control process workflow](sqs-creating-custom-policies-process-workflow.md)
         + [Amazon SQS Access Policy Language key concepts](sqs-creating-custom-policies-key-concepts.md)
         + [Amazon SQS Access Policy Language evaluation logic](sqs-creating-custom-policies-evaluation-logic.md)
         + [Relationships between explicit and default denials in the Amazon SQS Access Policy Language](sqs-creating-custom-policies-relationships-between-explicit-default-denials.md)
         + [Custom Amazon SQS Access Policy Language examples](sqs-creating-custom-policies-access-policy-examples.md)
      + [Using temporary security credentials with Amazon SQS](sqs-using-temporary-security-credentials.md)
      + [Amazon SQS API permissions: Actions and resource reference](sqs-api-permissions-reference.md)
   + [Logging and monitoring in Amazon SQS](sqs-logging-monitoring.md)
      + [Logging Amazon SQS API calls using AWS CloudTrail](sqs-logging-using-cloudtrail.md)
      + [Monitoring Amazon SQS queues using CloudWatch](sqs-monitoring-using-cloudwatch.md)
         + [Accessing CloudWatch metrics for Amazon SQS](sqs-access-metrics.md)
         + [Creating CloudWatch alarms for Amazon SQS metrics](set-cloudwatch-alarms-for-metrics.md)
         + [Available CloudWatch metrics for Amazon SQS](sqs-available-cloudwatch-metrics.md)
   + [Compliance validation for Amazon SQS](sqs-compliance-validation.md)
   + [Resilience in Amazon SQS](sqs-resilience.md)
   + [Infrastructure security in Amazon SQS](sqs-infrastructure-security.md)
   + [Amazon SQS security best practices](sqs-security-best-practices.md)
+ [Working with Amazon SQS APIs](sqs-working-with-apis.md)
   + [Making Query API requests](sqs-making-api-requests.md)
      + [Authenticating requests](sqs-api-request-authentication.md)
      + [Interpreting responses](sqs-api-responses.md)
   + [Amazon SQS batch actions](sqs-batch-api-actions.md)
      + [Enabling client-side buffering and request batching](sqs-client-side-buffering-request-batching.md)
      + [Increasing throughput using horizontal scaling and action batching](sqs-throughput-horizontal-scaling-and-batching.md)
+ [Related Amazon SQS resources](related-resources.md)
+ [Documentation history](sqs-release-notes.md)
+ [AWS glossary](glossary.md)