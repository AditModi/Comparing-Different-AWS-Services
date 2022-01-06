# Introduction

The Comparison between Different AWS Services is a Series containing different blog posts that provide a basic understanding of key differences Between different aws services. Each post covers the detailed guide on difference between the AWS Services and Which is preferred more . This series aims at providing "Comparison Between Different AWS Services."

## What is AWS CodeBuild? What is AWS CodePipeline?

**AWS CodeBuild** is a fully managed build service in the cloud. AWS CodeBuild compiles the source code, runs unit tests, and produces artifacts that are ready to deploy. CodeBuild eliminates the need to provision, manage, and scale own build servers. It provides prepackaged build environments for popular programming languages and build tools such as Apache Maven, Gradle, and more. You can also customize build environments in CodeBuild to use your own build tools. CodeBuild scales automatically to meet peak build requests

**AWS CodePipeline** on the other hand, is a fully managed continuous delivery service that helps to automate the release pipelines for fast and reliable application and infrastructure updates. CodePipeline automates the build, test, and deploy phases of the release process every time there is a code change, based on the release model you define. This enables a rapid and reliable delivery of features and updates. AWS CodePipeline can easily integrate with third-party services such as GitHub or any other custom plugin.


![image](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/vzvxteb1vwu50a3winfd.png)

My Background: I am Cloud , DevOps & Big Data Enthusiast | 4x AWS Certified | 3x OCI Certified | 3x Azure Certified . 



## What are the differences?

The main difference between the two is; AWS CodeBuild can be classified as a tool in the Continuous Integration category, while AWS CodePipeline is grouped under Continuous Deployment.


## What is Continuous Integration?

Continuous integration is a software development method where members of the team can integrate their work at least once a day. In this method, every integration is checked by an automated build to search the error.

In continuous integration after a code commit, the software is built and tested immediately. In a large project with many developers, commits are made many times during a day. With each commit code is built and tested. If the test is passed, build is tested for Deployment. If the Deployment is a success, the code is pushed to production. This commit, build, test, and deploy is a continuous process, and hence the name continuous integration/deployment.

## What is Continuous Delivery?

Continuous delivery is a software engineering method in which a team develops software products in a short cycle. It ensures that software can be easily released at any time.

The main aim of continuous delivery is to build, test, and release software with good speed and frequency. It helps you to reduce the cost time and risk of delivering changes by allowing for frequent updates in production.

## What is Continuous Deployment

Continuous deployment is a software engineering process in which product functionalities are delivered using automatic deployment. It helps testers to validate whether the codebase changes are correct and stable or not.

The team can achieve continuous deployment by relying on infrastructure that automates different testing steps. Once each integration meets this release criteria, the application is updated with a new code.


 ## How do you run AWS CodeBuild and AWS CodePipeline?

You can use the AWS CodeBuild or AWS CodePipeline console to run CodeBuild. You can also automate the running of CodeBuild by using the AWS Command Line Interface (AWS CLI) or the AWS SDKs.

![image](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/2u8085gkpy5bihz6d53h.png)
 

Source: stackshare.io

 

You can then add CodeBuild as a build or test action to the build or test stage of a pipeline in AWS CodePipeline. AWS CodePipeline is a continuous delivery service that you can use to model, visualize, and automate the steps required to release your code. This includes building your code. 

A pipeline is a workflow construct that describes how code changes go through a release process. See the illustration below; 

![image](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/esp0wlxm5cdtcog793kx.png)
 

Source: stackshare.io



## What are some of the tools that integrate with AWS CodeBuild and AWS CodePipeline?

Some of the tools that integrate with AWS CodeBuild include; GitHub, GitHub Enterprise, Jenkins, Bitbucket, AWS CodeCommit, AWS CodeFormation, AWS Elastic Beanstalk, and Amazon S3.

On the other hand, some of the tools that integrate with AWS CodePipeline include; GitHub, AWS Elastic Beanstalk, Amazon EC2, Amazon S3, Jenkins, Cloudbees, and Runscope. 

## What are some alternatives to AWS CodeBuild and AWS CodePipeline?

#### Jenkins 

Jenkins is the leading open-source continuous integration server. Built with Java, it provides over 300 plugins to support building and testing virtually any project.

#### AWS CodeDeploy

AWS CodeDeploy is a service that automates code deployments to Amazon EC2 instances. AWS CodeDeploy makes it easier to rapidly release new features, helps you avoid downtime during deployment, and handles the complexity of updating your applications.

#### AWS CodeStar

AWS CodeStar provides a unified user interface, enabling you to easily manage your software development activities in one place. 

#### Apache Maven

Maven allows a project to build using its project object model (POM) and a set of plugins that are shared by all projects using Maven, providing a uniform build system.

#### GitLab CI

GitLab offers a continuous integration service. If you add a .gitlab-ci.yml file to the root directory of your repository, and configure your GitLab project to use a Runner, then each merge request or push triggers your CI pipeline.

## Conclusion

Every project has its own requirements and every CI/CD is unique. But when you have such great and easy to use tools available for you, you might as well want to make smarter use of them. AWS CodeBuild and AWS CodePipeline protects your secrets, automates jobs, reduces chances of error, and saves time and effort. In a poll by Stackshare in its community, “Pay per minute” is the primary reason why developers consider AWS CodeBuild over the competitors, whereas “Simple to set up” was stated as the key factor in picking AWS CodePipeline.

Hope this guide helps you understand the key differences between two of most used CI/CD services of aws, feel free to contact me on [LinkedIn.](https://www.linkedin.com/in/adit-modi-2a4362191/)
You can view my badges [here.](https://www.youracclaim.com/users/adit-modi/badges)
If you are interested in learning more about AWS then follow me on [github.](https://github.com/AditModi)
If you liked this content then do clap and share it . Thank You .
