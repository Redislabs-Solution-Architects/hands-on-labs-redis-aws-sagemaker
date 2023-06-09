# Lab 01 - Building Fraud Detection using Amazon SageMaker
Are you ready to get into action?
So, here is what you are going to build.

Duration: 30 mins

## Architecture Overview
We are going to build a Real-time Fraud detection system leveraging both Redis and AWS technologies.
Here is a quick overview of the system.

[Demo - Real-time Fraud Detection ](https://docs.google.com/presentation/d/1h6GrhdR6_Dt-NP9BEcea5mlGtYE4Atk1QlBvCMu1WCA/edit#slide=id.g24608284783_0_1198) (2 min)

And here is the Solution Architecture.

![](images/01-arch-overview.png)

We are going to start with provisioning cloud resources needed to do the rest of the labs.
In this lab, you will build the Jupyter Notebooks needed to run SageMaker models.

![](images/WhereAmI-Lab1.png)

## Cloud Formation Template

You will find a CloudFormation template [here](https://github.com/Redislabs-Solution-Architects/aws-fraud-detection/blob/main/aws/sagemaker/fraud-detection-using-machine-learning.template).  We will use this to create a Cloud Formation stack in AWS.

1. Download the [CloudFormation template](https://github.com/Redislabs-Solution-Architects/aws-fraud-detection/blob/main/aws/sagemaker/fraud-detection-using-machine-learning.template) to your local desktop/Mac, by clicking on the download button shown here.
![](images/02-download-cf-template.png)


2. In the AWS console, select CloudFormation service.

![](images/03-cloudformation.png)

3. Click create stack

![](images/04-create-stack.png)

4. Upload the template from step#1 from your local machine.

![](images/05-create-stack.png)

![](images/06-create-stack.png)

Click next

![](images/07-create-stack.png)

5. Give stack a name. Also configure the Amazon S3 bucket names, as shown below.
> NOTE:S3 Bucket name must be globally unique and must not contain spaces or uppercase letters. Hence, give it a unique name like : lastname-{random-4-digit-number}.
Example: fowler-3245-model-bucket , fowler-3245-results-bucket

![](images/08-create-stack.png)

6. Ensure Rollback is selected.

![](images/09-create-stack.png)

7. And then click Next

![](images/10-create-stack.png)

You may have to acknowledge the following prompt and continue by clikcing `submit` button
![](images/10b-create-stack.png)

8. CloudFormation stack gets kicked-off with the status = `CREATE_IN_PROGRESS`

![](images/11-create-stack.png)

9. Let this run for 5 mins or so. While the cloud resources creation is in progress, you can click on the `Resources` tab to see Cloud resources being provisioned in real time.

![](images/12-create-stack.png)

10. Switch to `Stack info` tab and wait for the stack creation to complete.

![](images/13-create-stack.png)

11. Now its complete.

![](images/14-create-stack.png)

12. If you switch back to the `Resources` tab, you will see all of the cloud resources that were provisioned.

![](images/15-create-stack-status.png)

13. In the AWS web console, search for `SageMaker` and right click in the results to open `SageMaker` in a new window.

![](images/16-sagemaker.png)

14. Navigate yourself to `Amazon SageMaker` ==> `Notebook Instances`. Click on the notebook that got provisioned with your CloudFormation template.

![](images/17-sagemaker.png)

15. Open the Python Jupyter Lab. This will open in a new tab.

![](images/18-sagemaker.png)

16. Now you have just now launched a Python Jupyter Lab. In the left hand navigation bar, you will see the Jupyter Notebook. Please double click on it to open it.

![](images/19-sagemaker.png)

17. This opens up Jupyter Notebook in the right hand side main window. Each cell highlighted has a python code that will be executed when you press `COMMAND` + `ENTER` on a Mac OR `Cntrl` + `ENTER` on a Window's machine.

![](images/20-sagemaker.png)

You are now ready to run the Amazon SageMaker Notebook. You will create the following cloud resources, when you do so:

* Model training jobs for Random Cut Forest & XGBoost algorithms
* Deployed Model endpoint configurations and Model endpoints
* S3 buckets that has the input and output buckets with trained data and results

See you in the next lab.  [Go back](..)

## Quick Note on Redis Enterprise Cloud Deployment
If you are running this lab as a part of an Immersion Day or a Webinar run by AWS or Redis Inc, you will be provided with the Redis Database endpoints information. Simply ask your Instructor.

If you are running these labs on your own and if you are deploying your own instance of the Redis Enterprise Cloud database, please use the following configurations for the database.

* Database size: 1GB
* Modules: RedisJSON, RediSearch, RedisTimeseries
* No HA needed as this is not a production workload.
* No Replication needed as this is not a production workload.

Make sure to clean up the cloud resources after you are done with these labs.
