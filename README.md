# hands-on-labs-redis-aws-sagemaker
Hands on labs for Redis AWS Webinars, Immersion Days etc

Redis Enterprise Cloud (RC) is a DBaaS (Database-as-a-Service) offering from Redis Inc, the home of RedisOSS. RC is build on top of Redis open source and adds support for other data models, like native JSON and search, graph, and timeseries.  In addition it has  enterprise features like Active-Active Geo replication, High Availability - guaranteeing upto 5 9's (99.999%) uptime and the ability to use tiered storage, Redis on Flash, all built in to our managed service.

Amazon SageMaker is a comprehensive service for machine learning that is fully managed. It enables data scientists and developers to swiftly construct and train machine learning models, and seamlessly deploy them in a ready-to-use production environment. SageMaker offers an integrated Jupyter notebook instance that simplifies access to data sources, allowing for effortless exploration and analysis, all without the need for server management.

In this lab, you will gain direct hands-on experience of building a Realtime Fraud Detection system powered by Redis Enterprise Cloud on AWS, leveraging AWS SageMaker.

You can find the System Reference Architecture [here](https://d1.awsstatic.com/architecture-diagrams/ArchitectureDiagrams/aws_redis_realtime_fraud_detection_ra.pdf?did=wp_card&trk=wp_card).

You will utilize Amazon SageMaker to work with a dataset containing historical financial transactional data. Using SageMaker, you will create, train, test, and deploy machine learning models. These models will be made accessible through published endpoints for future inference. Additionally, you will deploy an AWS Lambda function that responds to incoming real-time transactional data from end users as they swipe their credit cards. This lambda function will store the data in Redis Enterprise Cloud and perform real-time inferences using the machine learning endpoints. The resulting ML scores will be further stored in a Redis Timeseries database, allowing for data visualization and analysis.


If you are a business in financial markets space, we believe that this hands-on experience labs will directly benefit in serving as an impetus in designing your business critical applications that are more smarter and can respond for real-time SLA demands. If you are not in financial markets space, still this hands-on experience will serve as a great learning experience of how to build real-time intelligent applications leveraging Redis Enterprise Cloud and AWS SageMaker.

## Venue
These hands-on workshops are designed for in-person and for virtual experiences.

## Duration
4 to 5 hours.

## Prerequisites
These hands-on labs are very intense from technical experience standpoint (Level 300 to 400). These hands-on labs are targeted for Technical stakeholders like ML engineers, Data scientists, Data Engineers, Application Developers, DevOps, Technical Leads and Architects.  If you are not in any of the above mentioned roles, it would be a disservice for yourself to go any further beyond this point. But if you are one of those most curious souls who do not shy away from getting hands-dirty, we still welcome you to hop on the journey.

Here are few hard skills that you would want to bring to the table:
- Very comfortable with AWS web console, AWS CLI.
- Very comfortable running SSH terminal session in connecting to remote servers (ec2 machines)
- You breath in and out Docker, Containers etc, all through the day.
- Terraform is your bread and butter. You live on it.
- You have a general idea of Machine Learning and what it means by training, testing and deploying ML models. You don't need to be an expert nor the scope of this lab includes a very deep dive on ML subject matter. We will just barely scratch the surface on this.
- You have good understanding of Data analytics, Data visualization etc, to tell business stories based on data.

You will also bring your own laptop / desktop with a browser. You will also bring your AWS account. But don't worry, AWS is giving credits that you can use to run these labs up until you exhaust these credits. We will also help you with cleanup scripts so that you do not get a surprise bill at the end. More on it in the labs.

## Agenda

### Part 1
* Introductions
* [Lecture - Introduction to Redis](https://docs.google.com/presentation/d/1-2aRQEQQ0LS97OGv2D_nIaoJK2w1-2XY/edit#slide=id.p1) (15mins)
  *	Introduction to Redis Enterprise Cloud
  * Customer Use Cases
  * Why customers love Redis
* [Demo - Deploying Redis Enterprise Cloud on AWS](https://docs.google.com/presentation/d/1-2aRQEQQ0LS97OGv2D_nIaoJK2w1-2XY/edit#slide=id.p11)  (5mins)
* [Lab 0 - Signup for AWS](Lab%200%20-%20Signup%20for%20AWS)
  * Signup
  * Applying Credits
* [Lecture - Building Real-Time Apps with Redis Enterprise Cloud on AWS](https://docs.google.com/presentation/d/1-2aRQEQQ0LS97OGv2D_nIaoJK2w1-2XY/edit#slide=id.p13) (10mins )
  * Why modern data platform matters?
  * Redis Enterprise Cloud as a modern data platform
  * Why Real-time matters?
  * Redis for Real-time ML Database
  * What makes an App Real-time and Intelligent?
* [Lab 1 - Building Fraud Detection with SageMaker and Redis](Lab%201%20-%20Building%20Fraud%20Detection%20with%20SageMaker%20and%20Redis)
  * Architecture overview
  * Provision Cloud Resources
  * Review Amazon SageMaker Jupyter Notebook

### Part 2

* [Lecture - Building Intelligent Apps with Amazon SageMaker](https://docs.google.com/presentation/d/1-2aRQEQQ0LS97OGv2D_nIaoJK2w1-2XY/edit#slide=id.p21)
  * Amazon SageMaker Intro
  * Amazon SageMaker Benefits
  * Amazon SageMaker Features
* [Lab 2 - Train, Test and Deploy SageMaker Models and Endpoints](Lab%202%20-%20Train,%20Test%20and%20Deploy%20SageMaker%20Models)
  * Model training jobs for Random Cut Forest & XGBoost algorithms
  * Deployed Model endpoint configurations and Model endpoints
* [Lab 3 - Build and Deploy Lambda function](Lab%203%20-%20Build%20and%20Deploy%20Lambda%20function)
  * Build Lambda function as a Docker container
  * Configure Lambda function
* [Lab 4 - Amazon Kinesis](Lab%204%20-%20Amazon%20Kinesis)
  *	Configure Amazon Kinesis Data stream
  * Configure Amazon Kinesis data stream to trigger AWS lambda function, to invoke fraud detection.

### Part 3

* [Lab 5 - Run Fraud Detection in Real-time](Lab%205%20-%20Run%20Fraud%20Detection%20in%20Real-time)
  * Simulate transactional events
  * Run Fraud detection
  * Lambda Deepdive
* [Lab 6 - Data Visualization (Optional)](Lab%206%20-%20Data%20Visualization%20(Optional))
  * Run Data Visualizations on your Redis Data
  * Configure Grafana and Terraform
  * Configure custom dashboards using Terraform
  * Run Data Visualizations
* [Lab 7 - Cleanup](Lab%207%20-%20Cleanup)
* [Conclusion and Next Steps](https://docs.google.com/presentation/d/1h6GrhdR6_Dt-NP9BEcea5mlGtYE4Atk1QlBvCMu1WCA/edit#slide=id.g1d1930c12ae_1_876)
