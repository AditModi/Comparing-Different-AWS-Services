# Introduction

The Comparison between Different AWS Services is a Series containing different blog posts that provide a basic understanding of key differences Between different aws services. Each post covers the detailed guide on difference between the AWS Services and Which is preferred more . This series aims at providing "Comparison Between Different AWS Services."

**Infrastructure as code [IaC]** is a big buzzword these days, and it’s no mystery why. IaC, referred to as software-defined infrastructure, is defined as an IT setup wherein developers or operations teams automatically manage and provision the technology stack for an application through software, rather than using a manual process to configure discrete hardware devices and operating systems. It’s a cornerstone of DevOps, designed to boost the agility, productivity and quality of work within organizations.

When people look for tools to implement infrastructure as code on AWS, they often narrow the choice between AWS CloudFormation or the open-source tool Terraform. Let’s review the differences between the two so you can determine which is right for your needs.

![image](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/lxyj39005us8i9308ist.png)
 
*My Background: I am Cloud , DevOps & Big Data Enthusiast | 4x AWS Certified | 3x OCI Certified | 3x Azure Certified .* 

![image](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/xx5nd97sf7xub58rahyx.png)

## CloudFormation

AWS CloudFormation is a managed AWS service with a common language for you to model and provision AWS and third-party application resources for your cloud environment in a secure and repeatable manner. This provides a single reference point for both AWS infrastructure mapping and development.  

CloudFormation abstracts away many of the subtleties involved in managing dependencies between AWS resources. Additionally, CloudFormation allows for the modification and destruction of provisioned resources in a prescribed and predictable manner, making versioning and iterating on your infrastructure much more accessible. CloudFormation is AWS-focused, and AWS-native. 

With CloudFormation, you don’t need to figure out which AWS services need to be provisioned or the subtleties of how to make these dependencies connect together  — CloudFormation takes care of this for you in a siloed kind of manner. Once deployed, you can destroy and modify AWS resources in a controlled and predictable way within CloudWatch, allowing you to version control your own AWS infrastructure. This allows for iterative testing, as well as rollback (when configured properly).  

## Terraform‍

Created by HashiCorp, Terraform is an open-source infrastructure-as-code software tool that helps users with the task of setting up and provisioning datacenter infrastructure. A cloud-agnostic tool, Terraform codifies APIs into declarative configuration files that can be shared amongst team members, treated as code, edited, reviewed, and versioned.

Now that we’ve defined these two IaC platforms, let’s review some of the key differences in more depth. 

## State Management

With both CloudFormation and Terraform, you need to keep track of all resources under management.

With CloudFormation, users can perform regular drift detection on their entire provisioned infrastructure, and receive detailed responses if anything has changed. Some resources in a CloudFormation stack are able to have parameters changed without destroying and rebuilding the targeted resource, while others are considered immutable and will be rebuilt.  Additionally, before CloudFormation will delete a resource, it will determine dependencies and fail the command if any exist (which would remain after resource removal). 

Terraform stores the state of the infrastructure on the provisioning computer, or in a remote site (for team use). This state file is a custom JSON format which serves as a map for Terraform, describing which resources it manages, and how those resources should be configured.

Since CloudFormation is a managed AWS service, it does this for you. CloudFormation will consistently check infrastructure it has provisioned to detect if it is maintaining that state and configuration.  If you’re using Terraform, it stores its state on a local disk, and there is a remote state option, which writes the state data to a remote data store, to be shared between all members of a team. Remote state supports Amazon S3, but you need to configure it yourself.

Now that we’ve covered differences in state management, let’s move on to the topic of modularity.

## Modularity

In the constantly changing world of infrastructure requirements,  flexibility is key. CloudFormation and Terraform have unique ways of addressing this need.

Terraform has a modules, which are containers for multiple resources that are used together. Modules allow developers to abstract their infrastructure into reusable, shareable code and increases iteration speed for teams (much like functions do in a programming language like Ruby).

CloudFormation utilizes a system called “nested stacks.” That is, CloudFormation  templates being called from within CloudFormation templates. These nested stacks can further be abstracted into StackSets. It should be noted that StackSets require additional permissions, beyond those of normal AWS CloudFormation.  

A benefit of Terraform is increased flexibility over CloudFormation with regards to modularity. Terraform modules can be pulled in for any provider supported, or organizations can roll their own.

Conversely, in a multi-cloud or hybrid environment, CloudFormation doesn’t easily allow users to provision or natively coordinate non-AWS resources. It’s not impossible, as there is a custom resources feature in CloudFormation, but it requires additional templating and design to bring in third party resources, or those AWS services not available organically.

## Configuration

CloudFormation and Terraform differ in how they handle configuration and parameters.

Terraform uses provider specific data sources. The implementation is in a modular fashion, allowing data to be fetched or computed for use elsewhere in a Terraform configuration. This lets a Terraform configuration make use of information defined outside of Terraform (such as an Elastic IP address), to update or provision infrastructure.

CloudFormation uses parameters, and has a maximum of 60 parameters per template. Each parameter must have a logical and unique ID among all others in the template. The parameters must be of a type supported by CloudFormation and they have to be provided at the stack’s runtime. Additionally, each parameter must be declared and referenced from within the same template. CloudFormation does have the capability to use Dynamic References to retrieve parameters at runtime from AWS Systems Manager parameter store, if one has been configured properly. 

## Language‍

Terraform uses HashiCorp Configuration Language (HCL), a language built by HashiCorp. It is fully compatible with JSON, and was created to strike a balance between human-friendly and machine-friendly languages, while remaining interpretable to humans.

AWS CloudFormation utilizes either JSON or YAML, with the YAML version being slightly easier to read (as well as more compact). CloudFormation also has a limit of 51,000 bytes for the template body itself. If a larger template is needed, AWS advises developers to separate resources into nested stacks.



![Alt Text](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/3p6pm88p29jl5mqwo4op.png)

## The Bigger Picture — CloudFormation or Terraform‍

Both are powerful cloud infrastructure management tools. If you’re already on AWS and using all AWS tools, CloudFormation may be more convenient, especially if you have no external tie ins from 3rd parties. However, if you’re looking for additional flexibility from a cloud-agnostic platform that integrates with AWS services (and those of all other popular providers), Terraform might be of greater utility for your organization. It’s important to not only look at what is working currently - but what the future state of any infrastructure might be. There are long-term benefits with both toolsets, and the final decision may come down to simple usability and developer comfort. Whichever choice you make, using either of these “swiss army knives” of AWS infrastructure is sure to increase productivity, portability, and efficiency.


---

Hope this guide helps you understand the key differences between AWS CloudFormation and Terraform, feel free to connect with me on [LinkedIn.](https://www.linkedin.com/in/adit-modi-2a4362191/)
You can view my badges [here.](https://www.youracclaim.com/users/adit-modi/badges)
If you are interested in learning more about AWS then follow me on [github.](https://github.com/AditModi)
If you liked this content then do clap and share it . Thank You .