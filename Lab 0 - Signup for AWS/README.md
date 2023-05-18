# Lab 0 - Signup for AWS
To begin, it is essential to have an AWS account.

If you already possess an AWS account, it is possible that you can utilize it. However, certain permissions are required, enabling you to deploy a SageMaker domain and run SageMaker Notebooks. If your current access fulfills these prerequisites, you may proceed to omit the "Signup for AWS" section of this lab and proceed straight to "IAM Permissions Setup"

## Feedback
As you progress through these labs, we highly value your feedback. To assist us in enhancing our offerings, we encourage you to provide your insights by opening an issue using the following link: [here](https://github.com/Redislabs-Solution-Architects/hands-on-labs-redis-aws-sagemaker/issues).

We genuinely appreciate any input you can provide, whether it is regarding any identified bugs, suggestions to improve usability, or general comments. We also welcome pull requests if you wish to contribute directly to the project.

## Signup for AWS
If you haven't registered for an account yet, please visit [here](https://aws.amazon.com/) to initiate the signup process.

During the registration, you will be required to provide your phone number and credit card details. The overall expenses for the lab are expected to remain below $50. However, it's worth noting that AWS is offering a credit specifically for lab participants, which will more than offset these costs.

At the conclusion of the lab, we will guide you through the process of deleting any resources you have deployed, ensuring proper resource management.

Start by clicking on "Create an AWS Account" in the upper right corner.

![](images/01-signup.png)

Please enter an email address and a name for the account.

![](images/02-signup.png)

Please kindly check your email and enter the code to verify your account.

![](images/03-verify.png)

Its time now to set a password.

![](images/04-password.png)

Select "Personal" for the account type and fill out the form.  Review and accept the terms.  Then click "Continue."

![](images/05-signup.png)

Enter a credit card.  Note that this card will only be charged if you exceed the credits provided for this lab.  Nothing we're doing in this lab would exceed those credits.  We're going to deploy the SageMaker cloud resources in this AWS account.  The IaaS charges for that will total a few dollars for the duration of the lab.  All the other resources we're using will be provisioned for you by Redis Inc.

After you finishing working with all of the labs, you can follow the instructions in "Cleanup" lab to turn off the resources you deployed and still you'll be left with some credits in your account that you can use to get your hands more dirty on the AWS technologies.

![](images/06-card.png)

Now enter your phone number to receive a verification code.

![](images/07-phone.png)

Enter the verification code that was texted to you.  Click "Continue."

![](images/08-verify.png)

Select "Basic Support - Free" and click "Complete sign up."

![](images/09-support.png)

Congratulations!  You've just signed up for an AWS account.  Click "Go to the AWS Management Console."

![](images/10-complete.png)

## Login
Enter the email address you provided during signup to login to your new AWS account.

![](images/11-login.png)

Enter the password you provided during signup and click "Sign in."

![](images/12-login.png)

Complete the captcha and click "Submit."

![](images/13-login.png)

Click "Switch to new Console Home" to use the latest console.

![](images/14-console.png)

You're now in the console!  Click next to move through the tutorial.

![](images/15-console.png)

Click "Done" to dismiss the tutorial.

![](images/16-console.png)

Click the "X" in the upper right to dismiss the help menu.

![](images/17-console.png)

Click "X" again to dismiss another help menu.

![](images/18-console.png)

You're now all logged in to your environment and ready to use it.

![](images/19-console.png)

## Apply AWS Credits
As an integral component of the labs, AWS is generously offering credits that surpass the expenses incurred from utilizing resources throughout this lab. You can conveniently apply these credits to your account by navigating [here](https://console.aws.amazon.com/billing/home?#/credits)

Once there, click on "Redeem credit."

![](images/20-credit.png)

You'll then need to enter the code for the credit and answer the captcha.  With that complete, click "Redeem credit."

![](images/21-redeem.png)

## IAM Permissions Setup

<center><img src="images/IAM-1.png" width="261" height="260"></center>


If you are bringing your AWS account with Root access, you do not need to setup any additional IAM policies.
However ever, if you are going to use an IAM user, then you need to set the following privileges for your IAM user.
* AdministratorAccess
* AmazonEC2FullAccess
* AmazonElasticContainerRegistryPublicFullAccess
* CloudWatchFullAccess
* IAMUserChangePassword
* PowerUserAccess
* AWSCloudFormationFullAccess

Here is how you will add these policies to your IAM user.
<TBD>
