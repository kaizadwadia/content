---
title: "What is SageMaker?"
description: "Simplifying Machine Learning on AWS"
tags:
    - ai-ml
    - SageMaker
    - generative-ai
    - machine-learning
    - artificial-intelligence
authorGithubAlias: najibkado
authorName: Najib Muhammad Kado
additionalAuthors:
  - authorName: Kaizad Wadia
    authorGithubAlias: kaizadwadia
date: 2023-11-14
---

## Introduction

Machine learning is a field of artificial intelligence that enables computers to learn and improve from experience without being explicitly programmed. The goal of machine learning is to develop algorithms that can receive input data and use statistical analysis to identify patterns and build models that can make predictions or decisions without human intervention. The extensive skills needed to build such teachnologies leaves many businesses unable to tap the potential of ML. Amazon SageMaker makes ML practical by providing a fully managed platform to build, train, and deploy models with ease. In this post, we’ll explore how SageMaker eliminates the heavy lifting of ML, making it possible for any team to generate value from data. You’ll learn what capabilities SageMaker offers to accelerate development and simplify deployment of ML models. With SageMaker, you can finally put machine learning to work for your business.

## What is Amazon SageMaker?

Amazon SageMaker is a fully managed machine learning service that makes it easy for developers to build, train and deploy scalable machine learning models quickly in the cloud. This is because it removes most of the difficulties associated with turning raw data into finished machine learning models and ready for production. SageMaker also gives developers the opportunity to skip the manual process of setting up servers and clusters to train models. Instead, you can provide training data, choose an algorithm, and let SageMaker handle the rest on a fully managed infrastructure. In addition to that you can deploy your models with a single click to perform predictions in real-time. SageMaker reduces the complexity of developing impactful machine learning models by providing end-to-end capabilities of machine learning workflow. Companies are using SageMaker to solve challenging problems in areas like forecasting, personalized product recommendations, and fraud detection.

## Key Capabilities and features of Amazon SageMaker

### Building Models

SageMaker makes model building easier by providing pre-built containers and algorithms. you don't need to setup environments or configure training scripts with SageMaker's fully managed infrastracture. Instead you provide an algorithm, training code, and dataset; Then let SageMaker handle the rest. In addition SageMaker supports popular frameworks like TensorFlow, PyTorch, and XGBoost. Or Bring your own frameworks using custom containers. This flexibility allows rapid testing of different approaches. 

### Managing Machine Learning Workflows

SageMaker Studio provides an integrated web environment for end-to-end ML workflows. This will let you to easily setup projects, track experiments, organize models and data, visualize results, and collaborate. SageMaker Studio gives you a single pane of glass for an end-to-end machine learning workflow. These involves the provision of an integrated development environment (IDE) which will allow you to access jupyter notebooks, build and debug models, and more from a single interface. In addition, SageMaker Studio manages the ML pipelines for you which will allow you to visually create, execute, and track end-to-end ML workflows with components such as data processing, feature engineering, model training and more. SageMaker Studio also integrates with other AWS Services as well as other third-party services like github to allow you to manage you model code and track model versions. Finally, SageMaker Studio has more capabilities you can explore [here](https://aws.amazon.com/sagemaker/studio/?nc=sn&loc=1), and in summary SageMaker Studio simplifies and accelerates the machine learning workflow for developers and data scientists. It offers a versatile visual interface with everything needed for ML projects integrated in a single platform. By handling infrastructure and operations in the cloud backend, Studio allows users to focus on high-value model development, experimentation, and deployment.


### Training Models

SageMaker offers a fully-managed machine learning platform to help engineers and data scientists quickly build, train, and deploy high-quality models at any scale. With SageMaker, you don't have to worry about managing the infrastructure needed for distributed, large-scale model training. Simply specify the compute resources you need like GPU type and number of instances, and SageMaker handles the rest. By using features such as [GPU instances and training compilers](https://aws.amazon.com/SageMaker/faqs), training time and costs can be significantly reduced.

### Deploying Models

You can use SageMaker to easily deploy machine learning models for real-time or batch predictions. Once the model is trained, developers create an endpoint configuration that specifies where the trained model artifacts are stored in S3. You can indicate what type of instance and number of instances are needed to host the model. SageMaker then launches the endpoint and loads the model onto these instances. An endpoint URL is created that allows sending prediction requests to the model. To make predictions, the developer sends requests to the endpoint URL with JSON data payloads. The model loaded on the endpoint processes this data, makes predictions/inferences, and returns responses. CloudWatch logs collect metrics on usage and performance. Developers benefits from simplified deployment, auto-scaling based on usage, monitoring dashboards, A/B testing capabilities, integration with other AWS services, and automated retraining workflows to keep models accurate over time.


### Monitoring Models

SageMaker provides tools to monitor the health and performance of machine learning models deployed as endpoints. Developers can enable continuous monitoring on a model endpoint which will track key performance metrics like invocation count, latency, and memory usage. Basically, it automatically collects performance metrics on your endpoints - things like how many requests they are serving, any errors or failures, how long each request takes, etc. All this data gets sent to CloudWatch. So then you can check out the metrics on CloudWatch dashboards and graphs. You can set up alarms as well, so you get notified if something looks off or crosses a threshold. This makes it a lot easier to monitor your models and catch any issues quickly. You can see how they are performing over time and spot problems before your customers even notice them. Plus, you get access to detailed request logs too. So, you can really drill down into any specific requests that looked weird in the metrics and debug what went wrong.


### Build Machine Learning Pipelines With Drag and Drop

SageMaker Canvas is a GUI interface that allows you to quickly build, train and deploy machine learning models without writing any code. With SageMaker Canvas you can drag and drop prebuilt components like datasets, algorithms, and training configurations onto canvas to assemble a full machine learning pipeline. Behind the scenes, SageMaker Canvas translates the visual workflow into a SageMaker Pipeline, which is a Python script that executes the components. So Canvas handles the coding automatically. Developers just need to configure each component by specifying parameters like compute resources, datasets, algorithms etc rather than coding the components from scratch. Canvas components are powered by other SageMaker services. For example, the training component uses SageMaker training jobs and same for other components of SageMaker Canvas. In the Canvas editor, developers can drag and drop pre-built components like data processing, model training, hosting, and inference steps. These components can be connected to create an end-to-end ML workflow. The workflow is visualized as a graph with nodes for each component and edges connecting them in sequence. In addition to pre-built components, developers can also author their own custom components in Python if they need additional logic or capabilities. These custom components get containerized and can be invoked as part of the workflow. As developers build their pipeline, SageMaker Canvas manages provisioning of underlying resources like compute instances, orchestrating the execution of steps, and tracking metadata. Once a pipeline is defined, developers can execute it with one click. SageMaker Canvas manages the full lifecycle - kicking off data processing, training, deployment, and monitoring jobs while providing logs and status in the UI. Pipelines can be saved for re-use and iterative improvement over time. Developers can tweak parameters, add/remove steps, and re-run as needed for experimentation and development.


### SageMaker Clarify

SageMaker clarify lets you detect bias in models and explains predictions by providing metrics to identify biases against certain groups in training data and models. you can get individual predictions, which will show you which input features most influenced a specific prediction, which will help in debugging the behaviour of the model. To use Clarify, a developer first trains their model in SageMaker. Clarify can analyze the training data to detect biases before the model is even trained. It generates statistical reports about the distribution of sensitive attributes in the training data. Clarify can also analyze a trained ML model to detect biases. It does this by running the trained model on sample test datasets and comparing the model's predictions for different groups. For example, it can compare predictions for male vs female groups to detect gender bias.
Specifically, Clarify will analyze the trained model for Predictive parity, Equal opportunity, Demographic parity. The developer can configure the sensitive attributes and analysis methods in Clarify. They provide their training dataset and the trained model. Clarify produces detailed reports analyzing the data and model. This includes bias analysis graphs, aggregated confusion matrices, and statistics like p-values and correlation coefficients. Based on these reports, the developer can fine-tune the model and data to remove undesirable biases. They may pre-process data, adjust sample sizes, or apply techniques like re-weighting. Clarify provides bias mitigation strategies. This allows developers to detect and mitigate biases before deploying ML models in production. Clarify integrates seamlessly with SageMaker, making bias detection a built-in part of the model development lifecycle.


### SageMaker Data Wrangler 

You can use this feature to quickly prepare and clean data for machine learning without writing any code. you can also use it to combine datasets, transform data, handle missing values, and perform other data preparation and feature engineering tasks to get data ready for training machine learning models. To use Data Wrangler, a developer first uploads their dataset to an S3 bucket. Data Wrangler supports multiple data formats including CSV, JSON, Parquet, etc. Once the data is uploaded, the developer opens the Data Wrangler studio in SageMaker. Here they can visually explore the data, identify issues, and transform the data iteratively. The data transformations are done using an underlying Scala/Spark backend. Data Wrangler auto-generates the Scala code for the transformation steps. The transformed dataset can then be consumed for model training in SageMaker. The developer can build an end-to-end ML workflow encompassing data preparation, model training, deployment and inference within the SageMaker environment. In summary, SageMaker Data Wrangler provides an easy to use visual interface and Scala-based backend to prepare noisy raw data for machine learning model development. It integrates tightly with other SageMaker services for a streamlined ML application development experience.

### SageMaker Jumpstart

Amazon SageMaker JumpStart gives you quick access to prebuilt machine learning solutions, sample notebooks, and hosted models that can be customized and deployed with little machine learning expertise required. JumpStart allows you to choose from a catalog of solutions like tabular data processing, computer vision, and natural language processing to get started quickly on building and training ML models. Also JumpStart integrates with other SageMaker capabilities. The notebooks leverage features like Clarify, Data Wrangler, Feature Store, and Model Monitor. You can use sagemake jumpstart to acceleratr your machine learning journey through reusable assets, templates, and models. 

### Create Training Datasets

You can use SageMaker Ground Truth to create highly accurate training datasets. Ground Truth helps you with data labeling tasks at sacle. And ground truth provides you with tools to verify, analyze and monitor labeling quality. The integration with S3 also gives you the ability to store your dataset which can later be used to train models with SageMaker training jobs. When it comes to using Ground Truth, a developer first uploads their unlabeled dataset to an S3 bucket. This can be images, text, video, etc. The developer then creates a labeling job in Ground Truth, specifying the S3 location of the data, the task type (image classification, object detection, text classification etc.), and the worker UI they want to use for labeling. Ground Truth launches human labeling tasks on AWS Mechanical Turk, or the developer can use their own private workforce. Workers will be shown the UI to label the data through boundary boxes, text, classifiers etc. As the labeling job progresses, Ground Truth stores the labels in an output manifest file in S3. The developer can check the job dashboard in Ground Truth console to monitor progress. Once the labeling job is complete, the developer gets a manifest file with the location of the labeled dataset in S3. This can be directly used to train SageMaker machine learning models.


### Machine Learning Governance

You can use SageMaker ML Governance to monitor the entire process of your machine learning models from training to deployment. This give you the ability to deploy responsible models by monitoring the model, detecting biases and more to meet regulatory requirements and increase trust in AI systems. To use SageMaker Model Monitor, a developer first trains and deploys a machine learning model using SageMaker. When deploying the model, they specify a monitoring schedule and constraints like data quality rules or drift limits. SageMaker Model Monitor will then automatically collect data from the endpoints the model is deployed to and run bias and explainability checks on a regular schedule. It evaluates the live traffic against the constraints set by the developer. If any violations are detected, SageMaker Model Monitor will trigger configured notifications and alerts. The developer can view reports on the SageMaker console to analyze the failures and understand what data caused the drift or quality issues. Based on the monitoring results, the developer can then improve the model by retraining it with updated data that is more representative of the real world. They can also adjust the constraints to focus on what matters most for model performance. The key benefits are automatic monitoring of all deployed models, drift detection, and bias and explainability checks. Developers don't have to build custom monitoring tools. With built-in integration in SageMaker, they have a smoother machine learning operations workflow to maintain and improve models in production.


### Deploying Machine Learning Models at Scale

Sgaemaker MLOps gives you the abilities to deploy ML models at scale by providing CI/CD pipelines for model building and deployment, model monitoring, automated drift detection and retraining, integration with Git/GitHub for version control and collaboration, and tools for experiment tracking and model lineage. With these capablities you can operationalize ML models into production, manage large volume of ML expirements, and more to improve efficiency and reduce errors while improving the productivity of teams. To implement MLOPs, developers can set up continuous integration/continuous delivery workflows using SageMaker Pipelines. Pipelines automates the process of retraining models and updating the hosted endpoints with new model versions. Developers define a pipeline workflow consisting of steps for data processing, model training, evaluation, and deployment. The pipeline is executed each time a new model version needs to be created. This enables a repeatable ML workflow from new data to deployed model.

## Use Cases

### Fraud Detection

Fraud is a major challenge that many companies face today, including [Mastercard](https://aws.amazon.com/solutions/case-studies/mastercard-ai-ml-testimonial). With the rise of online transactions and digital payments, fraudsters are constantly finding new ways to game systems and commit fraud. Companies are leveraging Amazon SageMaker to build highly accurate fraud detection models in order to counteract this. These models are trained by using anomaly detection, a principal that determines whether a certain transaction is unusual, relative to the rest. These models usually come with their own set of challenges, such as the imbalanced data problem, which happens because fraudulent transactions occur much less frequently than non-fradulent transactions, thereby resulting in an imbalanced data set. This results in a bias in the model, which makes it less likely to detect fraud since it doesn't know enough about what fraud could look like. To mitigate such challenges, SageMaker also comes with managed (and no code) data preprocessing solutions such as [SageMaker Data Wrangler](https://aws.amazon.com/SageMaker/data-wrangler), that can process the data using techniques that help improve the model predictions.

### Personalized Recommendations

Companies like [Natwest Group](https://aws.amazon.com/solutions/case-studies/natwest-group-case-study) are leveraging Amazon SageMaker to build personalized recommendation systems that identify and suggest relevant products or content for each user to drive user engagement and increase sales. 

### Forecasting

Companies such as [Visualfabriq](https://aws.amazon.com/solutions/case-studies/visualfabriq-case-study) are leveraging Amazon SageMaker to build forecasting models that predict future sales, demand, and other metrics. Forecasting takes past data and uses it to predict trends that may reoccur in the future. SageMaker provides built-in algorithms like DeepAR that are optimized for time-series forecasting. By bringing your historical time-series data into SageMaker notebooks, you can train forecasting models that learn patterns and seasonality in the data. These models can then be deployed into production to generate forecasts on an ongoing basis.


## Conclusion

Through this post, you have learned how amazon SageMaker removes the barriers to successfully leveraging machine learning and i'ts capabilities of simplifying and accelerating the process of developing, training, deploying, and managing ML models in the cloud. You can use SageMaker to create impactful ML solutions for a wide variety of use cases. By handling much of the complexity, SageMaker makes it easier to build machine learning products, reduce ML operational costs, and deploy models reliably at scale. This fully managed platform represents a major step forward in making machine learning more accessible. 
