# Rekognition
This application was created in Beck Et Al Brazil using an AWS Deeplens

<h4>Preparation</h4>
<ul>
  <li>Create a bucket in S3 with "Block all public access" unchecked;</li>
  <li>Create a collection Faces in the Rekognition service. <a href='https://docs.aws.amazon.com/rekognition/latest/dg/create-collection-procedure.html' target='_blank'>Documentation</a>;</li>
  <li>Create a app with a bot in Slack and save the Bot User OAuth Access Token. <a href='https://slack.com/intl/pt-br/help/articles/115005265703-criar-um-bot-para-o-workspace' target='_blank'>Documentation</a>;</li>
  <li>Create a Lambda Function with a trigger in your bucket. Set the prefix with "images/" and the sufix with ".jpg";</li>
  <li>Upload the function.zip to the Lambda Function;</li>
  <li>Add the Slack Token, Slack Channel, name of the bucket and the collection Id the variables of the code;</li>
  <li>Save and add a jpg file in the folder images of your bucket. This will create a table in DynamoDB;</li>
  <li>Comment the line 33 (return createTable()) and add a jpg file again;</li>
</ul>

