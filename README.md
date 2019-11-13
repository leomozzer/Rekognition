# Rekognition
This application was created in Beck Et Al Brazil using an AWS Deeplens.
<b>It is not necessary to use a Deeplens. This function will run every time that a jpg file is added in the bucket </b>

<h4>Preparation</h4>
<ul>
  <li>Create a bucket in S3 with "Block all public access" unchecked;</li>
  <li>In the IAM page, create a function with FullAccess and an user with FullAccess permissions;</li>
  <li>Use the CLI to create a collection Faces in the Rekognition service. <a href='https://docs.aws.amazon.com/rekognition/latest/dg/create-collection-procedure.html' target='_blank'>Documentation</a>;</li>
  <li>Create a app with a bot in Slack and save the Bot User OAuth Access Token. <a href='https://slack.com/intl/pt-br/help/articles/115005265703-criar-um-bot-para-o-workspace' target='_blank'>Documentation</a>;</li>
  <li>Create a Lambda Function with a trigger in your bucket. Set the prefix with "images/" and the sufix with ".jpg";</li>
  <li>Upload the function.zip to the Lambda Function;</li>
  <li>Add the Slack Token, Slack Channel, name of the bucket and the collection Id in the variables of the code;</li>
  <li>Save and add a jpg file in the folder images of your bucket. This will create a table in DynamoDB;</li>
  <li>Comment the line 33 (return createTable()) and add a jpg file again;</li>
</ul>

<h4>Todo</h4>
<ul>
  <li>Create a table in DynamoDB automatically</li>
  <li>Create the Face colletion automatically</li>
</ul>

<h4>References</h4>
<ul>
  <li>Track the number of cofffes consumed. <a href='https://aws.amazon.com/pt/blogs/machine-learning/track-the-number-of-coffees-consumed-using-aws-deeplens/'>Link</a>;</li>
  <li>Doorman. <a href='https://aws.amazon.com/pt/deeplens/community-projects/Doorman/'>Link</a>;</li>
  <li>Python and DynamoDB. <a href='https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/GettingStarted.Python.html'>Link</a>;</li>
  <li>Rekognition Service. <a href='https://docs.aws.amazon.com/rekognition/latest/dg/collections.html'>Link</a>;</li>
</ul>
