Running the S3_SimpleDB_SNS_SQS_DemoTVMIdentity Sample
======================================================
This sample demonstrates interaction with a <a href="http://aws.amazon.com/articles/4611615499399490">Token Vending Machine</a> where a username/password combination is required, the <a href="http://aws.amazon.com/code/7351543942956566">IdentityTVM</a>.  The IdentityTVM requires the user to register with the App by first connecting to an external website and provide a username and password.  The username and username will then be required to log into the sample App.  In this sample the registration website is a specific page on the IdentityTVM.  

It is assumed that you were able to previously run the S3_SimpleDB_SNS_SQS_Demo sample.  Also, you need to be running an 
IdentityTVM which this sample App will connect to.  

To run this specific sample you will need to do the following:

1. Import the project into Eclipse 
   * Go to File -> Import.  Import Wizard will open.
   * Select General -> Existing Projects into Workspace.  Click Next.
   * In Select root directory, browse to samples directory.  List of all samples projects will appear.
   * Select the projects you want to import
   * Click Finish.

2. Add the AWS SDK for Android jar file to your project:
   * Right-click on the Project and select Build Path -> Configure Build Path...
   * Click on the Libraries tab.
   * Click Add External JARs...
   * Navigate to the location where you downloaded the AWS SDK for Android and go into the lib directory.
   * Select aws-android-sdk-X.X.X-debug.jar and press Open.
   * Click on the Order and Export tab.
   * Make sure that the aws-android-sdk-X.X.X-debug.jar is checked and press OK.

3. Update your App configuration:
   * Open the AwsCredential.properties file located in src/com/amazonaws/demo/identity.
   * Edit the file and provide:
     + The DNS domain name where your Token Vending Machine is running (ex: tvm.elasticbeanstalk.com)
     + The App Name you configured your Token Vending Machine with (ex: MyMobileAppName)
     + Set useSSL to "true" or "false" based on whether your configured your Token Vending Machine with SSL or not.

4. Run the project:
   * Go to Project ->  Clean.
   * Go to Project ->  Build All.
   * Go to Run -> Run.
