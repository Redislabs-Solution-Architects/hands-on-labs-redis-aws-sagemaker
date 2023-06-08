# Lab 07 - Cleanup

Duration: 15 mins

We deployed a lot of resources in these labs.  Clearly, you want to make sure they don't run up a bill from unused AWS resources.  This lab will help you clean up the resources you provisioned.



## The Nuclear Option
If you really want to stop AWS billing, close your AWS account.  If you've already stopped your active VMs and other cloud resources, you could still close your account to make very sure no additional charges are incurred.  Alternatively, in the rest of the lab, we'll walk through options that will allow you to continue to experiment and play with AWS.  But, if you prefer the nuclear approach, follow the instructions [here](https://aws.amazon.com/premiumsupport/knowledge-center/close-aws-account/).



# Cleaning up the resources

1.Go to `CloudFormation` service.

![](images/01-cleanup.png)

2. Delete it.
![](images/02-cleanup.png)

3. Delete the stack.
![](images/03-cleanup.png)

4. Delete initiated message confirms the process.

![](images/04-cleanup.png)

5. You can check in the `Resources` tab to ensure all cloud resources are deleted.
![](images/05-cleanup.png)

6. `Stack Info` tab indicates the status. In this case, its `DELETE_IN_PROGRESS`

![](images/06-cleanup.png)

7. At times, you may encounter `DELETE_FAILED`. In that case, go to `Resources`

![](images/07-cleanup.png)

8. Identify the failed resource. IN this case, it seems to be an S3 bucket. You can click on the link to open the page in a different window.

![](images/08-cleanup.png)
9. You see an S3 bucket with contents in it. Click on this resource to see the contents inside the object.
![](images/09-cleanup.png)

10. Select all these objects and click Delete button to delete these resources.
![](images/10-cleanup.png)

11. Confirm deletion and delete the objects.
![](images/11-cleanup.png)

12. Upon successful confirmationn, close this screen and go back to the bucket.

![](images/12-cleanup.png)

13. Go further one level up.
![](images/13-cleanup.png)

14. Now select this bucket and click on `Delete` button.

![](images/14-cleanup.png)

15. Confirm deletion.
![](images/15-cleanup.png)

16. Now go back to the `CloudFormation` template and hit the Delete button again
![](images/16-cleanup.png)

17. Confirm deletion.
![](images/17-cleanup.png)

18. This time around the stack is completed deleted.
![](images/18-cleanup.png)

19. Hence if you go back to the CloudFormation stacks dashboard, you do not see any stack installed.
![](images/19-cleanup.png)

20. In the `Amazon SageMaker` ==> "Training Jobs" page, these training jobs that were already run and completed, will still be there. There is no way to delete them at the moment.
![](images/20-cleanup.png)

21. Lets go to the `Models` and delete the models. Select and click `Delete` from `Actions` menu.
![](images/21-cleanup.png)

22. Delete the model.
![](images/22-cleanup.png)

23. Confirm
![](images/23-cleanup.png)

24. Now you have all of the models deleted.
![](images/24-cleanup.png)

25. Similary delete endpoint configurations
![](images/25-cleanup.png)

26. Just do it.
![](images/26-cleanup.png)

27. Go ahead and delete the other one too.
![](images/27-cleanup.png)

28. All done with the end point configurations.
![](images/28-cleanup.png)

29. Lets do the same for `Endpoints`
![](images/29-cleanup.png)

30. Go for it.
![](images/30-cleanup.png)

31. Why think twice. Just do it.

![](images/31-cleanup.png)

32. No mercy. Just do it. Delete the Lambda function.

![](images/32-cleanup.png)

33. Yes.Delete.

![](images/33-cleanup.png)

34. All empty. No more lambda functions.

![](images/34-cleanup.png)

35. Also lets delete the `Elstic Container Registry` Repository.
![](images/35-cleanup.png)

36. Just delete.
![](images/36-cleanup.png)

37. Yes.

![](images/37-cleanup.png)

38. All gone.

![](images/38-cleanup.png)

39. Go to IAM roles.
![](images/39-cleanup.png)

![](images/40-cleanup.png)

40. Select the role that was created by your lambda function. In this case: `aws-redis-fraud-detection-processor-role-ddsfsfds`.

![](images/41-cleanup.png)

41. Similarly delete AWS Lambda Basic Execution Role policies.

![](images/42-cleanup.png)

![](images/43-cleanup.png)

![](images/44-cleanup.png)

![](images/45-cleanup.png)

42. Lets also delete the EC2 machine. Go to ec2.

![](images/46-cleanup.png)

43. Terminate the instance.

![](images/47-cleanup.png)

![](images/48-cleanup.png)

44. Delete the S3 bucket that had the cloud formation template in it.

![](images/49-cleanup.png)

![](images/50-cleanup.png)

![](images/51-cleanup.png)


You are pretty much done  [Go back](..)
