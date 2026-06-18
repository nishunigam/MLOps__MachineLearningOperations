# **DevOps, DataOps, MLOps** 

## Key Terms 

- **MLOps** - Combination of DevOps-style automation methods and ML best practices focused on deployment and operations of ML models into production systems. 

- **DevOps** - Culture of collaboration and automation of developer operations to continuously improve deployment and reduce friction between business units. Includes automation tools and principles like CI/CD. 

- **CI/CD** - Continuous integration and continuous delivery - key practices in DevOps workflows. CI involves regular automated testing and validation of incrementally-built software while CD focuses on automatically releasing updates to environments like production. 

- **Maturity Model** - Concept in MLOps defining ascending levels, typically 4-5, of MLOps sophistication and effectiveness, from manual, siloed, unreliable to scalable, autonomous, and resilient systems. 

- **Data Ops** - Specific focus on use of DevOps concepts and automation principles to manage data workloads like aggregation, transformation, storage, analysis, etc. 

- **Feature Store** - Central repository to manage, store, and serve ML features for model building and retraining. Optimizes data pipelines and reuse. 

<img width="940" height="742" alt="image" src="https://github.com/user-attachments/assets/f829ea0c-b5cf-4ef1-b02f-6188dabf400d" />

<img width="940" height="518" alt="image" src="https://github.com/user-attachments/assets/c8f87945-51c0-4b2a-b659-2a0275db9987" />


There's tons of environments, GitHub code spaces is one of my favorite, but the idea here is that you mount a network file system. In this case, we have Amazon EFS or 

elastic file system. And in fact, the build system in this case is Jenkins and the deploy process all have access to the same mount point. And because the disc IO is distributed across the system, you essentially have real time access to both deployment and the data that the machine learning system uses. So I think this NFSOps style deployment is really going to make a comeback. 

<img width="940" height="584" alt="image" src="https://github.com/user-attachments/assets/1be1dc11-fa2d-4925-968c-d5324597820b" />


ow Kubernetes is not going anywhere as well. It's definitely a very complex system, but there are a lot of tools here that fit into the Kubernetes and cube flow workflow, all cloud providers supported. 

<img width="940" height="478" alt="image" src="https://github.com/user-attachments/assets/d6c57622-0b81-4ae7-9bca-2caa43733bc6" />


So the idea here is that you use an ML framework, you do a transformation, and you can deploy to many different locations including a physical device, like a hardware USB device or a mobile phone that has an inference chip that allows you to do predictions on the mobile phone or even an operating system. So edge ML is something that we're going to see more and more of 

<img width="940" height="542" alt="image" src="https://github.com/user-attachments/assets/a2656ed9-0222-4e00-91be-884d5efc172f" />


Another thing that is coming up is this concept of sustainability. We see there is a climate change problem. We want to be careful about how we do things. 

We want to also not only take care of the environment, but we want to care about people, right? Are we delivering recommendation engine results that radicalize people or really destroy democracy? These are important things to consider, and then governance, right? Are we building things in a way that we're able to make a profit, but we're doing it in a way that doesn't dump negative externalities onto people that can't afford them, right? Like for example building a right share system that destroys the traffic in a city and pollutes it and destroys jobs and then you walk away, right? That would be a good example of maybe some bad governance. 

<img width="940" height="660" alt="image" src="https://github.com/user-attachments/assets/c94c443c-74eb-4f0f-8ed7-30e3b1b6ae44" />


It depends on what it is you're trying to do. 

<img width="940" height="478" alt="image" src="https://github.com/user-attachments/assets/bac6616c-1879-4d7e-9e09-db5887d29979" />


Model portability as well is a huge trend we're seeing where you can take a model that was built in many different frameworks. Keras, TensorFlow, pytorch, scikit-learn, XGBoost, and convert it to a universal format like ONNX. 

<img width="940" height="480" alt="image" src="https://github.com/user-attachments/assets/98cc9aba-3f31-4345-95f5-cc33f0afc31d" />


the idea here is that what we're probably going to see is that data scientists really becomes more of a bimodal type position where there will be these chief data scientists who get paid, I don't know, $1 million a year or more. And they're really making key decisions in our organization. But some of the things that the data scientists were doing that were on Kaggle may get completely automated because AutoML in fact can do many of the things that they were doing and also data automation can do many of the things they're doing. So really we're seeing potentially the ML engineer and the data 

engineer really driving the cost, I think at a median level where the data scientists will be at a bimodal level. And so when we think about Kaizen ML, it's really an automated process improvement. So we're not just improving the machine learning model, we're improving every single thing about it 

<img width="940" height="458" alt="image" src="https://github.com/user-attachments/assets/7fc0b872-f0fb-44f2-b0cc-a8faccc7eb64" />


nd with a production first mindset, you don't focus just on 5% of the problem, which is the model, you focus on the whole system. So the behavior as a data scientist, the problem framing, you also automate the data engineering pipeline, get job systems that go through and collect the data and clean it. You have automated feature engineering using things like feature store. You have automated testing, you have automatic business intelligence, automated model accuracy, you have automatic scaling. So you can see that every single thing needs to be automated, if you just pick one thing because it is your favorite, that's not doing a production first mindset. And that's why I call this Kaizen ML is every single thing that's necessary to drive machine learning into production has to be automated. 

And I think this is really a trend that we will see in the future. 

<img width="940" height="535" alt="image" src="https://github.com/user-attachments/assets/fe566e10-91cd-42ed-b1d2-5ede08cd0219" />


we have more of a batch or a static workflow where you would take something directly from GitHub, potentially even the model lives in GitHub, because it's a very small model. You would build it with a cloud native build system, in this case, Google Cloud Build. And then there's a pass or a platform as a service offering, in this case, Google App Engine. And you would serve out a prediction, and then this would be your AI API. So this is a very lightweight kind of hobbyist workflow. Although also it could work very well with, maybe, pretrained model workflows. 

In a more sophisticated MLOps workflow, you could call this a heavy workflow. And there's really a data-centric type approach, versus a model-centric type approach. In the data centric approach, the data is maybe the most important aspect of what you're building. You maybe don't even do any modeling at all, and you could go through and use AutoML point it at a dataset, and then create a model, and then later deploy it. Now notice there's some components of an MLOps system. A platform, in this case, this is vertex AI, there's other AI platforms like for example, SageMaker, there's also Databricks has MLOps/ AI platform. But in general, they all do similar things in that there's data labeling, there's data drift detection, and again, data drift is something where you could tell whether the data has changed underneath the hood, and then trigger a new training run, and then a new model, there's feature stores, where you've got the features that are collected in a way that are really convenient to make new models. 

You have all the models actually registered, you have model monitoring, to make sure that it's performing correctly, you have experiment tracking, so you can see the accuracy of the different systems that have been created and actually go back in time and recreate things, you have explainable AI, and these systems like the shapely extension can show which features are driving which model. And then finally, you have the prediction component. So, all of these are features that really depend on what it is you're doing. Are you more of a data-centric or more of a model-centric? And then finally, you have Pipeline Orchestration, the entire process of building this system. And you have Notebooks and Containers. These are all components that often go together in an MLOps system. 

And then underneath the hood, this is also not necessarily talked about enough, but in any modern system, most likely you're going to have a data management system on the Google Cloud. BigQuery is one of the systems that people often use to query the data. In fact, you can even do machine learning directly inside of this. So this is really a high level overview of some of the the main things to consider when building an MLOps system. Do you want to go light, do you want to go heavy? Do you want to pick data centric, or do you want to pick model centric? 

<img width="940" height="434" alt="image" src="https://github.com/user-attachments/assets/d61e280b-5526-4fd6-a86c-4a58f819d688" />


Let's dive into the concept of MLOps hierarchy of needs. Really, it is like a pyramid and that at the bottom is DevOps. If you don't have DevOps, there's no possibility of an organization doing MLOps. And some of the key components of DevOps include infrastructure as code, right? Are you able to automatically provision environments and check that into your build system? Can you do continuous delivery of your software stack? So a micro service is being delivered in the staging environment and then automatically being propagated to production. 

And also, have you designed around a build system? Next up, we have data operations. So similarly, once you've gone through and you've got that base level of DevOps, you have to look at your data management platforms. And really, are you using a platform? Are you using something like Google BigQuery, or Databricks, or Snowflake or ,Amazon Athena? Some platform that makes a server less query and visualization workflow very straightforward, and also has the ability to do data jobs and data tasks. The next layer up then would be to use some kind of MLOps platform. 

You don't want to be building things yourself, going through and taking a lot of time away from your core business goals. So, there are things like feature stores that can store the pro-curated features that you can use. You can use specific models serving platforms, you can do experiment tracking with tools that are designed to help you look at different metrics and different explanatory techniques, and then also take a look at things like data drift, where you can look at the measure impact of a particular model in production and see how the actual underlying data changed. Finally, once you've got these three things, you're at that MLOps layer. Now, in order to fully implement the MLOps layer, though, you need to think about two things from a business perspective. One, the business ROI. So is the machine learning model that you're creating, is it adding value to the organization, right? 

That's the business ROI. And then second, are you framing the problem correctly? If you don't frame the problem correctly, it's possible that you're solving the wrong problem for your organization. Once you've done that, you can do things like forecasting, predicting the correct amount of inventory, using things like unsupervised machine learning to discover new patterns. And really this is just a an automation of workflow. That's really what MLOps is. Is just going through step by step and automating the stack from the software stack to the data stack, to the platform stack, to ,ultimately, the MLOps stack, which serves as an accelerant to the business value that's already there in an organization. 

This is the MLOps hierarchy of needs. 

## **Data Poisoning Machine Learning Systems** 

Let's take a look at some insider threats that could occur via data poisoning. This is often not looked at in terms of a threat, is what could an insider do into your organization? This is why it's important to carefully consider the concept of principle of least privilege. Let's say in this first attack vector here, we have a corporate owned system, let's say Google Drive, e-mail, et cetera, and we know that there's a particular type of image that could cause your Google Drive to go offline. What can happen is that someone inside a corporation could willfully put a prohibited image inside of the Google 

Drive, which would then make sure that the corporation is offline, and it take some time for that organization to be able to contact Google and explain exactly what happened. This could be an extended denial of service attack on a corporation as the corporation tries to turn the Google assets back online. This is actually pretty sneaky, but easy to do depending on what privileges a employee has in organization. 

They know that in fact, they could even put something that is very hard to find out that it's a prohibited image. Maybe it's a World War II image or something like that. Now a second one that is an attack vector is that potentially an insider could secretly seed training data with images that are known to trigger some forbidden attack, and in this case, they could plant a file on a customer system, and that system would train the data, and eventually the multiclass classification model would see something that wasn't really there. They could plant essentially a false flag of forbidden content, and that particular organization could constantly get a denial of service attack because an insider was explicitly trying to take out another organization. In both cases here, the training data that's planted or in the case of the prohibited image, one of the ways that this could be mitigated is through regular auditing, reducing the principle of least privilege approach, so making sure that people don't have more access than they need to. These are not theoretical attacks. It's very important to consider data poisoning as a real threat to many organizations as data in ML gets more popular. 

<img width="940" height="507" alt="image" src="https://github.com/user-attachments/assets/7d9bf534-7572-41bf-939b-b3e6c5ebeb76" />


## Key Points:

- MLOps inherits from DevOps and brings automation to ML 

- A lightweight or heavy MLOps approach depends on needs 

- Must have DevOps first, then data ops, MLOps platform, and business alignment 

## **5 Reflection Questions:** 

1. How is MLOps different from traditional software engineering? 

2. When would you choose a lightweight vs heavy MLOps system? 

3. What cultural changes are needed to adopt MLOps practices? 

4. How could data poisoning threats impact an organization? 

5. Why is business alignment important for MLOps success? 

## **5 Challenge Exercises:** 

1. Diagram a lightweight MLOps workflow for a hobby project 

2. Set up a basic MLOPs pipeline using open source tools 

3. Interview DevOps teams on lessons for MLOps adoption 

4. Research real-world examples of data poisoning issues 

5. Analyze costs/benefits of ML for a business case 



## MLOps Platform: 

A specialized software solution and workflow for operationalizing machine learning models. MLOps platforms have capabilities like data labeling, model monitoring, feature stores, and optimized model serving. 

## Continuous Integration (CI): 

An automated software development practice where developers frequently merge code changes into a shared repository. Changes are then automatically built and tested to catch issues early. 

## Continuous Delivery:

A software engineering approach where teams produce software in short cycles, ensuring software can be reliably released at any time. It depends on automation like infrastructure as code to replicate test/prod environments. 

## Infrastructure as Code:

Managing and provisioning infrastructure through code instead of manual processes. This allows environment configuration, deployment, and management to be consistent and repeatable across development stages. 

## Feature Store:

A centralized repository that stores curated features for machine learning model training. This helps manage data for model creation, storage, and discovery while preventing drift. 

## Key components in MLops:

<img width="940" height="480" alt="image" src="https://github.com/user-attachments/assets/146e3db7-c9b6-4b4d-b993-9ae53dcf722c" />

> ASCIS that allow you to do things like maybe run TensorFlow inference on a TPU.

There's data ops. You can look at things like Databricks or Snowflakes, MLOps as well. There's lots of MLOps platforms, specialized databases, maybe graph databases or time series databases, monitoring and observability. Things like Datadog or New Relic 

Really, when someone is thinking of MLOps, they need to also be aware of the entire ecosystem behind MLOps and choose what are the things that are more commodity that you want to actually use and what are the specialized services where you want to pay a vendor a premium because they give you a premium ROI. 

## **Mlops maturity level:** 

All major vendors in the MLOps space have the concept of an MLOps maturity model. Really what it means is there are several different phases of going from a crude working where you can barely get things into production and things are error-prone and manual all the way to a very sophisticated system that has really end-to-end automation and uses the next-generation features. 

### AWS: 

<img width="940" height="515" alt="image" src="https://github.com/user-attachments/assets/ef8360b1-3b0e-4370-8116-a51c1b7b7b61" />


make sure that there's maybe a platform that you're using that can actually deploy the solution. 

you're able to templatize and productionize a lot of different ML solutions, not just one, but actually have a scalable system that you can repeat over and over again 

### Azure:

<img width="940" height="530" alt="image" src="https://github.com/user-attachments/assets/302b989a-4fea-4aba-bff5-e96940ccd5d2" />


### Google: 

MLOps level 0 is a manual process. 

There's many teams that have data scientists and ML researchers. 

You can see here that there's a separation though between machine-learning and Ops. Everything is entirely manual. 

If we go to the next level, which is a pipeline automation level, the goal here is that you continuously train the model because things are automated. You have some level of automation because potentially there's a data drift detected, and you have all of your features at a feature store, and you're able to automatically train the model when it's appropriate. 

Finally, we have the CI/CD pipeline automation. 

Finally, the last phase here is not only do you have the model training automatically, but your continuous integration, your continuous delivery system is able to fully deploy the system. It's packaged up correctly. you've got 100 percent end-to-end automation. 

This is really the key with three of these vendors, is the concept of continuously deploying systems through automation and having enough integration. You have a production first mindset. 


## Reflection Questions:

### In MLOps, beyond protecting the environment, what else is sustainability primarily concerned with protecting?

The well-being of people

### To what does MLOps apply DevOps ideas?  

Machine learning systems

### What does enforcing least privilege prevent users from having?  

More access than they need

### What GitHub feature allows pre-configuration of development environments? 

Dev containers

### What is recommended as a direct incentive for employees to learn? 

Pay people to learn

### According to the source, what type of practices form one main technical component of DevOps?  

Software engineering best practices

### What uncertainty does “data science on your first day” aim to address? 

Not knowing what to do

### Where does the insider upload the prohibited image to initiate the attack? 

Inside the corporate Google Drive

### MLOps is modeled after automation methods from which discipline?  

devOps  
### What is the primary focus of MLOps?

Deployment and operations of ML models 

### What is the primary goal of MLOps in machine learning systems?  

Continuous improvement of ML systems 

### What is described as having no substitute in the learning process?  

Hands-on practice 

### What organizational tool does the source recommend for managing best practices?  

A Checklist 

### In DevOps, what kind of changes does the methodology favor?  

Incremental changes 

### What is the primary business effect of the MLOps stack?  

Accelerates business value 

### Which existing methodology's concepts does Data Ops specifically use? 
DevOps concepts 

### What is the primary focus of CI/CD as described in the text?  

Continuous code delivery 

### What specific type of insider threat is highlighted as often overlooked in organizations?  

Insider threats via data poisoning 

### What step precedes deployment in edge-based machine learning?  

Model transformation using an ML framework  

### In the MLOps rule of 25, which component of MLOps deals with business requirements?  

Framing business requirements 

### In the analogy, what real-world object represents ML containers?  

A shipping container 

### What overarching software development methodology uses infrastructure as code and continuous integration?  

DevOps methodology 

### What example task might a scientist use machine learning for, according to the text?  

Detect endangered animals 

### In terms of process behavior, how does the source describe DevOps?  

A feedback loop  

### For the corporation, what does the Google Drive outage effectively create?  

An extended denial of service 

### Beyond DevOps, what broader historical area does MLOps draw from?  

History of automation 

### What type of platform in the MLOps layer is used to expose trained models for use? 
Model serving platform 

### In DevOps, what organizational barrier is targeted for removal?  

Silos between teams 

### What event can data drift detection be used to trigger?  

Initiating a new model training run 

### What kind of models are highlighted for use in Lesson 3?  

Pre-trained models  

### What key benefit does a feature store provide regarding feature reuse?  

Enables reuse of ML features 

### What does Kaizen emphasize in the Japanese automobile industry? 

Continuous improvement 

### What does the source highlight as under-discussed in modern systems? 

The data management system layer 

### What hiring advantage comes from choosing a popular cloud platform?  

Easier replacement of team members 

### In MLOps, what does "going heavy" primarily refer to?  

Using a more complex MLOps setup 

### After establishing a base level of DevOps, what should organizations examine next?  

Their data management platforms 

### What is the ultimate goal of combining Hugging Face and pre-trained models in Lesson 3?  

Solve a problem for a customer 

### What cultural aspect is identified as a main component of DevOps?  

Culture of continuous improvement 

### What is the primary security concern mentioned as machine learning data use grows?  

Data poisoning attacks 

### What is the primary cultural focus of DevOps?  

Collaboration between development and operations  

### What type of mandate is Kaizen described as within a company in the source? 

Cultural mandate 

### What must be established before implementing data ops in an organization? 

A solid DevOps foundation 

### Where is the model source stored in this lightweight MLOps workflow?  

Directly in GitHub 

### What is a key mitigation for prohibited images entering training data?  

Regular data audits 

### In the rideshare example, what environmental effect indicates bad governance? 

Increased city pollution 

### From which recent software practice does MLOps inherit many concepts?  

DevOps 

### In DevOps, which practice automates releasing software updates?  

Continuous delivery 

### What is the primary contribution of MLOps to machine learning workflows?  

Automation of ML workflows 

### In MLOps, what is the ethical concern about the impact of recommendation engine results on users?  

Potential to radicalize people 

### What is a proactive measure against data poisoning in training pipelines?  

Routine dataset auditing 

### What capability does the shapely extension provide in explainable AI?  

Shows feature contributions to predictions 

### What interpersonal practice is central to DevOps?  

Collaboration with teammates  

### What misconception about data poisoning does the source correct?  

That it is only theoretical 

### What is the primary purpose of infrastructure as code in DevOps?  

Automatically provision environments 

### What is a key security concern highlighted in MLOps?  

Data poisoning threats 

### What does a feature store contain for machine learning workflows?  

Precomputed, reusable machine learning features 

### Who is identified as capable of performing data poisoning in the described scenario?  

An insider within the organization 

### What historical capability does experiment tracking provide?  

Ability to go back in time 

### which concept is explicitly contrasted with heuristics?  

Optimization 

### According to the source, what plays a role in achieving automation alongside CI/CD?  

Infrastructure as code 

### What key metric does experiment tracking allow you to compare between systems?  

The accuracy of different systems 

### What is the main goal of DataOps for data systems over time?  

Constant, incremental improvement 

### In the MLOps rule of 25, which component of MLOps is about improving models?  

Modeling 

### Which tool is given as an example of AI pair programming?  

GitHub Copilot 

### What is identified as the end result component of DevOps in the source?  

Automation  

### Under DataOps, what should happen to your data system every day?  

It should get a little better 

### What market position does Amazon hold in cloud computing in the example?  

Market leader in cloud computing 

### In NFSOps, what is mounted to enable shared access?  

A network file system 

### In the MLOps platform layer, what does data drift analysis focus on regarding the data?  

How underlying data has changed 

### What does business ROI evaluate for a machine learning model?  

Its value to the organization 

### What is the typical number of levels in an MLOps maturity model?  

4-5 

### In DevOps, what type of change is avoided in favor of incremental updates?  

All-or-nothing changes 

### Besides data quality, what organizational capability should DataOps improve? 

Effective communication across the organization 

### In MLOps, what is the main risk of not framing a problem correctly?  

Solving the wrong organizational problem 

### What is the primary purpose of a feature store?  

to store curated machine learning features for reuse in model training and serving 

### Which type of machine learning is used to discover new patterns in inventory data? 

Unsupervised machine learning 

### What characterizes the lowest level in an MLOps maturity model?  

Manual, siloed, unreliable practices 

### In the MLOps rule of 25, what aspect of MLOps focuses on automating data?  

Data operations 

### What does the source suggest is transferable from DevOps and DataOps to MLOps?  

The operational mindset  

### What key DevOps capability allows software to move from staging to production automatically?  

Continuous delivery 

### In the MLOps hierarchy of needs, what follows data ops?  

An MLOps platform 

### What DevOps concept is described as embodying automation in the passage?  

Ci/cd 

### What type of cloud service is Google App Engine in this workflow?  

Paas 

### In a data-centric workflow, what tool type can be used instead of manual modeling?  

AutoML 

### In the MLOps hierarchy of needs, what is the final layer after the MLOps platform?

Business alignment  

### Which type of data activity involving extracting insights is managed by Data Ops? 

Data analysis 

### What is Kaizen ML primarily defined as?  

Automated process improvement  

### According to the source, what idea is at the root of DevOps?  

The idea of automation 

### What practice helps mitigate planted or malicious training data in a system? 

Regular auditing of data 

### In a production-first mindset, roughly what fraction of the overall problem does the model itself represent? 

About 5% of the problem
