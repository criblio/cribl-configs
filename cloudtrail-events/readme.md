These configs support the blog post here:  
http://blog.cribl.io/2019/04/16/threat-hunting-while-staying-compliant-categorizing-and-scoring-aws-cloudtrail-events-in-real-time

To apply confgurations please follow these steps
------------------------------------------------

* Have a running instance of Cribl in your environment.

* Use the Cribl S3 Log Collector serverless app to collect CloudTrail data from your S3 bucket: 
    * Serverless App: https://serverlessrepo.aws.amazon.com/applications/arn:aws:serverlessrepo:us-east-1:496698360409:applications~Cribl-S3-Log-Collector
    * Blog post guide about the serverless app: https://blog.cribl.io/2018/11/27/serverless-data-forwarding-to-cribl-for-aws-services/
    * Alternatively use the Lambda function here: https://github.com/criblio/cribl-integrations/tree/master/aws/src/lambda/S3EventsToCribl

* Create an empty pipeline. 
    * Go to Advanced Mode and paste the content of cloudtrail_events_pipeline.json

* Create a lookup table and upload cloudtrail_events.csv.
* Attach the pipeline to a Route.


References:
* Cribl docs: https://docs.cribl.io
* Join us in Slack #cribl: https://cribl.io/community
* Tweet at us @cribl_io: https://twitter.com/cribl_io
