These configs support the blog post here: 
<url>


To apply confgurations please follow these steps
------------------------------------------------

* Have a running instance of Cribl with the following outputs configured per your environment:
    * Splunk: Output Name "default"
    * S3: Output Name "Web Access Logs To S3"
* Create an empty pipeline destined for S3. 
    * In Advanced Mode paste the content of weblogs-pipeline-to-s3.json
* Create an empty pipeline destined for Splunk. 
    * In Advanced Mode paste the content of weblogs-pipeline-to-splunk.json
* If your Routes are empty then use routes.json as is.
    * If you have own routes then add only the two routes from routes.json at the top