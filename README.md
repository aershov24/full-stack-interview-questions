1001 (actually more than ~1500) Full Stack Interview Questions And Answers sourced from all around the Internet to help you to prepare to an interview, conduct one, mock your lead dev or completely ignore. Answers provided for Junior and Middle-Level questions. Other answers available on [FullStack.Cafe](https://www.fullstack.cafe).

## <a name='toc'>Table of Contents</a>
 * [ASP.NET](#ASP.NET)
 * [AWS](#AWS)
 * [Agile](#Agile)
 * [Angular](#Angular)
 * [AngularJS](#AngularJS)
 * [Azure](#Azure)
 * [Behavioral](#Behavioral)
 * [Bootstrap](#Bootstrap)
 * [CSS](#CSS)
 * [Code Problems](#CodeProblems)
 * [Data Structures](#DataStructures)
 * [Design Patterns](#DesignPatterns)
 * [DevOps](#DevOps)
 * [Git](#Git)
 * [Golang](#Golang)
 * [GraphQL](#GraphQL)
 * [HTML 5](#HTML5)
 * [Java](#Java)
 * [JavaScript](#JavaScript)
 * [Laravel](#Laravel)
 * [MongoDB](#MongoDB)
 * [Node.js](#Node.js)
 * [Performance Testing](#PerformanceTesting)
 * [Questions to Ask](#QuestionstoAsk)
 * [REST API](#RESTAPI)
 * [React](#React)
 * [Ruby](#Ruby)
 * [Sass](#Sass)
 * [Scrum](#Scrum)
 * [Software Architecture](#SoftwareArchitecture)
 * [TypeScript](#TypeScript)
 * [UX Design](#UXDesign)
 * [Vue.js](#Vue.js)
 * [Web Security](#WebSecurity)
 * [Webpack](#Webpack)
## [[⬆]](#toc) <a name=ASP.NET>ASP.NET</a> Interview Questions
#### Q1: What is .NET Core? ⭐
**Answer:**
The .NET Core platform is a new .NET stack that is optimized for open source development and agile delivery on NuGet. 

.NET Core has two major components. It includes a small runtime that is built from the same codebase as the .NET Framework CLR. The .NET Core runtime includes the same GC and JIT (RyuJIT), but doesn’t include features like Application Domains or Code Access Security. The runtime is delivered via NuGet, as part of the ASP.NET Core package.

.NET Core also includes the base class libraries. These libraries are largely the same code as the .NET Framework class libraries, but have been factored (removal of dependencies) to enable to ship a smaller set of libraries. These libraries are shipped as `System.*` NuGet packages on NuGet.org.

**Source:** _stackoverflow.com_

#### Q2: What is ASP.NET Core? ⭐⭐
**Answer:**
ASP.NET Core is a brand new cross-platform web framework built with .NET Core framework. It is not an update to existing ASP.NET framework. It is a complete rewrite of the ASP.NET framework. It works with both .NET Core and .NET Framework.

Main characterestics of ASP.NET Core:

*   DI Container which is quite simple and built-in. You can extend it with other popular DI containers
*   Built-in and extensible structured logging. You can redirect output to as many sources as you want (file, Azure, AWS, console)
*   Extensible strongly typed configuration, which can also be used to reload at run-time
*   Kestrel – new, cross-platform and super fast web server which can stand alone without IIS, Nginx or Apache
*   New, fully async pipeline. It is easily configured via middleware
*   ASP.NET All meta package which improves development speed, and enables you to reference all Microsoft packages for ASP.NET Core and it will deploy only those that are being used by your code
*   There is no _web.config_. We now use _appsettings.json_ file in combination with other sources of configuration (command line args, environment variables, etc.)
*   There is no _Global._asax – We have _Startup.cs_ which is used to set up Middleware and services for DI Container.

**Source:** _talkingdotnet.com_

#### Q3: Can ASP.NET Core work with the .NET framework? ⭐⭐
**Answer:**
Yes. This might surprise many, but ASP.NET Core works with .NET framework and this is officially supported by Microsoft.

ASP.NET Core works with:

*   .NET Core framework
*   .NET framework

**Source:** _talkingdotnet.com_

#### Q4: How to configure your ASP.NET Core app? ⭐⭐
**Answer:**
Another crucial part of ASP.NET Core Framework is Configuration. Also, it is part of Dependency Injection. Use it anywhere in your code with an option to [reload on changes](https://codingblast.com/asp-net-core-configuration-reloading-binding-injecting/) of configuration values from sources (appsettings.json, environment variables, command line arguments, etc.). It is also easy to override, extend and customize the Configuration. No more extensive configurations in web.config, the preferred way now is _**appsettings.json**_ in combination with a mix of Environment variables and cmd-line args.

**Source:** _talkingdotnet.com_

#### Q5: Talk about Logging in ASP.NET Core? ⭐⭐
**Answer:**
**Logging** is built-in and you get access to structured logs from the ASP.NET Core host itself to your application. With tools like [Serilog,](https://github.com/serilog/serilog-aspnetcore) you can extend your logging [easily](https://github.com/serilog/serilog-sinks-rollingfile) and save your logs to file, Azure, Amazon or any other output provider. You can configure verbosity and log levels via configuration (appsettings.json by default), and you can configure log levels by different categories.

**Source:** _talkingdotnet.com_

#### Q6: Explain startup process in ASP.NET Core? ⭐⭐
**Answer:**
Everything starts from Program.cs
```csharp
public static void Main(string[] args)
{
    BuildWebHost(args).Run();
}
 
public static IWebHost BuildWebHost(string[] args) =>
    WebHost.CreateDefaultBuilder(args)
        .UseStartup<Startup>()
        .Build();
```

CreateDefaultBuilder extension method will create a default configuration which will look first into `appsettings.json` files then will look for Environment variables and at the end, it will use command line arguments.

This part will also set up default logger sources (debug and console) and load the settings for logging from appsettings.json.

After the `CreateDefaultBuilder` finishes, then `Startup` class is executed. First, the constructor code is executed. After that, services are added to DI container via `AddServices` method that lives in Startup class. After that, an order of middleware that will handle every incoming request is set up.

**Source:** _codingblast.com_

#### Q7: What is the difference between .NET Core and Mono? ⭐⭐
**Answer:**
To be simple:
* Mono is third party implementation of .Net Framework for Linux/Android/iOs
* .Net Core is Microsoft's own implementation for same.

**Source:** _stackoverflow.com_

#### Q8: What is Razor Pages? ⭐⭐
**Answer:**
[Razor Pages](https://codingblast.com/asp-net-core-razor-pages/) is a new feature of ASP.NET Core that makes coding page-focused scenarios easier and more productive.

With Razor Pages, you have this one Razor file (_.cshtml_), and the code for a single page lives inside of that file, and that file also represents the URL structure of the app. Therefore, you got everything inside of one file, and it just works.

However, you can separate your code to the _code behind_ file with _.cshtml.cs_ extension. You would usually have your view model and handlers (like action methods in MVC) in that file and handle the logic there. Of course, you could also have your view model moved to separate place.

Since Razor Pages is part of the MVC stack, you can use anything that comes with MVC inside of our Razor Pages.

**Source:** _codingblast.com_

#### Q9: What are some characteristics of .NET Core? ⭐⭐
**Answer:**
* **Flexible deployment**: Can be included in your app or installed side-by-side user- or machine-wide.

* **Cross-platform**: Runs on Windows, macOS and Linux; can be ported to other OSes. The supported Operating Systems (OS), CPUs and application scenarios will grow over time, provided by Microsoft, other companies, and individuals.

* **Command-line tools**: All product scenarios can be exercised at the command-line.

* **Compatible**: .NET Core is compatible with .NET Framework, Xamarin and Mono, via the .NET Standard Library.

* **Open source**: The .NET Core platform is open source, using MIT and Apache 2 licenses. Documentation is licensed under CC-BY. .NET Core is a .NET Foundation project.

* **Supported by Microsoft**: .NET Core is supported by Microsoft, per .NET Core Support

**Source:** _stackoverflow.com_

#### Q10: What's the difference between SDK and Runtime in .NET Core? ⭐⭐
**Answer:**
* The SDK is all of the stuff that is needed/makes developing a .NET Core application easier, such as the CLI and a compiler.

* The runtime is the "virtual machine" that hosts/runs the application and abstracts all the interaction with the base operating system.

**Source:** _stackoverflow.com_

#### Q11: What about NuGet packages and packages.config? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q12: Explain two types of deployment for .NET Core applications ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q13: What is Kestrel? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q14: What is difference between .NET Core and .NET Framework? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q15: Explain Middleware in ASP.NET Core? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q16: Explain usage of Dependency Injection in ASP.NET Core ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q17: Explain what is included in .NET Core? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q18: Talk about new .csproj file? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q19: What is .NET Standard? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q20: What's the difference between .NET Core, .NET Framework, and Xamarin? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q21: What is new in ASP.NET Core 2, compared to ASP.NET Core 1? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q22: What is the difference between .NET Framework/Core and .NET Standard Class Library project types? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

## [[⬆]](#toc) <a name=AWS>AWS</a> Interview Questions
#### Q1: What is AWS? ⭐
**Answer:**
**AWS** stands for Amazon Web Services and is a platform that provides database storage, secure cloud services, offering to compute power, content delivery, and many other services to develop business levels.

**Source:** _onlineinterviewquestions.com_

#### Q2: Explain the key components of AWS? ⭐
**Answer:**
* **Simple Storage Service (S3)**: S3 is most widely used AWS storage web service.
* **Simple E-mail Service (SES)**: SES is a hosted transactional email service and allows one to fluently send deliverable emails using a RESTFUL API call or through a regular SMTP.
* **Identity and Access Management (IAM)**: IAM provides improved identity and security management for AWS account.
* **Elastic Compute Cloud (EC2)**: EC2 is an AWS ecosystem central piece. It is responsible for providing on-demand and flexible computing resources with a “pay as you go” pricing model.
* **Elastic Block Store (EBS)**: EBS offers continuous storage solution that can be seen in instances as a regular hard drive.
* **CloudWatch**: CloudWatch allows the controller to outlook and gather key metrics and also set a series of alarms to be notified if there is any trouble.

**Source:** _whizlabs.com_

#### Q3: What is buckets in AWS? ⭐
**Answer:**
An Amazon S3 bucket is a public cloud storage resource available in Amazon Web Services' (AWS) Simple Storage Service (S3), an object storage offering. Amazon S3 buckets, which are similar to file folders, store objects, which consist of data and its descriptive metadata.

By default, you can create up to 100 buckets in each of your AWS accounts. If you need more buckets, you can increase your bucket limit by submitting a service limit increase.

**Source:** _whizlabs.com_

#### Q4: What is AWS Cloudfront? ⭐⭐
**Answer:**
Amazon **CloudFront** is a content delivery network (CDN) offered by Amazon Web Services. Content delivery networks provide a globally-distributed network of proxy servers which cache content, such as web videos or other bulky media, more locally to consumers, thus improving access speed for downloading the content.

**Source:** _en.wikipedia.org_

#### Q5: What do you mean by AMI? What does it include? ⭐⭐
**Answer:**
**AMI** stands for the term **Amazon Machine Image**.  It’s an AWS template which provides the information (an application server, and operating system, and applications) required to perform the launch of an instance. This AMI is the copy of the AMI that is running in the cloud as a virtual server.  You can launch instances from as many different AMIs as you need. AMI consists of the followings:

* A root volume template for an existing instance
* Launch permissions to determine which AWS accounts will get the AMI in order to launch the instances
* Mapping for block device to calculate the total volume that will be attached to the instance at the time of launch

**Source:** _whizlabs.com_

#### Q6: How can I download a file from EC2? ⭐⭐
**Answer:**
Use scp:

```sh
scp -i ec2key.pem username@ec2ip:/path/to/file .
```

**Source:** _stackoverflow.com_

#### Q7: Is it possible to clone a EC2 instance data? ⭐⭐
**Answer:**
You can make an AMI of an existing instance, and then launch other instances using that AMI.

**Source:** _stackoverflow.com_

#### Q8: What is AWS Data Pipeline? ⭐⭐
**Answer:**
**AWS Data Pipeline** is a web service that you can use to automate the movement and transformation of data. With AWS Data Pipeline, you can define data-driven workflows, so that tasks can be dependent on the successful completion of previous tasks.

**Source:** _docs.aws.amazon.com_

#### Q9: Explain the features of Amazon EC2 services ⭐⭐
**Answer:**
Amazon EC2 services have following features:

* Virtual Computing Environments
* Proffers Persistent storage volumes
* Firewall validating you to specify the protocol
* Pre-configured templates
* Static IP address for dynamic Cloud Computing

**Source:** _whizlabs.com_

#### Q10: What is the connection between AMI and Instance? ⭐⭐
**Answer:**
Many different types of *instances* can be launched from one *AMI*. The type of an instance generally regulates the hardware components of the host computer that is used for the instance. Each type of instance has distinct computing and memory efficacy.

Once an instance is launched, it casts as host and the user interaction with it is same as with any other computer but we have a completely controlled access to our instances. AWS developer interview questions may contain one or more AMI based questions, so prepare yourself for the AMI topic very well.

**Source:** _whizlabs.com_

#### Q11: Are S3 buckets region specific? ⭐⭐
**Answer:**
Yes, buckets exist in a specific region and you need to specify that region when you create a bucket. Amazon S3 creates bucket in a region you specify. You can choose any AWS region that is geographically close to you to optimize latency, minimize costs, or address regulatory requirements.

**Source:** _stackoverflow.com_

#### Q12: What is AWS Direct Connect? ⭐⭐
**Answer:**
**AWS Direct Connect** bypasses the public Internet and establishes a secure, dedicated connection from your infrastructure into AWS. With established connectivity via AWS Direct Connect, you can access your Amazon VPC and all AWS services.

**Source:** _coresite.com_

#### Q13: What is AWS EBS? ⭐⭐
**Answer:**
**Amazon Elastic Block Store** (Amazon EBS) provides persistent block storage volumes for use with Amazon EC2 instances in the AWS Cloud. Each Amazon EBS volume is automatically replicated within its Availability Zone to protect you from component failure, offering high availability and durability.

**Source:** _aws.amazon.com_

#### Q14: What is AWS Lambda? ⭐⭐
**Answer:**
**AWS Lambda** is a serverless compute service that runs your code in response to events and automatically manages the underlying compute resources for you. You can use AWS Lambda to extend other AWS services with custom logic, or create your own back-end services that operate at AWS scale, performance, and security.

**Source:** _aws.amazon.com_

#### Q15: What is AWS DynamoDB? ⭐⭐
**Answer:**
**Amazon DynamoDB** is a fully managed NoSQL database service that provides fast and predictable performance with seamless scalability. With DynamoDB, you can create database tables that can store and retrieve any amount of data, and serve any level of request traffic.

**Source:** _docs.aws.amazon.com_

#### Q16: What is AWS EMR? ⭐⭐
**Answer:**
**Amazon Elastic MapReduce (EMR)** is an Amazon Web Services (AWS) tool for big data processing and analysis. Amazon EMR offers the expandable low-configuration service as an easier alternative to running in-house cluster computing.

Amazon EMR is based on Apache Hadoop, a Java-based programming framework that supports the processing of large data sets in a distributed computing environment. MapReduce is a software framework that allows developers to write programs that process massive amounts of unstructured data in parallel across a distributed cluster of processors or stand-alone computers.

**Source:** _searchaws.techtarget.com_

#### Q17: Is data stored in S3 is always encrypted? ⭐⭐
**Answer:**
By default data on S3 is not encrypted, but all you could enable server-side encryption in your object metadata when you upload your data to Amazon S3. As soon as your data reaches S3, it is encrypted and stored.

**Source:** _aws.amazon.com_

#### Q18: Can we attach single EBS to multiple EC2s same time? ⭐⭐
**Answer:**
No. After you create a volume, you can attach it to any EC2 instance in the same Availability Zone. An EBS volume can be attached to **only one EC2 instance at a time**, but multiple volumes can be attached to a single instance.

**Source:** _docs.aws.amazon.com_

#### Q19: What is AWS API gateway? ⭐⭐
**Answer:**
Amazon **API Gateway** is an AWS service that enables developers to create, publish, maintain, monitor, and secure APIs at any scale. You can create APIs that access AWS or other web services, as well as data stored in the AWS Cloud.

**Source:** _aws.amazon.com_

#### Q20: What is AWS Direct Connect? ⭐⭐
**Answer:**
Using **AWS Direct Connect**, you can establish private connectivity between AWS and your datacenter, office, or colocation environment, which in many cases can reduce your network costs, increase bandwidth throughput, and provide a more consistent network experience than Internet-based connections.

**Source:** _aws.amazon.com_

#### Q21: What are the security best practices for Amazon EC2 instances? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q22: Can I automatically start and terminate my Amazon instance using Amazon API?  ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q23: Can we still continue working on EBS while creating snapshot of it? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q24: What is AWS Auto Scaling? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q25: What is AWS Auto Scaling group? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q26: What is the maximum size of a single S3 object? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q27: What is AWS bucket policy? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q28: Does AWS has the option for vertical "auto" scaling of EC2 instance? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q29: What is AWS WAF? What are the potential benefits of using WAF? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q30: How to get the instance id from within an EC2 instance? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q31: What is AWS Cloudwatch? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q32: What is the difference between Amazon EC2 and AWS Elastic Beanstalk? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q33: How many storage options are there for EC2 Instance? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q34: What is AWS Route 53? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q35: How would you implement vertical auto scaling of EC2 instance? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q36: What is Amazon Kinesis? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q37: How to find a region from within an EC2 instance? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q38: Where are EC2 snapshots stored? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q39: When should one use the following: Amazon EC2, Google App Engine, Microsoft Azure and Salesforce.com? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q40: When to use Amazon CloudFront and when S3? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q41: Our EC2 micro instance occasionally runs out of memory. Other than using a larger instance size, what else can be done? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q42: What is difference between Lightsail and EC2? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q43: What is the underlying hypervisor for EC2? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q44: How to safely upgrade an Amazon EC2 instance from t1.micro to large? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

## [[⬆]](#toc) <a name=Agile>Agile</a> Interview Questions
#### Q1: Explain what is Refactoring? ⭐
**Answer:**
To improve the performance, the existing code is modified; this is re-factoring. During re-factoring the code functionality remains same.

**Source:** _career.guru99.com_

#### Q2: What is User Stories? ⭐
**Answer:**
**User stories** are features customers might want to see in their software. They are written on index cards to encourage face-to-face communication. Typically no more than a couple days work, they form the basis of our Agile plans.

#### Q3: What is an Agile iteration? ⭐
**Answer:**
An Agile **iteration** is a short one to two week period where a team takes most important user stories,  builds them completely and deliver as running-tested-software to the customer. Analysis, design, coding, testing happen during an iteration.

#### Q4: What is test driven development? ⭐⭐
**Answer:**
**Test driven development (TDD)** is also known as test-driven design. In this method, developer first writes an automated test case which describes new function or improvement and then creates small codes to pass that test, and later re-factors the new code to meet the acceptable standards.

**Source:** _career.guru99.com_

#### Q5: Explain what is Velocity in Agile? ⭐⭐
**Answer:**
**Velocity** is a metric that is calculated by addition of all efforts estimates related with user stories completed in an iteration. It figures out how much work Agile can complete in a sprint and how much time will it need to finish a project.

**Source:** _career.guru99.com_

#### Q6: Explain what does it mean by product roadmap? ⭐⭐
**Answer:**
A **product roadmap** is referred for the holistic view of product features that create the product vision.

**Source:** _career.guru99.com_

#### Q7: What is Agile? ⭐⭐
**Answer:**
**Agile** is a time boxed, **iterative approach (framework) to software delivery** that builds software incrementally from the start of the project, instead of trying to deliver it all at once near the end.

It works by breaking projects down into little bits of user functionality called **user stories**, prioritizing them, and then continuously delivering them in short two week cycles called **iterations**.

Agile refers to any process that aligns with the concepts of the [Agile Manifesto](http://agilemanifesto.org/). 

**Source:** _agilemanifesto.org_

#### Q8: How is Agile different from other software delivery aproaches? ⭐⭐
**Answer:**
* Analysis, design, coding, and testing are continuous activities
* Development is iterative
* Planning is adaptive
* Roles blur
* Scope can vary
* Requirements can change
* Working software is the primary measure of success



#### Q9: Mention what should a burndown chart should highlight? ⭐⭐
**Answer:**
The burn-down chart shows the remaining work to complete before the timebox (iteration) ends.

**Source:** _career.guru99.com_

#### Q10: If a timebox plan needs to be reprioritized who should re-prioritise it? ⭐⭐
**Answer:**
If a timebox plan needs to be reprioritized it should include whole team, product owner, and developers.

**Source:** _career.guru99.com_

#### Q11: What is story points/efforts/ scales? ⭐⭐
**Answer:**
It is used to discuss the difficulty of the story without assigning actual hours. The most common scale used is a Fibonacci sequence (1, 2, 3, 5, 8,1 3,….100) although some teams use linear scale (1, 2, 3, 4….), Powers of 2 (1, 2, 4, 8……) and cloth size (XS, S ,M, L, XL)

**Source:** _career.guru99.com_

#### Q12: Explain in Agile, burn-up and burn-down chart? ⭐⭐
**Answer:**
To track the project progress burnup and burn down, charts are used

* Burnup Chart: It shows the progress of stories done over time
* Burndown Chart: It shows how much work was left to do overtime

**Source:** _career.guru99.com_

#### Q13: Mention what are the challenges involved in Agile software development? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q14: What is the Agile Manifesto? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q15: What does project velocity mean? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q16: Can you explain the purpose of a burndown chart? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q17: Mention what are the advantages of maintaining consistent iteration length throughout the project? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q18: What are four Agile Manifesto values? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q19: What are the qualities of a good Agile tester should have? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q20: What are some methodologies used to implement Agile? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q21: Why Continuous Integration is important for Agile? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q22: Mention what are the Agile quality strategies? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q23: When not to use Agile? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q24: Name the 12 Agile Principles ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q25: In Agile mention what is the difference between the Incremental and Iterative development? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q26: Mention what is the difference between Scrum and Agile? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q27: Explain what is Spike and Zero sprint in Agile? What is the purpose of it? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

## [[⬆]](#toc) <a name=Angular>Angular</a> Interview Questions
#### Q1: What is Routing Guard in Angular? ⭐
**Answer:**
Angular’s route guards are interfaces which can tell the router whether or not it should allow navigation to a requested route. They make this decision by looking for a true or false return value from a class which implements the given guard interface.

**Source:** _medium.com_

#### Q2: What is a module, and what does it contain? ⭐
**Answer:**
An Angular module is set of Angular basic building blocks like component, directives, services etc. An app can have more than one module.

A module can be created using `@NgModule` decorator.

```js
@NgModule({
  imports:      [ BrowserModule ],
  declarations: [ AppComponent ],
  bootstrap:    [ AppComponent ]
})
export class AppModule { }
```

**Source:** _stackoverflow.com_

#### Q3: What are pipes? Give me an example. ⭐
**Answer:**
A **pipe** takes in data as input and transforms it to a desired output. You can chain pipes together in potentially useful combinations. You can write your own custom pipes. Angular comes with a stock of pipes such as `DatePipe`, `UpperCasePipe`, `LowerCasePipe`, `CurrencyPipe`, and `PercentPipe`.

Consider:
```html
<p>The hero's birthday is {{ birthday | date }}</p>
```
In this page, you'll use pipes to transform a component's birthday property into a human-friendly date.

**Source:** _angular.io_

#### Q4: What's the difference between an Angular component and module? ⭐⭐
**Answer:**
*Components* control views (html). They also communicate with other components and services to bring functionality to your app.

*Modules* consist of one or more components. They do not control any html. Your modules declare which components can be used by components belonging to other modules, which classes will be injected by the dependency injector and which component gets bootstrapped. Modules allow you to manage your components to bring modularity to your app.

**Source:** _stackoverflow.com_

#### Q5: What are the differences between AngularJS (angular 1.x) and Angular (Angular 2.x and beyond)? ⭐⭐
**Answer:**
Angular and AngularJS is basically a different framework with the same name.

Angular is more ready for the current state of web standards and the future state of the web (ES6\7, immutiablity, components, shadow DOM, service workers, mobile compatibilty, modules, typescript and so on and so on... )

Angular killed many main features in AngularJS like - controllers, $scope, directives (replaced with `@component` annotations), the module definition, and much more, even simple things like ng-repeat has not left the same as it was.

Also: 
1. They added an angular `cli`.
2. Your angular code is written in ES6 Typescript and it compiles at runtime to Javascript in the browser.
3. You bind to your HTML similarly like how you would if in an Angular 1 directive. So variable like $scope and $rootScope have been deprecated.

**Source:** _stackoverflow.com_

#### Q6: What is a service, and when will you use it? ⭐⭐
**Answer:**
*Angular services* are singleton objects which get instantiated only once during the lifetime of an application. They contain methods that maintain data throughout the life of an application, i.e. data does not get refreshed and is available all the time. The main objective of a service is to organize and share business logic, models, or data and functions with different components of an Angular application.

The *separation of concerns* is the main reason why Angular services came into existence. An Angular service is a stateless object and provides some very useful functions. 

**Source:** _dzone.com_

#### Q7: What is the equivalent of ngShow and ngHide in Angular? ⭐⭐
**Answer:**
Just bind to the `hidden` property

**Source:** _stackoverflow.com_

#### Q8: What is the minimum definition of a component? ⭐⭐
**Answer:**
The absolute minimal configuration for a `@Component` in Angular is a template. Both template properties are set to optional because you have to define either `template` or `templateUrl`.

When you don't define them, you will get an exception like this:
```sh
No template specified for component 'ComponentName'
```
A selector property is not required, as you can also use your components in a route.

**Source:** _stackoverflow.com_

#### Q9: You have an HTML response I want to display. How do I do that?  ⭐⭐
**Answer:**
The correct syntax is the following:
```html
<div [innerHTML]="theHtmlString"></div>
```
Working in `5.2.6`

**Source:** _medium.com_

#### Q10: What is a component? Why would you use it? ⭐⭐
**Answer:**
*Components* are the most basic building block of an UI in an Angular application. An Angular application is a tree of Angular components. Angular components are a subset of directives. Unlike directives, components always have a template and only one component can be instantiated per an element in a template.

A component must belong to an NgModule in order for it to be usable by another component or application. To specify that a component is a member of an NgModule, you should list it in the `declarations` field of that NgModule.

```js
@Component({selector: 'greet', template: 'Hello {{name}}!'})
class Greet {
  name: string = 'World';
}
```

**Source:** _angular.io_

#### Q11: How can I select an element in a component template? ⭐⭐
**Answer:**
You can get a handle to the DOM element via ElementRef by injecting it into your component's constructor:

```js
constructor(myElement: ElementRef) { ... }
```

**Source:** _medium.com_

#### Q12: What is the equivalent of "ngShow" and "ngHide" in Angular? ⭐⭐
**Answer:**
Just bind to the hidden property:

```js
[hidden]="!myVar"
```

**Source:** _medium.com_

#### Q13: What is the difference between *ngIf vs [hidden]? ⭐⭐
**Answer:**
`*ngIf` effectively removes its content from the DOM while `[hidden]` modifies the `display` property and only instructs the browser to not show the content but the DOM still contains it.

**Source:** _medium.com_

#### Q14: What is the difference between "@Component" and "@Directive" in Angular?  ⭐⭐
**Answer:**
* **Directives** add behaviour to an existing DOM element or an existing component instance.
* **A component**, rather than adding/modifying behaviour, actually creates its own view (hierarchy of DOM elements) with attached behaviour.

Write a component when you want to create a reusable set of DOM elements of UI with custom behaviour. Write a directive when you want to write reusable behaviour to supplement existing DOM elements.

**Source:** _medium.com_

#### Q15: What are some differences between Angular 2 and 4? ⭐⭐
**Answer:**
Just to name a few:
* Improvements in AOT, 
* allowing the "else" clause in ngIf, 
* support for TypeScript 2.1
* breaking out the animations package

**Source:** _github.com/WebPredict_

#### Q16: How would you protect a component being activated through the router? ⭐⭐
**Answer:**
The Angular router ships with a feature called guards. These provide us with ways to control the flow of our application. We can stop a user from visitng certain routes, stop a user from leaving routes, and more. The overall process for protecting Angular routes:

* Create a guard service: `ng g guard auth`
* Create `canActivate()` or `canActivateChild()` methods
* Use the guard when defining routes

```js
// import the newly created AuthGuard
const routes: Routes = [
  {
    path: 'account',
    canActivate: [AuthGuard]
  }
];
```

Some other available guards:

* `CanActivate`: Check if a user has access
* `CanActivateChild`: Check if a user has access to any of the child routes
* `CanDeactivate`: Can a user leave a page? For example, they haven't finished editing a post
* `Resolve`: Grab data before the route is instantiated
* `CanLoad`: Check to see if we can load the routes assets

**Source:** _scotch.io_

#### Q17: What does this line do? ⭐⭐
**Details:**
```js
@HostBinding('[class.valid]') isValid;
```

**Answer:**
`@HostBinding` lets you set properties on the element or component that hosts the directive.

The code applies the css class `valid` to whatever is using this directive conditionally based on the value of isValid.

**Source:** _alligator.io_

#### Q18: How would you run unit test? ⭐⭐
**Answer:**
The Angular CLI downloads and install everything you need to test an Angular application with the Jasmine test framework.

The project you create with the CLI is immediately ready to test. Just run this one CLI command:

```sh
ng test
```

**Source:** _angular.io_

#### Q19: When would you use eager module loading? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q20:  Explain the difference between `Promise` and `Observable` in Angular? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q21: How to bundle an Angular app for production? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q22: How to inject base href? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q23: Can you explain the difference between `Promise` and `Observable` in Angular? In what scenario can we use each case? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q24: What is the use of codelyzer? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q25: Why should `ngOnInit` be used, if we already have a `constructor`? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q26: What is difference between "declarations", "providers" and "import" in NgModule? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q27: What is Redux and how does it relate to an Angular app? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q28: What is AOT? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q29: Explain the difference between "Constructor" and "ngOnInit" ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q30: How would you control size of an element on resize of the window in a component? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q31: What is the point of calling "renderer.invokeElementMethod(rendererEl, methodName)"? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q32: What is Reactive Programming and how to use one with Angular? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q33: What's new in Angular 6 and why shall we upgrade to it? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q34: What is Protractor? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q35: What is the difference between `@Component` and `@Directive` in Angular? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q36: Why would you use a spy in a test? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q37: What is TestBed? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q38: How to set headers for every request in Angular? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q39: What does "detectChanges" do in Angular jasmine tests? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q40: Are there any pros/cons (especially performance-wise) in using local storage to replace cookie functionality? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q41: Why would you use renderer methods instead of using native element methods? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q42: When does a lazy loaded module is loaded? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q43: What is the need for SystemJS in Angular? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q44: What would be a good use for NgZone service? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q45: What is Zone in Angular? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q46: Why would you use lazy loading modules in Angular app? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q47: What are the lifecycle hooks for components and directives? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q48: How would you insert an embedded view from a prepared TemplateRef? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q49: How to detect a route change in Angular? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q50: Name and explain some Angular Module Loading examples ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q51: What does a just-in-time (JIT) compiler do (in general)? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q52: How do you create application to use scss? What changed for Angular 6? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q53: When should I store the "Subscription" instances and invoke `unsubscribe()` during the NgOnDestroy life cycle and when can I simply ignore them? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q54: What is ngUpgrage?  ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q55: What is Reactive programming and how does it relate to Angular? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q56: Name some security best practices in Angular ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q57: Could I use jQuery with Angular? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q58: What is the default compilation for Angular 5? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q59: Can Node.js use other engines than V8? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q60: How would you extract webpack config from angular cli project? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q61: What is the difference between BehaviorSubject vs Observable? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q62: What is the Angular equivalent to an AngularJS "$watch"? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q63: Just-in-Time (JiT) vs Ahead-of-Time (AoT) compilation. Explain the difference. ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q64: Do you know how you can run angularJS and angular side by side? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q65: Is there no equivalent to `$scope.emit()` or `$scope.broadcast()` in Angular? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q66: Could you provide some particular examples of using ngZone? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q67: Name some differences between SystemJS vs WebPack? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q68: Why angular uses url segment? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q69: When to use query parameters versus matrix parameters? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

## [[⬆]](#toc) <a name=AngularJS>AngularJS</a> Interview Questions
#### Q1: Why to use AngularJS? ⭐
**Answer:**
There are following reasons to choose AngularJS as a web development framework:

1. It is based on MVC pattern which helps you to organize your web apps or web application properly.
2. It extends HTML by attaching directives to your HTML markup with new attributes or tags and expressions
in order to define very powerful templates.
3. It also allows you to create your own directives, making reusable components that fill your needs and
abstract your DOM manipulation logic.
4. It supports two-way data binding i.e. connects your HTML (views) to your JavaScript objects (models)
seamlessly. In this way any change in model will update the view and vice versa without any DOM
manipulation or event handling.
5. It encapsulates the behavior of your application in controllers which are instantiated with the help of
dependency injection.
6. It supports services that can be injected into your controllers to use some utility code to fullfil your need.
For example, it provides $http service to communicate with REST service.
7. It supports dependency injection which helps you to test your angular app code very easily.
8. Also, AngularJS is mature community to help you. It has widely support over the internet.

**Source:** _github.com/krosti_

#### Q2: What is the difference between "ng-show"/"ng-hide" and "ng-if" directives? ⭐
**Answer:**
`ng-show`/`ng-hide` will always insert the DOM element, but will display/hide it based on the condition. `ng-if` will not insert the DOM element until the condition is not fulfilled.

`ng-if` is better when we needed the DOM to be loaded conditionally, as it will help load page bit faster compared to `ng-show`/`ng-hide`.

We only need to keep in mind what the difference between these directives is, so deciding which one to use totally depends on the task requirements.


**Source:** _codementor.io_

#### Q3: Does AngularJS has dependency on jQuery? ⭐⭐
**Answer:**
AngularJS has no dependency on jQuery library. But it can be used with jQuery library.

**Source:** _ github.com/krosti_

#### Q4: How do you hide an HTML element via a button click in AngularJS? ⭐⭐
**Answer:**
This can be done by using the `ng-hide` directive in conjunction with a controller to hide an HTML element on button click.

```html
<div ng-controller="MyCtrl">
    <button ng-click="hide()">Hide element</button>
    <p ng-hide="isHide">Hello World!</p>
</div>
```

```js
function MyCtrl($scope) {
	$scope.isHide = false;
	$scope.hide = function () {
		$scope.isHide = true;
	};
}
```
    

**Source:** _codementor.io_

#### Q5: What is a singleton pattern and where we can find it in AngularJS? ⭐⭐
**Answer:**
Is a great pattern that restricts the use of a class more than once. We can find singleton pattern in angular in dependency injection and in the services.

In a sense, if the you do 2 times `new Object()` without this pattern, the you will be alocating 2 pieces of memory for the same object. With singleton pattern, if the object exists, it'll be reused.

**Source:** _codementor.io_

#### Q6: What are the AngularJS features? ⭐⭐
**Answer:**
The features of AngularJS are listed below:

1. Modules
2. Directives
3. Templates
4. Scope
5. Expressions
6. Data Binding
7. MVC (Model, View & Controller)
8. Validations
9. Filters
10. Services
11. Routing
12. Dependency Injection
13. Testing

**Source:** _github.com/krosti_

#### Q7: When dependent modules of a module are loaded? ⭐⭐
**Answer:**
A module might have dependencies on other modules. The dependent modules are loaded by angular
before the requiring module is loaded.

In other words the configuration blocks of the dependent modules execute before the configuration blocks of the requiring module. The same is true for the run blocks. Each module can only be loaded once, even if multiple other modules require it.

**Source:** _github.com/krosti_

#### Q8: What is Angular’s prefixes $ and $$? ⭐⭐
**Answer:**
To prevent accidental name collisions with your code, Angular prefixes names of public objects with $ and names of private objects with `$$`. So, do not use the `$` or `$$` prefix in your code.

**Source:** _github.com/krosti_

#### Q9: What are Filters in AngularJS? ⭐⭐
**Answer:**
*Filters* are used to format data before displaying it to the user. They can be used in view templates, controllers, services and directives. There are some built-in filters provided by AngularJS like as `Currency`, `Date`, `Number`, `OrderBy`, `Lowercase`, `Uppercase` etc. You can also create your own filters.

Filter Syntax:

```{{ expression | filter}}```

**Source:** _github.com/krosti_

#### Q10: What are Directives in AngularJS? ⭐⭐
**Answer:**
AngularJS directives are a combination of AngularJS template markups (HTML attributes or elements, or CSS classes) and supporting JavaScript code. The JavaScript directive code defines the template data and behaviors of the HTML elements.

AngularJS directives are used to extend the HTML vocabulary i.e. they decorate html elements with new behaviors and help to manipulate html elements attributes in interesting way.

There are some built-in directives provided by AngularJS like as ng-app, ng-controller, ng-repeat, ng-model etc.


**Source:** _github.com/krosti_

#### Q11: What are Directives? ⭐⭐
**Answer:**
**Directives** are markers on a DOM element (such as an attribute, element name, comment or CSS class) that tell AngularJS’s HTML compiler ($compile) to attach a specified behavior to that DOM element (e.g. via event listeners), or even to transform the DOM element and its children. 

Angular comes with a set of these directives built-in, like `ngBind`, `ngModel`, and `ngClass`. Much like you create controllers and services, you can create your own directives for Angular to use. When Angular bootstraps your application, the HTML compiler traverses the DOM matching directives against the DOM elements.

**Source:** _codementor.io_

#### Q12: Explain what is a "$scope" in AngularJS ⭐⭐
**Answer:**
**Scope** is an object that refers to the application model. It is an execution context for expressions. Scopes are arranged in hierarchical structure which mimic the DOM structure of the application. Scopes can watch expressions and propagate events. Scopes are objects that refer to the model. They act as glue between controller and view.

**Source:** _codementor.io_

#### Q13: What directive would you use to hide elements from the HTML DOM by removing them from that DOM not changing their styling? ⭐⭐
**Answer:**
The `ngIf` Directive, when applied to an element, will remove that element from the DOM if it’s condition is false.

**Source:** _codementor.io_

#### Q14: What is the difference between one-way binding and two-way binding? ⭐⭐
**Answer:**
* One way binding implies that the scope variable in the html will be set to the first value its model is bound to (i.e. assigned to)  
* Two way binding implies that the scope variable will change it’s value everytime its model is assigned to a different value

**Source:** _codementor.io_

#### Q15: What is auto bootstrap process in AngularJS? ⭐⭐
**Answer:**
Angular initializes automatically upon ```DOMContentLoaded``` event or when the angular.js script is downloaded to the browser and the ```document.readyState``` is set to ```complete```. At this point AngularJS looks for the ```ng-app``` directive which is the root of angular app compilation and tells about AngularJS part within DOM. When the ```ng-app``` directive is found then Angular will:

1. Load the module associated with the directive.
2. Create the application injector.
3. Compile the DOM starting from the ng-app root element.
This process is called auto-bootstrapping.

```html
<html>
<body ng-app="myApp">
<div ng-controller="Ctrl"> Hello {{msg}}!
</div>
    <script src="lib/angular.js"></script>
    <script>
var app = angular.module('myApp', []); app.controller('Ctrl', function ($scope) {
              $scope.msg = 'World';
          });
    </script>
</body>
</html>
```

**Source:** _github.com/krosti_

#### Q16: How would you specify that a scope variable should have one-time binding only? ⭐⭐
**Answer:**
By using “`::`” in front of it. 

**Source:** _codementor.io_

#### Q17: What is scope in AngularJS? ⭐⭐
**Answer:**
Scope is a JavaScript object that refers to the application model. It acts as a context for evaluating angular expressions. Basically, it acts as glue between controller and view.

Scopes are hierarchical in nature and follow the DOM structure of your AngularJS app. AngularJS has two scope objects: **$rootScope** and **$scope**.

**Source:** _github.com/krosti_

#### Q18: How do you disable a button depending on a checkbox’s state? ⭐⭐
**Answer:**
We can use the `ng-disabled` directive and bind its condition to the checkbox’s state.

```html
<body ng-app>
    <label>
        <input type="checkbox" ng-model="checked" />Disable Button
    </label>
    <button ng-disabled="checked">Select me</button>
</body>
```
    

**Source:** _codementor.io_

#### Q19: What is scope hierarchy? ⭐⭐
**Answer:**
The **$scope** object used by views in AngularJS are organized into a hierarchy. There is a root scope, and the **$rootScope** can has one or more child scopes. Each controller has its own **$scope** (which is a child of the **$rootScope**), so whatever variables you create on $scope within controller, these variables are accessible by the view based on this controller.

For example, suppose you have two controllers: ParentController and ChildController as given below:
```html
<html>
  <head>
    <script src="lib/angular.js"></script>
    <script>
      var app = angular.module('ScopeChain', []); app.controller("parentController", function ($scope) {
      	$scope.managerName = 'Shailendra Chauhan';
      	$scope.$parent.companyName = 'Dot Net Tricks'; //attached to $rootScope
      });
      app.controller("childController", function ($scope, $controller) {
                 $scope.teamLeadName = 'Deepak Chauhan';
             });
         
    </script>
  </head>
  <body ng-app="ScopeChain">
    <div ng-controller="parentController ">
      <table style="border:2px solid #e37112">
        <caption>Parent Controller</caption>
        <tr>
          <td>Manager Name</td>
          <td>{{managerName}}</td>
        </tr>
        <tr>
          <td>Company Name</td>
          <td>{{companyName}}</td>
        </tr>
        <tr>
          <td>
            <table ng-controller="childController" style="border:2px solid #428bca">
              <caption>Child Controller</caption>
              <tr>
                <td>Team Lead Name</td>
                <td>{{ teamLeadName }}</td>
              </tr>
              <tr>
                <td>Reporting To</td>
                <td>{{managerName}}</td>
              </tr>
              <tr>
                <td>Company Name</td>
                <td>{{companyName}}</td>
              </tr>
            </table>
          </td>
        </tr>
      </table>
    </div>
  </body>
</html>
```


**Source:** _github.com/krosti_

#### Q20: How do you share data between controllers? ⭐⭐
**Answer:**
Create an AngularJS service that will hold the data and inject it inside of the controllers.

Using a service is the cleanest, fastest and easiest way to test. However, there are couple of other ways to implement data sharing between controllers, like:

– Using `events`  
– Using `$parent`, `nextSibling`, `controllerAs`, etc. to directly access the controllers  
– Using the `$rootScope` to add the data on (not a good practice)

The methods above are all correct, but are not the most efficient and easy to test.

**Source:** _codementor.io_

#### Q21: What are the basic steps to unit test an AngularJS filter? ⭐⭐
**Answer:**
* Inject the module that contains the filter.
* Provide any mocks that the filter relies on.
* Get an instance of the filter using `$filter('yourFilterName')`.
* Assert your expectations.

**Source:** _codementor.io_

#### Q22: What are the basic steps to unit test an AngularJS filter? ⭐⭐
**Answer:**
1.  Inject the module that contains the filter.
2.  Provide any mocks that the filter relies on.
3.  Get an instance of the filter using `$filter('yourFilterName')`.
4.  Assert your expectations.

**Source:** _codementor.io_

#### Q23:  What are the advantage of AngularJS? ⭐⭐
**Answer:**
There are following advantages of AngularJS:

1. **Data Binding** - AngularJS provides a powerful data binding mechanism to bind data to HTML elements by using scope.
2. **Customize & Extensible** - AngularJS is customized and extensible as per you requirement. You can create your own custom components like directives, services etc.
3. **Code Reusability** - AngularJS allows you to write code which can be reused. For example custom directive which you can reuse.
4. **Support** – AngularJS is mature community to help you. It has widely support over the internet. Also, AngularJS is supported by Google which gives it an advantage.
5. **Compatibility** - AngularJS is based on JavaScript which makes it easier to integrate with any other JavaScript library and runnable on browsers like IE, Opera, FF, Safari, Chrome etc.
6. **Testing** - AngularJS is designed to be testable so that you can test your AngularJS app components as easy as possible. It has dependency injection at its core, which makes it easy to test.

**Source:** _github.com/krosti_

#### Q24: Explain what is services in AngularJS ⭐⭐
**Answer:**
In AngularJS *services* are the singleton objects or functions that are used for carrying out specific tasks.  It holds some business logic and these function can be called as controllers, directive, filters and so on.

**Source:** _github.com/krosti_

#### Q25: Explain what is directive and mention what are the different types of Directive? ⭐⭐
**Answer:**
During compilation process when specific HTML constructs are encountered a behaviour or function is triggered, this function is referred as *directive*.  It is executed when the compiler encounters it in the DOM.

Different types of directives are:

* Element directives
* Attribute directives
* CSS class directives
* Comment directives

**Source:** _guru99.com_

#### Q26: How would you validate a text input field for a twitter username, including the @ symbol? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q27: Explain what is the difference between link and compile in AngularJS? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q28: How would you react on model changes to trigger some further action?  ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q29: What is jQLite/jQuery Lite? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q30: What should be the maximum number of concurrent “watches”? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q31: What is a digest cycle in AngularJS? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q32: Where should we implement the DOM manipulation in AngularJS? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q33: Is it a good or bad practice to use AngularJS together with jQuery? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q34: If you were to migrate from Angular 1.4 to Angular 1.5, what is the main thing that would need refactoring? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q35:  Explain what Angular JS routes does? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q36: Explain what is Angular Expression? Explain what is key difference between angular expressions and JavaScript expressions? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q37: What is restrict option in directive? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q38: How would you make an Angular service return a promise? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q39: What is the role of services in AngularJS and name any services made available by default? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q40: How do you reset a "$timeout", "$interval()", and disable a "$watch()"? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q41: What are different ways to invoke a directive? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q42: What is the role of ng-app, ng-init and ng-model directives? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q43: How to access jQLite? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q44: What is an interceptor? What are common uses of it? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q45: What is manual bootstrap process in AngularJS? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q46: What makes the `angular.copy()` method so powerful? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q47: Explain what is linking function and type of linking function? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q48: Explain what is injector? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q49: When creating a directive, it can be used in several different ways in the view. Which ways for using a directive do you know? How do you define the way your directive will be used? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q50: When should you use an attribute versus an element? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q51: Explain what is DI (Dependency Injection ) and how an object or function can get a hold of its dependencies? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q52: Explain how `$scope.$apply()` works? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q53: How AngularJS is compiled? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q54: What is DDO (Directive Definition Object)? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q55: Can you define multiple restrict options on a directive? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q56: What is the difference between $scope and scope? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q57: How would you implement application-wide exception handling in your Angular app? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q58:  What is $scope and $rootScope? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q59: How would you programatically change or adapt the template of a directive before it is executed and transformed? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q60: How AngularJS compilation is different from other JavaScript frameworks? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q61: How Directives are compiled? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q62: What are Compile, Pre and Post linking in AngularJS? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

## [[⬆]](#toc) <a name=Azure>Azure</a> Interview Questions
#### Q1: What are the benefits of severless applications? ⭐
**Answer:**
* Avoid managing servers
* Flexible scaling by demand
* Pay for time and resources it takes to execute your code

#### Q2: What is Azure Cloud Service? ⭐
**Answer:**
By creating a cloud service, you can deploy a multi-tier web application in Azure, defining multiple roles to distribute processing and allow flexible scaling of your application. A cloud service consists of one or more web roles and/or worker roles, each with its own application files and configuration. Azure Websites and Virtual Machines also enable web applications on Azure. The main advantage of cloud services is the ability to support more complex multi-tier architectures

**Source:** _mindmajix.com_

#### Q3: What is a web role? ⭐
**Answer:**
A web role provides a dedicated Internet Information Services (IIS) web-server used for hosting front-end web applications.

**Source:** _mindmajix.com_

#### Q4: What is Azure Functions? ⭐
**Answer:**
Azure Functions is a solution for easily running small pieces of code, or "functions," in the cloud. We can write just the code we need for the problem at hand, without worrying about a whole application or the infrastructure to run it and use language of our choice such as C#, F#, Node.js, Java, or PHP. Azure Functions lets us develop serverless applications on Microsoft Azure.

#### Q5: What is serverless computing? ⭐
**Answer:**
Serverless computing is the abstraction of servers, infrastructure, and operating systems. When you build serverless apps you don’t need to provision and manage any servers, so you can take your mind off infrastructure concerns. Serverless computing is driven by the reaction to events and triggers happening in near-real-time—in the cloud. 

As a fully managed service, server management and capacity planning are invisible to the developer and billing is based just on resources consumed or the actual time your code is running.

#### Q6: What is Azure Resource Group? ⭐⭐
**Answer:**
Resource groups (RG) in Azure is an approach to group a collection of assets in logical groups for easy or even automatic provisioning, monitoring, and access control, and for more effective management of their costs. The underlying technology that powers resource groups is the Azure Resource Manager (ARM).

**Source:** _onlinetech.com_

#### Q7: What is Kudu? ⭐⭐
**Answer:**
Every Azure App Service web application includes a "hidden" service site called **Kudu**.

Kudu Console for example is a debugging service for Azure platform which allows you to explore your web app and surf the bugs present on it, like deployment logs, memory dump, and uploading files to your web app, and adding JSON endpoints to your web apps, etc.


#### Q8: What is a role instance? ⭐⭐
**Answer:**
A role instance is a virtual machine on which the application code and role configuration run. A role can have multiple instances, defined in the service configuration file.

**Source:** _mindmajix.com_

#### Q9: What is a guest operating system? ⭐⭐
**Answer:**
The guest operating system for a cloud service is the operating system installed on the role instances (virtual machines) on which your application code runs.

**Source:** _mindmajix.com_

#### Q10: What is Azure Blob Storage? ⭐⭐
**Answer:**
*Azure Blob storage* is Microsoft's object storage solution for the cloud. Blob storage is optimized for storing massive amounts of unstructured data, such as text or binary data. Azure Storage offers three types of blobs:
* **Block blobs** store text and binary data, up to about 4.7 TB. Block blobs are made up of blocks of data that can be managed individually.
* **Append blobs** are made up of blocks like block blobs, but are optimized for append operations. Append blobs are ideal for scenarios such as logging data from virtual machines.
* **Page blobs** store random access files up to 8 TB in size. Page blobs store the VHD files that back VMs.


**Source:** _docs.microsoft.com_

#### Q11: How to include external dll into Azure Function? ⭐⭐
**Answer:**
* Add the assembly to the BIN directory using KUDU
* Include the assembly and code the Azure Function to use it
* Add the using declaration so that the methods within the DLL can be accessed. 

```cs
#r "D:\home\site\wwwroot\GreetingsAssemblyReference\bin\benjamin.dll"

using benjamin;
```

#### Q12: Is Azure Table Storage Nosql? ⭐⭐
**Answer:**
**Azure Table storage** is a service that stores structured NoSQL data in the cloud, providing a key/attribute store with a schemaless design.

**Source:** _docs.microsoft.com_

#### Q13: What is an Azure subscription? ⭐⭐
**Answer:**
A Windows **Azure subscription** grants you access to Windows Azure services and to the Windows Azure Platform Management Portal. A Windows Azure subscription has two aspects: 
* The Windows Azure account, through which resource usage is reported
* Services are billed.

**Source:** _blogs.msdn.microsoft.com_

#### Q14: What is Azure ARM? ⭐⭐
**Answer:**
The **Azure Resource Manager (ARM)** is the service used to provision resources in your Azure subscription. It was first announced at Build 2014 when the new Azure portal ( portal.azure.com) was announced and provides a new set of API's that are used to provision resources. The ARM is:

* Template-driven – Using templates to deploy all resources.
* Declarative – You declare the resources you want to have instead of imperative where you need to make rules.
* Idempotent – You can deploy the template over and over again without affecting the current state of resources.
* Multi-service – All services can be deployed using Azure Resource Manager, Website, Storage, VMs etc.
* Multi region - You can choose in which region you would like to deploy the resources.
* Extensible – Azure Resource Manager is extensible with more resource providers and thus resources.


**Source:** _azurestack.blog_

#### Q15: Explain the Azure ARM Templates ⭐⭐
**Answer:**
An Azure Resource Template is a JSON file used to deploy resources with Azure Resource Manager. It defines:
* Parameters
* Variables
* Resources - the actual resources that you are going to deploy or update
* Outputs

**Source:** _onlinetech.com_

#### Q16: What is a cloud service role? ⭐⭐
**Answer:**
A cloud service role is comprised of application files and a configuration. A cloud service can have two types of roles:
* web role
* worker role

**Source:** _mindmajix.com_

#### Q17: What is Azure Redis Cache? ⭐⭐
**Answer:**
*Redis* is an open source (BSD licensed), in-memory data structure store, used as a database, cache and message broker. **Azure Redis Cache** is based on the popular open-source Redis cache. It gives you access to a secure, dedicated Redis cache, managed by Microsoft, and accessible from any application within Azure. It supports data structures such as strings, hashes, lists, sets, sorted sets with range queries, bitmaps, hyperloglogs and geospatial indexes with radius queries.

**Source:** _quora.com_

#### Q18: What is Azure Service Fabric? ⭐⭐
**Answer:**
**Azure Service Fabric** is a distributed systems platform that makes it easy to package, deploy, and manage scalable and reliable micro-services. Service Fabric also addresses the significant challenges in developing and managing cloud applications. Developers and administrators can avoid complex infrastructure problems and focus on implementing mission-critical, demanding workloads that are scalable, reliable, and manageable. Service Fabric represents the next-generation middleware platform for building and managing these enterprise-class, tier-1, cloud-scale applications.

**Source:** _quora.com_

#### Q19: How can I use applications with Azure AD that I’m using on-premises? ⭐⭐
**Answer:**
*Azure AD* gives you an easy and secure way to connect to the web applications you choose. You can access these applications in the same way you access your SaaS apps in Azure AD, no need for a VPN to change your network infrastructure.

**Source:** _quora.com_

#### Q20: What Is Azure Key Vault? ⭐⭐
**Answer:**
**Key Vault** help you safeguard cryptographic keys and other secrets used by your applications whenever they are On-Premise or in the cloud. More and more services on Azure are now integrating Azure Key Vault as their secret/key source for things like deployments, data or even disk encryption.

**Source:** _codeisahighway.com_

#### Q21: What is a Blob Container? ⭐⭐
**Answer:**
A container organizes a set of blobs, similar to a folder in a file system. All blobs reside within a container. A storage account can contain an unlimited number of containers, and a container can store an unlimited number of blobs.

**Source:** _docs.microsoft.com_

#### Q22: How can you stop a VM using Power Shell? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q23: How can you retrieve the state of a particular VM? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q24: How can one create a VM in Azure CLI? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q25: What do you know about Azure WebJobs? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q26: What is a worker role? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q27: How can one create a Virtual Machine in Powershell? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q28: How much storage can I use with a virtual machine? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q29: Is it possible to add an existing VM to an availability set? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q30: What is deployment environments? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q31: What is Azure VPN? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q32: What is the difference between Service Bus Queues and Storage Queues? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q33: What are the differences between Subscription Administrator and Directory Administrator? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q34: What is a VNet? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q35: What are stateful and stateless microservices for Service Fabric? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q36: What is key vault in Azure? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q37: Do scale sets work with Azure availability sets? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q38: What are Network Security Groups? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q39: What are Update Domains? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q40: What are Fault Domains? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q41: What is an Availability Set? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q42: What are virtual machine scale sets in Azure? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q43: What is Azure MFA? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q44: What are Cloud Service Roles and why do we use them? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q45: What is Azure Table Storage? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q46: What is Azure Resource Manager and why we need to use one? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q47: What is Azure Search? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q48: What are Redis databases? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q49: Is it possible to create a Virtual Machine using Azure Resource Manager in a Virtual Network that was created using classic deployment? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q50: How to create a new storage account and container using Power Shell? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q51:  What is the meaning of application partitions? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q52: What is Azure VNET? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q53: What is the difference between “price,” “software price,” and “total price” in the cost structure for Virtual Machine offers in the Azure Marketplace? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q54: How to create a Network Security Group and a Network Security Group Rule? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q55: How are Azure Marketplace subscriptions priced? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q56: Explain Azure NSG ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q57: What VPN types are supported by Azure? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q58: What are special Azure Regions? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

## [[⬆]](#toc) <a name=Behavioral>Behavioral</a> Interview Questions
#### Q1: How do you spend your time outside work? ⭐
**Answer:**


#### Q2: What are your hobbies? ⭐
**Answer:**


#### Q3: Why do you want to work for X company? ⭐
**Answer:**
The interviewer is looking for similar things whether asking about company or position. The hiring manager wants to:

* Learn about your career goals and how this position fits into your plan
* Make sure that you are sincerely interested in the job and will be motivated to perform if hired
* Find out what you know about the company, industry, position (and if you took the time to research)
* Understand your priorities and preferences — which aspects of the company and/or job are appealing to you and why?

**Source:** _github.com/yangshun/tech-interview-handbook_

#### Q4: Why do you want to leave your current/last company? ⭐
**Answer:**
Here are some things your interviewer is likely looking for:

* Did you leave for a good reason?
* Did you leave voluntarily?
* Did you leave on good terms?
* What are your work values?

**Source:** _biginterview.com_

#### Q5: A hammer and a nail cost $1.10 together, and the hammer costs one dollar more than the nail. How much does the nail cost? ⭐
**Answer:**


**Source:** _startups.co_

#### Q6: What are you looking for in your next role? ⭐
**Answer:**


**Source:** _github.com/yangshun/tech-interview-handbook_

#### Q7: How large was the last team that you worked on? ⭐
**Answer:**


#### Q8: Why are you interested in this opportunity? ⭐
**Answer:**


#### Q9: Do you plan to advance your education while working here? ⭐
**Answer:**


#### Q10: Tell me the story of how you became who you are today and what made you apply to X. ⭐
**Answer:**


#### Q11: State an experience about how you solved a technical problem. Be specific about the diagnosis and process. ⭐⭐
**Answer:**


#### Q12: Why do you want to come work at a startup, as opposed to an established company? ⭐⭐
**Answer:**


#### Q13: What does "belong anywhere" mean to you? ⭐⭐
**Answer:**


#### Q14: What are you excited about? ⭐⭐
**Answer:**


#### Q15: What project are you currently working on? ⭐⭐
**Answer:**


#### Q16: Do prefer to work at a single company for a long time or would you rather take a job that suits you at the time? ⭐⭐
**Answer:**


#### Q17: Can you give an example of a career goal that you set and how you went about meeting it? ⭐⭐
**Answer:**


#### Q18: How quickly can you learn to use a new technology? ⭐⭐
**Answer:**


#### Q19: Share one of your trips with us. ⭐⭐
**Answer:**


#### Q20: What is your biggest strength and area of growth? ⭐⭐
**Answer:**


#### Q21: Why do people resist change? ⭐⭐
**Answer:**


**Source:** _github.com_

#### Q22: Can you list any deal breakers that would deter you from working for an employer? ⭐⭐
**Answer:**


#### Q23: How do you deal with difficult coworkers? Think about specific instances where you resolved conflicts. ⭐⭐
**Answer:**


#### Q24: Are you more interested in a career that offers great compensation, flexibility or the chance to do something meaningful? ⭐⭐
**Answer:**


#### Q25: If someone has a different viewpoint to do a project like different programming language, how would handle this situation? ⭐⭐
**Answer:**


#### Q26: What was the most fun thing you did recently? ⭐⭐
**Answer:**


#### Q27: Have you worked in a distributed team before? What challenges did you face? ⭐⭐
**Answer:**


#### Q28: What’s are your favorite five apps? ⭐⭐
**Answer:**


#### Q29: What are your personal goals? ⭐⭐
**Answer:**


#### Q30: What have you built as your side project? ⭐⭐
**Answer:**


#### Q31: What is the hardest technical problem you have run into? ⭐⭐
**Answer:**


#### Q32: How do you stay up to date with the latest technologies? ⭐⭐
**Answer:**


#### Q33: What would your previous boss say your biggest strength was? ⭐⭐
**Answer:**


#### Q34: Why do you think you’re a good fit for this company? ⭐⭐
**Answer:**


#### Q35: Tell me about your last project - what worked and what didn’t? ⭐⭐
**Answer:**


#### Q36:  Can you tell me what part of your resume you are most proud of? ⭐⭐
**Answer:**


#### Q37: Tell me a situation where you would have done something differently from what you actually did. ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q38: If you were to open your own business in the future, what kind of business will you open and why? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q39: Tell me about a time in which you had a conflict and needed to influence somebody else. ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q40: What does your best day of work look like? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q41: What is something that you had to push for in your previous projects? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q42: Tell me about a time your work responsibilities got a little overwhelming. What did you do? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q43: Tell me about a challenge you faced recently in your role. How did you tackle it? What was the outcome? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q44: Where do you want to be in five years? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q45: What does it mean to be a "Professional Developer"? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q46: Would you rather be good at a lot of things or an expert at one thing? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q47: How did you win over the difficult employees? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q48: What are your three strengths and three weaknesses? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q49: Would you prefer working on Green Field or Brown Field projects? Why? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q50: What large problems in the world would you solve today? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q51: Describe company X to your grandmother. ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q52: Tell me a time when you predicted something. ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q53: What makes good code good? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q54: If you had an unlimited budget and you could go somewhere, where would you go? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q55: Explain me your toughest project and the working architecture. ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q56: What is something that you don't want from your last internship/job? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q57: Tell me something you are learning right now. ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q58: What is the best gift you have ever given or received? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q59: What’s the most difficult part of being a member of a team for you? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q60:  What can you actually do for us? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q61: What frustrates you? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q62: Can you explain this gap in your resume? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q63: Tell me about a time when you had a conflict with a co-worker. ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q64: In my professional experience have you worked on something without getting approval from your manager? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q65: What’s the best advice you’ve recently received? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q66: How do you respond to constructive criticism? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q67: What are some of the new ideas you would implement in this position? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q68: What are some of the best and worst things about your current company? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q69: Tell me about a time you needed information from someone who wasn't responsive. What did you do? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q70: What is the most exceedingly bad misstep you've made at any point? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q71: How do you deal with a failed deadline? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q72: What books have inspired you in you live? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q73:  What is the biggest mistake that you made in your last position? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q74: Are you comfortable assuming responsibilities outside your job description? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q75: Tell me something about yourself and why you'd be a good fit for the position. ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q76: Apart from technical knowledge, what did you learn during your work at Y? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q77: What is something new that you can teach your interviewer in a few minutes? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q78: If you had an unlimited budget and you could buy one gift for one person, what would you buy and who would you buy it for? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q79: Talk about a project you are most passionate about, or one where you did your best work. ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q80: Do you prefer to work in a team or individually? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q81: Imagine it is your first day here at the company. What do you want to work on? What features would you improve on? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q82: How do you tackle challenges? Name a difficult challenge you faced while working on a project, how you overcame it, and what you learned. ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q83: What was the most difficult bug that you fixed in the past 6 months? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q84: Explain streaming and how you would implement it. ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q85: What is the most challenging aspect of your current project? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q86: Name a situation where you were impressed by a company's customer service. ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q87: What is something you had to persevere at for multiple months? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q88: What is your superpower? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q89:  In one word, describe yourself. ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q90: What is the most constructive feedback you have received in your career? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q91: Who do you look to as a role model? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q92: What is something 90% of people disagree with you about? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q93: Tell me about a time you had a disagreement with your manager. ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q94: What are the most interesting projects you have worked on and how might they be relevant to this company's environment? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q95: Tell me about a time you were uncomfortable and how you dealt with it. ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q96: What risks do you feel you should never take? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q97: Imagine there's a perfect clone of yourself. Imagine that that clone is your boss. Would you like to work for him/her? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q98: Interview me ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q99: Why are Quora's answers better than Yahoo Answers' ones? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q100: Let's play a game: defend Cobol against modern languages, and try to find as many reasonable arguments as you can. ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q101: Where will you be in 10 years? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q102: You are my boss and I'm fired. Inform me. ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q103: I want to refactor a legacy system. You want to rewrite it from scratch. Argument. Then, switch our roles. ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q104: Your boss asks you to lie to the Company. What's your reaction? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q105: If you could travel back in time, which advice would you give to your younger self? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q106: What would happen if you put a mirror in a scanner? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q107: As a software engineer you want both to innovate and to be predictable. How those 2 goals can coexist in the same strategy? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q108: Is developing software an art, a craftsmanship or an engineering endeavour? Your opinion. ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q109: If you were given $1 million dollars every year for the rest of your life, what would you do? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q110: Tell me about a time you had to give someone terrible news. ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q111: What is broken around you? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q112: What is the craziest thing you’ve ever done? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

## [[⬆]](#toc) <a name=Bootstrap>Bootstrap</a> Interview Questions
#### Q1: Explain Bootstrap? ⭐
**Answer:**
Bootstrap is a platform for web development that is based on front-end framework
and creates exceptional responsive designs. It is fast, easy and has multiple
templates designed using HTML, and CSS. These templates are used for forms,
tables, buttons, typography, modals, tables, navigation, carousels and images.
Bootstrap also has Javascript plugins, which are optional. Bootstrap is
preferred for developing mobile web applications.

**Source:** _medium.com/@onlineinerview_

#### Q2: Explain what is Bootstrap? ⭐
**Answer:**
Bootstrap is CSS/Javascript framework for building the rich web applications with
minimal effort. This framework emphasis more on building mobile web
applications.

**Source:** _medium.com/@alisonbenhar_

#### Q3: Explain the two codes that are used for code display in Bootstrap? ⭐⭐
**Answer:**
There are two simple ways to display a code in Bootstrap:

* `<code>` tag: In case you wish to display an inline code
* `<pre>` tag: In case you have a code with several lines or even a block element

**Source:** _medium.com/@onlineinerview_

#### Q4: What are the types of layout available in Bootstrap? ⭐⭐
**Answer:**
In Bootstrap there are two types of Layout available

* Fluid Layout: Fluid layout is used when you want to create a app that is 100%
wide and use up all the width of the screen
* Fixed Layout: For a standard screen you will use fixed layout (940 px) option

**Source:** _medium.com/@alisonbenhar_

#### Q5: What will be the output of the following HTML code ⭐⭐
**Answer:**
**Consider:**
```js
<ul class="list-unstyled">
  <li>Item 1</li>
  <li>Item 2</li>
    <ul>
      <li>Nested item 2.1</li>
      <li>Nested item 2.2</li>
      <li>Nested item 2.3</li>
    </ul>     
  <li>Item 3</li>
</ul>
```
What will be the output of the following HTML code?

**Answer:**

If we apply `.list-unstyled` to a list, it will remove the default list-style and left margin on the list items. But *only* for the immediate children. Main list items will be without any style, and nested list items will still have default unordered nested list-style.

**Source:** _toptal.com_

#### Q6: Explain why you prefer Bootstrap for website development? ⭐⭐
**Answer:**
Bootstrap has features that are way better than other web development platforms.
It provides an extensive browser support for almost every known browser such as
Opera, Chrome, Firefox, Safari etc. With adequate knowledge of CSS and HTML, web
development becomes easy on Bootstrap. Also, it supports mobile applications
with the help of responsive design. It can adjust CSS as per the device, screen
size etc. Instead of creating multiple files, it creates only a single file,
which reduces any extra effort by the developer.

**Source:** _medium.com/@onlineinerview_

#### Q7: What are the key components of Bootstrap? ⭐⭐
**Answer:**
In total, there are five key components of Bootstrap i.e. **CSS** (multiple CSS
files), **Scaffolding (**essential for the basic system that consist of Grid
system, background and link styles), **Layout Components:** (shares a list of
all layouts), **JavaScript Plugins** (includes jQuery and JavaScript plugins)
and **Customization **(Allows customization of all components for a desired
framework)

**Source:** _medium.com/@onlineinerview_

#### Q8: How many types of layout are available in Bootstrap? ⭐⭐
**Answer:**
There are two major layouts for Bootstrap i.e. Fluid Layout and Fixed Layout.
Fluid layout is necessary for creating an app that is 100 % wider and covers all
the screen width. Fixed Layout is used only for a standard screen (940px). Both
layouts can be used for creating a responsive design.

**Source:** _medium.com/@onlineinerview_

#### Q9: Why do we use Jumbotron in Bootstrap? ⭐⭐
**Answer:**
*Jumbotron* has a very basic function in bootstrap i.e. highlighting a content. It
could either be a slogan/uvp (unique value proposition) or probably a headline. It increases the heading size
and gives a margin for content of the landing page. In order to implement
Jumbotron in a Bootstrap use:

```html
 <div class=”jumbotron”>
```

Jumbotron can have any valid HTML along with other functions and classes.

**Source:** _medium.com/@onlineinerview_

#### Q10: What is Twitter Bootstrap? ⭐⭐
**Answer:**
Bootstrap is a sleek, intuitive, and powerful mobile first front-end framework
for faster and easier web development. It uses HTML, CSS and Javascript.

**Source:** _medium.com/@alisonbenhar_

#### Q11: Explain why to choose Bootstrap for building the websites? ⭐⭐
**Answer:**
There are few reason why we choose Bootstrap for building websites

* Mobile Support: For mobile devices it provides full support in one single file
rather than in separate file. It supports the responsive design including
adjusting the CSS based on the different types of device, size of the screen
etc. It reduces extra effort for developers.
* Easy to learn: Writing application in bootstrap is easy if you know CSS and HTML
* Browser Support: It supports all the popular browsers like Firefox, Opera,
Safari, IE etc.

**Source:** _medium.com/@alisonbenhar_

#### Q12: What global styles are applied as a part of Bootstrap’s default typography? ⭐⭐
**Answer:**
Bootstrap sets the global default font-size to `14px`, with a line-height of `1.428`. The default font is changed to `Helvetica` and `Arial` with `sans serif` fallback. 

All these styles are applied to the `<body>` and all paragraphs, with the addition that `<p>` (paragraphs) receive a bottom margin of half their computed line-height, which is `10px` by default.

**Source:** _toptal.com_

#### Q13: What is the procedure to create Nav elements in Bootstrap? ⭐⭐
**Answer:**
There are several styling navigation elements available on bootstrap and every
style uses the same function i.e. class `.nav`. In order to create tabs or a
tabular navigation, you can begin with a simple or rather basic unordered list
using the function class `.nav`. To add the tabs the function class `.nav-tabs` can
be used.

**Source:** _medium.com/@onlineinerview_

#### Q14:  What are Glyphicons? ⭐⭐
**Answer:**
Glyphicons are icon fonts which you can use in your web projects. Glyphicons
Halflings are not free and require licensing, however their creator has made
them available for Bootstrap projects free of cost.

To use the icons, simply use the following code just about anywhere in your
code. Leave a space between the icon and text for proper padding.

```html
<span class="glyphicon glyphicon-search"></span>
```

**Source:** _medium.com/@alisonbenhar_

#### Q15: When to use "lead" in Bootstrap? ⭐⭐
**Answer:**
To add some emphasis to a paragraph, add class `.lead`. This will give you
larger font size, lighter weight, and a taller line height.

**Source:** _medium.com/@alisonbenhar_

#### Q16: Explain the typography and links in Bootstrap. ⭐⭐
**Answer:**
Bootstrap sets a basic global display (background), typography, and link styles:

* **Basic Global display** − sets *background-color: #fff;* on the *<body>*
* **Typography** − uses the *@font-family-base*, *@font-size-base*,
and *@line-height-base* attributes as the typographic base
* **Link styles** − sets the global link color via attribute *@link-color* and
apply link underlines only on *:hover*.

**Source:** _medium.com/@alisonbenhar_

#### Q17: How do you make images responsive? ⭐⭐
**Answer:**
Bootstrap 3 allows to make the images responsive by adding a class
`.img-responsive` to the `<img>` tag. This class applies `max-width: 100%;` and
`height: auto;` to the image so that it scales nicely to the parent element.

**Source:** _medium.com/@alisonbenhar_

#### Q18: What is missing for a tooltip to show properly? ⭐⭐
**Answer:**
Consider:
```html
<button type="button" class="btn btn-default" data-toggle="tooltip" data-placement="top" title="Example tooltip">Hover over me</button>
```
What is missing for a tooltip to show properly?

**Answer**

Bootstrap’s Tooltip plugin is not CSS-only, like other plugins are. For performance reasons, the Tooltip plugin is opt-in, and to use it you must initialize it using JavaScript with the following example code:
```js
$(function () {
  $('[data-toggle="tooltip"]').tooltip();
});
```

**Source:** _medium.com/@alisonbenhar_

#### Q19: What do you mean by Bootstrap collapsing elements? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q20: What is a list group in Bootstrap and where does it finds its application? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q21: Explain Modal plugin in Bootstrap? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q22: What is a Bootstrap Container? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q23: Why do we use Bootstrap Carousel plugin? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q24: What is the role of media object in Bootstrap and how many types are available? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q25: What are the key components of Bootstrap? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q26: What is the step-wise procedure for creating basic or vertical forms? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q27: What do you mean by Bootstrap "well"? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q28: What is the difference between the following two lines of code? Explain your answer. ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q29: What will be the default Bootstrap look of the alert created with this following code? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q30: Explain what the following code does, and where they are useful ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q31: What is the role of pagination in bootstrap and what are their classifications? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q32: What is Normalize in Bootstrap? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q33: Consider the HTML code snippet below. What will the output be, and why? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q34: Explain column ordering in Bootstrap? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q35: What is screen reader in bootstrap documentation? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q36: How can you differentiate between Bootstrap and Foundation? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q37: How many different media queries are used by the Bootstrap grid system by default? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q38: What is the class sr-only used for? Is it important or can I remove it? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

## [[⬆]](#toc) <a name=CSS>CSS</a> Interview Questions
#### Q1: Explain the three main ways to apply CSS styles to a web page ⭐
**Answer:**
Using the inline style attribute on an element
```html
<div>
    <p style="color: maroon;"></p>
</div>
```
Using a `<style>` block in the `<head>` section of your HTML
```html
<head>
    <title>CSS Refresher</title>
    <style>
        body {
            font-family: sans-serif;
            font-size: 1.2em;
        }
    </style>
</head>
```
Loading an external CSS file using the `<link>` tag
```html
<head>
    <title>CSS Refresher</title>
    <link rel="stylesheet" href="/css/styles.css" />
</head>
```

**Source:** _goskills.com_

#### Q2: What is CSS? ⭐
**Answer:**
**CSS** stands for **Cascading Style Sheets**. CSS is used to define styles for your web pages, including the design, layout and variations in display for different devices and screen sizes.

CSS was intended to allow web professionals to separate the content and structure of a website's code from the visual design.

**Source:** _w3schools.com_

#### Q3: What is DOM (Document Object Model) and how is it linked to CSS? ⭐⭐
**Answer:**
The *Document Object Model (DOM)* is a cross-platform and language-independent *application programming interface* that treats an HTML, XHTML, or XML document as a tree structure wherein each node is an object representing a part of the document. 

With the Document Object Model, programmers can create and build documents, navigate their structure, and add, modify, or delete elements and content. The DOM specifies interfaces which may be used to manage XML or HTML documents. 

When a browser displays a document, it must combine the document's content with its style information. The browser converts HTML and CSS into the DOM (Document Object Model). The DOM represents the document in the computer's memory. It combines the document's content with its style.

**Source:** _en.wikipedia.org_

#### Q4: Explain the CSS “box model” and the layout components that it consists of ⭐⭐
**Answer:**
The CSS box model is a rectangular layout paradigm for HTML elements that consists of the following:

* **Content** - The content of the box, where text and images appear
* **Padding** - A transparent area surrounding the content (i.e., the amount of space between the border and the content)
* **Border** - A border surrounding the padding (if any) and content
* **Margin** - A transparent area surrounding the border (i.e., the amount of space between the border and any neighboring elements)

**Source:** _toptal.com_

#### Q5: What is a CSS rule? ⭐⭐
**Answer:**
Web browsers apply **CSS rules** to a document to affect how they are displayed. A CSS rule is formed from:

* A **set of properties**, which have values set to update how the HTML content is displayed,
* A **selector**, which selects the element(s) you want to apply the updated property values to.

A set of CSS rules contained within a stylesheet determines how a webpage should look. 

**Source:** _developer.mozilla.org_

#### Q6: What existing CSS frameworks have you used locally, or in production? How would you change/improve them? ⭐⭐
**Answer:**
* **Bootstrap** - Slow release cycle. Bootstrap 4 has been in alpha for almost 2 years. Add a spinner button component, as it is widely used.
* **Semantic UI** - Source code structure makes theme customization extremely hard to understand. Its unconventional theming system is a pain to customize. Hardcoded config path within the vendor library. Not well-designed for overriding variables unlike in Bootstrap.
* **Bulma** - A lot of non-semantic and superfluous classes and markup required. Not backward compatible. Upgrading versions breaks the app in subtle manners.

**Source:** _codeburst.io_

#### Q7: Have you played around with the new CSS Flexbox or Grid specs? ⭐⭐
**Answer:**
Yes. Flexbox is mainly meant for 1-dimensional layouts while Grid is meant for 2-dimensional layouts.

Flexbox solves many common problems in CSS, such as vertical centering of elements within a container, sticky footer, etc. Bootstrap and Bulma are based on Flexbox, and it is probably the recommended way to create layouts these days. Have tried Flexbox before but ran into some browser incompatibility issues (Safari) in using `flex-grow`, and I had to rewrite my code using `inline-blocks` and math to calculate the widths in percentages, it wasn't a nice experience.

Grid is by far the most intuitive approach for creating grid-based layouts (it better be!) but browser support is not wide at the moment.

**Source:** _codeburst.io_

#### Q8: What is the difference between classes and IDs in CSS? ⭐⭐
**Answer:**
* **IDs** — Meant to be unique within the document. Can be used to identify an element when linking using a fragment identifier. Elements can only have one id attribute.

* **Classes** — Can be reused on multiple elements within the document. Mainly for styling and targeting elements.

**Source:** _codeburst.io_

#### Q9: Describe floats and how they work ⭐⭐
**Answer:**
*Float* is a CSS positioning property. Floated elements remain a part of the flow of the web page. This is distinctly different than page elements that use absolute positioning. Absolutely positioned page elements are removed from the flow of the webpage.

```css
#sidebar {
  float: right; // left right none inherit			
}
```
The CSS clear property can be used to be positioned below `left`/`right`/`both` floated elements.

**Source:** _css-tricks.com_

#### Q10: Explain CSS sprites, and how you would implement them on a page or site. ⭐⭐
**Answer:**
*CSS sprites* combine multiple images into one single larger image. It is commonly used technique for icons (Gmail uses it). 

* Use a sprite generator that packs multiple images into one and generate the appropriate CSS for it.
* Each image would have a corresponding CSS class with `background-image`, `background-position` and `background-size` properties defined.
* To use that image, add the corresponding class to your element.

**Advantages**:

* Reduce the number of HTTP requests for multiple images (only one single request is required per spritesheet). But with HTTP2, loading multiple images is no longer much of an issue.
* Advance downloading of assets that won’t be downloaded until needed, such as images that only appear upon `:hover` pseudo-states. Blinking wouldn't be seen.

**Source:** _codeburst.io_

#### Q11: How would you approach fixing browser-specific styling issues? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q12: What is CSS preprocessor and why to user one? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q13: Have you ever worked with retina graphics? If so, when and what techniques did you use? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q14: How is responsive design different from adaptive design? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q15: How to create a zebra striped table with CSS? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q16: What’s the difference between “resetting” and “normalizing” CSS? Which would you choose, and why? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q17: How does CSS actually work (under the hood of browser)? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q18: Explain your understanding of the box model and how you would tell the browser in CSS to render your layout in different box models. ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q19: What is CSS selectors? Name some. ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q20: Explain the usage of "table-layout" property ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q21: Describe pseudo-elements and discuss what they are used for. ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q22: What does Accessibility (a11y) mean? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q23: What are the advantages/disadvantages of using CSS preprocessors? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q24: What is a Grid System in CSS? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q25: What's the difference between a `relative`, `fixed`, `absolute` and `static`ally positioned element? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q26: Explain the purpose of clearing floats in CSS ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q27: How do you optimize your webpages for print? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q28: Have you ever used a grid system, and if so, what do you prefer? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q29: What are the different ways to visually hide content (and make it available only for screen readers)? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q30: Describe z-index and how a stacking context is formed ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q31: What does * { box-sizing: border-box; } do? What are its advantages? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q32: Can you explain the difference between coding a website to be responsive versus using a mobile-first strategy? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q33: Explain the basic rules of CSS Specificity ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q34: Is there any reason you'd want to use `translate()` instead of `absolute` positioning, or vice-versa? And why? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q35: What the code fragment has the greater CSS specificity?  ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q36: What clearfix methods do you know? Provide some examples. ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q37: How to style every element which has an adjacent item right before it? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q38: Write down a selector that will match any links end in .zip, .ZIP, .Zip etc... ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

## [[⬆]](#toc) <a name=CodeProblems>Code Problems</a> Interview Questions
#### Q1: Test divisors of three ⭐
**Details:**
You will be given 2 parameters: a low and high number. Your goal is to print all numbers between low and high, and for each of these numbers print whether or not the number is divisible by 3. If the number is divisible by 3, print the word "div3" directly after the number.

**Answer:**
We'll solve this problem by first creating a loop that will print each number from low to high. Once we have the code for that written, we'll add a conditional that will check if the number is evenly divisible by 3 by using the mod operator.

```js
function test_divisors(low, high) {
  
  // we'll store all numbers and strings within an array
  // instead of printing directly to the console
  var output = [];
  
  for (var i = low; i <= high; i++) {
    
    // simply store the current number in the output array
    output.push(i);
    
    // check if the current number is evenly divisible by 3
    if (i % 3 === 0) { output.push('div3'); }
    
  }
  
  // return all numbers and strings
  return output;
  
}

test_divisors(2, 10);
```

**Source:** _coderbyte.com_

#### Q2: Sum of Array Plus One ⭐
**Details:**
Write a function that takes an array of integers and returns the sum of the integers after adding 1 to each.

**Answer:**
```js
// ES5 method is nice and clean
exports.es5 = function (array) {
  return array.reduce(function (memo, num) {
    return memo + num;
  }, array.length);
};

// Without array.reduce method isn't much different
exports.iterative = function (array) {
  var result = array.length;

  for (var i = 0; i < array.length; i++) {
    result += array[i];
  }

  return result;
};
```

**Source:** _github.com/blakeembrey_

#### Q3: String Rotation ⭐
**Details:**
Find out if a string is a rotation of another string. E.g. `ABCD` is a rotation of `BCDA` but not `ACBD`.

**Answer:**
First make sure `a` and `b` are of the same length. Then check to see if `b` is a substring of `a` concatenated with `a`:

```js
module.exports = function (a, b) {
  return a.length === b.length && (a + a).indexOf(b) > -1;
};
```



**Source:** _github.com/blakeembrey_

#### Q4: Oddball sum ⭐
**Details:**
Write a function called `oddball_sum` which takes in a list of numbers and returns the sum of all the odd elements. Try to solve with and without `reduce` function.

**Answer:**
To solve this challenge we'll simply loop through the array while maintaining a final count, and every time an odd number is encountered we'll add it to the count.

Without `reduce`:
```js
function oddball_sum(nums) {
 
  // final count of all odd numbers added up
  var final_count = 0;
  
  // loop through entire list
  for (var i = 0; i < nums.length; i++) {
    
    // we divide by 2, and if there is a remainder then
    // the number must be odd so we add it to final_count
    if (nums[i] % 2 === 1) {
      final_count += nums[i]
    }
    
  }
  
  return final_count;
  
}

oddball_sum([1, 2, 3, 4, 5]); 
```

With `reduce`:

```js
function oddball_sum(nums) {
  return nums.reduce(function(total, item){
  	if (item % 2 === 1) {
  		return total += item;
  	}
  	return total;
  });
}
```

**Source:** _prepwork.appacademy.io_

#### Q5: Simple clock angle ⭐
**Details:**
You will be given a number `N` that represents where the minute hand currently is on a clock. Your program should return the angle that is formed by the minute hand and the `12` o'clock mark on the clock.

**Answer:**
If the input is `15` then your program should return `90` because a `90`-degree angle is formed by the minute hand and the `12` o'clock mark on the clock. We'll solve this challenge by first calculating what angle is created by each minute passing on a clock. Once we calculate this number, we multiply it by the input to determine the final angle. 

A method to solve such problems is to consider the rate of change of the angle in degrees per minute. The hour hand of a normal `12-hour` analogue clock turns `360°` in `12` hours (`720` minutes) or `0.5°` per minute. The minute hand rotates through `360°` in `60` minutes or `6°` per minute.

```js
function simpleClockAngle(num) {

  // we got 6 because 360/60 = 6
  // 360 represents the full number of a degrees in a circle and
  // 60 is the number of minutes on a clock, so dividing these two numbers
  // gives us the number of degrees for one minute
  return 6 * num;

}

simpleClockAngle(15);
```



**Source:** _coderbyte.com_

#### Q6: Sum of several arrays ⭐
**Details:**
You will be given an array of several arrays that each contain integers and your goal is to write a function that will sum up all the numbers in all the arrays. For example, if the input is `[[3, 2], [1], [4, 12]]` then your program should output `22` because `3 + 2 + 1 + 4 + 12 = 22`. Solve without and with `reduce`.

**Answer:**
We will solve this challenge by looping through the entire array, and then looping through each inner array adding up all the numbers.

```js
function sum_array(arr) {
  // store our final answer
  var sum = 0;
  // loop through entire array
  for (var i = 0; i < arr.length; i++) {
    // loop through each inner array
    for (var j = 0; j < arr[i].length; j++) {
      // add this number to the current final sum
      sum += arr[i][j];
    }
  }
  
  return sum;
}

sum_array([[3, 2], [1], [4, 12]]);
```

With `reduce`:

```js
function sumArray(arr) {
  return arr.reduce((t, e) => t.concat(e)).reduce((t, e) => t + e)
}
```

**Source:** _coderbyte.com_

#### Q7: Lucky sevens ⭐
**Details:**
Write a function called `lucky_sevens` which takes an array of integers and returns true if any three consecutive elements sum to 7.

**Answer:**
To solve this challenge we'll simply loop through the array starting at the 3rd position, and checking if the number at this index plus the two previous elements sums to 7. We continue doing this as we loop through the entire array. Once we find three elements that sum to 7, we simply return `true`. If we reach the end of the array without finding elements that sum to 7, we return `false`.

```js
function lucky_sevens(arr) {
  
  // if less than 3 elements then this challenge is not possible
  if (arr.length < 3) {
    return "not possible";
  }
  
  // because we know there are at least 3 elements we can
  // start the loop at the 3rd element in the array (i=2)
  // and check it along with the two previous elements (i-1) and (i-2)
  for (var i = 2; i < arr.length; i++) {
    if (arr[i] + arr[i-1] + arr[i-2] === 7) {
      return true; 
    }
  }
  
  // if loop is finished and no elements summed to 7
  return false;
  
}

lucky_sevens([2, 1, 5, 1, 0]);
``` 



**Source:** _coderbyte.com_

#### Q8: Two sum problem ⭐⭐
**Details:**
Given an integer `x` and a sorted array a of `N` distinct integers, design a linear-time algorithm to determine if there exists two distinct indices `i` and `j` such that `a[i] + a[j] == x`

For example, if the array is `[3, 5, 2, -4, 8, 11]` and the sum is `7`, 
your program should return `[[11, -4], [2, 5]]` because `11 + -4 = 7` and `2 + 5 = 7`.

**Answer:**
The algorithm below makes use of hash tables which have a constant lookup time. As we pass through each element in the array, we check to see if S minus the current element exists in the hash table. We only need to loop through the array once, resulting in a running time of `O(n)` since each lookup and insertion in a hash table is `O(1)`.

```js
// our two sum function which will return
// all pairs in the array that sum up to S
function twoSum(arr, S) {

  var sums = [];
  var hashTable = {};

  // check each element in array
  for (var i = 0; i < arr.length; i++) {
 
    // calculate S - current element
    var sumMinusElement = S - arr[i];

    // check if this number exists in hash table
    // if so then we found a pair of numbers that sum to S
    if (hashTable[sumMinusElement.toString()] !== undefined) { 
      sums.push([arr[i], sumMinusElement]);
    }

    // add the current number to the hash table
    hashTable[arr[i].toString()] = arr[i];

  }

  // return all pairs of integers that sum to S
  return sums;

}

twoSum([3, 5, 2, -4, 8, 11], 7);
```



**Source:** _coderbyte.com_

#### Q9: Implement a queue using a linked list ⭐⭐
**Answer:**
We will store a reference to the front and back of the queue in order to make enqueuing and dequeuing run in `O(1)` constant time. Every time we want to insert into the queue, we add the new element to the end of the linked list and update the back pointer. When we want to dequeue we return the first node in the linked list and update the front pointer.

```js
// queue is initially empty
var Queue = {front: null, back: null};

// we will use a node to keep track of the elements
// in the queue which is represented by a linked list
function Node(data, next) {
  this.data = data;
  this.next = next;
} 

// add elements to queue in O(1) time
function Enqueue(element) {
  var N = new Node(element, null);
  if (Queue.back === null) {
    Queue.front = N;
    Queue.back = N; 
  } else { 
    Queue.back.next = N; 
    Queue.back = Queue.back.next;
  } 
}

// remove first element from queue in O(1) time
function Dequeue() {
  if (Queue.front !== null) { 
    var first = Queue.front;
    Queue.front = Queue.front.next; 
    return first.data;
  } else {
    if (Queue.back !== null) { Queue.back = null; }
    return 'Cannot dequeue because queue is empty';
  }
}

Enqueue('a'); 
Enqueue('b'); 
Enqueue('c'); 
Dequeue();
```

**Source:** _codeisahighway.com_

#### Q10: Tree Level Order Print ⭐⭐
**Details:**
Given a binary tree of integers, print it in level order. The output will contain space between the numbers in the same level, and new line between different levels.

**Answer:**
```js
module.exports = function (root) {
  // Doing a breadth first search using recursion.
  (function walkLevel (children) {
    // Create a new queue for the next level.
    var queue = [],
        output;

    // Use the map function to easily join all the nodes together while pushing
    // it's children into the next level queue.
    output = children.map(function (node) {
      // Assuming the node has children stored in an array.
      queue = queue.concat(node.children || []);
      return node.value;
    }).join(' ');

    // Log the output at each level.
    console.log(output);

    // If the queue has values in it, recurse to the next level and walk
    // along it.
    queue.length && walkLevel(queue);
  })([root]);
};
```


**Source:** _ardendertat.com_

#### Q11: Stock maximum profit ⭐⭐
**Details:**
You will be given a list of stock prices for a given day and your goal is to return the maximum profit that could have been made by buying a stock at the given price and then selling the stock later on. 

For example if the input is: 

```js
[45, 24, 35, 31, 40, 38, 11] 
```

then your program should return 16 because if you bought the stock at $24 and sold it at $40, a profit of $16 was made and this is the largest profit that could be made. If no profit could have been made, return -1.

**Answer:**
We'll solve the challenge the following way:

1. Iterate through each number in the list.
2. At the ith index, get the `i+1` index price and check if it is larger than the ith index price.
3. If so, set `buy_price = i` and `sell_price = i+1`. Then calculate the profit: `sell_price - buy_price`.
4. If a stock price is found that is cheaper than the current `buy_price`, set this to be the new buying price and continue from step 2.
5. Otherwise, continue changing only the `sell_price` and keep `buy_price` set.

This algorithm runs in linear time, making only one pass through the array, so the running time in the worst case is `O(n)`.

```js
function StockPicker(arr) { 
  
  var max_profit = -1;
  var buy_price = 0;
  var sell_price = 0;
  
  // this allows our loop to keep iterating the buying
  // price until a cheap stock price is found
  var change_buy_index = true;
  
  // loop through list of stock prices once
  for (var i = 0; i < arr.length-1; i++) {
    
    // selling price is the next element in list
    sell_price = arr[i+1]; 
    
    // if we have not found a suitable cheap buying price yet
    // we set the buying price equal to the current element
    if (change_buy_index) { buy_price = arr[i]; }
    
    // if the selling price is less than the buying price
    // we know we cannot make a profit so we continue to the 
    // next element in the list which will be the new buying price
    if (sell_price < buy_price) {
      change_buy_index = true; 
      continue;
    }
    
    // if the selling price is greater than the buying price
    // we check to see if these two indices give us a better 
    // profit then what we currently have
    else { 
      var temp_profit = sell_price - buy_price;
      if (temp_profit > max_profit) { max_profit = temp_profit; }
      change_buy_index = false;
    }
    
  }
  
  return max_profit;
         
}

StockPicker([44, 30, 24, 32, 35, 30, 40, 38, 15]);  
```

**Source:** _coderbyte.com_

#### Q12: Find Word Positions in Text ⭐⭐
**Details:**
Given a text file and a word, find the positions that the word occurs in the file. We’ll be asked to find the positions of many words in the same file.

**Answer:**
Since we’ll have to answer multiple queries, precomputation would be useful. We’ll build a data structure that stores the positions of all the words in the text file. This is known as inverted index.

```js
module.exports = function (text) {
  var trie   = {},
      pos    = 0,
      active = trie; // Start the active structure as the root trie structure

  // Suffix a space after the text to make life easier
  text += ' ';

  // Loop through the input text adding it to the trie structure
  for (var i = 0; i < text.length; i++) {
    // When the character is a space, restart
    if (text[i] === ' ') {
      // If the current active doesn't equal the root, set the position
      if (active !== trie) {
        (active.positions = active.positions || []).push(pos);
      }
      // Reset the positions and the active part of the data structure
      pos    = i;
      active = trie;
      continue;
    }

    // Set the next character in the structure up
    active[text[i]] = (active[text[i]] || {});
    active = active[text[i]];
  }

  // Return a function that accepts a word and looks it up in the trie structure
  return function (word) {
    var i      = -1,
        active = trie;

    while (word[++i]) {
      if (!active[word[i]]) { return []; }
      active = active[word[i]];
    }

    return active.positions;
  };
};
```

**Source:** _github.com/blakeembrey_

#### Q13: Determine overlapping numbers in ranges ⭐⭐
**Details:**
You will be given an array with `5` numbers. The first 2 numbers represent a range, and the next two numbers represent another range. The final number in the array is `X`. The goal of your program is to determine if both ranges overlap by at least `X` numbers. For example, in the array `[4, 10, 2, 6, 3]` the ranges `4` to `10` and `2` to `6` overlap by at least `3` numbers `(4, 5, 6)`, so your program should return `true`. Solve with and without looping.

If the array is `[10, 20, 4, 14, 4]` then the ranges are:

```sh
10 11 12 13 14 15 16 17 18 19 20
4 5 6 7 8 9 10 11 12 13 14
```

These ranges overlap by at least `4` numbers, namely: `10, 11, 12, 13, 14` so your program should return `true`.

**Answer:**
With loop:
```js
function OverlappingRanges(arr) {

  // keep a count of how many numbers overlap
  var counter = 0;
  
  // loop through one of the ranges
  for (var i = arr[0]; i < arr[1]; i++) {

    // check if a number within the first range exists
    // in the second range
    if (i >= arr[2] && i <= arr[3]) { 
      counter += 1;
    }

  }
 
  // check if the numbers that overlap is equal to or greater
  // than the last number in the array
  return (counter >= arr[4]) ? true : false;
}

OverlappingRanges([4, 10, 2, 6, 3]); 
```

Without loop:

```js
function overlapping(input){
  var nums1 = listOfNums(input[0], input[1]);
  var nums2 = listOfNums(input[2], input[3]);
  var overlappingNum = 0;

  if(nums1[0] >= nums2[0] && nums1[0] <= nums2[1]){
    overlappingNum =  nums2[1] - nums1[0] + 1;
  } else {
    overlappingNum =  nums1[1] - nums2[0] + 1;
  }
  if(overlappingNum >= input[4]){
    return true;
  }
}

function listOfNums(a, b){
  var start = a;
  var end = b;
  if(a > b){
    start = b;
    end = a;
  }

  return [a, b];
}

var a = [4, 10, 2, 6, 3];
overlapping(a)
```


**Source:** _coderbyte.com_

#### Q14: Throttle Function Implementation ⭐⭐
**Details:**
Write a function that accepts a function and timeout, `x`, in number of milliseconds. It returns a function that can only be executed once per `x` milliseconds. This can be useful for limiting the number of time and computation heavy function that are run. For example, making AJAX requests to an autocompletion API.

Once written, add a third parameter that will allow the function to be executed immediately if set to true. Otherwise the function will run at the end of the timeout period.

**Answer:**
```js
module.exports = function (fn, delay, execAsap) {
  var timeout; // Keeps a reference to the timeout inside the returned function

  return function () {
    // Continue to pass through the function execution context and arguments
    var that = this,
        args = arguments;

    // If there is no timeout variable set, proceed to create a new timeout
    if (!timeout) {
      execAsap && fn.apply(that, args);

      timeout = setTimeout(function () {
        execAsap || fn.apply(that, args);
        // Remove the old timeout variable so the function can run again
        timeout = null;
      }, delay || 100);
    }
  };
};
```


**Source:** _github.com/blakeembrey_

#### Q15: Dutch national flag sorting problem ⭐⭐
**Details:**
For this problem, your goal is to sort an array of `0`, `1`, `2` but you must do this in place, in linear time and without any extra space (such as creating an extra array). This is called the *Dutch national flag sorting problem*. For example, if the input array is `[2,0,0,1,2,1]` then your program should output `[0,0,1,1,2,2]` and the algorithm should run in `O(n)` time.

**Answer:**
The solution to this algorithm will require 3 pointers to iterate throughout the array, swapping the necessary elements.

1. Create a low pointer at the beginning of the array and a high pointer at the end of the array.
2. Create a mid pointer that starts at the beginning of the array and iterates through each element.
3. If the element at `arr[mid]` is a `2`, then swap `arr[mid]` and `arr[high]` and decrease the high pointer by `1`.
4. If the element at `arr[mid]` is a `0`, then swap `arr[mid]` and `arr[low]` and increase the low and mid pointers by `1`.
5. If the element at `arr[mid]` is a `1`, don't swap anything and just increase the mid pointer by `1`.

```js
function swap(arr, i1, i2) {
  var temp = arr[i1];
  arr[i1] = arr[i2];
  arr[i2] = temp;
}

function dutchNatFlag(arr) {
  
  var low = 0;
  var mid = 0;
  var high = arr.length - 1;
  
  // one pass through the array swapping
  // the necessary elements in place
  while (mid <= high) {
    if      (arr[mid] === 0) { swap(arr, low++, mid++); }
    else if (arr[mid] === 2) { swap(arr, mid, high--); }
    else if (arr[mid] === 1) { mid++; }
  }
  
  return arr;
  
}

dutchNatFlag([2,2,2,0,0,0,1,1]); 
```

**Source:** _coderbyte.com_

#### Q16: Step-by-step solution for step counting using recursion ⭐⭐
**Details:**

Suppose you want climb a staircase of N steps, and on each step you can take either 1 or 2 steps. How many distinct ways are there to climb the staircase? For example, if you wanted to climb 4 steps, you can take the following distinct number of steps:

```sh
1) 1, 1, 1, 1
2) 1, 1, 2
3) 1, 2, 1
4) 2, 1, 1
5) 2, 2
```

So there are 5 distinct ways to climb 4 steps. We want to write a function, using recursion, that will produce the answer for any number of steps. 


**Answer:**
The solution to this problem requires recursion, which means to solve for a particular `N`, we need the solutions for previous N's. The solution for N steps is equal to the solutions for `N - 1` steps plus `N - 2` steps.

```js
function countSteps(N) {
  
  // just as in our solution explanation above, we know that to climb 1 step
  // there is only 1 solution, and for 2 steps there are 2 solutions
  if (N === 1) { return 1; }
  if (N === 2) { return 2; }
  
  // for all N > 2, we add the previous (N - 1) + (N - 2) steps to get
  // an answer recursively
  return countSteps(N - 1) + countSteps(N - 2);
  
}

// the solution for N = 6 will recursively be solved by calculating
// the solution for N = 5, N = 4, N = 3, and N = 2 which we know is 2
countSteps(6); 
```


**Source:** _coderbyte.com_

#### Q17: Implement Bubble Sort ⭐⭐
**Answer:**
The steps in the bubble sort algorithm are:

1. Loop through the whole array starting from index `1`
2. If the number in the array at index `i-1` is greater than i, swap the numbers and continue
3. Once the end of the array is reached, start looping again from the beginning
4. Once no more elements can be swapped, the sorting is complete

```js
function swap(arr, i1, i2) {
  var temp = arr[i1];
  arr[i1] = arr[i2];
  arr[i2] = temp;
}

function bubblesort(arr) {
  
  var swapped = true;
  
  // keep going unless no elements can be swapped anymore
  while (swapped) {
    
    // set swapped to false so that the loop stops
    // unless two element are actually swapped
    swapped = false;

    // loop through the whole array swapping adjacent elements
    for (var i = 1; i < arr.length; i++) {
      if (arr[i-1] > arr[i]) {
        swap(arr, i-1, i);
        swapped = true;
      }
    }
    
  }
  
  return arr;
         
}

bubblesort([103, 45, 2, 1, 97, -4, 67]); 
```

**Source:** _coderbyte.com_

#### Q18: Implement a queue using two stacks ⭐⭐
**Answer:**
Suppose we push `a`, `b`, `c` to a stack. If we are trying to implement a queue and we call the dequeue method 3 times, we actually want the elements to come out in the order: `a`, `b`, `c`, which is in the opposite order they would come out if we popped from the stack. So, basically, we need to access the elements in the reverse order that they exist in the stack. 

*Algorithm* for queue using two stacks:

1. When calling the enqueue method, simply push the elements into the stack 1.
2. If the dequeue method is called, push all the elements from stack 1 into stack 2, which reverses the order of the elements. Now pop from stack 2.

The worst case running time for implementing these operations using stacks is `O(n)` because you need to transfer n elements from stack 1 to stack 2 when a dequeue method is called. Pushing to stack 1 is simply `O(1)`.

```js
// implement stacks using plain arrays with push and pop functions
var Stack1 = [];
var Stack2 = [];

// implement enqueue method by using only stacks
// and the push and pop functions
function Enqueue(element) {
  Stack1.push(element);
}

// implement dequeue method by pushing all elements
// from stack 1 into stack 2, which reverses the order
// and then popping from stack 2
function Dequeue() {
  if (Stack2.length === 0) {
    if (Stack1.length === 0) { return 'Cannot dequeue because queue is empty'; }
    while (Stack1.length > 0) {
      var p = Stack1.pop();
      Stack2.push(p);
    }
  }
  return Stack2.pop();
}

Enqueue('a');
Enqueue('b');
Enqueue('c');
Dequeue(); 
```

**Source:** _coderbyte.com_

#### Q19: Implement pow(a,b) without multiplication or division ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q20: Generate all balanced bracket combinations ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q21: All Permutations (Anagrams) of a String ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q22: Merge two sorted linked lists ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q23: Insert an interval into a list of sorted disjoint intervals ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q24: Find all string combinations consisting only of 0, 1 and ? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q25: Quickly calculate the cube root of 6 digit numbers ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q26: Transform Word ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

## [[⬆]](#toc) <a name=DataStructures>Data Structures</a> Interview Questions
#### Q1: What is data-structure? ⭐
**Answer:**
Data structure availability may vary by programming languages. Commonly available data structures are:
* list, 
* arrays, 
* stack, 
* queues, 
* graph, 
* tree etc.

**Source:** _tutorialspoint.com_

#### Q2: What is algorithm? ⭐
**Answer:**
**Algorithm** is a step by step procedure, which defines a set of instructions to be executed in certain order to get the desired output.

**Source:** _tutorialspoint.com_

#### Q3: What is linear searching? ⭐
**Answer:**
**Linear search** or sequential search is a method for finding a target value within a list. It sequentially checks each element of the list for the target value until a match is found or until all the elements have been searched. Linear search runs in at worst *linear time* and makes at most `n` comparisons, where `n` is the length of the list. 

* Worst-case performance	`O(n)`
* Best-case performance	`O(1)`
* Average performance	`O(n)`
* Worst-case space complexity	`O(1)` iterative

In theory other search algorithms may be faster than linear search (for instance binary search), in practice even on medium-sized arrays (around 100 items or less) it might be infeasible to use anything else. 

**Source:** _wikipedia.org_

#### Q4: What is asymptotic analysis of an algorithm? ⭐⭐
**Answer:**
**Asymptotic analysis** of an algorithm, refers to defining the mathematical boundation/framing of its run-time performance. Using asymptotic analysis, we can very well conclude the best case, average case and worst case scenario of an algorithm.

Asymptotic analysis can provide three levels of mathematical binding of execution time of an algorithm:

*   Best case is represented by Ω(n) notation.
*   Worst case is represented by Ο(n) notation.
*   Average case is represented by Θ(n) notation.

**Source:** _tutorialspoint.com_

#### Q5: What is linear data structure and what are common operations to perform on it? ⭐⭐
**Answer:**
A *linear data-structure* has sequentially arranged data items. The next item can be located in the next memory address. It is stored and accessed in a sequential manner. **Array** and **list** are example of linear data structure.

The following operations are commonly performed on any data-structure:

*   **Insertion** − adding a data item
*   **Deletion** − removing a data item
*   **Traversal** − accessing and/or printing all data items
*   **Searching** − finding a particular data item
*   **Sorting** − arranging data items in a pre-defined sequence

**Source:** _tutorialspoint.com_

#### Q6: What is an average case complexity of Bubble Sort? ⭐⭐
**Answer:**
**Bubble sort**, sometimes referred to as sinking sort, is a simple sorting algorithm that repeatedly steps through the list to be sorted, compares each pair of adjacent items and swaps them if they are in the wrong order. The pass through the list is repeated until no swaps are needed, which indicates that the list is sorted. 

Bubble sort has a worst-case and average complexity of `О(n2)`, where `n` is the number of items being sorted. Most practical sorting algorithms have substantially better worst-case or average complexity, often `O(n log n)`. Therefore, bubble sort is not a practical sorting algorithm.



**Source:** _wikipedia.org_

#### Q7: What examples of greedy algorithms do you know? ⭐⭐
**Answer:**
The below given problems find their solution using greedy algorithm approach:

*   Travelling Salesman Problem
*   Prim's Minimal Spanning Tree Algorithm
*   Kruskal's Minimal Spanning Tree Algorithm
*   Dijkstra's Minimal Spanning Tree Algorithm
*   Graph - Map Coloring
*   Graph - Vertex Cover
*   Knapsack Problem
*   Job Scheduling Problem

**Source:** _tutorialspoint.com_

#### Q8: What are some examples of divide and conquer algorithms? ⭐⭐
**Answer:**
The below given problems find their solution using divide and conquer algorithm approach:

*   Merge Sort
*   Quick Sort
*   Binary Search
*   Strassen's Matrix Multiplication
*   Closest pair (points)

**Source:** _tutorialspoint.com_

#### Q9: What are some examples of dynamic programming algorithms? ⭐⭐
**Answer:**
The below given problems find their solution using divide and conquer algorithm approach:

*   Fibonacci number series
*   Knapsack problem
*   Tower of Hanoi
*   All pair shortest path by Floyd-Warshall
*   Shortest path by Dijkstra
*   Project scheduling

**Source:** _tutorialspoint.com_

#### Q10: Why do we use stacks? ⭐⭐
**Answer:**
In data-structure, **stack** is an Abstract Data Type (ADT) used to store and retrieve values in Last In First Out (LIFO) method.

Stacks follows LIFO method and addition and retrieval of a data item takes only `Ο(n)` time. Stacks are used where we need to access data in the reverse order or their arrival. Stacks are used commonly in recursive function calls, expression parsing, depth first traversal of graphs etc.

The below operations can be performed on a stack:

*   **push()** − adds an item to stack
*   **pop()** − removes the top stack item
*   **peek()** − gives value of top item without removing it
*   **isempty()** − checks if stack is empty
*   **isfull()** − checks if stack is full

**Source:** _tutorialspoint.com_

#### Q11: Why do we use queues? ⭐⭐
**Answer:**
**Queue** is an abstract data structure (ADS), somewhat similar to stack. In contrast to stack, queue is opened at both end. One end is always used to insert data (enqueue) and the other is used to remove data (dequeue). Queue follows First-In-First-Out (FIFO) methodology, i.e., the data item stored first will be accessed first.

As queues follows FIFO method, they are used when we need to work on data-items in exact sequence of their arrival. Every operating system maintains queues of various processes. Priority queues and breadth first traversal of graphs are some examples of queues.

The below operations can be performed on a queue:
*   **enqueue()** − adds an item to rear of the queue
*   **dequeue()** − removes the item from front of the queue
*   **peek()** − gives value of front item without removing it
*   **isempty()** − checks if stack is empty
*   **isfull()** − checks if stack is full

**Source:** _tutorialspoint.com_

#### Q12: What is the difference between Linear search and Binary search? ⭐⭐
**Answer:**
* A **linear search** looks down a list, one item at a time, without jumping. In complexity terms this is an `O(n)` search - the time taken to search the list gets bigger at the same rate as the list does.

* A **binary search** is when you start with the middle of a sorted list, and see whether that's greater than or less than the value you're looking for, which determines whether the value is in the first or second half of the list. Jump to the half way through the sublist, and compare again etc. In complexity terms this is an `O(log n)` search - the number of search operations grows more slowly than the list does, because you're halving the "search space" with each operation.

Comparing the two:

- Binary search requires the input data to be sorted; linear search doesn't
- Binary search requires an *ordering* comparison; linear search only requires equality comparisons
- Binary search has complexity `O(log n)`; linear search has complexity O(n)
- Binary search requires random access to the data; linear search only requires sequential access (this can be very important - it means a linear search can *stream* data of arbitrary size)

**Source:** _wikipedia.org_

#### Q13: Why we need to do algorithm analysis? ⭐⭐
**Answer:**
A problem can be solved in more than one ways. So, many solution algorithms can be derived for a given problem. We analyze available algorithms to find and implement the best suitable algorithm.

An algorithm are generally analyzed on two factors − time and space. That is, how much **execution** time and how much **extra space** required by the algorithm.

**Source:** _tutorialspoint.com_

#### Q14: What is Circular Queue and why will you use one? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q15: Name some approaches to develop algorithms ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q16: What is Bucket Sort? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q17: Is there any advantages of Bubble Sort? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

## [[⬆]](#toc) <a name=DesignPatterns>Design Patterns</a> Interview Questions
#### Q1: What are the main categories of Design Patterns? ⭐
**Answer:**
The Design patterns can be classified into three main categories:

* Creational Patterns
* Behavioral Patterns
* Functional Patterns

**Source:** _www.educba.com_

#### Q2: What is a pattern? ⭐
**Answer:**
*Patterns* in programming are like recipes in cooking. They are not ready dishes, but instructions for slicing and dicing products, cooking them, serving them and so forth.

**Pattern content**
As a rule, a pattern description consists of the following:

* a problem that the pattern solves;
* motivation for solving the the problem using the method suggested by the pattern;
* structures of classes comprising the solution;
* an example in one of the programming languages;
* a description of the nuances of pattern implementation in various contexts;
relations with other patterns.

**Source:** _refactoring.guru_

#### Q3: What is Singleton pattern? ⭐
**Answer:**
**Singleton pattern** comes under *creational* patterns category and introduces a single class which is responsible to create an object while making sure that only single object gets created. This class provides a way to access its only object which can be accessed directly without need to instantiate the object of the class.

<div class="text-center">
<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/f/fb/Singleton_UML_class_diagram.svg/220px-Singleton_UML_class_diagram.svg.png" class="img-fluid"/>
</div>


**Source:** _refactoring.guru_

#### Q4: What is Design Patterns and why anyone should use them? ⭐
**Answer:**
Design patterns are a well-described solution to the most commonly encountered problems which occur during software development. 

Design pattern represents the best practices evolved over a period of time by experienced software developers. They promote reusability which leads to a more robust and maintainable code.

**Source:** _www.educba.com_

#### Q5: What is Factory pattern? ⭐⭐
**Answer:**
**Factory pattern** is one of most used design pattern and comes under *creational* patterns category.

In Factory pattern, we create object without exposing the creation logic to the client and refer to newly created object using a *common interface*.

<div class="text-center">
<img src="https://www.tutorialspoint.com/design_pattern/images/factory_pattern_uml_diagram.jpg" class="img-fluid"/>
</div>

<br/>
**Pro's**:  

*   Allows you to hide implementation of an application seam (the core interfaces that make up your application)
*   Allows you to easily test the seam of an application (that is to mock/stub) certain parts of your application so you can build and test the other parts
*   Allows you to change the design of your application more readily, this is known as loose coupling

**Con's**  

*   Makes code more difficult to read as all of your code is behind an abstraction that may in turn hide abstractions.
*   Can be classed as an anti-pattern when it is incorrectly used, for example some people use it to wire up a whole application when using an IOC container, instead use Dependency Injection.

**Source:** _tutorialspoint.com_

#### Q6: What is Iterator pattern? ⭐⭐
**Answer:**
**Iterator pattern** is very commonly used design pattern in Java and .Net programming environment. This pattern is used to get a way to access the elements of a collection object in sequential manner without any need to know its underlying representation. Iterator pattern falls under _behavioral_ pattern category.

<div class="text-center">
<img src="https://upload.wikimedia.org/wikipedia/commons/c/c5/W3sDesign_Iterator_Design_Pattern_UML.jpg" class="img-fluid"/>
</div>

**Source:** _tutorialspoint.com_

#### Q7: What is Inversion of Control? ⭐⭐
**Answer:**

*Inversion of control* is a broad term but for a software developer it's most commonly described as a pattern used for decoupling components and layers in the system. 

For example, say your application has a text editor component and you want to provide spell checking. Your standard code would look something like this:
```js
public class TextEditor {

    private SpellChecker checker;

    public TextEditor() {
        this.checker = new SpellChecker();
    }
}
```
What we've done here creates a dependency between the TextEditor and the SpellChecker. In an IoC scenario we would instead do something like this:
```js
public class TextEditor {

    private IocSpellChecker checker;

    public TextEditor(IocSpellChecker checker) {
        this.checker = checker;
    }
}
```

You have *inverted control* by handing the responsibility of instantiating the spell checker from the TextEditor class to the caller.

```js
SpellChecker sc = new SpellChecker; // dependency
TextEditor textEditor = new TextEditor(sc);
```


**Source:** _stackoverflow.com_

#### Q8: Can we create a clone of a singleton object? ⭐⭐
**Answer:**
Yesl, we can but the purpose of Singleton Object creation is to have single instance serving all requests. 

**Source:** _tutorialspoint.com_

#### Q9: Name types of Design Patterns? ⭐⭐
**Answer:**
Design patterns can be classified in three categories: Creational, Structural and Behavioral patterns.

-   Creational Patterns - These design patterns provide a way to create objects while hiding the creation logic, rather than instantiating objects directly using new opreator. This gives program more flexibility in deciding which objects need to be created for a given use case.

-   Structural Patterns - These design patterns concern class and object composition. Concept of inheritance is used to compose interfaces and define ways to compose objects to obtain new functionalities.

-   Behavioral Patterns - These design patterns are specifically concerned with communication between objects.

**Source:** _tutorialspoint.com_

#### Q10: What is Template pattern? ⭐⭐
**Answer:**
In **Template pattern**, an abstract class exposes defined way(s)/template(s) to execute its methods. Its subclasses can override the method implementation as per need but the invocation is to be in the same way as defined by an abstract class. This pattern comes under _behavior_ pattern category.

<div class="text-center">
<img src="https://upload.wikimedia.org/wikipedia/commons/2/2a/W3sDesign_Template_Method_Design_Pattern_UML.jpg" class="img-fluid"/>
</div>

**Source:** _tutorialspoint.com_

#### Q11: What is Filter pattern? ⭐⭐
**Answer:**
**Filter pattern** or **Criteria pattern** is a design pattern that enables developers to filter a set of objects using different criteria and chaining them in a decoupled way through logical operations. This type of design pattern comes under *structural* pattern as this pattern combines multiple criteria to obtain single criteria.

**Filter design pattern** is useful where you want to add filters dynamically or you are implementing multiple functionalities and most of them require different filter criteria to filter something. In that case instead of hard coding the filters inside the functionalities, you can create filter criteria and re-use it wherever required.

```js
List<Laptop> laptops = LaptopFactory.manufactureInBulk();
AndCriteria searchCriteria = new AndCriteria(
  new HardDisk250GBFilter(), 
  new MacintoshFilter(), 
  new I5ProcessorFilter());
List<Laptop> filteredLaptops = searchCriteria.meets(laptops);
```

**Source:** _tutorialspoint.com_

#### Q12: What is Strategy pattern? ⭐⭐
**Answer:**
In **Strategy pattern**, a class behavior or its algorithm can be changed at run time. This type of design pattern comes under _behavior_ pattern.

In Strategy pattern, we create objects which represent various strategies and a context object whose behavior varies as per its strategy object. The strategy object changes the executing algorithm of the context object.

<div class="text-center">
<img src="https://upload.wikimedia.org/wikipedia/commons/4/45/W3sDesign_Strategy_Design_Pattern_UML.jpg" class="img-fluid"/>
</div>



**Source:** _tutorialspoint.com_

#### Q13: What is Dependency Injection? ⭐⭐
**Answer:**
*Dependency injection* makes it easy to create loosely coupled components, which typically means that components consume functionality defined by interfaces without having any first-hand knowledge of which implementation classes are being used.

*Dependency injection* makes it easier to change the behavior of an application by changing the components that implement the interfaces that define application features. It also results in components that are easier to isolate for unit testing.

**Source:** _Pro ASP.NET Core MVC 2_

#### Q14: What is Null Object pattern? ⭐⭐
**Answer:**
In **Null Object pattern**, a null object replaces check of NULL object instance. Instead of putting if check for a null value, Null Object reflects a do nothing relationship. Such Null object can also be used to provide default behaviour in case data is not available.

In Null Object pattern, we create an abstract class specifying various operations to be done, concrete classes extending this class and a null object class providing do nothing implementation of this class and will be used seamlessly where we need to check null value.

<div class="text-center">
<img src="https://www.tutorialspoint.com/design_pattern/images/null_pattern_uml_diagram.jpg" class="img-fluid"/>
</div>


**Source:** _tutorialspoint.com_

#### Q15: What is State pattern? ⭐⭐
**Answer:**
In **State pattern** a class behavior changes based on its state. This type of design pattern comes under _behavior_ pattern. In State pattern, we create objects which represent various states and a context object whose behavior varies as its state object changes.

<div class="text-center">
<img src="https://upload.wikimedia.org/wikipedia/commons/e/ec/W3sDesign_State_Design_Pattern_UML.jpg" class="img-fluid"/>
</div>

**Source:** _tutorialspoint.com_

#### Q16: What is Proxy pattern? ⭐⭐
**Answer:**
In **proxy pattern**, a class represents functionality of another class. This type of design pattern comes under _structural_ pattern.

In proxy pattern, we create object having original object to interface its functionality to outer world.

<div class="text-center">
<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/7/75/Proxy_pattern_diagram.svg/439px-Proxy_pattern_diagram.svg.png" class="img-fluid"/>
</div>

**Source:** _tutorialspoint.com_

#### Q17: What is Builder pattern? ⭐⭐
**Answer:**
*Builder pattern* builds a complex object using simple objects and using a step by step approach. This builder is independent of other objects.

<img src="https://www.plantuml.com/plantuml/svg/TOux3i8m343tdC9ZE_G234YqIAo86mJ7WqMQLeupS7kSqY90iCJsU_4dtpZDNlm8MU-Hx1L6BMDqHfMHPvyK_12PQio0d-B8GgYJL1M-UgQ4GafzuHXe-O5NvunvfPeYTDtU4jZ14sukh2gy6LXhcset5jIcTG6s_cN7sROVcXP-yVuF7oh75p-HNYYNQDCV" class="image-fluid center"/>

*The Director* class is optional and is used to make sure that the building steps are executed in the *right order* with the right data by the right builder. It's about validation and delegation.

Builder/Director pattern's steps invocations could be semantically presented by *method chaining* or so called *Fluent Interface* syntax. 

```js
Pizza pizza = new Pizza.Builder()
                       .cheese(true)
                       .pepperoni(true)
                       .bacon(true)
                       .build();
```

**Source:** _tutorialspoint.com_

#### Q18: What are the difference between a static class and a singleton class? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q19: When should I use composite design pattern? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q20: What does “program to interfaces, not implementations” mean? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q21: What is Abstract Factory pattern? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q22: What is Decorator pattern? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q23: What is Prototype pattern? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q24: What is Memento pattern? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q25: Can you give any good explanation what is the difference between Proxy and Decorator? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q26: What is Adapter Pattern? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q27: What is Bridge pattern? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q28: What is the Chain of Responsibility pattern? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q29: What is Observer pattern? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q30: What is Command pattern? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q31: What is Interpreter pattern? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q32: What is Facade pattern? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q33: What is Mediator pattern? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q34: When would you use the Builder Pattern? Why not just use a Factory Pattern? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q35: Why would I ever use a Chain of Responsibility over a Decorator? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q36: What is Flyweight pattern? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q37: Explain usage of Service Locator Pattern ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q38: What is the difference between Strategy design pattern and State design pattern? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q39: How is Bridge pattern is different from Adapter pattern? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q40: Explain what is Composition over inheritance? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q41: Could you explain the difference between Façade vs. Mediator? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q42: Explain difference between the Facade, Proxy, Adapter and Decorator design patterns? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q43: What is the difference between the template patterns and the strategy pattern? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q44: What's the difference between the Dependency Injection and Service Locator patterns? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q45: Could you explain what is the "deadly diamond of death"? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

## [[⬆]](#toc) <a name=DevOps>DevOps</a> Interview Questions
#### Q1: What is the most important thing DevOps helps us achieve? ⭐
**Answer:**
The most important thing that DevOps helps us achieve is to get the changes into production as quickly as possible while minimising risks in software quality assurance and compliance. This is the primary objective of DevOps.

**Source:** _edureka.co_

#### Q2: What is meant by Continuous Integration? ⭐
**Answer:**
*Continuous Integration (CI)* is a development practice that requires developers to integrate code into a shared repository several times a day. Each check-in is then verified by an automated build, allowing teams to detect problems early. 

**Source:** _edureka.co_

#### Q3: Explain what is DevOps ? ⭐
**Answer:**
**DevOps** is a newly emerging term in IT field, which is nothing but a practice that emphasizes the collaboration and communication of both software developers and other information-technology (IT) professionals. It focuses on delivering software product faster and lowering the failure rate of releases.

**Source:** _quora.com_

#### Q4: What is the need for DevOps? ⭐
**Answer:**
Nowadays instead of releasing big sets of features, companies are trying to see if small features can be transported to their customers through a series of release trains. This has many advantages like quick feedback from customers, better quality of software etc. which in turn leads to high customer satisfaction. To achieve this, companies are required to:

1.  Increase deployment frequency
2.  Lower failure rate of new releases
3.  Shortened lead time between fixes
4.  Faster mean time to recovery in the event of new release crashing

DevOps fulfills all these requirements and helps in achieving seamless software delivery. 

**Source:** _edureka.co_

#### Q5: Are you more Dev or Ops? ⭐
**Answer:**
What the interview means is do you do more sysadmin work, or do you spend a lot of time working with developers on coding?

**Source:** _vminstall.com_

#### Q6: Mention what are the key aspects or principle behind DevOps? ⭐⭐
**Answer:**
The key aspects or principle behind DevOps are:

* Infrastructure as code
* Continuous deployment
* Automation
* Monitoring
* Security

**Source:** _quora.com_

#### Q7: What are the success factors for Continuous Integration? ⭐⭐
**Answer:**
*   Maintain a code repository
*   Automate the build
*   Make the build self-testing
*   Everyone commits to the baseline every day
*   Every commit (to baseline) should be built
*   Keep the build fast
*   Test in a clone of the production environment
*   Make it easy to get the latest deliverables
*   Everyone can see the results of the latest build
*   Automate deployment

**Source:** _edureka.co_

#### Q8: How have you handled failed deployments? ⭐⭐
**Answer:**


**Source:** _logz.io_

#### Q9: Why is Continuous monitoring necessary? ⭐⭐
**Answer:**
*Continuous Monitoring* allows timely identification of problems or weaknesses and quick corrective action that helps reduce expenses of an organization. Continuous monitoring provides solution that addresses three operational disciplines known as:

* continuous audit
* continuous controls monitoring
* continuous transaction inspection

**Source:** _quora.com_

#### Q10: What are the advantages of DevOps? ⭐⭐
**Answer:**
Technical benefits:

*   Continuous software delivery
*   Less complex problems to fix
*   Faster resolution of problems

Business benefits:

*   Faster delivery of features
*   More stable operating environments
*   More time available to add value (rather than fix/maintain)

**Source:** _edureka.co_

#### Q11: How is DevOps different from Agile/SDLC? ⭐⭐
**Answer:**
* Agile software development methodology focuses on the development of software.
* DevOps on the other hand is responsible for development as well as deployment of the software in the safest and most reliable way possible.


**Source:** _edureka.co_

#### Q12: What is post mortem meetings? ⭐⭐
**Answer:**
*Post mortem meeting* is a meeting where we discuss what went wrong and what steps should be taken so that failure doesn't happen again. Post mortem meetings are not about finding the one to be blamed, they are for preventing outages from reoccurring and planing redesign of the infrastructure so that downtime can be minimised. It is about learning from mistakes.

**Source:** _linoxide.com_

#### Q13: What's the next thing you would automate in your current workflow? ⭐⭐
**Answer:**


**Source:** _github.com_

#### Q14: Can we consider DevOps as an Agile methodology? ⭐⭐
**Answer:**
*DevOps* is a movement to reconcile and synchronize development and production start through a set of good practices . Its emergence is motivated by a deep changing demands of business, who want to speed up the changes to stick closer to the requirements of business and the customer.

**Source:** _linoxide.com_

#### Q15: What is DevOps engineer's duty with regards to Agile development? ⭐⭐
**Answer:**
DevOps engineer work very closely with Agile development teams to ensure they have an environment necessary to support functions such as automated testing, continuous Integration and continuous Delivery. DevOps engineer must be in constant contact with the developers and make all required parts of environment work seamlessly.

**Source:** _linoxide.com_

#### Q16: What does Containerization mean? ⭐⭐
**Answer:**
*Containerisation* is a type of *virtualization* strategy that emerged as an alternative to traditional hypervisor-based virtualization. 

In containerization, the operating system is shared by the different containers rather than cloned for each virtual machine. For example Docker provides a container virtualization platform that serves as a good alternative to hypervisor-based arrangements.

**Source:** _linoxide.com_

#### Q17: What is the function of CI (Continuous Integration) server? ⭐⭐
**Answer:**
CI server function is to continuously integrate all changes being made and committed to repository by different developers and check for compile errors. It needs to build code several times a day, preferably after every commit so it can detect which commit made the breakage if the breakage happens.

**Source:** _linoxide.com_

#### Q18: Which are the top DevOps tools? Which tools have you worked on? ⭐⭐
**Answer:**
The most popular DevOps tools are:

*   **Git**: Version Control System tool
*   **Jenkins**: Continuous Integration tool
*   **Selenium**: Continuous Testing tool
*   **Puppet, Chef, Ansible**: Configuration Management and Deployment tools
*   **Nagios**: Continuous Monitoring tool
*   **Docker**: Containerization tool

**Source:** _edureka.co_

#### Q19: What is the role of a configuration management tool in DevOps? ⭐⭐
**Answer:**
*Configuration Management* tools' purpose is to automatize deployment and configuration of software on big number of servers. Most CM tools usually use agent architecture which means that every machine being manged needs to have agent installed. 

One tool that uses agentless architecture is Ansible. It only requires SSH and Python. And if raw module is being used, not even Python is required because it can run raw bash commands. Other available and popular CM tools are Puppet, Chef, SaltStack.

**Source:** _linoxide.com_

#### Q20: Tell me about the worst-run/best-run outage you’ve been a part of. What made it bad/well-run? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q21: What is Chef? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q22: What is the difference between resource allocation and resource provisioning? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q23: How do all DevOps tools work together? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q24: What are the differences between continuous integration, continuous delivery, and continuous deployment? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q25: What's the difference between a blue/green deployment and a rolling deployment? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q26: Explain a use case for Docker ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q27: How would you assess how “deployable” a system is? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q28: How would you prepare for a migration from one platform to another? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q29: If something breaks in production, how do you know about it? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q30: Classify Cloud Platforms by category ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q31: How would you make key aspects of a software system traceable? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q32: What do you know about serverless model? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q33: What is Vagrant and what is it used for? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q34: How is container different from a virtual machine? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q35: How would you deploy software to 5000 nodes? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q36: How would you introduce Continuous Delivery in a successful, huge company for which the change from Waterfall to Continuous Delivery would be not trivial, because of the size and complexity of the business? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

## [[⬆]](#toc) <a name=Git>Git</a> Interview Questions
#### Q1: What is the command to write a commit message in Git? ⭐
**Answer:**
Use:
```sh
git commit -a
```

 -a on the command line instructs git to commit the new content of all tracked files that have been modified. You can use 
```sh
git add <file>
```
or 
```sh
git add -A
```

before git commit -a if new files need to be committed for the first time.


**Source:** _edureka.co_

#### Q2: What is difference between Git vs SVN? ⭐
**Answer:**
The main point in Git vs SVN debate boils down to this: Git is a distributed version control system (DVCS), whereas SVN is a centralized version control system.

**Source:** _medium.com_

#### Q3: What is Git? ⭐
**Answer:**
Git is a Distributed Version Control system (DVCS). It can track changes to a file and allows you to revert back to any particular change.

Its distributed architecture provides many advantages over other Version Control Systems (VCS) like SVN one major advantage is that it does not rely on a central server to store all the versions of a project’s files. 

**Source:** _edureka.co_

#### Q4: How to undo the most recent commits in Git? ⭐⭐
**Details:**
You accidentally committed wrong files to Git, but haven't pushed the commit to the server yet.
How can you undo those commits from the local repository?

**Answer:**
```sh
$ git commit -m "Something terribly misguided"      
$ git reset HEAD~                                   # copied the old head to .git/ORIG_HEAD
# edit files as necessary                     
$ git add ...                                       
$ git commit -c ORIG_HEAD                           # will open an editor, which initially contains the log message from the old commit and allows you to edit it
```

**Source:** _stackoverflow.com_

#### Q5: What is Git fork? What is difference between fork, branch and clone? ⭐⭐
**Answer:**
* A **fork** is a remote, server-side copy of a repository, distinct from the original. A fork isn't a Git concept really, it's more a political/social idea. 
* A **clone** is not a fork; a clone is a local copy of some remote repository.  When you clone, you are actually copying the entire source repository, including all the history and branches.
* A **branch** is a mechanism to handle the changes within a single repository in order to eventually merge them with the rest of code. A branch is something that is within a repository. Conceptually, it represents a thread of development.

**Source:** _stackoverflow.com_

#### Q6: What is the difference between "git pull" and "git fetch"? ⭐⭐
**Answer:**
In the simplest terms, `git pull` does a `git fetch` followed by a `git merge`.

* When you use `pull`, Git tries to automatically do your work for you. **It is context sensitive**, so Git will merge any pulled commits into the branch you are currently working in.  `pull` **automatically merges the commits without letting you review them first**. If you don’t closely manage your branches, you may run into frequent conflicts.

* When you `fetch`, Git gathers any commits from the target branch that do not exist in your current branch and **stores them in your local repository**. However, **it does not merge them with your current branch**. This is particularly useful if you need to keep your repository up to date, but are working on something that might break if you update your files. To integrate the commits into your master branch, you use `merge`.

**Source:** _stackoverflow.com_

#### Q7: What's the difference between a "pull request" and a "branch"? ⭐⭐
**Answer:**
* A **branch** is just a separate version of the code.

* A **pull request** is when someone take the repository, makes their own branch, does some changes, then tries to merge that branch in (put their changes in the other person's code repository).

**Source:** _stackoverflow.com_

#### Q8: How does the Centralized Workflow work? ⭐⭐
**Answer:**
The **Centralized Workflow** uses a central repository to serve as the single point-of-entry for all changes to the project. The default development branch is called master and all changes are committed into this branch.

Developers start by cloning the central repository. In their own local copies of the project, they edit files and commit changes. These new commits are stored locally.

To publish changes to the official project, developers *push* their local master branch to the central repository. Before the developer can publish their feature, they need to *fetch* the updated central commits and rebase their changes on top of them. 

Compared to other workflows, the Centralized Workflow has no defined pull request or forking patterns. 

**Source:** _atlassian.com_

#### Q9: You need to update your local repos. What git commands will you use? ⭐⭐
**Answer:**
It’s a two steps process. First you fetch the changes from a remote named origin:

```sh
git fetch origin
```
Then you merge a branch master to local:

```sh
git merge origin/master
```
Or simply:

```sh
git pull origin master
```
If origin is a default remote and ‘master’ is default branch, you can drop it eg. `git pull`.

**Source:** _samwize.com_

#### Q10: You need to rollback to a previous commit and don't care about recent changes. What commands should you use? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q11: What is "git cherry-pick"? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q12: Tell me the difference between HEAD, working tree and index, in Git? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q13: When should I use "git stash"? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q14: How to revert previous commit in git? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q15: Explain the advantages of Forking Workflow ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q16: Could you explain the Gitflow workflow? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q17: Write down a sequence of git commands for a "Rebase Workflow" ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q18: What is the "HEAD" in Git? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q19: How to remove a file from git without removing it from your file system? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q20: What is difference between "git stash pop" and "git stash apply"? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q21: Can you explain what “git reset” does in plain english? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q22: Write down a git command to check difference between two commits ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q23: How to amend older Git commit? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q24: What git command do you need to use to know who changed certain lines in a specific file? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q25: When do you use "git rebase" instead of "git merge"? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q26: Do you know how to easily undo a git rebase?  ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

## [[⬆]](#toc) <a name=Golang>Golang</a> Interview Questions
#### Q1: What is Go? ⭐
**Answer:**
**Go** is a general-purpose language designed with systems programming in mind. It was initially developed at Google in year 2007 by Robert Griesemer, Rob Pike, and Ken Thompson. It is strongly and statically typed, provides inbuilt support for garbage collection and supports concurrent programming. Programs are constructed using packages, for efficient management of dependencies. Go programming implementations use a traditional compile and link model to generate executable binaries.

**Source:** _tutorialspoint.com_

#### Q2: Is Go a new language, framework or library? ⭐
**Answer:**
**Go** isn't a library and not a framework, it's a new language. 

Go is mostly in the C family (basic syntax), with significant input from the Pascal/Modula/Oberon family (declarations, packages). Go does have an extensive library, called the runtime, that is part of every Go program. Although it is more central to the language, Go's runtime is analogous to libc, the C library. It is important to understand, however, that Go's runtime does not include a virtual machine, such as is provided by the Java runtime. Go programs are compiled ahead of time to native machine code.

**Source:** _golang.org_

#### Q3: What is static type declaration of a variable in Go? ⭐⭐
**Answer:**
*Static type variable declaration* provides assurance to the compiler that there is one variable existing with the given type and name so that compiler proceed for further compilation without needing complete detail about the variable. A variable declaration has its meaning at the time of compilation only, compiler needs actual variable declaration at the time of linking of the program.

**Source:** _tutorialspoint.com_

#### Q4: What is dynamic type declaration of a variable in Go? ⭐⭐
**Answer:**
A *dynamic type variable declaration* requires compiler to interpret the type of variable based on value passed to it. Compiler don't need a variable to have type statically as a necessary requirement.

**Source:** _tutorialspoint.com_

#### Q5: Can you declared multiple types of variables in single declaration in Go? ⭐⭐
**Answer:**
Yes. Variables of different types can be declared in one go using type inference.

```go
var a, b, c =  3,  4,  "foo"  
```

**Source:** _tutorialspoint.com_

#### Q6: What is a pointer? ⭐⭐
**Answer:**
A **pointer variable** can hold the *address* of a variable.

Consider:
```go
var x =  5  var p *int p =  &x
fmt.Printf("x = %d",  *p)
```

Here `x` can be accessed by `*p`.

**Source:** _tutorialspoint.com_

#### Q7: Can you return multiple values from a function? ⭐⭐
**Answer:**
A Go function can return multiple values.

Consider:
```go
package main
import "fmt"

func swap(x, y string) (string, string) {
   return y, x
}
func main() {
   a, b := swap("Mahesh", "Kumar")
   fmt.Println(a, b)
}
```

**Source:** _tutorialspoint.com_

#### Q8: What are some advantages of using Go? ⭐⭐
**Answer:**
**Go** is an attempt to introduce a new, concurrent, garbage-collected language with fast compilation and the following benefits: 
* It is possible to compile a large Go program in a few seconds on a single computer.
* Go provides a model for software construction that makes dependency analysis easy and avoids much of the overhead of C-style include files and libraries.
* Go's type system has no hierarchy, so no time is spent defining the relationships between types. Also, although Go has static types, the language attempts to make types feel lighter weight than in typical OO languages.
* Go is fully garbage-collected and provides fundamental support for concurrent execution and communication.
* By its design, Go proposes an approach for the construction of system software on multicore machines.

**Source:** _golang.org_

#### Q9: What kind of type conversion is supported by Go? ⭐⭐
**Answer:**
Go is very strict about **explicit typing**. There is no automatic type promotion or conversion. Explicit type conversion is required to assign a variable of one type to another. 

Consider:
```go
i := 55      //int
j := 67.8    //float64
sum := i + int(j) //j is converted to int
```

**Source:** _golangbot.com_

#### Q10: What are the benefits of using Go programming? ⭐⭐
**Answer:**
Following are the benefits of using Go programming:

*   Support for environment adopting patterns similar to dynamic languages. For example type inference (`x := 0` is valid declaration of a variable `x` of type `int`).
*   Compilation time is fast.
*   In built concurrency support: light-weight processes (via goroutines), channels, select statement.
*   Conciseness, Simplicity, and Safety.
*   Support for Interfaces and Type embedding.
*   The go compiler supports static linking. All the go code can be statically linked into one big fat binary and it can be deployed in cloud servers easily without worrying about dependencies.

**Source:** _tutorialspoint.com_

#### Q11: Why the Go language was created? ⭐⭐
**Answer:**
**Go** was born out of frustration with existing languages and environments for systems programming. 

Go is an attempt to have:
* an interpreted, dynamically typed language with 
* the efficiency and safety of a statically typed, compiled language
* support for networked and multicore computing
* be fast in compilation

To meet these goals required addressing a number of linguistic issues: an expressive but lightweight type system; concurrency and garbage collection; rigid dependency specification; and so on. These cannot be addressed well by libraries or tools so a new language was born.


**Source:** _golang.org_

#### Q12: Does Go have exceptions? ⭐⭐
**Answer:**
No, Go takes a different approach. For plain error handling, Go's **multi-value returns** make it easy to report an error without overloading the return value. Go code uses error values to indicate an abnormal state. 

Consider:
```go
func Open(name string) (file *File, err error)
```
```go
f, err := os.Open("filename.ext")
if err != nil {
    log.Fatal(err)
}
// do something with the open *File f
```

**Source:** _golang.org_

#### Q13: What are Goroutines? ⭐⭐
**Answer:**
**Goroutines** are functions or methods that run concurrently with other functions or methods. Goroutines can be thought of as light weight threads. The cost of creating a Goroutine is tiny when compared to a thread. Its common for Go applications to have thousands of Goroutines running concurrently.

**Source:** _golangbot.com_

#### Q14: Let's talk variable declaration in Go. Could you explain what is a variable "zero value"? ⭐⭐
**Answer:**
Variable is the name given to a memory location to store a value of a specific type. There are various syntaxes to declare variables in go.

```go
// 1 - variable declaration, then assignment
var age int
age = 29

// 2 - variable declaration with initial value
var age2 int = 29

// 3 - Type inference
var age3 = 29

// 4 - declaring multiple variables
var width, height int = 100, 50

// 5 - declare variables belonging to different types in a single statement
var (  
      name1 = initialvalue1,
      name2 = initialvalue2
)
// 6 - short hand declaration
name, age4 := "naveen", 29 //short hand declaration
```

If a variable is not assigned any value, go automatically initialises it with the **zero value of the variable's type**. Go is strongly typed, so variables declared as belonging to one type cannot be assigned a value of another type.

**Source:** _golangbot.com_

#### Q15: Is Go an object-oriented language? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q16: Name some advantages of Goroutines over threads ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q17: Have you worked with Go 2? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q18: What is "rune" type in Go? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q19: What is so special about constants in Go? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

## [[⬆]](#toc) <a name=GraphQL>GraphQL</a> Interview Questions
#### Q1: What is GraphQL? ⭐
**Answer:**
GraphQL is a query language created by [Facebook](http://facebook.github.io/) in 2012 which provides a **common interface between the client and the server for data fetching and manipulations**.

The client asks for various data from the GraphQL server via queries. The response format is described in the query and defined by the client instead of the server: they are called **client‐specified queries**.  
The structure of the data is not hardcoded as in traditional REST APIs - this makes retrieving data from the server more efficient for the client.

**Source:** _howtographql.com_

#### Q2: Is GraphQL a Database Technology? ⭐
**Answer:**
No. GraphQL is often confused with being a database technology. This is a misconception, GraphQL is a _query language_ for APIs - not databases. In that sense it’s database agnostic and can be used with any kind of database or even no database at all.

**Source:** _howtographql.com_

#### Q3: Is GraphQL only for React / Javascript Developers? ⭐
**Answer:**
No. GraphQL is an API technology so it can be used in any context where an API is required.

On the _backend_, a GraphQL server can be implemented in any programming language that can be used to build a web server. Next to Javascript, there are popular reference implementations for Ruby, Python, Scala, Java, Clojure, Go and .NET.

Since a GraphQL API is usually operated over HTTP, any client that can speak HTTP is able to query data from a GraphQL server.

*Note*: GraphQL is actually transport layer agnostic, so you could choose other protocols than HTTP to implement your server.

**Source:** _howtographql.com_

#### Q4: How to do Error Handling? ⭐⭐
**Answer:**
A successful GraphQL query is supposed to return a JSON object with a root field called `"data"`. If the request fails or partially fails (e.g. because the user requesting the data doesn’t have the right access permissions), a second root field called `"errors"` is added to the response:
```js
    {
      "data": { ... },
      "errors": [ ... ]
    }
```   

**Source:** _howtographql.com_

#### Q5: Where is GraphQL useful? ⭐⭐
**Answer:**
GraphQL helps where your **client needs a flexible response** format to avoid extra queries and/or massive data transformation with the overhead of keeping them in sync.

Using a GraphQL server makes it very easy for a client side developer to change the response format without any change on the backend.

With GraphQL, you can describe the required data in a more natural way. It can speed up development, because in application structures like **top-down rendering** in React, the required data is more similar to your component structure.

**Source:** _blog.risingstack.com_

#### Q6: What is GraphQL schema? ⭐⭐
**Answer:**
Every GraphQL server has two core parts that determine how it works: a schema and resolve functions.

The *schema* is a model of the data that can be fetched through the GraphQL server. It defines what queries clients are allowed to make, what types of data can be fetched from the server, and what the relationships between these types are. 

Consider:

```css
type Author {
  id: Int
  name: String
  posts: [Post]
}
type Post {
  id: Int
  title: String
  text: String
  author: Author
}
type Query {
  getAuthor(id: Int): Author
  getPostsByTitle(titleContains: String): [Post]
}
schema {
  query: Query
}
```

**Source:** _dev-blog.apollodata.com_

#### Q7: How to do Authentication and Authorization? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q8: Does GraphQL Support Offline Usage? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q9: How to do Server-side Caching? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q10: List the key concepts of the GraphQL query language ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q11: Explain the main difference between REST and GraphQL ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q12: What kind of operations could GraphQL schema have? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q13: Are there any disadvantages to GraphQL? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

## [[⬆]](#toc) <a name=HTML5>HTML 5</a> Interview Questions
#### Q1: Write a HTML table tag sequence that outputs the following ⭐
**Answer:**
Write a HTML table tag sequence that outputs the following:
```
50 pcs 100 500
10 pcs 5 50
```

**Answer:**
```html
<table>
  <tr>
    <td>50 pcs</td>
    <td>100</td>
    <td>500</td>
  </tr>
  <tr>
    <td>10 pcs</td>
    <td>5</td>
    <td>50</td>
  </tr>
</table>
```

**Source:** _toptal.com_

#### Q2: What is an iframe and how it works? ⭐
**Answer:**
An **iframe** is an **HTML document** which can be embedded inside another HTML page.

**Example**:

```html
<iframe src="https://github.com" height="300px" width="300px"></iframe>
```

**Source:** _github.com/FuelFrontend_

#### Q3: Explain meta tags in HTML ⭐
**Answer:**
- **Meta tags** always go inside **head tag** of the HTML page
- **Meta tags** is always passed as name/value pairs
- **Meta tags** are not displayed on the page but intended for the browser
- **Meta tags** can contain information about **character encoding**, **description**, **title** of the document etc,

**Example**:

```html
<!DOCTYPE html>
<html>
<head>
  <meta name="description" content="I am a web page with description"> 
  <title>Home Page</title>
</head>
<body>
  
</body>
</html>
```


**Source:** _github.com/FuelFrontend_

#### Q4: What is the purpose of the alt attribute on images? ⭐
**Answer:**
The `alt` attribute provides alternative information for an image if a user cannot view it. The `alt` attribute should be used to describe any images except those which only serve a decorative purposes, in which case it should be left empty.


**Source:** _developer.mozilla.org_

#### Q5: What is a self closing tag?  ⭐⭐
**Answer:**
In HTML5 it is not strictly necessary to close certain HTML tags. The tags that aren’t required to have specific closing tags are called “self closing” tags.

An example of a self closing tag is something like a line break (`<br />`) or the meta tag (`<meta>`). This means that the following are both acceptable:

```html
<meta charset="UTF-8">
...
<meta charset="UTF-8" />
```

**Source:** _blog.teamtreehouse.com_

#### Q6: What is the difference between span and div? ⭐⭐
**Answer:**
* `div` is a block element
* `span` is inline element 

For bonus points, you could point out that it’s illegal to place a block element inside an inline element, and that while `div` can have a `p` tag, and a `p` tag can have a `span`, it is not possible for `span` to have a `div` or `p` tag inside.

**Source:** _thatjsdude.com_

#### Q7: How Can I Get Indexed Better by Search Engines? ⭐⭐
**Answer:**
It is possible to get indexed better by placing the following two statements in the `<HEAD>` part of your documents:

```html
<META NAME="keywords" CONTENT="keyword keyword keyword keyword">
<META NAME="description" CONTENT="description of your site">
```
Both may contain up to 1022 characters. If a keyword is used more than 7 times, the keywords tag will be ignored altogether. Also, you cannot put markup (other than entities) in the description or keywords list.

**Source:** _freejavaguide.com_

#### Q8: How can you highlight text in HTML? ⭐⭐
**Answer:**
If you are working with an HTML5 page, the `<mark>` tag can be a quick and easy way of highlighting or marking text on a page:

```html
<mark>highlighted text</mark>
```

To highlight text with just HTML code and support for all browsers, set the background-color style, as shown in the example below, using the <span> HTML tag.
```html
<span style="background-color: #FFFF00">Yellow text.</span>
```

**Source:** _computerhope.com_

#### Q9: Briefly describe the correct usage of the following HTML5 semantic elements: <header>, <article>, <section>, <footer> ⭐⭐
**Answer:**
* `<header>` is used to contain introductory and navigational information about a section of the page. This can include the section heading, the author’s name, time and date of publication, table of contents, or other navigational information.

* `<article>` is meant to house a self-contained composition that can logically be independently recreated outside of the page without losing it’s meaining. Individual blog posts or news stories are good examples.

* `<section>` is a flexible container for holding content that shares a common informational theme or purpose.

* `<footer>` is used to hold information that should appear at the end of a section of content and contain additional information about the section. Author’s name, copyright information, and related links are typical examples of such content.


**Source:** _w3schools.com_

#### Q10: What is Character Encoding? ⭐⭐
**Answer:**
To display an HTML page correctly, a web browser must know which character set (character encoding) to use. This is specified in the <meta> tag:

**HTML4:**
```html
<meta http-equiv="Content-Type" content="text/html;charset=ISO-8859-1">
```

**HTML5:**
```html
<meta charset="UTF-8">
```


**Source:** _w3schools.com_

#### Q11: What were some of the key goals and motivations for the HTML5 specification? ⭐⭐
**Answer:**
HTML5 was designed to replace HTML 4, XHTML, and the HTML DOM Level 2. The key goals and motivations behind the HTML5 specification were to:

* Deliver rich content (graphics, movies, etc.) without the need for additional plugins, such as Flash.
* Provide better semantic support for web page structure through new structural element tags.
* Provide a stricter parsing standard to simplify error handling, ensure more consistent cross-browser behaviour, and simplify compatibility with documents written to older standards.
* Provide better cross-platform support whether running on a PC, Tablet, or Smartphone.

**Source:** _toptal.com_

#### Q12: How do you change the direction of html text? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q13: What is WebSQL? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q14: Explain the difference between block elements and inline elements ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q15: What is an optional tag? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q16: When is it appropriate to use the small element? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q17: What is the difference between <section> and <div>? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q18: What are Web Workers? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q19: What does a DOCTYPE do? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q20: How do you serve a page with content in multiple languages? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q21: What is the purpose of cache busting and how can you achieve it? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q22: Can a web page contain multiple <header> elements? What about <footer> elements? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q23: What are `data-` attributes good for? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q24: What are `defer` and `async` attributes on a `<script>` tag? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q25: What is the DOM? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q26: Discuss the differences between an HTML specification and a browser’s implementation thereof. ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q27: What are some differences that XHTML has compared to HTML? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q28: Where and why is the `rel="noopener"` attribute used? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q29: What is HTML5 Web Storage? Explain `localStorage` and `sessionStorage`. ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q30: What is WebSQL? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q31: Describe the difference between a 'cookie', 'sessionStorage' and 'localStorage'. ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q32: How do you set IE compatibility mode? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q33: What's new in HTML 5? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q34: Have you used different HTML templating languages before? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q35: Explain the difference between cookies, session and local storage ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q36: Explain almost standard, full standard and quirks mode ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q37: Describe the difference between <script>, <script async> and <script defer>. ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q38: What is WebP? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q39: What is progressive rendering? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q40: Why you would use a `srcset` attribute in an image tag? Explain the process the browser uses when evaluating the content of this attribute. ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q41: Why to use HTML5 semantic tags? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q42: HTML Markup Validity ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q43: Why do I need a doctype and what does it do? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q44: What's the difference between Full Standard, Almost Standard and Quirks Mode? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q45: What kind of things must you be wary of when designing or developing for multilingual sites? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q46: How would you select svg or canvas for your site? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q47: What are the building blocks of HTML5? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q48: What is an HTML preprocessor and are you using it? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q49: What is the purpose of 'main' element? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q50: What are Web Components? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q51: What is accessibility & ARIA role means in a web application? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q52: Could you generate a public key in HTML? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q53: Why is it generally a good idea to position CSS <link>s between <head></head> and JS <script>s just before </body>? Do you know any exceptions? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q54: What is an IndexedDB? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

## [[⬆]](#toc) <a name=Java>Java</a> Interview Questions
#### Q1: What is JVM? Why is Java called the “Platform Independent Programming Language”?  ⭐
**Answer:**
A Java virtual machine (JVM) is a process virtual machine that can execute Java bytecode. Each Java source file is compiled into a bytecode file, which is executed by the JVM. Java was designed to allow application programs to be built that could be run on any platform, without having to be rewritten or recompiled by the programmer for each separate platform. A Java virtual machine makes this possible, because it is aware of the specific instruction lengths and other particularities of the underlying hardware platform.

**Source:** _github.com/snowdream_

#### Q2: What is a Servlet? ⭐
**Answer:**
The servlet is a Java programming language class used to process client requests and generate dynamic web content. Servlets are mostly used to process or store data submitted by an HTML form, provide dynamic content and manage state information that does not exist in the stateless HTTP protocol.

**Source:** _github.com/snowdream_

#### Q3: What is a JSP Page? ⭐
**Answer:**
A Java Server Page (JSP) is a text document that contains two types of text: static data and JSP elements. Static data can be expressed in any text-based format, such as HTML or XML. JSP is a technology that mixes static content with dynamically-generated content.

**Source:** _github.com/snowdream_

#### Q4: Let's talk Swing. What is the difference between a Choice and a List? ⭐
**Answer:**
A Choice is displayed in a compact form that must be pulled down, in order for a user to be able to see the list of all available choices. Only one item may be selected from a Choice. A List may be displayed in such a way that several List items are visible. A List supports the selection of one or more List items.

**Source:** _github.com/snowdream_

#### Q5: What is the difference between an Applet and a Java Application? ⭐
**Answer:**
Applets are executed within a java enabled browser, but a Java application is a standalone Java program that can be executed outside of a browser. However, they both require the existence of a Java Virtual Machine (JVM). Furthermore, a Java application requires a main method with a specific signature, in order to start its execution. Java applets don’t need such a method to start their execution. Finally, Java applets typically use a restrictive security policy, while Java applications usually use more relaxed security policies.

**Source:** _github.com/snowdream_

#### Q6: What is the Difference between JDK and JRE?  ⭐
**Answer:**
The Java Runtime Environment (JRE) is basically the Java Virtual Machine (JVM) where your Java programs are being executed. It also includes browser plugins for applet execution. The Java Development Kit (JDK) is the full featured Software Development Kit for Java, including the JRE, the compilers and tools (like JavaDoc, and Java Debugger), in order for a user to develop, compile and execute Java applications.

**Source:** _github.com/snowdream_

#### Q7: What are the two types of Exceptions in Java? Which are the differences between them?  ⭐
**Answer:**
Java has two types of exceptions: checked exceptions and unchecked exceptions. Unchecked exceptions do not need to be declared in a method or a constructor’s throws clause, if they can be thrown by the execution of the method or the constructor, and propagate outside the method or constructor boundary. On the other hand, checked exceptions must be declared in a method or a constructor’s throws clause. See here for tips on [Java exception handling](http://www.javacodegeeks.com/2013/07/java-exception-handling-tutorial-with-examples-and-best-practices.html).

**Source:** _github.com/snowdream_

#### Q8: Explain the architechure of a Servlet. ⭐⭐
**Answer:**
The core abstraction that must be implemented by all servlets is the javax.servlet.Servlet interface. Each servlet must implement it either directly or indirectly, either by extending javax.servlet.GenericServlet or javax.servlet.http.HTTPServlet. Finally, each servlet is able to serve multiple requests in parallel using multithreading.

**Source:** _github.com/snowdream_

#### Q9: What is the difference between an Interface and an Abstract class?  ⭐⭐
**Answer:**
Java provides and supports the creation both of [abstract classes](http://examples.javacodegeeks.com/java-basics/java-abstract-class-example/) and interfaces. Both implementations share some common characteristics, but they differ in the following features:

* All methods in an interface are implicitly abstract. On the other hand, an abstract class may contain both abstract and non-abstract methods.
* A class may implement a number of Interfaces, but can extend only one abstract class.
* In order for a class to implement an interface, it must implement all its declared methods. However, a class may not implement all declared methods of an abstract class. Though, in this case, the sub-class must also be declared as abstract.
* Abstract classes can implement interfaces without even providing the implementation of interface methods.
* Variables declared in a Java interface is by default final. An abstract class may contain non-final variables.
* Members of a Java interface are public by default. A member of an abstract class can either be private, protected or public.
* An interface is absolutely abstract and cannot be instantiated. An abstract class also cannot be instantiated, but can be invoked if it contains a main method.
* 
Also check out the [Abstract class and Interface differences for JDK 8](http://www.javacodegeeks.com/2014/04/abstract-class-versus-interface-in-the-jdk-8-era.html).

**Source:** _github.com/snowdream_

#### Q10: What are pass by reference and pass by value?  ⭐⭐
**Answer:**
When an object is passed by value, this means that a copy of the object is passed. Thus, even if changes are made to that object, it doesn’t affect the original value. When an object is passed by reference, this means that the actual object is not passed, rather a reference of the object is passed. Thus, any changes made by the external method, are also reflected in all places.

**Source:** _github.com/snowdream_

#### Q11: What is the difference between processes and threads? ⭐⭐
**Answer:**
A process is an execution of a program, while a [Thread](http://docs.oracle.com/javase/7/docs/api/java/lang/Thread.html) is a single execution sequence within a process. A process can contain multiple threads. A [Thread](http://docs.oracle.com/javase/7/docs/api/java/lang/Thread.html) is sometimes called a lightweight process.

**Source:** _github.com/snowdream_

#### Q12: Explain Serialization and Deserialization.  ⭐⭐
**Answer:**
Java provides a mechanism, called object serialization where an object can be represented as a sequence of bytes and includes the object’s data, as well as information about the object’s type, and the types of data stored in the object. Thus, serialization can be seen as a way of flattening objects, in order to be stored on disk, and later, read back and reconstituted. Deserialisation is the reverse process of converting an object from its flattened state to a live object.

**Source:** _github.com/snowdream_

#### Q13: What are Expressions? ⭐⭐
**Answer:**
A JSP expression is used to insert the value of a scripting language expression, converted into a string, into the data stream returned to the client, by the web server. Expressions are defined between <% = and %> tags.

**Source:** _github.com/snowdream_

#### Q14: What are Decalarations? ⭐⭐
**Answer:**
Declarations are similar to variable declarations in Java. Declarations are used to declare variables for subsequent use in expressions or scriptlets. To add a declaration, you must use the sequences to enclose your declarations.

**Source:** _github.com/snowdream_

#### Q15: What are JSP actions? ⭐⭐
**Answer:**
JSP actions use constructs in XML syntax to control the behavior of the servlet engine. JSP actions are executed when a JSP page is requested. They can be dynamically inserted into a file, re-use JavaBeans components, forward the user to another page, or generate HTML for the Java plugin.Some of the available actions are listed below:

* jsp:include – includes a file, when the JSP page is requested.
* jsp:useBean – finds or instantiates a JavaBean.
* jsp:setProperty – sets the property of a JavaBean.
* jsp:getProperty – gets the property of a JavaBean.
* jsp:forward – forwards the requester to a new page.
* jsp:plugin – generates browser-specific code.


**Source:** _github.com/snowdream_

#### Q16: What are Directives? ⭐⭐
**Answer:**
What are the different types of Directives available in JSP ? Directives are instructions that are processed by the JSP engine, when the page is compiled to a servlet. Directives are used to set page-level instructions, insert data from external files, and specify custom tag libraries. Directives are defined between < %@ and % >.The different types of directives are shown below:

* Include directive: it is used to include a file and merges the content of the file with the current page.
* Page directive: it is used to define specific attributes in the JSP page, like error page and buffer.
* Taglib: it is used to declare a custom tag library which is used in the page.

**Source:** _github.com/snowdream_

#### Q17: How are the JSP requests handled? ⭐⭐
**Answer:**
On the arrival of a JSP request, the browser first requests a page with a .jsp extension. Then, the Web server reads the request and using the JSP compiler, the Web server converts the JSP page into a servlet class. Notice that the JSP file is compiled only on the first request of the page, or if the JSP file has changed.The generated servlet class is invoked, in order to handle the browser’s request. Once the execution of the request is over, the servlet sends a response back to the client. See [how to get Request parameters in a JSP](http://examples.javacodegeeks.com/enterprise-java/jsp/get-request-parameter-in-jsp-page/).

**Source:** _github.com/snowdream_

#### Q18: What are the basic interfaces of Java Collections Framework?  ⭐⭐
**Answer:**
[Java Collections Framework](http://docs.oracle.com/javase/7/docs/technotes/guides/collections/overview.html) provides a well designed set of interfaces and classes that support operations on a collections of objects. The most basic interfaces that reside in the Java Collections Framework are:

* [Collection](http://docs.oracle.com/javase/7/docs/api/java/util/Collection.html), which represents a group of objects known as its elements.
* [Set](http://docs.oracle.com/javase/7/docs/api/java/util/Set.html), which is a collection that cannot contain duplicate elements.
* [List](http://docs.oracle.com/javase/7/docs/api/java/util/List.html), which is an ordered collection and can contain duplicate elements.
* [Map](http://docs.oracle.com/javase/7/docs/api/java/util/Map.html), which is an object that maps keys to values and cannot contain duplicate keys.

**Source:** _github.com/snowdream_

#### Q19: What does the “static” keyword mean? Can you override private or static method in Java? ⭐⭐
**Answer:**
The static keyword denotes that a member variable or method can be accessed, without requiring an instantiation of the class to which it belongs. A user cannot override static methods in Java, because method overriding is based upon dynamic binding at runtime and static methods are statically binded at compile time. A static method is not associated with any instance of a class so the concept is not applicable.

**Source:** _github.com/snowdream_

#### Q20: What is an Iterator?  ⭐⭐
**Answer:**
The [Iterator](http://docs.oracle.com/javase/7/docs/api/java/util/Iterator.html) interface provides a number of methods that are able to iterate over any [Collection](http://docs.oracle.com/javase/7/docs/api/java/util/Collection.html). Each Java [Collection](http://docs.oracle.com/javase/7/docs/api/java/util/Collection.html) contains the [Iterator](http://docs.oracle.com/javase/7/docs/api/java/util/Iterator.html)  method that returns an [Iterator](http://docs.oracle.com/javase/7/docs/api/java/util/Iterator.html)  instance. Iterators are capable of removing elements from the underlying collection during the iteration.

**Source:** _github.com/snowdream_

#### Q21: What is the purpose Class.forName method? ⭐⭐
**Answer:**
This method is used to method is used to load the driver that will establish a connection to the database.

**Source:** _github.com/snowdream_

#### Q22: What is JDBC? ⭐⭐
**Answer:**
JDBC is an abstraction layer that allows users to choose between databases. [JDBC enables developers to write database applications in Java](http://www.javacodegeeks.com/2014/03/java-8-friday-java-8-will-revolutionize-database-access.html), without having to concern themselves with the underlying details of a particular database.

**Source:** _github.com/snowdream_

#### Q23: How HashMap works in Java?  ⭐⭐
**Answer:**
[A HashMap in Java stores key-value pairs](http://www.javacodegeeks.com/2014/03/how-hashmap-works-in-java.html). The [HashMap](http://docs.oracle.com/javase/7/docs/api/java/util/HashMap.html) requires a hash function and uses hashCode and equals methods, in order to put and retrieve elements to and from the collection respectively. When the put method is invoked, the [HashMap](http://docs.oracle.com/javase/7/docs/api/java/util/HashMap.html) calculates the hash value of the key and stores the pair in the appropriate index inside the collection. If the key exists, its value is updated with the new value. Some important characteristics of a [HashMap](http://docs.oracle.com/javase/7/docs/api/java/util/HashMap.html) are its capacity, its load factor and the threshold resizing.

**Source:** _github.com/snowdream_

#### Q24: What is the design pattern that Java uses for all Swing components? ⭐⭐
**Answer:**
The design pattern used by Java for all Swing components is the Model View Controller (MVC) pattern.

**Source:** _github.com/snowdream_

#### Q25: What differences exist between HashMap and Hashtable?  ⭐⭐
**Answer:**
Both the [HashMap](http://docs.oracle.com/javase/7/docs/api/java/util/HashMap.html) and [Hashtable](http://docs.oracle.com/javase/7/docs/api/java/util/Hashtable.html) classes implement the Map interface and thus, have very similar characteristics. However, they differ in the following features:

* A [HashMap](http://docs.oracle.com/javase/7/docs/api/java/util/HashMap.html) allows the existence of null keys and values, while a [Hashtable](http://docs.oracle.com/javase/7/docs/api/java/util/Hashtable.html) doesn’t allow neither null keys, nor null values.
* A [Hashtable](http://docs.oracle.com/javase/7/docs/api/java/util/Hashtable.html) is synchronized, while a [HashMap](http://docs.oracle.com/javase/7/docs/api/java/util/HashMap.html) is not. Thus, [HashMap](http://docs.oracle.com/javase/7/docs/api/java/util/HashMap.html) is preferred in single-threaded environments, while a [Hashtable](http://docs.oracle.com/javase/7/docs/api/java/util/Hashtable.html) is suitable for multi-threaded environments.
* A [HashMap](http://docs.oracle.com/javase/7/docs/api/java/util/HashMap.html) provides its set of keys and a Java application can iterate over them. Thus, a [HashMap](http://docs.oracle.com/javase/7/docs/api/java/util/HashMap.html) is fail-fast. On the other hand, a [Hashtable](http://docs.oracle.com/javase/7/docs/api/java/util/Hashtable.html) provides an [Enumeration](http://docs.oracle.com/javase/7/docs/api/java/util/Enumeration.html) of its keys.
* The [Hashtable](http://docs.oracle.com/javase/7/docs/api/java/util/Hashtable.html) class is considered to be a legacy class.

**Source:** _github.com/snowdream_

#### Q26: What advantage do Java’s layout managers provide over traditional windowing systems? ⭐⭐
**Answer:**
Java uses layout managers to lay out components in a consistent manner, across all windowing platforms. Since layout managers aren’t tied to absolute sizing and positioning, they are able to accomodate platform-specific differences among windowing systems

**Source:** _github.com/snowdream_

#### Q27: How can a GUI component handle its own events? ⭐⭐
**Answer:**
A GUI component can handle its own events, by implementing the corresponding event-listener interface and adding itself as its own event listener.

**Source:** _github.com/snowdream_

#### Q28: What is a layout manager? ⭐⭐
**Answer:**
A layout manager is the used to organize the components in a container.

**Source:** _github.com/snowdream_

#### Q29: What’s the difference between sendRedirect and forward methods? ⭐⭐
**Answer:**
The sendRedirect method creates a new request, while the forward method just forwards a request to a new target. The previous request scope objects are not available after a redirect, because it results in a new request. On the other hand, the previous request scope objects are available after forwarding. FInally, in general, the sendRedirect method is considered to be slower compare to the forward method.

**Source:** _github.com/snowdream_

#### Q30: What do you know about the big-O notation and can you give some examples with respect to different data structures? ⭐⭐
**Answer:**
The Big-O notation simply describes how well an algorithm scales or performs in the worst case scenario as the number of elements in a data structure increases. The Big-O notation can also be used to describe other behavior such as memory consumption. Since the collection classes are actually data structures, we usually use the Big-O notation to chose the best implementation to use, based on time, memory and performance. Big-O notation can give a good indication about performance for large amounts of data.

**Source:** _github.com/snowdream_

#### Q31: What are the Data Types supported by Java? What is Autoboxing and Unboxing? ⭐⭐
**Answer:**
The eight primitive data types supported by the Java programming language are:

* byte
* short
* int
* long
* float
* double
* boolean
* char

Autoboxing is [the automatic conversion made by the Java compiler](http://www.javacodegeeks.com/2013/07/java-generics-tutorial-example-class-interface-methods-wildcards-and-much-more.html) between the primitive types and their corresponding object wrapper classes. For example, the compiler converts an int to an [Integer](http://docs.oracle.com/javase/7/docs/api/java/lang/Integer.html?is-external=true), a double to a [Double](http://docs.oracle.com/javase/7/docs/api/java/lang/Double.html), and so on. If the conversion goes the other way, this operation is called unboxing.

**Source:** _github.com/snowdream_

#### Q32: What is Function Overriding and Overloading in Java? ⭐⭐
**Answer:**
Method overloading in Java occurs when two or more methods in the same class have the exact same name, but different parameters. On the other hand, method overriding is defined as the case when a child class redefines the same method as a parent class. Overridden methods must have the same name, argument list, and return type. The overriding method may not limit the access of the method it overrides.

**Source:** _github.com/snowdream_

#### Q33: What is an Java Applet? ⭐⭐
**Answer:**
A Java Applet is program that can be included in a HTML page and be executed in a java enabled client browser. Applets are used for creating dynamic and interactive web applications.

**Source:** _github.com/snowdream_

#### Q34: What will happen to the Exception object after exception handling? ⭐⭐
**Answer:**
The [Exception](http://docs.oracle.com/javase/7/docs/api/java/lang/Exception.html) object will be garbage collected in the next garbage collection.

**Source:** _github.com/snowdream_

#### Q35:  What is the purpose of garbage collection in Java, and when is it used? ⭐⭐
**Answer:**
The purpose of garbage collection is to identify and discard those objects that are no longer needed by the application, in order for the resources to be reclaimed and reused.

**Source:** _github.com/snowdream_

#### Q36: What does System.gc() and Runtime.gc() methods do? ⭐⭐
**Answer:**
These methods can be used as a hint to the JVM, in order to start a garbage collection. However, this it is up to the Java Virtual Machine (JVM) to start the garbage collection immediately or later in time.


**Source:** _github.com/snowdream_

#### Q37: What is the importance of finally block in exception handling? ⭐⭐
**Answer:**
A *finally* block will always be executed, whether or not an exception is actually thrown. Even in the case where the catch statement is missing and an exception is thrown, the finally block will still be executed. Last thing to mention is that the finally block is used to release resources like I/O buffers, database connections, etc.

**Source:** _github.com/snowdream_

#### Q38: What is the difference between Exception and Error in java? ⭐⭐
**Answer:**
[Exception](http://docs.oracle.com/javase/7/docs/api/java/lang/Exception.html) and [Error](http://docs.oracle.com/javase/7/docs/api/java/lang/Error.html) classes are both subclasses of the [Throwable](http://docs.oracle.com/javase/7/docs/api/java/lang/Throwable.html) class. The [Exception](http://docs.oracle.com/javase/7/docs/api/java/lang/Exception.html)  class is used for exceptional conditions that a user’s program should catch. The [Error](http://docs.oracle.com/javase/7/docs/api/java/lang/Error.html)  class defines exceptions that are not excepted to be caught by the user program.

**Source:** _github.com/snowdream_

#### Q39: What is meant by a Web Application? ⭐⭐
**Answer:**
A Web application is a dynamic extension of a Web or application server. There are two types of web applications: presentation-oriented and service-oriented. A presentation-oriented Web application generates interactive web pages, which contain various types of markup language and dynamic content in response to requests. On the other hand, a service-oriented web application implements the endpoint of a web service. In general, a Web application can be seen as a collection of servlets installed under a specific subset of the server’s URL namespace.

**Source:** _github.com/snowdream_

#### Q40: When does an Object becomes eligible for Garbage collection in Java ?  ⭐⭐
**Answer:**
A Java object is subject to garbage collection when it becomes unreachable to the program in which it is currently used.

**Source:** _github.com/snowdream_

#### Q41: Why Collection doesn’t extend Cloneable and Serializable interfaces?  ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q42: What happens when an applet is loaded? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q43: What is the role of stub in RMI? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q44: What is structure of Java Heap? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q45: If an object reference is set to null, will the Garbage Collector immediately free the memory held by that object? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q46: What is the difference between throw and throws? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q47: When is the finalize() called? What is the purpose of finalization?  ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q48: What are the steps involved to make work a RMI program?  ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q49: How does finally block differ from finalize() method? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q50: What’s the difference between Enumeration and Iterator interfaces?  ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q51: Explain the life cycle of an Applet.  ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q52: Can you access non static variable in static context? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q53: What is the tradeoff between using an unordered array versus an ordered array?  ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q54: What are the restrictions imposed on Java applets? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q55: What are untrusted applets? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q56:  What is a Server Side Include (SSI)? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q57: What is a Constructor, Constructor Overloading in Java and Copy-Constructor?  ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q58: What is the applet security manager, and what does it provide? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q59: What is Java Priority Queue? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q60: What is Comparable and Comparator interface? List their differences. ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q61: Which Swing methods are thread-safe? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q62: What is the relationship between an event-listener interface and an event-adapter class? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q63: What is difference between ArrayList and LinkedList ?  ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q64: What is difference between Array and ArrayList ? When will you use Array over ArrayList? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q65: What is the importance of hashCode() and equals() methods?  ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q66: What is difference between fail-fast and fail-safe?  ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q67: Explain the role of Driver in JDBC.  ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q68: What differences exist between Iterator and ListIterator?  ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q69: What is the advantage of PreparedStatement over Statement? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q70: What is the use of CallableStatement? Name the method, which is used to prepare a CallableStatement. ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q71: What is the difference between doGet() and doPost()? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q72: Explain the life cycle of a Servlet. ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q73: What is the difference between GenericServlet and HttpServlet? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q74: What are the advantages of JSP? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q75: What’s a deadlock?  ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q76: What is the difference between an Applet and a Servlet? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q77: What are Scriptlets? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q78: Does Java support multiple inheritance?  ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q79: Explain different ways of creating a thread. Which one would you prefer and why? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q80: What is meant by JSP implicit objects and what are they? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q81: What is RMI? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q82: Explain the available thread states in a high-level. ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q83: Explain Marshalling and demarshalling. ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q84: How do you ensure that N threads can access N resources without deadlock?  ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q85: What is Perm Gen space in Heap? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q86: What does Connection pooling mean? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q87: What is the applet class loader, and what does it provide? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q88:  What is the difference between applets loaded over the internet and applets loaded via the file system? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q89: What is Servlet Chaining? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q90: How do you find out what client machine is making a request to your servlet? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q91: What are some of the best practices relating to the Java Collection framework? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q92: What is the difference between a synchronized method and a synchronized block? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q93: What is the basic principle of RMI architecture? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q94: What is the purpose of using RMISecurityManager in RMI? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q95: What is the role of Remote Interface in RMI? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q96: What is the role of the java.rmi.Naming Class?  ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q97: What is meant by binding in RMI? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q98: What is the difference between Serial and Throughput Garbage collector? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q99: What is the difference between HashSet and TreeSet? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q100: Does Garbage collection occur in permanent generation space in JVM? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q101: What is DGC ? And how does it work? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q102: What are the layers of RMI Architecture? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q103: How does thread synchronization occurs inside a monitor? What levels of synchronization can you apply?  ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

## [[⬆]](#toc) <a name=JavaScript>JavaScript</a> Interview Questions
#### Q1: What is Coercion in JavaScript? 
**Answer:**
In JavaScript conversion between different two build-in types called `coercion`.  Coercion comes in two forms in JavaScript: *explicit* and *implicit*.

Here's an example of explicit coercion:
```js
var a = "42";

var b = Number( a );

a;				// "42"
b;				// 42 -- the number!
```
And here's an example of implicit coercion:
```js
var a = "42";

var b = a * 1;	// "42" implicitly coerced to 42 here

a;				// "42"
b;				// 42 -- the number!
``` 

#### Q2: What is typeof operator? ⭐
**Answer:**
JavaScript provides a `typeof` operator that can examine a value and tell you what type it is:
```js
var a;
typeof a;				// "undefined"

a = "hello world";
typeof a;				// "string"

a = 42;
typeof a;				// "number"

a = true;
typeof a;				// "boolean"

a = null;
typeof a;				// "object" -- weird, bug

a = undefined;
typeof a;				// "undefined"

a = { b: "c" };
typeof a;				// "object"
```


#### Q3: What is the object type? ⭐
**Answer:**
The object type refers to a compound value where you can set properties (named locations) that each hold their own values of any type. 

```js
var obj = {
	a: "hello world", // property
	b: 42,
	c: true
};

obj.a;		// "hello world", accessed with doted notation
obj.b;		// 42
obj.c;		// true

obj["a"];	// "hello world", accessed with bracket notation
obj["b"];	// 42
obj["c"];	// true
```
Bracket notation is also useful if you want to access a property/key but the name is stored in another variable, such as:
```js
var obj = {
	a: "hello world",
	b: 42
};

var b = "a";

obj[b];			// "hello world"
obj["b"];		// 42
```

#### Q4: Explain arrays in JavaScript ⭐
**Answer:**
An `array` is an object that holds values (of any type) not particularly in named properties/keys, but rather in numerically indexed positions:

```js
var arr = [
	"hello world",
	42,
	true
];

arr[0];			// "hello world"
arr[1];			// 42
arr[2];			// true
arr.length;		// 3

typeof arr;		// "object"
```


#### Q5: Explain equality in JavaScript ⭐
**Answer:**
JavaScript has both strict and type–converting comparisons: 
* **Strict comparison (e.g., ===)** checks for value equality without allowing *coercion*
* **Abstract comparison (e.g. ==)** checks for value equality with *coercion* allowed

```js
var a = "42";
var b = 42;

a == b;			// true
a === b;		// false
```
Some simple equalityrules:
* If either value (aka side) in a comparison could be the `true` or `false` value, avoid `==` and use `===`.
* If either value in a comparison could be of these specific values (`0`, `""`, or `[]` -- empty array), avoid `==` and use `===`.
* In all other cases, you're safe to use `==`. Not only is it safe, but in many cases it simplifies your code in a way that improves readability.

#### Q6: What is Scope in JavaScript? ⭐
**Answer:**
In JavaScript, each function gets its own *scope*. Scope is basically a collection of variables as well as the rules for how those variables are accessed by name. Only code inside that function can access that function's scoped variables.

A variable name has to be unique within the same scope. A scope can be nested inside another scope. If one scope is nested inside another, code inside the innermost scope can access variables from either scope.

#### Q7: What is let keyword in JavaScript? ⭐⭐
**Answer:**
In addition to creating declarations for variables at the function level, ES6 lets you declare variables to belong to individual blocks (pairs of { .. }), using the `let` keyword. 

**Source:** _https://github.com/getify/You-Dont-Know-JS/blob/master/up%20%26%20going/ch2.md_

#### Q8: Explain what a callback function is and provide a simple example. ⭐⭐
**Answer:**
A `callback` function is a function that is passed to another function as an argument and is executed after some operation has been completed. Below is an example of a simple callback function that logs to the console *after* some operations have been completed.

```js
function modifyArray(arr, callback) {
  // do something to arr here
  arr.push(100);
  // then execute the callback function that was passed
  callback();
}

var arr = [1, 2, 3, 4, 5];

modifyArray(arr, function() {
  console.log("array has been modified", arr);
});
```

**Source:** _coderbyte.com_

#### Q9: What is strict mode? ⭐⭐
**Answer:**
*Strict Mode* is a new feature in ECMAScript 5 that allows you to place a program, or a function, in a "strict" operating context. This strict context prevents certain actions from being taken and throws more exceptions.

```js
// Non-strict code...

(function(){
  "use strict";

  // Define your library strictly...
})();

// Non-strict code...
```

#### Q10: What does "use strict" do? ⭐⭐
**Answer:**
The `use strict` literal is entered at the top of a JavaScript program or at the top of a function and it helps you write safer JavaScript code by throwing an error if a global variable is created by mistake. For example, the following program will throw an error:

```js
function doSomething(val) {
  "use strict"; 
  x = val + 10;
}`
```

It will throw an error because `x` was not defined and it is being set to some value in the global scope, which is not allowed with `use strict` The small change below fixes the error being thrown:

```js
function doSomething(val) {
  "use strict"; 
  var x = val + 10;
}
```

**Source:** _coderbyte.com_

#### Q11: What is a Polyfill? ⭐⭐
**Answer:**
A polyfill is essentially the specific code (or plugin) that would allow you to have some specific functionality that you expect in current or “modern” browsers to also work in other browsers that do not have the support for that functionality built in.
* Polyfills are not part of the HTML5 standard
* Polyfilling is not limited to Javascript

**Source:** _programmerinterview.com_

#### Q12: How would you check if a number is an integer? ⭐⭐
**Answer:**
A very simply way to check if a number is a decimal or integer is to see if there is a remainder left when you divide by 1.

```js
function isInt(num) {
  return num % 1 === 0;
}

console.log(isInt(4)); // true
console.log(isInt(12.2)); // false
console.log(isInt(0.3)); // false
```

**Source:** _coderbyte.com_

#### Q13: Explain Values and Types in JavaScript ⭐⭐
**Answer:**
JavaScript has typed values, not typed variables. The following built-in types are available:
* `string`
* `number`
* `boolean`
* `null` and `undefined`
* `object`
* `symbol` (new to ES6)

#### Q14: Being told that an unsorted array contains (n - 1) of n consecutive numbers (where the bounds are defined), find the missing number in O(n) time ⭐⭐
**Answer:**
```js
// The output of the function should be 8
var arrayOfIntegers = [2, 5, 1, 4, 9, 6, 3, 7];
var upperBound = 9;
var lowerBound = 1;

findMissingNumber(arrayOfIntegers, upperBound, lowerBound); // 8

function findMissingNumber(arrayOfIntegers, upperBound, lowerBound) {
  // Iterate through array to find the sum of the numbers
  var sumOfIntegers = 0;
  for (var i = 0; i < arrayOfIntegers.length; i++) {
    sumOfIntegers += arrayOfIntegers[i];
  }

  // Find theoretical sum of the consecutive numbers using a variation of Gauss Sum.
  // Formula: [(N * (N + 1)) / 2] - [(M * (M - 1)) / 2];
  // N is the upper bound and M is the lower bound

  upperLimitSum = (upperBound * (upperBound + 1)) / 2;
  lowerLimitSum = (lowerBound * (lowerBound - 1)) / 2;

  theoreticalSum = upperLimitSum - lowerLimitSum;

  return theoreticalSum - sumOfIntegers;
}
```

**Source:** _https://github.com/kennymkchan_

#### Q15: Remove duplicates of an array and return an array of only unique elements ⭐⭐
**Answer:**
```js
// ES6 Implementation
var array = [1, 2, 3, 5, 1, 5, 9, 1, 2, 8];

Array.from(new Set(array)); // [1, 2, 3, 5, 9, 8]

// ES5 Implementation
var array = [1, 2, 3, 5, 1, 5, 9, 1, 2, 8];

uniqueArray(array); // [1, 2, 3, 5, 9, 8]

function uniqueArray(array) {
  var hashmap = {};
  var unique = [];

  for(var i = 0; i < array.length; i++) {
    // If key returns undefined (unique), it is evaluated as false.
    if(!hashmap.hasOwnProperty(array[i])) {
      hashmap[array[i]] = 1;
      unique.push(array[i]);
    }
  }

  return unique;
}
```

**Source:** _https://github.com/kennymkchan_

#### Q16: Given a string, reverse each word in the sentence ⭐⭐
**Details:**
For example `Welcome to this Javascript Guide!` should be become `emocleW ot siht tpircsavaJ !ediuG`

**Answer:**
```js
var string = "Welcome to this Javascript Guide!";

// Output becomes !ediuG tpircsavaJ siht ot emocleW
var reverseEntireSentence = reverseBySeparator(string, "");

// Output becomes emocleW ot siht tpircsavaJ !ediuG
var reverseEachWord = reverseBySeparator(reverseEntireSentence, " ");

function reverseBySeparator(string, separator) {
  return string.split(separator).reverse().join(separator);
}
```

**Source:** _https://github.com/kennymkchan_

#### Q17: Write a function that would allow you to do this. ⭐⭐
**Details:**
```js
var addSix = createBase(6);
addSix(10); // returns 16
addSix(21); // returns 27
```

**Answer:**
You can create a closure to keep the value passed to the function `createBase` even after the inner function is returned. The inner function that is being returned is created within an outer function, making it a closure, and it has access to the variables within the outer function, in this case the variable `baseNumber`.

```js
function createBase(baseNumber) {
  return function(N) {
    // we are referencing baseNumber here even though it was declared
    // outside of this function. Closures allow us to do this in JavaScript
    return baseNumber + N;
  }
}

var addSix = createBase(6);
addSix(10);
addSix(21);
```

**Source:** _coderbyte.com_

#### Q18: Implement enqueue and dequeue using only two stacks ⭐⭐
**Answer:**
*Enqueue* means to add an element, *dequeue* to remove an element.

```js
var inputStack = []; // First stack
var outputStack = []; // Second stack

// For enqueue, just push the item into the first stack
function enqueue(stackInput, item) {
  return stackInput.push(item);
}

function dequeue(stackInput, stackOutput) {
  // Reverse the stack such that the first element of the output stack is the
  // last element of the input stack. After that, pop the top of the output to
  // get the first element that was ever pushed into the input stack
  if (stackOutput.length <= 0) {
    while(stackInput.length > 0) {
      var elementToOutput = stackInput.pop();
      stackOutput.push(elementToOutput);
    }
  }

  return stackOutput.pop();
}
```

**Source:** _https://github.com/kennymkchan_

#### Q19: Explain Null and Undefined in JavaScript ⭐⭐
**Answer:**
JavaScript (and by extension TypeScript) has two bottom types: `null` and `undefined`. They are *intended* to mean different things:
* Something hasn't been initialized : `undefined`.
* Something is currently unavailable: `null`.

#### Q20: How would you use a closure to create a private counter? ⭐⭐
**Answer:**
You can create a function within an outer function (a closure) that allows you to update a private variable but the variable wouldn't be accessible from outside the function without the use of a helper function.

```js
function counter() {
  var _counter = 0;
  // return an object with several functions that allow you
  // to modify the private _counter variable
  return {
    add: function(increment) { _counter += increment; },
    retrieve: function() { return 'The counter is currently at: ' + _counter; }
  }
}

// error if we try to access the private variable like below
// _counter;

// usage of our counter function
var c = counter();
c.add(5); 
c.add(9); 

// now we can access the private variable in the following way
c.retrieve(); // => The counter is currently at: 14
```

**Source:** _coderbyte.com_

#### Q21: Explain event bubbling and how one may prevent it ⭐⭐
**Answer:**
**Event bubbling** is the concept in which an event triggers at the deepest possible element, and triggers on parent elements in nesting order. As a result, when clicking on a child element one may exhibit the handler of the parent activating.

One way to prevent event bubbling is using `event.stopPropagation()` or `event.cancelBubble` on IE < 9.

**Source:** _https://github.com/kennymkchan_

#### Q22: How to check if an object is an array or not? Provide some code. ⭐⭐
**Answer:**
> The best way to find whether an object is instance of a particular class or not using `toString` method from `Object.prototype`

```javascript
var arrayList = [1 , 2, 3];
```

One of the best use cases of type checking of an object is when we do method overloading in JavaScript. For understanding this let say we have a method called `greet` which take one single string and also a list of string, so making our `greet` method workable in both situation we need to know what kind of parameter is being passed, is it single value or list of value?

```javascript
function greet(param) {
  if() {
    // here have to check whether param is array or not
  }
  else {
  }
}
```

However, in above implementation it might not necessary to check type for array, we can check for single value string and put array logic code in else block, let see below code for the same.

```javascript
 function greet(param) {
   if(typeof param === 'string') {
   }
   else {
     // If param is of type array then this block of code would execute
   }
 }
```

Now it's fine we can go with above two implementations, but when we have a situation like a parameter can be `single value`, `array`, and `object` type then we will be in trouble.

Coming back to checking type of object, As we mentioned that we can use `Object.prototype.toString`

```javascript
if(Object.prototype.toString.call(arrayList) === '[object Array]') {
  console.log('Array!');
}
```

If you are using `jQuery` then you can also used jQuery `isArray` method:

```javascript
if($.isArray(arrayList)) {
  console.log('Array');
} else {
  console.log('Not an array');
}
```

FYI jQuery uses `Object.prototype.toString.call` internally to check whether an object is an array or not.

In modern browser, you can also use:

```javascript
Array.isArray(arrayList);
```

`Array.isArray` is supported by Chrome 5, Firefox 4.0, IE 9, Opera 10.5 and Safari 5

**Source:** _github.com/ganqqwerty_

#### Q23: Write a "mul" function which will properly when invoked as below syntax. ⭐⭐
**Details:**
```javascript
console.log(mul(2)(3)(4)); // output : 24
console.log(mul(4)(3)(4)); // output : 48
```

**Answer:**
```javascript
function mul (x) {
  return function (y) { // anonymous function
    return function (z) { // anonymous function
      return x * y * z;
    };
  };
}
```

Here `mul` function accept the first argument and return anonymous function which take the second parameter and return anonymous function which take the third parameter and return multiplication of arguments which is being passed in successive

In JavaScript function defined inside has access to outer function variable and function is the first class object so it can be returned by function as well and passed as argument in another function.
- A function is an instance of the Object type
- A function can have properties and has a link back to its constructor method
- Function can be stored as variable
- Function can be pass as a parameter to another function
- Function can be returned from function

**Source:** _github.com/ganqqwerty_

#### Q24: How to empty an array in JavaScript? ⭐⭐
**Details:**
```js
var arrayList =  ['a', 'b', 'c', 'd', 'e', 'f'];
```
How could we empty the array above?

**Answer:**
**Method 1**

```javascript
arrayList = [];
```

Above code will set the variable `arrayList` to a new empty array. This is recommended if you don't have **references to the original array** `arrayList` anywhere else because It will actually create a new empty array. You should be careful with this way of empty the array, because if you have referenced this array from another variable, then the original reference array will remain unchanged, Only use this way if you have only referenced the array by its original variable `arrayList`.

For Instance:

```javascript
var arrayList = ['a', 'b', 'c', 'd', 'e', 'f']; // Created array
var anotherArrayList = arrayList;  // Referenced arrayList by another variable
arrayList = []; // Empty the array
console.log(anotherArrayList); // Output ['a', 'b', 'c', 'd', 'e', 'f']
```

**Method 2**

```javascript
arrayList.length = 0;
```

Above code will clear the existing array by setting its length to 0. This way of empty the array also update all the reference variable which pointing to the original array. This way of empty the array is useful when you want to update all the another reference variable which pointing to `arrayList`.

For Instance:

```javascript
var arrayList = ['a', 'b', 'c', 'd', 'e', 'f']; // Created array
var anotherArrayList = arrayList;  // Referenced arrayList by another variable
arrayList.length = 0; // Empty the array by setting length to 0
console.log(anotherArrayList); // Output []
```

**Method 3**

```javascript
arrayList.splice(0, arrayList.length);
```

Above implementation will also work perfectly. This way of empty the array will also update all the references of the original array.

```javascript
var arrayList = ['a', 'b', 'c', 'd', 'e', 'f']; // Created array
var anotherArrayList = arrayList;  // Referenced arrayList by another variable
arrayList.splice(0, arrayList.length); // Empty the array by setting length to 0
console.log(anotherArrayList); // Output []
```

**Method 4**

```javascript
while(arrayList.length) {
  arrayList.pop();
}
```

Above implementation can also empty the array. But not recommended to use often.

**Source:** _github.com/ganqqwerty_

#### Q25: What is IIFEs l(Immediately Invoked Function Expressions)? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q26: Describe closure concept in JavaScript as best as you could ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q27: Given an array of integers, find the largest difference between two elements such that the element of lesser value must come before the greater element ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q28: Find the intersection of two arrays. An intersection would be the common elements that exists within both arrays. In this case, these elements should be unique! ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q29: How to compare two objects in JavaScript? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q30: Given two strings, return true if they are anagrams of one another ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q31: Write a function that would allow you to do this ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q32: Check if a given string is a palindrome. Case sensitivity should be taken into account. ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q33: What is the difference between a shim and a polyfill? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q34: Write a recursive function that returns the binary string of a given decimal number ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q35: What will the following code output? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q36: What will be the output of the following code? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q37: What will be the output of the following code? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q38: Could you explain the difference between ES5 and ES6 ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q39: Explain the difference between "undefined" and "not defined" in JavaScript ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q40: What will be the output of the following code? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q41: What is the drawback of creating true private in JavaScript? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q42: Provide some examples of non-bulean value coercion to a boolean one ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q43: What is the difference between anonymous and named functions?  ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q44: Given an array of integers, find the largest product yielded from three of the integers ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q45: Explain prototype inheritance in JavaScript? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q46: What is “closure” in javascript? Provide an example? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q47: Explain what is hoisting in Javascript ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q48: Given an integer, determine if it is a power of 2. If so, return that number, else return -1 ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q49: What will be the output of the following code? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q50: Describe the JS module design pattern ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q51: How would you create a private variable in JavaScript? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q52: Explain the Prototype Design Pattern ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q53: Write a recursive function that performs a binary search ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q54: Check if a given string is a isomorphic ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q55: What will be the output of the following code? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q56: What does the term "Transpiling" stand for? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q57: What is the "new" keyword in JavaScript? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q58: When would you use the "bind" function? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q59: How does the “this” keyword work? Provide some code examples. ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q60: How would you add your own method to the Array object so the following code would work? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q61: What is Hoisting in JavaScript? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q62: What will the following code output? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q63: Create a function that will evaluate if a given expression has balanced parentheses using stacks ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q64: Describe the Revealing Module Pattern design pattern ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

## [[⬆]](#toc) <a name=Laravel>Laravel</a> Interview Questions
#### Q1: What is the Laravel? ⭐
**Answer:**
**Laravel** is a free, open-source PHP web framework, created by Taylor Otwell and intended for the development of web applications following the model–view–controller (MVC) architectural pattern.

**Source:** _codingcompiler.com_

#### Q2: What are some benefits of Laravel over other Php frameworks? ⭐
**Answer:**
* Setup and customisation process is  easy and fast as compared to others.
* Inbuilt Authentication System
* Supports multiple file systems
* Pre-loaded packages like Laravel Socialite, Laravel cashier, Laravel elixir, Passport, Laravel Scout
* Eloquent ORM (Object Relation Mapping) with PHP active record implementation
* Built in command line tool “Artisan” for creating a code skeleton ,database structure and build their migration

**Source:** _mytectra.com_

#### Q3: Is there any CLI for Laravel? ⭐
**Answer:**
PHP artisan is the command line interface/tool included with Laravel. It provides a number of helpful commands that can help you while you build your application easily. Here are the list of some artisian commands:

* php artisan list
* php artisan help
* php artisan tinker
* php artisan make
* php artisan –versian
* php artisan make modal modal_name
* php artisan make controller controller_name

**Source:** _mytectra.com_

#### Q4: What are Laravel events? ⭐⭐
**Answer:**
Laravel event provides a simple **observer pattern** implementation, that allow to subscribe and listen for events in the application. 

**Source:** _mytectra.com_

#### Q5: Explain Migrations in Laravel ⭐⭐
**Answer:**
**Laravel Migrations** are like version control for the database, allowing a team to easily modify and share the application’s database schema. Migrations are typically paired with Laravel’s schema builder to easily build the application’s database schema.

**Source:** _laravelinterviewquestions.com_

#### Q6: What is the Facade Pattern used for? ⭐⭐
**Answer:**
**Facades** provide a *static* interface to classes that are available in the application's service container. Laravel facades serve as *static proxies* to underlying classes in the service container, providing the benefit of a terse, expressive syntax while maintaining more testability and flexibility than traditional static methods.

All of Laravel's facades are defined in the `Illuminate\Support\Facades` namespace. 
Consider:
```php
use Illuminate\Support\Facades\Cache;

Route::get('/cache', function () {
    return Cache::get('key');
});
```

**Source:** _laravel.com_

## [[⬆]](#toc) <a name=MongoDB>MongoDB</a> Interview Questions
#### Q1: Explain what is MongoDB? ⭐
**Answer:**
Mongo-DB is a document database which provides high performance,
high availability and easy scalability.

**Source:** _medium.com/@hub4tech_

#### Q2: How many indexes does MongoDB create by default for a new collection? ⭐
**Answer:**
By default, MongoDB created the _id collection for every collection.

**Source:** _tutorialspoint.com_

#### Q3: Does Mongodb Support Foreign Key Constraints? ⭐
**Answer:**
No. MongoDB does not support such relationships.

**Source:** _interviewbubble.com_

#### Q4: Which are the most important features of MongoDB? ⭐
**Answer:**
* Flexible data model in form of documents
* Agile and highly scalable database
* Faster than traditional databases
* Expressive query language

**Source:** _tutorialspoint.com_

#### Q5: What are Indexes in MongoDB? ⭐⭐
**Answer:**
Indexes support the efficient execution of queries in MongoDB. Without indexes, MongoDB must perform a collection scan, i.e. scan every document in a collection, to select those documents that match the query statement. If an appropriate index exists for a query, MongoDB can use the index to limit the number of documents it must inspect.

**Source:** _tutorialspoint.com_

#### Q6: Why does Profiler use in MongoDB? ⭐⭐
**Answer:**
MongoDB uses a database profiler to perform characteristics of each operation against the database. You can use a profiler to find queries and write operations

**Source:** _medium.com/@hub4tech_

#### Q7: If you remove an object attribute, is it deleted from the database? ⭐⭐
**Answer:**
Yes, it be. Remove the attribute and then re-save () the object.

**Source:** _medium.com/@hub4tech_

#### Q8: Does MongoDB need a lot space of Random Access Memory (RAM)? ⭐⭐
**Answer:**
No. MongoDB can be run on small free space of RAM.

**Source:** _medium.com/@hub4tech_

#### Q9: What is “Namespace” in MongoDB? ⭐⭐
**Answer:**
MongoDB stores BSON (Binary Interchange and Structure Object Notation) objects in the collection. The concatenation of the collection name and database name is called a namespace

**Source:** _medium.com/@hub4tech_

#### Q10: Mention the command to insert a document in a database called school and collection called persons. ⭐⭐
**Answer:**
```js
use school;
db.persons.insert( { name: "kadhir", dept: "CSE" } )
```

**Source:** _tutorialspoint.com_

#### Q11: What is a replica set? ⭐⭐
**Answer:**
It is a group of mongo instances that maintain same data set. Replica sets provide redundancy and high availability, and are the basis for all production deployments.

**Source:** _interviewbubble.com_

#### Q12: When should we embed one document within another in MongoDB? ⭐⭐
**Answer:**
You should consider embedding documents for:

* *contains* relationships between entities
* One-to-many relationships
* Performance reasons

**Source:** _tutorialspoint.com_

#### Q13: How is data stored in MongoDB? ⭐⭐
**Answer:**
Data in MongoDB is stored in BSON documents – JSON-style data structures. Documents contain one or more fields, and each field contains a value of a specific data type, including arrays, binary data and sub-documents. Documents that tend to share a similar structure are organized as collections.

It may be helpful to think of documents as analogous to rows in a relational database, fields as similar to columns, and collections as similar to tables.

**Source:** _mongodb.com_

#### Q14: What Is Replication In Mongodb? ⭐⭐
**Answer:**
Replication is the process of synchronizing data across multiple servers. Replication provides redundancy and increases data availability. With multiple copies of data on different database servers, replication protects a database from the loss of a single server. Replication also allows you to recover from hardware failure and service interruptions.

**Source:** _interviewbubble.com_

#### Q15: What are the differences between MongoDB and MySQL/SQL SERVER? ⭐⭐
**Answer:**
The MongoDB store the data in documents with JSON format but SQL store the data in Table format.

The MongoDB provides high performance, high availability, easy scalability etc.  rather than SQL Server.

In the MongoDB, we can change the structure simply by adding, removing column from the existing documents.

**Source:** _interviewbubble.com_

#### Q16: Compare SQL databases and MongoDB at a high level. ⭐⭐
**Answer:**
SQL databases store data in form of tables, rows, columns and records. This data is stored in a pre-defined data model which is not very much flexible for today's real-world highly growing applications. MongoDB in contrast uses a flexible structure which can be easily modified and extended.

**Source:** _tutorialspoint.com_

#### Q17: Can you create an index on an array field in MongoDB? If yes, what happens in this case? ⭐⭐
**Answer:**
Yes. An array field can be indexed in MongoDB. In this case, MongoDB would index each value of the array.

**Source:** _tutorialspoint.com_

#### Q18: How can you achieve transaction and locking in MongoDB? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q19: What are NoSQL databases? What are the different types of NoSQL databases? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q20: How is MongoDB better than other SQL databases? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q21: Does MongoDB support ACID transaction management and locking functionalities? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q22: How can I combine data from multiple collections into one collection? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q23: What does MongoDB not being ACID compliant really mean? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q24: Find objects between two dates MongoDB ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q25: How to query MongoDB with “like”? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q26: Should I normalize my data before storing it in MongoDB? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q27: Is there an “upsert” option in the mongodb insert command? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q28: What is oplog? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q29: How can you achieve primary key - foreign key relationships in MongoDB? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q30: Does MongoDB pushes the writes to disk immediately or lazily? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q31: If you remove a document from database, does MongoDB remove it from disk? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q32: Can one MongoDB operation lock more than one databases? If yes, how? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q33: Explain the structure of ObjectID in MongoDB. ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q34: What is the difference b/w MongoDB and CouchDB? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q35: What is the difference between MongoDB and MySQL? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q36: What is a covered query in MongoDB? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q37: Mention the command to check whether you are on the master server or not. ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q38: Why MongoDB is not preferred over a 32-bit system? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q39: What do you understand by NoSQL databases? Explain. ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q40: Why are MongoDB data files large in size? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q41: What is Sharding in MongoDB? Explain. ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q42: What is sharding? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q43: What is Aggregation in MongoDB? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q44: How can you isolate your cursors from intervening with the write operations? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q45: At what interval does MongoDB write updates to the disk? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q46: By default, MongoDB writes and reads data from both primary and secondary replica sets. True or False. ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q47: Mention the command to list all the indexes on a particular collection. ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q48: What happens if an index does not fit into RAM? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q49: Does MongoDB provide a facility to do text searches? How? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q50: Where can I run MongoDB? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q51: How to remove a field completely from a MongoDB document? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q52: How does Journaling work in MongoDB? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q53: Why is a covered query important? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q54: How does MongoDB provide concurrency? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q55: What are Primary and Secondary Replica sets? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q56: How replication works in MongoDB? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q57: What are alternatives to MongoDB? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q58: Update MongoDB field using value of another field ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q59: How does MongoDB ensure high availability? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q60: Is MongoDB schema-less? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q61: What's the advantage of the backup features in Ops Manager versus traditional backup strategies? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q62: What is splitting in mongodb? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q63: Which are the two storage engines used by MongoDB? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q64: What is a Storage Engine in MongoDB ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q65: How to condense large volumes of data in Mongo? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

## [[⬆]](#toc) <a name=Node.js>Node.js</a> Interview Questions
#### Q1: What is Node.js? ⭐
**Answer:**
Node.js is a web application framework built on Google Chrome's JavaScript Engine (V8 Engine).

Node.js comes with runtime environment on which a Javascript based script can be interpreted and executed (It is analogus to JVM to JAVA byte code). This runtime allows to execute a JavaScript code on any machine outside a browser. Because of this runtime of Node.js, JavaScript is now can be executed on server as well.

*Node.js = Runtime Environment + JavaScript Library*

**Source:** _tutorialspoint.com_

#### Q2: What is npm? ⭐
**Answer:**
`npm` stands for Node Package Manager. npm provides following two main functionalities:

*   Online repositories for node.js packages/modules which are searchable on [search.nodejs.org](http://search.nodejs.org)
*   Command line utility to install packages, do version management and dependency management of Node.js packages.

**Source:** _tutorialspoint.com_

#### Q3: What are the two types of API functions in Node.js?  ⭐
**Answer:**
The two types of API functions in Node.js are: a) Asynchronous, non-blocking functions b) Synchronous, blocking functions

**Source:** _lazyquestion.com_

#### Q4: What are Event Listeners?   ⭐⭐
**Answer:**
**Event Listeners** are similar to call back functions but are associated with some event. For example when a server listens to http request on a given port a event will be generated and to specify http server has received and will invoke corresponding event listener. Basically, Event listener's are also call backs for a corresponding event.

Node.js has built in event's and built in event listeners. Node.js also provides functionality to create Custom events and Custom Event listeners.

**Source:** _lazyquestion.com_

#### Q5: What is global installation of dependencies? ⭐⭐
**Answer:**
Globally installed packages/dependencies are stored in **<user-directory>**/npm directory. Such dependencies can be used in CLI (Command Line Interface) function of any node.js but can not be imported using require() in Node application directly. To install a Node project globally use -g flag.

**Source:** _tutorialspoint.com_

#### Q6: What are the core modules of Node,js? ⭐⭐
**Answer:**
* EventEmitter
* Stream
* FS
* Net
* Global Objects

**Source:** _github.com/jimuyouyou_

#### Q7: What is an error-first callback? ⭐⭐
**Answer:**
*Error-first callbacks* are used to pass errors and data. The first argument is always an error object that the programmer has to check if something went wrong. Additional arguments are used to pass data.

```js
fs.readFile(filePath, function(err, data) {
  if (err) {
    //handle the error
  }
  // use the data object
});
```

**Source:** _tutorialspoint.com_

#### Q8:  How you can monitor a file for modifications in Node.js ? ⭐⭐
**Answer:**
We can take advantage of File System `watch()` function which watches the changes of the file.

**Source:** _codingdefined.com_

#### Q9: Could we run an external process with Node.js? ⭐⭐
**Answer:**
Yes. *Child process module* enables us to access operating system functionaries or other apps. Scalability is baked into Node and child processes are the key factors to scale our application. You can use child process to run system commands, read large files without blocking event loop,  decompose the application into various “nodes” (That’s why it’s called Node).

Child process module has following three major ways to create child processes –

* spawn  - child_process.spawn launches a new process with a given command.
* exec  - child_process.exec method runs a command in a shell/console and buffers the output.
* fork - The child_process.fork method is a special case of the spawn() to create child processes.

**Source:** _codeforgeek.com_

#### Q10: What's the difference between operational and programmer errors? ⭐⭐
**Answer:**
Operation errors are not bugs, but problems with the system, like _request timeout_ or _hardware failure_. On the other hand programmer errors are actual bugs.

**Source:** _blog.risingstack.com_

#### Q11: What are the benefits of using Node.js? ⭐⭐
**Answer:**
Following are main benefits of using Node.js

*   **Aynchronous and Event Driven**All APIs of Node.js library are aynchronous that is non-blocking. It essentially means a Node.js based server never waits for a API to return data. Server moves to next API after calling it and a notification mechanism of Events of Node.js helps server to get response from the previous API call.
    
*   **Very Fast** Being built on Google Chrome's V8 JavaScript Engine, Node.js library is very fast in code execution.
    
*   **Single Threaded but highly Scalable** \- Node.js uses a single threaded model with event looping. Event mechanism helps server to respond in a non-bloking ways and makes server highly scalable as opposed to traditional servers which create limited threads to handle requests. Node.js uses a single threaded program and same program can services much larger number of requests than traditional server like Apache HTTP Server.
    
*   **No Buffering** \- Node.js applications never buffer any data. These applications simply output the data in chunks.

**Source:** _tutorialspoint.com_

#### Q12: What is the difference between Nodejs, AJAX, and jQuery? ⭐⭐
**Answer:**
The one common trait between Node.js, AJAX, and jQuery is that all of them are the advanced implementation of JavaScript. However, they serve completely different purposes.

* Node.js –It is a server-side platform for developing client-server applications. For example, if we’ve to build an online employee management system, then we won’t do it using client-side JS. But the Node.js can certainly do it as it runs on a server similar to Apache, Django not in a browser.

* AJAX (aka Asynchronous Javascript and XML) –It is a client-side scripting technique, primarily designed for rendering the contents of a page without refreshing it. There are a no. of large companies utilizing AJAX such as Facebook and Stack Overflow to display dynamic content.

* jQuery –It is a famous JavaScript module which complements AJAX, DOM traversal, looping and so on. This library provides many useful functions to help in JavaScript development. However, it’s not mandatory to use it but as it also manages cross-browser compatibility, so can help you produce highly maintainable web applications.

**Source:** _techbeamers.com_

#### Q13: How to make Post request in Node.js? ⭐⭐
**Answer:**
Following code snippet can be used to make a Post Request in Node.js.

```js
var request = require('request');
request.post('http://www.example.com/action', {
  form: {
    key: 'value'
  }
}, function(error, response, body) {
  if (!error && response.statusCode == 200) {
    console.log(body)
  }
});
```

**Source:** _techbeamers.com_

#### Q14: What is Callback Hell? ⭐⭐
**Answer:**
The asynchronous function requires callbacks as a return parameter. When multiple asynchronous functions are chained together then callback hell situation comes up. 

**Source:** _codeforgeek.com_

#### Q15: If Node.js is single threaded then how it handles concurrency? ⭐⭐
**Answer:**
Node provides a single thread to programmers so that code can be written easily and without bottleneck. Node internally uses multiple POSIX threads for various I/O operations such as File, DNS, Network calls etc.

When Node gets I/O request it creates or uses a thread to perform that I/O operation and once the operation is done, it pushes the result to the event queue. On each such event, event loop runs and checks the queue and if the execution stack of Node is empty then it adds the queue result to execution stack.

This is how Node manages concurrency.

**Source:** _codeforgeek.com_

#### Q16: What do you mean by Asynchronous API? ⭐⭐
**Answer:**
All APIs of Node.js library are aynchronous that is non-blocking. It essentially means a Node.js based server never waits for a API to return data. Server moves to next API after calling it and a notification mechanism of Events of Node.js helps server to get response from the previous API call.

**Source:** _tutorialspoint.com_

#### Q17: What are the key features of Node.js? ⭐⭐
**Answer:**
Let’s look at some of the key features of Node.js.

*   **Asynchronous event driven IO helps concurrent request handling –** All APIs of Node.js are asynchronous. This feature means that if a Node receives a request for some Input/Output operation, it will execute that operation in the background and continue with the processing of other requests. Thus it will not wait for the response from the previous requests.
*   **Fast in Code execution –** Node.js uses the V8 JavaScript Runtime engine, the one which is used by Google Chrome. Node has a wrapper over the JavaScript engine which makes the runtime engine much faster and hence processing of requests within Node.js also become faster.
*   **Single Threaded but Highly Scalable –** Node.js uses a single thread model for event looping. The response from these events may or may not reach the server immediately. However, this does not block other operations. Thus making Node.js highly scalable. Traditional servers create limited threads to handle requests while Node.js creates a single thread that provides service to much larger numbers of such requests.
*   **Node.js library uses JavaScript –** This is another important aspect of Node.js from the developer’s point of view. The majority of developers are already well-versed in JavaScript. Hence, development in Node.js becomes easier for a developer who knows JavaScript.
*   **There is an Active and vibrant community for the Node.js framework –** The active community always keeps the framework updated with the latest trends in the web development.
*   **No Buffering –** Node.js applications never buffer any data. They simply output the data in chunks.

**Source:** _techbeamers.com_

#### Q18: What is control flow function?   ⭐⭐
**Answer:**
It is a generic piece of code which runs in between several asynchronous function calls is known as control flow function.

**Source:** _lazyquestion.com_

#### Q19: Is Node a single threaded application? ⭐⭐
**Answer:**
Yes! Node uses a single threaded model with event looping.

**Source:** _tutorialspoint.com_

#### Q20:  List out the differences between AngularJS and NodeJS? ⭐⭐
**Answer:**
AngularJS is a web application development framework. It’s a JavaScript and it is different from other web app frameworks written in JavaScript like jQuery. NodeJS is a runtime environment used for building server-side applications while AngularJS is a JavaScript framework mainly useful in building/developing client-side part of applications which run inside a web browser.

**Source:** _a4academics.com_

#### Q21: What is the purpose of setTimeout function? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q22: What is REPL in context of Node? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q23: How can you avoid callback hells? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q24: What is Callback? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q25: What's the event loop? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q26: What is a blocking code? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q27: How Node prevents blocking code? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q28: What is Event Loop? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q29: What is stream and what are types of streams available in Node.js? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q30: What is Event Emmitter? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q31: How to avoid callback hell in Node.js? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q32: What is purpose of Buffer class in Node? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q33: When should I use EventEmitter? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q34: What is difference between synchronous and asynchronous method of fs module? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q35: What are streams? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q36: What is the preferred method of resolving unhandled exceptions in Node.js? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q37: When should we use Node.js? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q38: How to use Buffer in Node.js? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q39: What is Chaining in Node? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q40: What are the global objects of Node.js? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q41: Explain how does Node.js work? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q42: How does Node.js handle child threads? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q43: What is the purpose of `__dirname` variable? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q44: When to not use Node.js? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q45: Is Node.js entirely based on a single-thread? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q46: Is Node.js entirely based on a single-thread? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q47: Does Node.js support multi-core platforms? And is it capable of utilizing all the cores? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q48: How would you handle errors for async code in Node.js? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q49: Why to use Buffers instead of binary strings to handle binary data ? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q50: What's a stub? Name a use case. ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q51: What tools can be used to assure consistent code style? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q52: How to gracefully Shutdown Node.js Server? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q53: Provide some example of config file separation for dev and prod environments ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q54: How can you listen on port 80 with Node? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q55: Explain usage of NODE_ENV ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q56: What is Piping in Node? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q57: What is the purpose of `__filename` variable? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q58: What are the timing features of Node.js? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q59: Name some of the events fired by streams. ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q60: Explain what is Reactor Pattern in Node.js? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q61: Consider following code snippet ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q62: Explain some Error Handling approaches in Node.js you know about. Which one will you use? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q63: How to solve "Process out of Memory Exception" in Node.js ? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q64: What is LTS releases of Node.js why should you care? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q65: Why should you separate Express 'app' and 'server'? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q66: What is the difference between process.nextTick() and setImmediate() ? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q67: How would you scale Node application? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q68: Rewrite the code sample without try/catch block ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

## [[⬆]](#toc) <a name=PerformanceTesting>Performance Testing</a> Interview Questions
#### Q1: What is the difference between load and stress testing? ⭐⭐
**Answer:**
A **load test** is usually conducted to understand the behaviour of the system under a specific expected load. This load can be the *expected concurrent number of users* on the application performing a specific number of transactions within the set duration. This test will give out the response times of all the important business critical transactions.

A **stress testing** instead is performed to understand the upper limits of capacity within the system. This kind of test is done to determine the system's robustness in terms of *extreme load* and helps application administrators to determine if the system will perform sufficiently if the current load goes well above the expected maximum.

**Source:** _en.wikipedia.org_

#### Q2: What is Load Testing? ⭐⭐
**Answer:**
**Load testing** measures system performance as the workload increases. That workload could mean concurrent users or transactions.The system is monitored to measure response time and system staying power as workload increases. That workload falls within the parameters of normal working conditions.

**Source:** _stackify.com_

#### Q3: Name some performance testing steps ⭐⭐
**Answer:**
Some of the performance testing steps are:

* Identify the testing environment
* Identify performance metrics
* Plan and design performance tests
* Configure the test environment
* Implement your test design
* Execute tests
* Analyze, report, retest

**Source:** _stackify.com_

#### Q4: Explain the purpose of Scalability testing ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q5: Name some Performance Testing best practices ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q6: What is Stress Testing? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q7: Name some performance testing mistakes ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q8: What is Endurance Testing? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q9: Name some Performance Testing metrics to measure ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q10: Name some types of performance testing for software ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q11: Name most common problems observed in performance testing ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q12: Explain some load testing metrics ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q13: What is Spike Testing? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q14: How to interpret load/stress test metrics? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q15: Why would you conduct Volume Testing? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q16: Could you name some common Performance Testing fallacies? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

## [[⬆]](#toc) <a name=QuestionstoAsk>Questions to Ask</a> Interview Questions
#### Q1: What would you change around here if you could? ⭐
**Answer:**


#### Q2: How do you measure individual performance? ⭐
**Answer:**


#### Q3: How do your clients and customers define success? ⭐
**Answer:**


#### Q4: How do you evaluate new technologies? Who makes the final decisions? ⭐
**Answer:**


#### Q5: How do you know what to work on each day? ⭐
**Answer:**


#### Q6: What is the most important/valuable thing you have learnt from working here? ⭐
**Answer:**


#### Q7: Do you tend to roll your own solutions more often or rely on third party tools? What's the rationale in a specific case? ⭐
**Answer:**


#### Q8: What is the most fulfilling/exciting/technically complex project that you've worked on here so far? ⭐⭐
**Answer:**


#### Q9: How do you train/ramp up engineers who are new to the team? ⭐⭐
**Answer:**


#### Q10: What does a typical day look like for you? ⭐⭐
**Answer:**


#### Q11: What do you think the company can improve at? ⭐⭐
**Answer:**


#### Q12: What is your policy on working from home/remotely? ⭐⭐
**Answer:**


#### Q13: What is your stack? What is the rationale for/story behind this specific stack? ⭐⭐
**Answer:**


#### Q14: What are the engineering challenges that the company/team is facing? ⭐⭐
**Answer:**


#### Q15: What do you measure? What are your most important product metrics? ⭐⭐
**Answer:**


#### Q16: What does the company do to nurture and train its employees? ⭐⭐
**Answer:**


#### Q17: If you hire person, what do you have for him to study product you're working on and processes in general? Do you have specifications, requirements, documentation? ⭐⭐
**Answer:**


#### Q18: Tell me about the main products of your company. ⭐⭐
**Answer:**


#### Q19: What are some weaknesses of the organization? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q20: What is your team's biggest challenge right now? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q21: Why did you choose to come to this company? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q22: How does the engineering team balance resources between feature requests and engineering maintenance? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q23: What makes your product competitive? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q24: What is the most frustrating part about working here? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q25: Is the team growing, and what sort of opportunities will there be in the next year/3 years? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q26: What is the current team composition like? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q27: There's "C++" (or Python, Swift or any other tech) in the job description. How will you estimate my proficiency in this tech in 3 months? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q28: Why have the last few people left? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q29: When was the last time you interacted with a founder? What was it regarding? Generally how involved are the founders in the day-to-day? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q30: How much time do you spend on new project development versus maintenance? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q31: What are your highest priorities right now? For example, new features, new products, solidifying existing code, reducing operations overhead? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q32: What has been the worst technical blunder that has happened in the recent past? How did you guys deal with it? What changes were implemented afterwards to make sure it didn't happen again? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q33: What is unique about working at this company that you have not experienced elsewhere? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q34: What is the most costly technical decision made early on that the company is living with now? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q35: How are you funded? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q36: Does the company culture encourage entrepreneurship? Could you give me any specific examples? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q37: What would I work on if I joined this team and who would I work most closely with? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q38: Are you profitable? If no, what's your plan for becoming profitable? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q39: How long does the average engineer stay at the company? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

## [[⬆]](#toc) <a name=RESTAPI>REST API</a> Interview Questions
#### Q1: What is RESTful Web Services? ⭐
**Answer:**
*Web Services* work on client-server model where client applications can access web services over the network. Web services provide endpoint URLs and expose methods that can be accessed over network through client programs written in java, shell script or any other different technologies. Web services are stateless and doesn’t maintain user session like web applications.

**Source:** _What is a Web Service?_

#### Q2: What is caching? ⭐
**Answer:**
*Caching* refers to storing server response in client itself so that a client needs not to make server request for same resource again and again. A server response should have information about how a caching is to be done so that a client caches response for a period of time or never caches the server response.


**Source:** _tutorialspoint.com_

#### Q3: Which protocol is used by RESTful webservices? ⭐
**Answer:**
RESTful web services make use of HTTP protocol as a medium of communication between client and server.

**Source:** _tutorialspoint.com_

#### Q4: What is REST Web Services? ⭐
**Answer:**
*REST* is the acronym for *REpresentational State Transfer.* REST is an architectural style for developing applications that can be accessed over the network. REST architectural style was brought in light by Roy Fielding in his doctoral thesis in 2000.

REST is a stateless client-server architecture where web services are resources and can be identified by their URIs. Client applications can use HTTP GET/POST methods to invoke Restful web services. REST doesn’t specify any specific protocol to use, but in almost all cases it’s used over HTTP/HTTPS. 

When compared to SOAP web services, these are lightweight and doesn’t follow any standard. We can use XML, JSON, text or any other type of data for request and response.

**Source:** _journaldev.com_

#### Q5: What REST stands for? ⭐
**Answer:**
*REST* stands for *REpresentational State Transfer*. REST is web standards based architecture and uses HTTP Protocol for data communication. It revolves around resource where every component is a resource and a resource is accessed by a common interface using HTTP standard methods. REST was first introduced by Roy Fielding in 2000.

In REST architecture, a REST Server simply provides access to resources and REST client accesses and presents the resources. Here each resource is identified by URIs/ global IDs. REST uses various representations to represent a resource like text, JSON and XML. Now a days JSON is the most popular format being used in web services.

**Source:** _tutorialspoint.com_

#### Q6: What is purpose of a URI in REST based webservices? ⭐⭐
**Answer:**
*URI* stands for *Uniform Resource Identifier*. Each resource in REST architecture is identified by its URI. Purpose of an URI is to locate a resource(s) on the server hosting the web service.

A URI is of following format:
```sh
<protocol>://<service-name>/<ResourceType>/<ResourceID>
```

**Source:** _tutorialspoint.com_

#### Q7: What is WSDL? ⭐⭐
**Answer:**
*WSDL* stands for Web Service Description Language. WSDL is an XML based document that provides technical details about the web service. Some of the useful information in WSDL document are: 
* method name, 
* port types, 
* service end point, 
* binding, 
* method parameters etc.

**Source:** _journaldev.com_

#### Q8: What are the advantages of Web Services? ⭐⭐
**Answer:**
Some of the advantages of web services are:

* **Interoperability**: Web services are accessible over network and runs on HTTP/SOAP protocol and uses XML/JSON to transport data, hence it can be developed in any programming language. Web service can be written in java programming and client can be PHP and vice versa.
* **Reusability**: One web service can be used by many client applications at the same time.
* **Loose Coupling**: Web services client code is totally independent with server code, so we have achieved loose coupling in our application.
* **Easy to deploy and integrate**, just like web applications.
* **Multiple service versions** can be running at same time.

**Source:** _journaldev.com_

#### Q9: What are different types of Web Services? ⭐⭐
**Answer:**
There are two types of web services:

* **SOAP Web Services**: Runs on SOAP protocol and uses XML technology for sending data.
* **Restful Web Services**: It’s an architectural style and runs on HTTP/HTTPS protocol almost all the time. REST is a stateless client-server architecture where web services are resources and can be identified by their URIs. Client applications can use HTTP GET/POST methods to invoke Restful web services.

**Source:** _journaldev.com_

#### Q10: Mention some key characteristics of REST? ⭐⭐
**Answer:**
Some key characteristics of REST includes

* REST is stateless, therefore the SERVER has no state (or session data)
* With a well-applied REST API, the server could be restarted between two calls as every data is passed to the server
* Web service mostly uses POST method to make operations, whereas REST uses GET to access resources

**Source:** _career.guru99.com_

#### Q11: What is SOAP? ⭐⭐
**Answer:**
*SOAP* stands for Simple Object Access Protocol. SOAP is an XML based industry standard protocol for designing and developing web services. Since it’s XML based, it’s platform and language independent. So our server can be based on JAVA and client can be on .NET, PHP etc. and vice versa.

**Source:** _journaldev.com_

#### Q12: What are advantages of REST web services? ⭐⭐
**Answer:**
Some of the advantages of REST web services are:

* Learning curve is easy since it works on HTTP protocol
* Supports multiple technologies for data transfer such as text, xml, json, image etc.
* No contract defined between server and client, so loosely coupled implementation.
* REST is a lightweight protocol
* REST methods can be tested easily over browser.

**Source:** _journaldev.com_

#### Q13: Mention what is the difference between AJAX and REST? ⭐⭐
**Answer:**
**Ajax**

* In Ajax, the request are sent to the server by using `XMLHttpRequest` objects. The response is used by the JavaScript code to dynamically alter the current page
* Ajax is a set of technology; it is a technique of dynamically updating parts of UI without having to reload the page
* Ajax eliminates the interaction between the customer and server asynchronously

**REST**

* REST requires the interaction between the customer and server
* REST have a URL structure and a request/response pattern the revolve around the use of resources
* REST is a type of software architecture and a method for users to request data or information from servers
* REST requires the interaction between the customer and server

**Source:** _career.guru99.com_

#### Q14: What is a Resource in Restful web services? ⭐⭐
**Answer:**
*Resource* is the fundamental concept of Restful architecture. A resource is an object with:
*  a type, 
* relationship with other resources and 
* methods that operate on it. 

Resources are identified with:
* their URI, 
* HTTP methods they support and 
* request/response data type and format of data.

**Source:** _journaldev.com_

#### Q15: What are different HTTP Methods supported in Restful Web Services? ⭐⭐
**Answer:**
Restful web services supported HTTP methods are:
* GET, 
* POST, 
* PUT, 
* DELETE and 
* HEAD.

**Source:** _journaldev.com_

#### Q16: Mention what are resources in a REST architecture? ⭐⭐
**Answer:**
Resources are identified by logical URLs; it is the key element of a RESTful design.  Unlike, SOAP web services in REST, you view the product data as a resource and this resource should contain all the required information.

**Source:** _career.guru99.com_

#### Q17: Mention whether you can use GET request instead of PUT to create a resource? ⭐⭐
**Answer:**
No, you are not supposed to use POST or GET.  GET operations should only have view rights

**Source:** _career.guru99.com_

#### Q18: Explain the architectural style for creating web API? ⭐⭐
**Answer:**
The architectural style for creating web api are

* HTTP for client server communication
* XML/JSON as formatting language
* Simple URI as the address for the services
* Stateless communication

**Source:** _career.guru99.com_

#### Q19: What are the core components of a HTTP Request? ⭐⭐
**Answer:**
A HTTP Request has five major parts −

*   **Verb** − Indicate HTTP methods such as GET, POST, DELETE, PUT etc.
*   **URI** − Uniform Resource Identifier (URI) to identify the resource on server.
*   **HTTP Version** − Indicate HTTP version, for example HTTP v1.1 .
*   **Request Header** − Contains metadata for the HTTP Request message as key-value pairs. For example, client ( or browser) type, format supported by client, format of message body, cache settings etc.
*   **Request Body** − Message content or Resource representation.

**Source:** _tutorialspoint.com_

#### Q20: Mention what are the HTTP methods supported by REST? ⭐⭐
**Answer:**
HTTP methods supported by REST are:

* `GET`: It requests a resource at the request URL. It should not contain a request body as it will be discarded. Maybe it can be cached locally or on the server.
* `POST`: It submits information to the service for processing; it should typically return the modified or new resource
* `PUT`: At the request URL it update the resource
* `DELETE`: At the request URL it removes the resource
* `OPTIONS`: It indicates which techniques are supported
* `HEAD`: About the request URL it returns meta information

**Source:** _career.guru99.com_

#### Q21: What are disadvantages of SOAP Web Services? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q22: How would you choose between SOAP and REST web services? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q23: What are different ways to test web services? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q24: What are disadvantages of REST web services? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q25: Mention what are the different application integration styles? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q26: Mention what is the difference between PUT and POST? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q27: Mention what is the difference between RPC or document style web services? How you determine to which one to choose? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q28: What are the best practices to design a resource representation? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q29: What is UDDI? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q30: What is messaging in RESTful webservices? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q31: What are the core components of a HTTP response? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q32: What is addressing in RESTful webservices? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q33: Mention what are the HTTP methods supported by REST? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q34: What are the best practices to create a standard URI for a web service? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q35: What is statelessness in RESTful Webservices? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q36: What are the disadvantages of statelessness in RESTful Webservices? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q37: What is the use of Accept and Content-Type Headers in HTTP Request? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q38: What are the various approaches available for developing SOAP based web services? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q39: What are advantages of SOAP Web Services? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q40: What are the best practices for caching? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q41: What is the purpose of HTTP Status Code? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q42:  What is Payload? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q43: Define SOA? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q44: Explain WSDL? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q45: What are the primary security issues of web service? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q46: What should be the purpose of OPTIONS method of RESTful web services? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q47: Which header of HTTP response provides control over caching? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q48: What are the advantages of statelessness in RESTful Webservices? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q49: What are the important characteristics of SOAP envelope element? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q50: What is difference between SOA and Web Services? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q51: What do you mean by idempotent operation? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q52: Explain Cache-control header ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q53: What are the elements of a SOAP message? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q54: What are the two attributes of <Port> element in WSDL? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q55: Explain <definition> element? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q56: Which type of Webservices methods are to be idempotent? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q57: Enlist the operation types response used in WSDL? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q58: Explain the message element in WSDL? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q59: What are the different elements of WSDL documents? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q60: What is difference between Top Down and Bottom Up approach in SOAP Web Services? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q61: What are different components of WSDL? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q62: Is binding between SOAP and WSDL possible? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q63:  Enlist some important constraints for RESTful web services. ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q64: What are the best practices to be followed while designing a secure RESTful web service? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q65: What should be the purpose of HEAD method of RESTful web services? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q66: What is Open API Initiative? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q67: Name some best practices for better RESTful API design ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

## [[⬆]](#toc) <a name=React>React</a> Interview Questions
#### Q1: How would you write an inline style in React? ⭐
**Answer:**
For example: 

```html
<div style={{ height: 10 }}>
```

**Source:** _github.com/WebPredict_

#### Q2: What are props in React? ⭐
**Answer:**
Props are properties that are passed into a child component from its parent, and are readonly.

**Source:** _github.com/WebPredict_

#### Q3: How does React work? ⭐
**Answer:**
React creates a virtual DOM. When state changes in a component it firstly runs a "diffing" algorithm, which identifies what has changed in the virtual DOM. The second step is reconciliation, where it updates the DOM with the results of diff.

**Source:** _github.com/Pau1fitz_

#### Q4: What is React? ⭐
**Answer:**
React is an open-source JavaScript library created by Facebook for building complex, interactive UIs in web and mobile applications. React’s core purpose is to build UI components; it is often referred to as just the “V” (View) in an “MVC” architecture. 

**Source:** _codementor.io_

#### Q5: What happens when you call "setState"? ⭐⭐
**Answer:**
The first thing React will do when setState is called is merge the object you passed into setState into the current state of the component. This will kick off a process called reconciliation. The end goal of reconciliation is to, in the most efficient way possible, update the UI based on this new state.

To do this, React will construct a new tree of React elements (which you can think of as an object representation of your UI). Once it has this tree, in order to figure out how the UI should change in response to the new state, React will diff this new tree against the previous element tree.

By doing this, React will then know the exact changes which occurred, and by knowing exactly what changes occurred, will able to minimize its footprint on the UI by only making updates where absolutely necessary.

**Source:** _medium.freecodecamp.org/_

#### Q6: What is the difference between state and props? ⭐⭐
**Answer:**
The *state* is a data structure that starts with a default value when a Component mounts. It may be mutated across time, mostly as a result of user events.

*Props* (short for properties) are a Component's configuration. They are received from above and immutable as far as the Component receiving them is concerned. A Component cannot change its props, but it is responsible for putting together the props of its child Components. Props do not have to just be data - callback functions may be passed in as props.

**Source:** _github.com/Pau1fitz_

#### Q7: What is the point of Redux? ⭐⭐
**Answer:**
Application state management that is easy to reason about, maintain and manage in an asynchronous web application environment.

**Source:** _github.com/WebPredict_

#### Q8: Where in a React component should you make an AJAX request? ⭐⭐
**Answer:**
`componentDidMount` is where an AJAX request should be made in a React component. 

This method will be executed when the component “mounts” (is added to the DOM) for the first time. This method is only executed once during the component’s life. Importantly, you can’t guarantee the AJAX request will have resolved before the component mounts. If it doesn't, that would mean that you’d be trying to setState on an unmounted component, which would not work. Making your AJAX request in `componentDidMount` will guarantee that there’s a component to update.

**Source:** _github.com/Pau1fitz_

#### Q9: Where is the state kept in a React + Redux application? ⭐⭐
**Answer:**
In the store.

**Source:** _github.com/WebPredict_

#### Q10: What happens when you call setState? ⭐⭐
**Answer:**
The state property is updated in a React component with the object passed into setState, and this is done asynchronously. It tells React that this component and its children need to be re-rendered, but React may not do this immediately (it may batch these state update requests for better performance).

**Source:** _github.com/WebPredict_

#### Q11: What's the difference between a controlled component and an uncontrolled one in React? ⭐⭐
**Answer:**
* A controlled component has its state completely driven by React,
* Uncontrolled components can maintain their own internal state. E.g., a textarea's value.

**Source:** _github.com/WebPredict_

#### Q12: How would you prevent a component from rendering in React? ⭐⭐
**Answer:**
 Return `null` from the render method.

**Source:** _github.com/WebPredict_

#### Q13: How do you prevent the default behavior in an event callback in React? ⭐⭐
**Answer:**
You call `e.preventDefault();` on the event e passed into the callback.

**Source:** _github.com/WebPredict_

#### Q14: What does it mean for a component to be mounted in React? ⭐⭐
**Answer:**
It has a corresponding element created in the DOM and is connected to that.

**Source:** _github.com/WebPredict_

#### Q15: What is JSX? ⭐⭐
**Answer:**
JSX is JavaScript with extensions. Useful for creating React elements with the full power of JavaScript. Not required for a React app, but typically it's used.

**Source:** _github.com/WebPredict_

#### Q16: How do we pass a property from a parent component props to a child component? ⭐⭐
**Answer:**
For example: 
```html
<ChildComponent someProp={props.someProperty} />
```

**Source:** _github.com/WebPredict_

#### Q17: What are the advantages of using React? ⭐⭐
**Answer:**
- It is easy to know how a component is rendered, you just need to look at the render function.
- JSX makes it easy to read the code of your components. It is also really easy to see the layout, or how components are plugged/combined with each other.
- You can render React on the server-side. This enables improves SEO and performance.
- It is easy to test.
- You can use React with any framework (Backbone.js, Angular.js) as it is only a view layer.

**Source:** _github.com/Pau1fitz_

#### Q18: Describe how events are handled in React. ⭐⭐
**Answer:**
In order to solve cross browser compatibility issues, your event handlers in React will be passed instances of SyntheticEvent, which is React’s cross-browser wrapper around the browser’s native event. These synthetic events have the same interface as native events you’re used to, except they work identically across all browsers.

What’s mildly interesting is that React doesn’t actually attach events to the child nodes themselves. React will listen to all events at the top level using a single event listener. This is good for performance and it also means that React doesn’t need to worry about keeping track of event listeners when updating the DOM.

**Source:** _tylermcginnis.com_

#### Q19: What’s the difference between an "Element" and a "Component" in React? ⭐⭐
**Answer:**
Simply put, a React element describes what you want to see on the screen. Not so simply put, a React element is an object representation of some UI.

A React component is a function or a class which optionally accepts input and returns a React element (typically via JSX which gets transpiled to a createElement invocation).

**Source:** _medium.freecodecamp.org/_

#### Q20: When rendering a list what is a key and what is it's purpose? ⭐⭐
**Answer:**
*Keys* help React identify which items have changed, are added, or are removed. Keys should be given to the elements inside the array to give the elements a stable identity. The best way to pick a key is to use a string that uniquely identifies a list item among its siblings. 

```js
render () {
  return (
    <ul>
      {this.state.todoItems.map(({task, uid}) => {
        return <li key={uid}>{task}</li>
      })}
    </ul>
  )
}
```

Most often you would use IDs from your data as keys. When you don't have stable IDs for rendered items, you may use the item index as a key as a last resort. It is not recommend to use indexes for keys if the items can reorder, as that would be slow. 

**Source:** _github.com/Pau1fitz_

#### Q21: What are refs used for in React? ⭐⭐
**Answer:**
*Refs* are an escape hatch which allow you to get direct access to a DOM element or an instance of a component. In order to use them you add a ref attribute to your component whose value is a callback function which will receive the underlying DOM element or the mounted instance of the component as its first argument.

```js
class UnControlledForm extends Component {
  handleSubmit = () => {
    console.log("Input Value: ", this.input.value)
  }
  render () {
    return (
      <form onSubmit={this.handleSubmit}>
        <input
          type='text'
          ref={(input) => this.input = input} />
        <button type='submit'>Submit</button>
      </form>
    )
  }
}
```
Above notice that our input field has a ref attribute whose value is a function. That function receives the actual DOM element of input which we then put on the instance in order to have access to it inside of the handleSubmit function.

It’s often misconstrued that you need to use a class component in order to use refs, but refs can also be used with functional components by leveraging closures in JavaScript.

```js
function CustomForm ({handleSubmit}) {
  let inputElement
  return (
    <form onSubmit={() => handleSubmit(inputElement.value)}>
      <input
        type='text'
        ref={(input) => inputElement = input} />
      <button type='submit'>Submit</button>
    </form>
  )
}
```

**Source:** _github.com/Pau1fitz_

#### Q22: What is Flux? ⭐⭐
**Answer:**
Unidrectional application flow paradigm popular a few years back in React; mostly superceded by Redux these days.

**Source:** _github.com/WebPredict_

#### Q23: What do you like about React? ⭐⭐
**Answer:**


**Source:** _github.com/Pau1fitz_

#### Q24: What is the difference between a Presentational component and a Container component? ⭐⭐
**Answer:**
Presentational components are concerned with how things look. They generally receive data and callbacks exclusively via props. These components rarely have their own state, but when they do it generally concerns UI state, as opposed to data state.

Container components are more concerned with how things work. These components provide the data and behavior to presentational or other container components. They call Flux actions and provide these as callbacks to the presentational components. They are also often stateful as they serve as data sources. 

**Source:** _github.com/Pau1fitz_

#### Q25: What are the differences between a class component and functional component? ⭐⭐
**Answer:**
- **Class components** allows you to use additional features such as local state and lifecycle hooks. Also, to enable your component to have direct access to your store and thus holds state.

- When your component just receives props and renders them to the page, this is a **stateless component**, for which a pure function can be used. These are also called dumb components or presentational components.

**Source:** _github.com/Pau1fitz_

#### Q26: How is React different from AngularJS (1.x)? ⭐⭐
**Answer:**
For example, AngularJS (1.x) approaches building an application by extending HTML markup and injecting various constructs (e.g. Directives, Controllers, Services) at runtime. As a result, AngularJS is very opinionated about the greater architecture of your application — these abstractions are certainly useful in some cases, but they come at the cost of flexibility.

By contrast, React focuses exclusively on the creation of components, and has few (if any) opinions about an application’s architecture. This allows a developer an incredible amount of flexibility in choosing the architecture they deem “best” — though it also places the responsibility of choosing (or building) those parts on the developer.

**Source:** _codementor.io_

#### Q27: What happens during the lifecycle of a React component? ⭐⭐
**Answer:**
At the highest level, React components have lifecycle events that fall into three general categories:

1.  Initialization
2.  State/Property Updates
3.  Destruction

<img class="img-fluid" src="https://s3.amazonaws.com/codementor_content/2016-Jul/reactjs-qs1.png">

**Source:** _codementor.io_

#### Q28: What are some limitations of things you shouldn't do in the component's render method? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q29: What can you tell me about JSX? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q30: Name some popular Flux Libraries ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q31: What don't you like about React? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q32: Given the code defined above, can you identify two problems? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q33: What is an action? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q34: What is a store in redux? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q35:  What is state in react? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q36: What is equivalent of the following using React.createElement? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q37: What is the difference between createElement and cloneElement? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q38: What is JSX? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q39: What does "shouldComponentUpdate" do and why is it important? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q40: How would you prevent a component from rendering? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q41: What's the difference between a "smart" component and a "dumb" component? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q42: What is the alternative of binding `this` in the constructor? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q43: What is the render method for? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q44: What's the typical flow of data like in a React + Redux app? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q45: What's an alternative way to avoid having to bind to this in event callback methods? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q46: Why is it advised to pass a callback function to setState as opposed to an object? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q47: What advantages are using arrow functions? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q48: What is the point of using keys in React? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q49: What's the typical pattern for rendering a list of components from an array of data? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q50: What is a higher order component? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q51: How do you tell React to build in Production mode and what will that do? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q52: What is reconciliation in React? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q53: What's the difference between an Element and a Component in React? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q54: What is the point of shouldComponentUpdate() method? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q55: What are PropTypes in React? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q56: What are controlled components? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q57: What is ReactDOM? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q58: What are typical middleware choices for handling asynchronous calls in Redux? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q59: Name the different lifecycle methods. ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q60: What are stateless components? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q61: Are you familiar with Flux? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q62: Describe Flux vs MVC? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q63: What is wrong with this code? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q64: What is the second argument that can optionally be passed to setState and what is its purpose? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q65: What is the purpose of super(props)? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q66: What is "Children"? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q67: What is a reducer? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q68: If you created a React element like Twitter below, what would the component definition of Twitter look like? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q69: Why does React use SyntheticEvents? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q70: Why would you use forceUpdate in a React component? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q71: What is mapStateToProps and mapDispatchToProps? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q72: What's a pure functional component in React? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q73: Explain the Virtual DOM concept in React. ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q74: What are some recent changes in the React library (e.g. in version 14, 15)? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q75: Why would you eject from create-react-app? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q76: If you need to access the underlying DOM node for a React component, what's the typical way to do this in React? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q77: What is the React context? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q78: What is the difference between a controlled component and an uncontrolled component? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q79: Why would you need to bind event handlers to "this"? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q80: Why would you use React.Children.map(props.children, () => ) instead of props.children.map(() => )? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q81: Explain some difference between Flux and AngularJS (1.x) approach ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q82: What is a pure function? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q83: What is Redux Thunk used for? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q84: What is React Fiber? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

## [[⬆]](#toc) <a name=Ruby>Ruby</a> Interview Questions
#### Q1: What is the highest level in the object model? ⭐
**Answer:**
`BasicObject`

**Source:** _githubusercontent.com_

#### Q2: Which core object includes the "Kernel" module?   ⭐
**Answer:**
`Object`

**Source:** _githubusercontent.com_

#### Q3: What can you say about an identifier that begins with a capital letter?   ⭐
**Answer:**
It is a constant.

**Source:** _githubusercontent.com_

#### Q4: Why Ruby is known as a language of flexibility? ⭐
**Answer:**
Ruby is known as a language of flexibility because it facilitates its author to alter the programming elements. Some specific parts of the language can be removed or redefined. Ruby does not restrict the user. For example, to add two numbers, Ruby allows to use `+` sign or the word `plus`. This alteration can be done with Ruby's built-in class Numeric.

**Source:** _javatpoint.com_

#### Q5: What is an object? ⭐
**Answer:**
An instance of a class. To some, it's also the root class in ruby (Object). Classes themselves descend from the Object root class.

**Source:** _stackoverflow.com_

#### Q6: What is a class? ⭐
**Answer:**
Classes hold **data**, have **methods** that interact with that data, and are used to **instantiate objects**.

```ruby
class WhatAreClasses
  def initialize
    @data = "I'm instance data of this object. Hello."
  end

  def method
    puts @data.gsub("instance", "altered")
  end
end

object = WhatAreClasses.new
object.method
 #=> I'm altered data of this object. Hello.
```

**Source:** _stackoverflow.com_

#### Q7: What are rubygems? ⭐
**Answer:**
**rubygems** is package manager software for ruby libraries (i.e. gems). The package manager has basic CRUD operations, dependency trees, and supports asynchronous communication between multiple gem servers.

**Source:** _stackoverflow.com_

#### Q8: Is there an equivalent of “continue” in Ruby? ⭐
**Answer:**
Yes, it's called `next`.

```js
for i in 0..5
   if i < 2
     next
   end
   puts "Value of local variable is #{i}"
end
```

**Source:** _stackoverflow.com_

#### Q9: Is everything in Ruby an object?   ⭐
**Answer:**
Methods are not objects. Blocks are not objects. Keywords are not objects. However, there exist Method objects and Proc objects, and some keywords refer to objects.

**Source:** _githubusercontent.com_

#### Q10: Explain redo statement in Ruby ⭐⭐
**Answer:**
Ruby `redo` statement is used to repeat the current iteration of the loop. The redo statement is executed without evaluating loop's condition.

**Source:** _javatpoint.com_

#### Q11: Why are symbols typically used as hash keys instead of strings? ⭐⭐
**Answer:**
Strings are *mutable* while symbols are *immutable*. Though Ruby internally makes an immutable copy of a string when used as a hash key, comparing two symbols is faster than comparing two `String` objects. This is also a convention.

**Source:** _githubusercontent.com_

#### Q12: How might you specify a default value for a hash?  ⭐⭐
**Answer:**
Pass the default values as arguments to `::new` on initialization or change the default directly with the method `Hash#default`. You may also provide a default at the time of query with `Hash#fetch`.

**Source:** _githubusercontent.com_

#### Q13: What is the difference between nil and false in Ruby? ⭐⭐
**Answer:**
**nil**:
* nil cannot be a value
* nil is returned where there is no predicate
* nil is not a boolean data type
* nil is an object of nilclass

**false**:
* false can be a value
* in case of a predicate, true or false is returned by a method
* false is a boolean data type
* false is an object of falseclass


**Source:** _javatpoint.com_

#### Q14: Why might you use `Hash#fetch` over `Hash#[]` when querying values in a hash?   ⭐⭐
**Answer:**
`Hash#fetch` provides options for handling the case where a key does not exist in the hash.

**Source:** _githubusercontent.com_

#### Q15: Explain some differences between Ruby and Python ⭐⭐
**Answer:**
Similarities:

* High level language
* Support multiple platforms
* Use interactive prompt called irb
* Server side scripting language

Differences:

* Ruby is fully object oriented while Python is not.
* Ruby supports EclipseIDE while Python supports multiple IDEs.
* Ruby use Mixins while Python doesn't.
* Ruby supports blocks, procs and lambdas while Python doesn't.

**Source:** _javatpoint.com_

#### Q16: What are two uses of the splat operator?   ⭐⭐
**Answer:**
* Explode or expand the elements of an array. 
* Collect arguments of a parameter list into an array.

**Source:** _githubusercontent.com_

#### Q17: What is the difference between an instance variable and a class variable?   ⭐⭐
**Answer:**
A class variable is evaluated in reference to the class object created by the enclosing class definition while an instance variable is evaluated in reference to `self`. Instance variables cannot be referenced outside of instance methods.

**Source:** _githubusercontent.com_

#### Q18: What is the return value for ... ⭐⭐
**Details:**
For the class `ABC` the given as:

```ruby
class ABC
  def xyz
    puts "xyz in ABC"
  end
end
```

What is the return value for:

*   `ABC::new::xyz`
*   `ABC::new.xyz`
*   `ABC.new::xyz`
*   `ABC.new.xyz`

**Answer:**
All the statements for the invocation of the xyz method through the object are valid.

When run through `IRB`:

```ruby
irb(main):001:0> ABC::new::xyz
xyz in ABC
=> nil
irb(main):002:0> ABC::new.xyz
xyz in ABC
=> nil
irb(main):003:0> ABC.new::xyz
xyz in ABC
=> nil
irb(main):004:0> ABC.new.xyz
xyz in ABC
=> nil
```

**Source:** _toptal.com_

#### Q19:  What is the difference between `#==` and `#===`?   ⭐⭐
**Answer:**
`#==` performs the generic comparison while `#===` performs case equality comparison and is useful for providing meaningful semantics in case statements.


**Source:** _githubusercontent.com_

#### Q20: How do you remove `nil` values in array using ruby? ⭐⭐
**Answer:**
`Array#compact` removes `nil` values.

```ruby
>> [nil,123,nil,"test"].compact
=> [123, "test"]
```

**Source:** _toptal.com_

#### Q21: Can you call a private method outside a Ruby class using its object? ⭐⭐
**Answer:**
Yes, with the help of the `send` method.

Given the class `Test`:
```ruby
class Test
   private
       def method
         p "I am a private method"
      end
end
```
    
We can execute the private method using `send`:

```ruby
>> Test.new.send(:method)
"I am a private method"
```

**Source:** _toptal.com_

#### Q22: What will be the values of ... ⭐⭐
**Details:**
Consider the following code:
```ruby
class A
  def self.a(b)
    if b > 0
      b * b
    end
  end
end
```
What will be the values of:

*   `var1 = A.a(0)`
*   `var2 = A.a(2)`

**Answer:**
*   var1 will be equal to `nil`
*   var2 will be equal to `4`

A conditional statement in Ruby is an expression that returns `nil` if the conditional is `false`.  Ruby methods return the last expression in the method body.

**Source:** _toptal.com_

#### Q23: Explain each of the following operators and how and when they should be used ⭐⭐
**Details:**
* `==`
* `===`
* `eql?`
* `equal?`

**Answer:**
* `==` – Checks if the _value_ of two operands are equal (often overridden to provide a class-specific definition of equality).

* `===` – Specifically used to test equality within the `when` clause of a `case` statement (also often overridden to provide meaningful class-specific semantics in case statements).

* `eql?` – Checks if the _value_ and _type_ of two operands are the same (as opposed to the `==` operator which compares values but ignores types). For example, `1 == 1.0` evaluates to `true`, whereas `1.eql?(1.0)` evaluates to `false`.

* `equal?` – Compares the `identity` of two objects; i.e., returns `true` iff both operands have the same object id (i.e., if they both refer to the _same object_). Note that this will return `false` when comparing two identical _copies_ of the same object.


**Source:** _toptal.com_

#### Q24: Write a function that sorts the keys in a hash by the length of the key as a string. ⭐⭐
**Details:**
For instance, the hash:
```ruby
{ abc: 'hello', 'another_key' => 123, 4567 => 'third' }
```
should result in:
```ruby
["abc", "4567", "another_key"]
```

**Answer:**
As is always true in programming, there are in fact multiple ways to accomplish this.
The most straightforward answer would be of the form:
```ruby
hsh.keys.map(&:to_s).sort_by(&:length)
```    
or:
```ruby
hsh.keys.collect(&:to_s).sort_by { |key| key.length }
```

Alternatively, Ruby’s [`Enumerable` mixin](http://ruby-doc.org/core-2.1.2/Enumerable.html) provides many methods to operate on collections. The key here is to turn the hash keys into a collection, convert them all to strings, then sort the array.

```ruby
def key_sort hsh
   hsh.keys.collect(&:to_s).sort { |a, b| a.length <=> b.length }
end
```

An equivalent call of the [`collect` method](http://www.tutorialspoint.com/ruby/ruby_iterators.htm) is done with the usual block syntax of:

```ruby
collect { |x| x.to_s }
```

**Source:** _toptal.com_

#### Q25: Which of the expressions listed below will result in "false"? ⭐⭐
**Details:**
```ruby
true    ? "true" : "false"
false   ? "true" : "false"
nil     ? "true" : "false"
1       ? "true" : "false"
0       ? "true" : "false"
"false" ? "true" : "false"
""      ? "true" : "false"
[]      ? "true" : "false"
```

**Answer:**
In Ruby, the _only_ values that evaluate to false are `false` and `nil`. _Everything else_ – even zero (0) and an empty array (\[\]) – evaluates to true.

This comes as a real surprise to programmers who have previously been working in other languages like JavaScript.

**Source:** _toptal.com_

#### Q26: Why might you use `#each` instead of `for/in`?   ⭐⭐
**Answer:**
It's the "Ruby way" - an example of how Ruby defines methods that mimic natural language concepts. Iterator methods such as `#each` read more naturally. `#each` is a block so it defines a new variable scope. `for/in` depends on the existence of `#each` which implies that `#each` is a more fundamental aspect of the language.

**Source:** _githubusercontent.com_

#### Q27: There are three ways to invoke a method in ruby.  Can you give me at least two? ⭐⭐
**Answer:**
We are looking for the **dot operator** (or period operator), the **Object#send** method, or **method(:foo).call**

```ruby
object = Object.new
puts object.object_id
 #=> 282660

puts object.send(:object_id)
 #=> 282660

puts object.method(:object_id).call # (Kudos to Ezra)
 #=> 282660
```

**Source:** _gist.github.com_

#### Q28: What is a module?  Can you tell me the difference between classes and modules? ⭐⭐
**Answer:**
Modules serve as a mechanism for **namespaces**.

```ruby
module ANamespace
  class AClass
    def initialize
      puts "Another object, coming right up!"
    end
  end
end

ANamespace::AClass.new
 #=> Another object, coming right up!
```

Also, modules provide as a mechanism for multiple inheritance via **mix-ins** and **cannot be instantiated** like classes can.

```ruby
module AMixIn
  def who_am_i?
    puts "An existentialist, that's who."
  end
end

# String is already the parent class
class DeepString < String
  # extend adds instance methods from AMixIn as class methods
  extend AMixIn
end

DeepString.who_am_i?
 #=> An existentialist, that's who.

AMixIn.new
 #=> NoMethodError: undefined method ‘new’ for AMixIn:Module
```

**Source:** _gist.github.com_

#### Q29: What is a DSL and how does it pertain to Ruby?   ⭐⭐
**Answer:**
A **Domain Specific Language** is an API that allows a developer to solve a problem or represent data more naturally than they might otherwise. The flexible nature of Ruby's syntax and the ability to alias and alter existing methods and classes makes it conducive to creating rich DSL's.

**Source:** _githubusercontent.com_

#### Q30: What is duck typing and how does it pertain to Ruby?   ⭐⭐
**Answer:**
That an object may be acted upon even if it isn't the expected type as long as it looks and behaves like the expected object. This is a characteristic of Ruby because the lack of type checking of parameters makes this an effective programming technique.

**Source:** _githubusercontent.com_

#### Q31: Is Ruby a statically typed or a dynamically typed language?   ⭐⭐
**Answer:**
Dynamically typed since type checking is done at runtime.

**Source:** _githubusercontent.com_

#### Q32: Are instance methods public or private?   ⭐⭐
**Answer:**
They are public by default. You can change their visibility using `Module#private`, `Module#protected`, or back again using `Module#public`.

**Source:** _githubusercontent.com_

#### Q33: What is a predicate in the context of Ruby method naming conventions?  ⭐⭐
**Answer:**
A method that answers a question posed by the method invocation or method name. Predicates typically return a boolean.

```js
$ irb
> 5.odd?
=> true

> 5.even?
=> false

> 5.between?(1, 10)
=> true

> 5.between?(11, 20)
=> false
```

**Source:** _githubusercontent.com_

#### Q34: Is Ruby a strongly typed or a weakly typed language?   ⭐⭐
**Answer:**
Strongly typed since an object's type is checked before an operation is performed on it.

**Source:** _githubusercontent.com_

#### Q35: Check if a value exists in an array in Ruby ⭐⭐
**Details:**
I have a value `Dog` and an array `['Cat', 'Dog', 'Bird']`.

How do I check if it exists in the array without looping through it? Is there a simple way of checking if the value exists, nothing more?

**Answer:**
You're looking for include?:
```js
>> ['Cat', 'Dog', 'Bird'].include? 'Dog'
=> true
```

**Source:** _githubusercontent.com_

#### Q36: What is the difference between private and protected methods?   ⭐⭐
**Answer:**
A private method can only be called by any instance methods of the defining class or any subclasses and must be invoked in a functional style and not explicitly on `self` such as with `self.my_method`. A protected method may be explicitly invoked by any instance of the defining class, and is not restricted to implicit invocation on `self`.

**Source:** _githubusercontent.com_

#### Q37: Are class variables inherited?   ⭐⭐
**Answer:**
No. The behavior is different than inheritance. Any alteration of a class variable by a subclass affects that class variable in the superclass and all other subclasses of the superclass.

**Source:** _githubusercontent.com_

#### Q38: What is the difference between a class variable and a class instance variable?   ⭐⭐
**Answer:**
Class instance variables are instance variables of a class. Class instance variables cannot be used within instance methods.

**Source:** _githubusercontent.com_

#### Q39: What does it mean to coerce an object? Why would you do it?   ⭐⭐
**Answer:**
To *coerce an object* means to force it into an expected type. One might do this in order to try and force an unknown object type into the expected type or format required by the operation. This is a common practice involved in *duck typing*.

**Source:** _githubusercontent.com_

#### Q40: What will val1 and val2 equal after the code below is executed? Explain your answer. ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q41: Explain redo vs. retry usage ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q42: Why might you want to avoid using string literals within loops?   ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q43: What is the difference between Proc invocation and lambda invocation?   ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q44:  What is the main difference between procs and lambdas? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q45: Why can you safely use a string as a hash key, even though a string is mutable?  ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q46: What are two uses of ranges?   ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q47: What is the difference between `Module#remove_method` and `Module#undef_method`?   ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q48: Which operator must be defined in order to implement the `Comparable` module?   ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q49: What is the difference between `Kernel#require` and `Kernel#load`?   ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q50: How is the invocation of a private method different than the invocation of a public method from within its defining class?  ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q51: Why might you want to alias a method?   ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q52: What will be the value of ... ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q53: What does a bang `!` at the end of a method signify?   ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q54: What is the value of the variable "upcased" in the below piece of code? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q55: How does block invocation differ from method invocation? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q56: Can you tell me the three levels of method access control for classes and modules?  What do they imply about the method? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q57: What is the difference between `#==` and `#equal?`?  ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q58: Explain this ruby idiom: a ||= b ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q59: What does self mean? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q60: What is a Proc? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q61: What is the difference between `#==` and `#eql?`?   ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q62: Describe a closure in Ruby ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q63: What is the difference between `Array#map` and `Array#each`? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q64: What is an iterator?  ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q65: What is the difference between `throw/catch` and `raise/rescue`?   ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q66: What are some disadvantages of a case statement versus repeated `elsif` statements? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q67: What is the difference between calling "super" and calling "super()" ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q68: When might you use the `do`/`end` syntax versus using the curly bracket syntax for a block?   ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q69: Explain the difference between ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q70: What happens if a block is passed two arguments but only accepts one argument?   ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q71: How exactly does it work? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q72: Is the line of code below valid Ruby code? If so, what does it do? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q73: What will be the result of each of the following lines of code ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q74: What happens to a constant which is not assigned? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q75: Is a block an object?  ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q76: What is the primary difference in these two code snippets? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q77: Write a single line of Ruby code that prints the Fibonacci sequence of any length as an array. ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q78: Why doesn't Ruby support method overloading? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q79: Is a method an object?   ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q80: What is the difference between `BasicObject#instance_eval` and `BasicObject#instance_exec`? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q81: What is the difference between `Object#dup` and `#clone`?   ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q82: What is an eigenclass? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q83: When might you encounter a `LocalJumpError`?   ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q84: What is the differnece between `extend` and `include` in ruby? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

## [[⬆]](#toc) <a name=Sass>Sass</a> Interview Questions
#### Q1: How to use variables in Sass? ⭐
**Answer:**
Think of variables as a way to store information that you want to reuse throughout your stylesheet. You can store things like colors, font stacks, or any CSS value you think you'll want to reuse. Sass uses the `$` symbol to make something a variable.

```css
$font-stack:    Helvetica, sans-serif;
$primary-color: #333;

body {
  font: 100% $font-stack;
  color: $primary-color;
}
```


**Source:** _sass-lang.com_

#### Q2: What Selector Nesting in Sass is used for? ⭐⭐
**Answer:**
Sass *let you nest* your CSS selectors in a way that follows the same visual hierarchy of your HTML.  CSS, on the other hand, doesn't have any visual hierarchy.

Consider example (scss):
```css
.parent {
  color: red;

  .child {
    color: blue;
  }
}
```
Result (css):
```css
.parent {
  color: red;
}

.parent .child {
  color: blue;
}
```


**Source:** _sass-lang.com_

#### Q3: List out the key features for Sass? ⭐⭐
**Answer:**
Key features for Sass include

* Full CSS3-compatible
* Language extensions such as nesting, variables, and mixins
* Many useful functions for manipulating colors and other values
* Advanced features like control directives for libraries
* Well-formatted, customizable output

**Source:** _career.guru99.com_

#### Q4: What is variable interpolation in Sass? Provide some examples.  ⭐⭐
**Answer:**
 If you want to use variables inside a string, you will have to use a process called **variable interpolation**. To use it you will have to wrap your variables in `#{}`. 

Consider:
```css
$name: 'Gajendar';
$author: 'Author : $name'; // 'Author : $name'

$author: 'Author : #{$name}';
// 'Author : Gajendar'
```

The interpolation method could be useful in situations where the value of a variable is determined by some conditional statements. 

**Source:** _sitepoint.com_

#### Q5: List out the data types that Sass supports ⭐⭐
**Answer:**
Sass supports seven main data types:

* **Numbers** - most of the time they are accompanied by a unit of some sort but they are still technically numbers. You can perform basic mathematical operations on these values.

```css
$size: 18;                  // A number
$px-unit: $size * 1px;      // A pixel measurement
$px-string: $size + px;     // A string
$px-number: $px-unit / 1px; // A number
```
* **Strings** - just like CSS, accepts both quoted and unquoted strings, even if they contain spaces

```css
$website: 'SitePoint'; // Stores SitePoint
$name: 'Gajendar' + ' Singh';  // 'Gajendar Singh'
$date:  'Month/Year : ' + 3/2016; // 'Month/Year : 3/2016'
$date:  'Month/Year : ' + (3/2016); // 'Month/Year : 0.00149' 
// This is because 3/2016 is evaluated first.
$variable: 3/2016;      // Evaluated to 0.00149
```
* **Colors** - CSS color expressions come under the `color` data type. You can refer to the colors in hexadecimal notation, as `rgb`, `rgba`, `hsl` and `hsla` values or use native keywords like `pink`, `blue`, etc. 

```css
$color: yellowgreen;           // #9ACD32
color: lighten($color, 15%);    // #b8dc70
color: darken($color, 15%);     // #6c9023
color: saturate($color, 15%);   // #a1e01f
color: desaturate($color, 15%); // #93ba45
color: (green + red);           // #ff8000
```
* **Booleans** - has only two possible values: `true` and `false`

```css
$i-am-true: true;

body {
  @if not $i-am-true {
    background: rgba(255, 0, 0, 0.6);
  } @else {
    background: rgba(0, 0, 255, 0.6); // expected
  }
}
```

* **Null** -  is commonly used to define an empty state, neither `true` or `false`. This is typically the value you want to set when defining a variable without a value, only to prevent the parser from crashing.

```css
.foo {
  content: type-of(null); // null
  content: type-of(NULL); // string
  $bar: 'foo' + null; // invalid null operation: "foo plus null”.
}
```

* **Lists** - are just the Sass version of arrays. You can store multiple types of values in a list.

```css
$font-list: 'Raleway','Dosis','Lato'; // Three comma separated elements
$pad-list: 10px 8px 12px; // Three space separated elements
$multi-list: 'Roboto',15px 1.3em; // This multi-list has two lists.
```
* **Maps** -  Sass maps are like associative arrays. A map stores both keys and values associated with those keys.

```css
$styling: (
  'font-family': 'Lato',
  'font-size': 1.5em,
  'color': tomato,
  'background': black
);

h1 {
  color: map-get($styling, 'color');
  background: map-get($styling, 'background');
}
```

**Source:** _career.guru99.com_

#### Q6: What is Sass? ⭐⭐
**Answer:**
**Sass** or **Syntactically Awesome StyleSheets** is a *CSS* preprocessor that adds power and elegance to the basic language. It allows you to use variables, nested rules, mixins, inline imports, and more, all with a fully CSS-compatible syntax. Sass helps keep large stylesheets well-organized, and get small stylesheets up and running quickly.

A *CSS preprocessor* is a scripting language that extends CSS by allowing developers to write code in one language and then compile it into CSS. 


**Source:** _sass-lang.com_

#### Q7: Explain what is a @extend directive used for in Sass? ⭐⭐
**Answer:**
Using `@extend` lets you share a set of CSS properties from one selector to another. It helps keep your Sass very dry.

Consider:
```css
%message-shared {
  border: 1px solid #ccc;
  padding: 10px;
  color: #333;
}

.message {
  @extend %message-shared;
}

.success {
  @extend %message-shared;
  border-color: green;
}

.error {
  @extend %message-shared;
  border-color: red;
}

.warning {
  @extend %message-shared;
  border-color: yellow;
}
```
CSS output:
```css
.message, .success, .error, .warning {
  border: 1px solid #cccccc;
  padding: 10px;
  color: #333;
}

.success {
  border-color: green;
}

.error {
  border-color: red;
}

.warning {
  border-color: yellow;
}
```

 

**Source:** _career.guru99.comsass-lang.com_

#### Q8: What's the difference between SCSS and Sass? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q9: What is a Mixin and how to use on? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q10: What will be the CSS output for the following Sass code? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q11: What is the '@content' directive used for? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q12: What’s wrong with Sass nesting? Provide some example. ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

## [[⬆]](#toc) <a name=Scrum>Scrum</a> Interview Questions
#### Q1: What is Scrum? ⭐
**Answer:**
**Scrum** is one of the most popular frameworks for implementing *Agile*. Many people think scrum and agile are the same thing but they're not.

With scrum, the product is built in a series of fixed-length iterations called sprints that give teams a framework for shipping software on a regular cadence.

**Source:** _atlassian.com_

#### Q2: Name roles in Scrum ⭐
**Answer:**
Three essential roles for scrum success are:
* **The Product Owner** are the champions for their product. They are focused on understanding business and market requirements, then prioritizing the work to be done by the engineering team accordingly.
* ** The Scrum Master** are the champion for scrum within their team. They coach the team, the product owner, and the business on the scrum process and look for ways to fine-tune their practice of it.
* **The Scrum Team** are the champions for sustainable development practices. Scrum teams are cross-functional, "the development team" includes testers, designers, and ops engineers in addition to developers. 

**Source:** _atlassian.com_

#### Q3: What is an epic, user stories and task? ⭐
**Answer:**
**Epic:** A customer described software feature that is itemized in the product backlog is known as epic. Epics are sub-divided into stories.

**User Stories:** From the client perspective user stories are prepared which defines project or business functions, and it is delivered in a particular sprint as expected.

**Task:** Further down user stories are broken down into different task

**Source:** _career.guru99.com_

#### Q4: What is sprint in Scrum? ⭐
**Answer:**
In the Scrum methodology a **sprint** is the basic unit of development. Scrum sprints correspond to Agile iterations. 

Each sprint starts with 
* a **planning meeting**, where the tasks for the sprint are identified and an estimated commitment for the **sprint goal** is made. 

A Sprint ends with 
* a **review or retrospective meeting** where the progress is reviewed and lessons for the next sprint are identified. During each sprint, the team creates finished portions of a product.

**Source:** _stackoverflow.com_

#### Q5: Name some types of meetings or ceremonies in Scrum ⭐⭐
**Answer:**
Scrum calls for four ceremonies that bring structure to each sprint:

* **Sprint planning**: A team planning meeting that determines what to complete in the coming sprint.
* **Daily stand-up**: Also known as a daily scrum, a 15-minute mini-meeting for the software team to sync.
* **Sprint demo**: A sharing meeting where the team shows what they've shipped in that sprint.
* **Sprint retrospective**: A review of what did and didn't go well with actions to make the next sprint better.


**Source:** _atlassian.com_

#### Q6: Mention the key difference between sprint backlog and product backlog? ⭐⭐
**Answer:**
* **Product backlog**: It contains a list of all desired features and is owned by the product owner

* **Sprint backlog**: It is a subset of the product backlog owned by development team and commits to deliver it in a sprint. It is created in Sprint Planning Meeting

**Source:** _career.guru99.com_

#### Q7: Have you ever used Scrum Task Board? ⭐⭐
**Answer:**
In Scrum the *task board* is a visual display of the progress of the Scrum team during a sprint. It presents a snapshot of the current sprint backlog allowing everyone to see which tasks remain to be started, which are in progress and which are done.

Consider the following layout of the task board:
- Stories
- To Do
- In Progress
- Testing
- Done

**Source:** _manifesto.co.uk_

#### Q8: What is Sprint Planning? ⭐⭐
**Answer:**
The work to be performed in the Sprint is planned at the **Sprint Planning**. This plan is created by the collaborative work of the entire Scrum Team.

Sprint Planning answers the following:

* What can be delivered in the Increment resulting from the upcoming Sprint?
* How will the work needed to deliver the Increment be achieved?

The Sprint Goal is an objective set for the Sprint that can be met through the implementation of Product Backlog. 

**Source:** _scrum.org_

#### Q9: Explain difference between a Product and a Sprint Backlog ⭐⭐
**Answer:**
* The **Product Backlog** is an ordered list of everything that is known to be needed in the product. It is the single source of requirements for any changes to be made to the product.

* The **Sprint Backlog** is the set of Product Backlog items selected for the Sprint during the Sprint Planning, plus a plan for delivering the product Increment and realizing the Sprint Goal. 

**Source:** _scrum.org_

#### Q10: Mention in detail what are the role’s of Scrum Master? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q11: What is a Sprint Review? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q12: Explain the difference between Extreme programming and Scrum? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q13: What does the Scrum Framework consist from? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q14: What is Acceptance Criteria? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q15: Explain what is Scrum ban? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q16: What are the Scrum values? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q17: What the Scrum theory is based on? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q18: What is Scrum Increment? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q19: Explain how you can measure the velocity of the sprint with varying team capacity? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q20: Explain main differences between Scrum and Agile? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q21: What is a Sprint Retrospective? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q22: Provide some examples of burn-up chart ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q23: What are the benefits of Burn Up chart? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q24: What is the Scrum's definition of "Done"? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

## [[⬆]](#toc) <a name=SoftwareArchitecture>Software Architecture</a> Interview Questions
#### Q1: Why Do You Need Clustering? ⭐⭐
**Answer:**
*Clustering* is needed for achieving high availability for a server software. The main purpose of clustering is to achieve 100% availability or a zero down time in service. A typical server software can be running on one computer machine and it can serve as long as there is no hardware failure or some other failure. By creating a cluster of more than one machine, we can reduce the chances of our service going un-available in case one of the machine fails.  
  
Doing clustering does not always guarantee that service will be 100% available since there can still be a chance that all the machine in a cluster fail at the same time. However it in not very likely in case you have many machines and they are located at different location or supported by their own resources.  
  

**Source:** _fromdev.com_

#### Q2: What Is A Cluster? ⭐⭐
**Answer:**
A cluster is group of computer machines that can individually run a software. Clusters are typically utilized to achieve high availability for a server software. Clustering is used in many types of servers for high availability.  

*   **App Server Cluster**  
    An app server cluster is group of machines that can run a application server that can be reliably utilized with a minimum of down-time.
*   **Database Server Cluster**  
    An database server cluster is group of machines that can run a database server that can be reliably utilized with a minimum of down-time.

**Source:** _fromdev.com_

#### Q3: What Is Scalability? ⭐⭐
**Answer:**
Scalability is the ability of a system, network, or process to handle a growing amount of load by adding more resources. The adding of resource can be done in two ways  
  

*   **Scaling Up**  
    This involves adding more resources to the existing nodes. For example, adding more RAM, Storage or processing power.
*   **Scaling Out**  
    This involves adding more nodes to support more users.

Any of the approaches can be used for scaling up/out a application, however the cost of adding resources (per user) may change as the volume increases. If we add resources to the system It should increase the ability of application to take more load in a proportional manner of added resources.  
  
An ideal application should be able to serve high level of load in less resources. However, in practical, linearly scalable system may be the best option achievable. Poorly designed applications may have really high cost on scaling up/out since it will require more resources/user as the load increases.  
  

**Source:** _fromdev.com_

#### Q4: What Is Session Replication? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q5: What Is Load Balancing? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q6: What Is Sticky Session Load Balancing? What Do You Mean By "Session Affinity"? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q7: What Is Fail Over? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q8: What Do You Mean By High Availability? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q9: "People who like this also like... ". How would you implement this feature in an e-commerce shop? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q10: What Is ACID Property Of A System? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q11: What Is Middle Tier Clustering? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q12: How Do You Update A Live Heavy Traffic Site With Minimum Or Zero Down Time? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q13: Explain Blue-Green Deployment Technique ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q14: How can you keep one copy of your utility code and let multiple consumer components use and deploy it? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q15: What does SOLID stand for? What are its principles? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q16: Defend the monolithic architecture. ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q17: What Is Sharding? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q18: What Is IP Address Affinity Technique For Load Balancing? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q19: What Is BASE Property Of A System? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q20: Explain threads to your grandparents ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q21: Why layering your application is important? Provide some bad layering example. ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q22: Why should you structure your solution by components? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q23: Are you familiar with The Twelve-Factor App principles? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q24: What are heuristic exceptions? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q25: Why is writing software difficult? What makes maintaining software hard? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q26: What Is Shared Nothing Architecture? How Does It Scale? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q27: What Is CAP Theorem? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q28: What Does Eventually Consistent Mean? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

## [[⬆]](#toc) <a name=TypeScript>TypeScript</a> Interview Questions
#### Q1: What is TypeScript and why do we need it? ⭐
**Answer:**
JavaScript is the only client side language universally supported by all browsers. But JavaScript is not the best designed language. It’s not a class-based object-oriented language, doesn’t support class based inheritance, unreliable dynamic typing and lacks in compile time error checking. And TypeScript addresses all these problems. In other words, TypeScript is an attempt to “fix” JavaScript problems.

TypeScript is a free and open source programming language developed and maintained by Microsoft. It is a strict superset of JavaScript, and adds **optional static typing** and **class-based object-oriented programming** to the language. TypeScript is quite easy to learn and use for developers familiar with C#, Java and all strong typed languages. At the end of day “TypeScript is a language that generates plain JavaScript files.”

As stated on [Typescript official website](http://www.typescriptlang.org/), “TypeScript lets you write JavaScript the way you really want to. TypeScript is a typed superset of JavaScript that compiles to plain JavaScript. Any browser. Any host. Any OS. Open Source.” Where “**typed**” means that it considers the types of variables, parameters and functions.

**Source:** _talkingdotnet.com_

#### Q2: What are Modules in Typescript? ⭐
**Answer:**
Modules in Typescript helps in organizing the code. There are 2 types of Modules — Internal and External

* **Internal Modules** are now replaceable by using Typescript’s namespace.

* **External Modules** used to specify and load dependencies between multiple external js files. If there is only one js file used, then external modules are not relevant.

#### Q3:  What is Typescript and why one should use it? ⭐
**Answer:**
TypeScript is a free and open-source programming language developed and maintained by Microsoft. It is a strict syntactical superset of JavaScript, and adds optional static typing and class-based object-oriented programming to the language.

#### Q4: Explain generics in TypeScript ⭐
**Answer:**
Generics are able to create a component or function to work over a variety of types rather than a single one.

```js
/** A class definition with a generic parameter */
class Queue<T> {
  private data = [];
  push = (item: T) => this.data.push(item);
  pop = (): T => this.data.shift();
}

const queue = new Queue<number>();
queue.push(0);
queue.push("1"); // ERROR : cannot push a string. Only numbers allowed

```


**Source:** _basarat.gitbooks.io_

#### Q5: What is TypeScript and why would I use it in place of JavaScript? ⭐
**Details:**



**Answer:**
**TypeScript** is a superset of JavaScript which primarily provides optional static typing, classes and interfaces. One of the big benefits is to enable IDEs to provide a richer environment for spotting common errors as *you type the code*. For a large JavaScript project, adopting TypeScript might result in more robust software, while still being deployable where a regular JavaScript application would run.

In details:
* TypeScript supports new ECMAScript standards and compiles them to (older) ECMAScript targets of your choosing. This means that you can use features of ES2015 and beyond, like modules, lambda functions, classes, the spread operator, destructuring, today. 
* JavaScript code is valid TypeScript code; TypeScript is a superset of JavaScript. 
* TypeScript adds type support to JavaScript. The type system of TypeScript is relatively rich and includes: interfaces, enums, hybrid types, generics, union and intersection types, access modifiers and much more. TypeScript makes typing a bit easier and a lot less explicit by the usage of type inference.
* The development experience with TypeScript is a great improvement over JavaScript. The IDE is informed in real-time by the TypeScript compiler on its rich type information. 
* With strict null checks enabled (`--strictNullChecks` compiler flag) the TypeScript compiler will not allow undefined to be assigned to a variable unless you explicitly declare it to be of nullable type. 
* To use TypeScript you need a build process to compile to JavaScript code. The TypeScript compiler can inline source map information in the generated .js files or create separate .map files. This makes it possible for you to set breakpoints and inspect variables during runtime directly on your TypeScript code. 
* TypeScript is open source (Apache 2 licensed, see github) and backed by Microsoft. *Anders Hejlsberg*, the lead architect of C# is spearheading the project.

**Source:** _stackoverflow.com_

#### Q6: How to call base class constructor from child class in TypeScript? ⭐
**Answer:**
We can call base class constructor using `super()`.

**Source:** _http://www.talkingdotnet.com_

#### Q7: Do we need to compile TypeScript files and why? ⭐
**Answer:**
Yes we do. Typescript is just a language Extension browsers can't interpret it. Converting from TypeScript to JavaScript is called compiling. Compiling doesn't mean binary code is created in this case. For this kind of translation, also the term transpilation is used instead of compilation.

**Source:** _stackoverflow.com_

#### Q8: List the built-in types in Typescript ⭐
**Answer:**
These are also called the primitive types in TypeScript:
* **Number** type: it is used to represent number type values and represents double precision floating point values.
```js
var variable_name: number;
```
* **String** type: it represents a sequence of characters stored as Unicode UTF-16 code. It is the same as JavaScript primitive type.
```js
var variable_name: string;
```
* **Boolean** type: in Typescript, it is used to represent a logical value. When we use the Boolean type, we get output only in true or false. It is also the same as JavaScript primitive type.
```js
var variable_name: bool;
```
* **Null** type: it represents a null literal and it is not possible to directly reference the null type value itself.
```js
var variable_name:number = null;
```
* **Undefined** type: it is the type of undefined literal. This type of built-in type is the sub-type of all the types.
```js
var variable_name:number = undefined;
```


#### Q9: What are the benefits of TypeScript? ⭐
**Answer:**
TypeScript has following benefits.

*   It helps in code structuring.
*   Use class based object oriented programming.
*   Impose coding guidelines.
*   Offers type checking.
*   Compile time error checking.
*   Intellisense.

**Source:** _talkingdotnet.com_

#### Q10: What are the difference beetween Typescript and JavaScript? ⭐⭐
**Answer:**
* It is an object oriented programming language (not pure).
* Here it is static typing (We can declare a variable in multiple ways). ex: var num : number.
* It has interfaces.
* It has optional parameter feature.
* It has Rest Parameter feature.
* Supports generics.
* Supports Modules
* Number, string etc. are the interfaces.


#### Q11: What is Interface in TypeScript? ⭐⭐
**Answer:**
One of TypeScript’s core principles is that type-checking focuses on the *shape* that values have.

An `interface` is a virtual structure that only exists within the context of TypeScript. The TypeScript compiler uses interfaces solely for type-checking purposes.

When you define your interface you’re saying that any object (not an instance of a class) given this contract must be an object containing interfaces properties.

**Source:** _medium.com_

#### Q12: When to use interfaces and when to use classes in TypeScript? ⭐⭐
**Answer:**
If you need/wish to create an instance of perhaps a custom object, whilst getting the benefits of type-checking things such as arguments, return types or generics - a class makes sense. 

If you’re not creating instances - we have interfaces at our disposal, and their benefit comes from not generating any source code, yet allowing us to somewhat “virtually” type-check our code.

**Source:** _toddmotto.com_

#### Q13: Which object oriented terms are supported by TypeScript? ⭐⭐
**Answer:**
TypeScript supports following object oriented terms:

*   Modules
*   Classes
*   Interfaces
*   Data Types
*   Member functions

**Source:** _http://www.talkingdotnet.com_

#### Q14: What is getters/setters in TypeScript? ⭐⭐
**Answer:**
TypeScript supports **getters/setters** as a way of intercepting accesses to a member of an object. This gives you a way of having finer-grained control over how a member is accessed on each object.

```js
class foo {
  private _bar:boolean = false;

  get bar():boolean {
    return this._bar;
  }
  set bar(theBar:boolean) {
    this._bar = theBar;
  }
}

var myBar = myFoo.bar;  // correct (get)
myFoo.bar = true;  // correct (set)
```

**Source:** _typescriptlang.org_

#### Q15: Does TypeScript support all object oriented principles? ⭐⭐
**Answer:**
The answer is **YES**. There are 4 main principles to Object Oriented Programming: 

* Encapsulation, 
* Inheritance, 
* Abstraction, and 
* Polymorphism. 

TypeScript can implement all four of them with its smaller and cleaner syntax.

**Source:** _jonathanmh.com_

#### Q16: How could you check null and undefined in TypeScript? ⭐⭐
**Answer:**
Just use:
```js
if (value) {
}
```
It will evaluate to `true` if `value` is not:

* `null`
* `undefined`
* `NaN`
* empty string `''`
* `0`
* `false`

TypesScript includes JavaScript rules.


**Source:** _stackoverflow.com_

#### Q17: How to implement class constants in TypeScript? ⭐⭐
**Answer:**
In TypeScript, the `const` keyword cannot be used to declare class properties. Doing so causes the compiler to an error with "A class member cannot have the 'const' keyword." TypeScript 2.0 has the `readonly` modifier:

```js
class MyClass {
    readonly myReadonlyProperty = 1;

    myMethod() {
        console.log(this.myReadonlyProperty);
    }
}

new MyClass().myReadonlyProperty = 5; // error, readonly
```

**Source:** _stackoverflow.com_

#### Q18: Could we use TypeScript on backend and how? ⭐⭐
**Answer:**
Typescript doesn’t only work for browser or frontend code, you can also choose to write your backend applications. For example you could choose Node.js and have some additional type safety and the other abstraction that the language brings.

1. Install the default Typescript compiler  

```sh
npm i -g typescript
```
2. The TypeScript compiler takes options in the shape of a tsconfig.json file that determines where to put built files and in general is pretty similar to a babel or webpack config.

```sh
{
  "compilerOptions": {
    "target": "es5",
    "module": "commonjs",
    "declaration": true,
    "outDir": "build"
  }
}
```
3. Compile ts files

```sh
tsc
```
4. Run

```js
node build/index.js
```

**Source:** _jonathanmh.com_

#### Q19: What is the difference between Classes and Interfaces in Typescript? ⭐⭐
**Answer:**
We use classes as object factories. A class defines a blueprint of what an object should look like and act like and then implements that blueprint by initialising class properties and defining methods. Classes are present throughout all the phases of our code.

Unlike classes, an interface is a virtual structure that only exists within the context of TypeScript. The TypeScript compiler uses interfaces solely for type-checking purposes. Once code is transpiled to its target language, it will be stripped from interfaces.

A class may define a factory or a singleton by providing initialisation to its properties and implementation to its methods, an interface is simply a structural contract that defines what the properties of an object should have as a name and as a type.

**Source:** _toddmotto.com_

#### Q20: What is "Decorators" in TypeScript? ⭐⭐
**Answer:**
A *Decorator* is a special kind of declaration that can be attached to a class declaration, method, accessor, property, or parameter. Decorators are functions that take their target as the argument. With decorators we can run arbitrary code around the target execution or even entirely replace the target with a new definition.

There are 4 things we can decorate in ECMAScript2016 (and Typescript): constructors, methods, properties and parameters. 

**Source:** _www.sparkbit.pl_

#### Q21: What is a TypeScript Map file? ⭐⭐
**Answer:**
`.map` files are source map files that let tools map between the emitted JavaScript code and the TypeScript source files that created it. Many debuggers (e.g. Visual Studio or Chrome's dev tools) can consume these files so you can debug the TypeScript file instead of the JavaScript file.

**Source:** _stackoverflow.com_

#### Q22: What's wrong with that code? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q23: What are different components of TypeScript? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q24: Is that TypeScript code valid? Explain why. ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q25: What is Typings in Typescript? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q26: How To Use external plain JavaScript Libraries in TypeScript? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q27: How TypeScript is optionally statically typed language? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q28: Are strongly-typed functions as parameters possible in TypeScript? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q29: What is the default access modifier for members of a class in TypeScript? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q30: How can you allow classes defined in a module to accessible outside of the module? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q31: Explain how and why we could use property decorators in TS? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q32: Does TypeScript supports function overloading? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q33: Explain why that code is marked as WRONG? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q34: What is the difference between "interface vs type" statements? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q35: How would you overload a class constructor in TypeScript? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q36: What is one thing you would change about TypeScript? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q37: Explain when to use "declare" keyword in TypeScript ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q38: What are Ambients in TypeScripts and when to use them? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q39: Is it possible to generate TypeScript declaration files from JS library? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

## [[⬆]](#toc) <a name=UXDesign>UX Design</a> Interview Questions
#### Q1: Name some basic design elemnts ⭐
**Answer:**
The elements of design are:

* **LINE** – The linear marks made with a pen or brush or the edge created when two shapes meet.
* **SHAPE** – A shape is a self contained defined area of geometric (squares and circles), or organic (free formed shapes or natural shapes). A positive shape automatically creates a negative shape.
* **DIRECTION** – All lines have direction – Horizontal, Vertical or Oblique. Horizontal suggests calmness, stability and tranquillity. Vertical gives a feeling of balance, formality and alertness. Oblique suggests movement and action
* **SIZE** – Size is simply the relationship of the area occupied by one shape to that of another.
* **TEXTURE** – Texture is the surface quality of a shape – rough, smooth, soft hard glossy etc.
* **COLOUR** – Colour is light reflected off objects. Color has three main characteristics: hue or its name (red, green, blue, etc.), value (how light or dark it is), and intensity (how bright or dull it is).

<div class="text-center">
<img src="http://www.j6design.com.au/wp-content/uploads/2014/02/designelements-1024x640.jpg" class="img-fluid" style="max-width: 500px;"/>
</div>

**Source:** _j6design.com.au_

#### Q2: What is User Centered Design? ⭐⭐
**Answer:**
**User-centered design** is an iterative design process in which designers focus on the users and their needs in each phase of the design process. UCD calls for involving users throughout the design process via a variety of research and design techniques so as to create highly usable and accessible products for them.

User-centered design demands that designers employ a mixture of *investigative* (e.g., surveys and interviews) and *generative* (e.g., brainstorming) methods and tools to develop an understanding of user needs.

**Source:** _interaction-design.org_

#### Q3: What is User Research? ⭐⭐
**Answer:**
User research is conducted so as to understand users’ characteristics, aims, and behaviors towards achieving these aims. Its purpose is to produce designs that improve their working practices and lives. User research also involves the continuous evaluation of the impact of designs on the users, not only during the design and development phase but after long-term use, too.

**Source:** _interaction-design.org_

#### Q4: Name some UX Design tools you prefer to work with ⭐⭐
**Answer:**
Just to name a few: 

* Adobe XD, 
* Figma,
* Invision studio
* Sketch
* Balsamiq

**Source:** _uxplanet.org_

#### Q5: Is UX design UI design? What’s the difference? ⭐⭐
**Answer:**
User interface (UI) design is not the same as UX design. A seasoned UX design pro understands the vital difference and is able to articulate it clearly. Designing for the user interface often plays an important role in the work of a UX designer, but it is not the only function.

Whereas UI design is concerned with the effective layout of visual elements on a user interface, UX design is ‘people first.’ It’s about what motivates them—how they think and behave.

A great UX designer should be able to demonstrate knowledge describing the differences, in particular how UI design is only one slice of the UX design process ‘pie’, and only one of many different disciplines that reside under the UX banner. These include, but are not limited to: a user-centered design strategy, core user demographic definition, persona creation, user research, information architecture, content strategy, interaction design, visual design and usability testing.

**Source:** _toptal.com_

#### Q6: What is Graphic Design? ⭐⭐
**Answer:**
**Graphic designers** work with graphical images, whether they be illustrations, typography, or images, and on a variety of media including print and web. Graphic design is typically rendered in 2D — printed on a physical surface or displayed on a screen but not limited to 2D.

As a graphic designer, you can specialize in the following

* Logo design
* Brand design
* Print Designer

**Source:** _uxplanet.org_

#### Q7: What is Interaction Design? ⭐⭐
**Answer:**
Interaction designers, focus on digital products and interactive software design. **Interaction design** helps human
