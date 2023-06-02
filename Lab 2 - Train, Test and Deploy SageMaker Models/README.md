# Lab 02 - Train, Test and Deploy SageMaker Models and Endpoints


In this lab, we will do all things related to SageMaker. This includes:
- train
- test
- deploy
machine learning models using Amazon SageMaker.

![](images/WhereAmI-Lab2.png)

In addition, we will also publish the model endpoints so that real-time inferencing can be done on these machine learning endpoints.

You are now ready to run the Amazon SageMaker Notebook. You will create the following cloud resources, when you run this notebook.:

* Model training jobs for Random Cut Forest & XGBoost algorithms
* Deployed Model endpoint configurations and Model endpoints
* S3 buckets that has the input and output buckets with trained data and results

So, lets get started.

01. Each cell highlighted has a python code that will be executed when you press `COMMAND` + `ENTER` on a Mac OR `Cntrl` + `ENTER` on a Window's machine.
We are going to run this notebook, cell by cell in a sequential manner, after ensuring that the previous step is executed.

![](images/01-sagemaker-model.png)

To understand if a specific cell has been executed or not, please notice the `[ ]` in each cell.
- `[ ]` indicates that the cell has not been executed yet. (`Not started` state)
- `[*]` indicates that the current cell code is being executed (`In Progress` state)
- `[5]` any number (ex: 5) indicates that the cell has been executed.(`Execution Completed` state)

02. Lets start with executing the first cell. This downloads the credit card fraud data set.

![](images/02-sagemaker-model.png)

03. Once this cell executes, you will see the `[1]` indicating the successful run of the code. Also in the left hand navigation bar, you can now see new two files - namely `creditcard.csv` and `creditcardfraud.zip` files being downloaded.

![](images/03-sagemaker-model.png)

04. In this way, you are going to execute all fo the subsequent cells, one by one, in a sequential manner.

![](images/04-sagemaker-model.png)

05. We are going to use `numpy` and `pandas` data frames in our code. Go ahead and execute Cell #2 and #3.

![](images/05-sagemaker-model.png)

06. You are doing great. Keep going. Notice how the output gets printed in the web console of the Jupyter notebook itself.

![](images/06-sagemaker-model.png)

07. Here we are going to split the original data set so that we can use one set for training and another one for testing.

![](images/07-sagemaker-model.png)

08. Lets get started with Unsupervised Learning.

![](images/08-sagemaker-model.png)

09. Keep moving by pressing `COMMAND` + `ENTER` on a Mac OR `Cntrl` + `ENTER` on a Window's machine.

![](images/09-sagemaker-model.png)

10. This code will kick start a new training job. It will run for 5mins or so.

![](images/10-sagemaker-model.png)

11. Navigate yourself to `Amazon SageMaker` > `Training jobs`. Check the training job that is currently running in "InProgress" state.

![](images/11-sagemaker-model.png)

12. You can view the history of the training job here.

![](images/12-sagemaker-model.png)

13. Here you go. History.

![](images/13-sagemaker-model.png)

14. And in the jupyter notebook window you can continue to observe that the code is still executing.

![](images/14-sagemaker-model.png)


15. If you toggle back to Amazon SageMaker window, you will see that the Training job is `Completed`

![](images/15-sagemaker-model.png)


16. You can also see here that it is `Completed`

![](images/16-sagemaker-model.png)


17. Also in the Jupyter notebook,, the `[9]` indicates that the cell executed completly, which means that the training job that you were observing in the AWS Webconsole is `Completed`.

![](images/17-sagemaker-model.png)


18. Here are few metrics to observe how much time this training job took.

![](images/18-sagemaker-model.png)


19. Lets now deploy the model.

![](images/19-sagemaker-model.png)


20. Once executed the endpoints are created.

![](images/20-sagemaker-model.png)


21. Lets cross check these endpoints

![](images/21-sagemaker-model.png)


22. Here you can see that the endpoint configurations are created.

![](images/22-sagemaker-model.png)


23. And here you can verify that the endpoints are also created.

![](images/23-sagemaker-model.png)


24. When you execute this code, it may give an error, as shown below.

![](images/24-sagemaker-model.png)


25. Simply comment out the first line ending with `text/csv` and re-execute the cell. This time, it is erroring out on the ine ending as `application/json`.  Comment out this line too and re-execute.

![](images/25-sagemaker-model.png)


26. If you comment out the code as shown , then you shoudl be able to run the cell successfully

![](images/26-sagemaker-model.png)


27. Now its time to test our model. Go ahead and run these two cells.

![](images/27-sagemaker-model.png)

28. Continue executing.

![](images/28-sagemaker-model.png)

29. Here is the plotting.

![](images/29-sagemaker-model.png)

30. Now its time to do some Supervised Learning.

![](images/30-sagemaker-model.png)

31. Go ahead and run this code, to setup S3 buckets for training data and output data.

![](images/31-sagemaker-model.png)

32. Contiue executing.

![](images/32-sagemaker-model.png)

33. Keep moving on..

![](images/33-sagemaker-model.png)

34. This will start another training job.

![](images/34-sagemaker-model.png)

35. You can cross verify these training jobs in the `Amazon SageMaker` UI. Here you can notice that the jon is still in `InProgress` state.

![](images/35-sagemaker-model.png)

36. And you can view the entire job history info here.

![](images/36-sagemaker-model.png)

37. And here you go..

![](images/37-sagemaker-model.png)

38. And its still in progress.

![](images/38-sagemaker-model.png)

39. And now its `Completed`

![](images/39-sagemaker-model.png)

40. And the Jupyter notebook reflects the same by indicating the completion of the code in the cell `[18]`

![](images/30-sagemaker-model.png)

41. The first cell in the Host Classifier may run in to errors, like shown here.

![](images/41-sagemaker-model.png)

42. And here is the error.

![](images/42-sagemaker-model.png)

43. Simply comment out the last line and re-execute.

![](images/43-sagemaker-model.png)

44. When you re-execute the code, this time around it successfully executes the code and creates the endpoints

![](images/44-sagemaker-model.png)

45. And they can be cross verified in the UI by going to `Amazon SageMaker` ==> "Endpoint Configuration"

![](images/45-sagemaker-model.png)

46. And similar story here. You have your endpoints in the process of creation.

![](images/46-sagemaker-model.png)

47. And the endpoints are now successfully created.

![](images/47-sagemaker-model.png)

48. And without any surprise, even Jupyter notebook indicates the successful run of the code.

![](images/48-sagemaker-model.png)

49. Keep moving and continue executing the next cell.

![](images/49-sagemaker-model.png)

50. And here is the output.

![](images/50-sagemaker-model.png)

51. You are about to plot a confusion matrix.

![](images/51-sagemaker-model.png)

52. And here is the confusion matrix.

![](images/52-sagemaker-model.png)

53. And the output.

![](images/53-sagemaker-model.png)

54. You do not need to further execute the rest of the cells in this python book. We have enough AWS SageMaker resources that are good enough for us to proceed with the rest of the design of our Fraud detection system.

![](images/54-sagemaker-model.png)

### If you have made this far, you are doing a great job. Awesome.

## Conclusion

In this lab, so far you have done the following things.

Using SageMaker, you took a fraud credit card transactions dataset and applied both XGBoost and Anamoly detection algorithms and trained, tested and deployed your model.

In addition, you also published the model endpoints so that real-time inferencing can be done on these machine learning endpoints, in the subsequent labs.


See you in the next lab.  [Go back](..)
