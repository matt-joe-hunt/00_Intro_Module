## Justification

3 ways of thinking have driven this project, I have developed this approach over 4 years of working with DevOps and Cloud based technologies, 3 of these as a Trainer for one of the UK's largest commercial IT Training Provider. 

- When learning a new technology, keeping things simple in the first instance is of paramount importance.
- Practical application of principles is best.
- KT (Knowledge Transfer) is an important part of solidifying what you have learnt.

### Keeping things Simple

Lets say you have some experience with AWS, and are interested in learning how to deploy a Lambda Function.  You might find an online tutorial that introduces you to the tool, but wait! In order to follow the tutorial through you will be rail-roaded into using a particular Library or Framework, possibly even signing up to something in the process. If this sounds familiar then I sympathise, you set out to learn *A*, but have been coerced into learning about *B* and *C* as well.

But who has the time? And worst still, it can easily distract from your initial goal.

I'm a firm believer that when learning a new technology, keeping things simple in the first instance is of paramount importance.  Frankly all the frilly bits can come later!

I have tried to start simple, and build upon fundamentals in later lessons, staying as unopinonated as possible.  Technologies that I use that deviate from the central principle of the lesson will be minimal and easily replaced.

I will also only try to introduce one new concept at a time, hopefully making it obvious what components are new and of interest in each new section.

### Practical Application

I have studied and sat all of the Associate AWS Exams and some of the Professional, I started out like most by buying an expensive subscription to an online learning platform.  Now these resources are useful, there is no denying that, however my success with the exams improved dramatically when I started to learn to use AWS alongside Terraform.

My turning point was working with API Gateway, this serverless technology has alot of complexity to it and I did feel like I was learning about the content in online videos.  However it was only when I actually started to create my own using Terraform did I start to understand the real depth fo API GW. Since then I have spent more time creating the resources I have learnt about then I have watching videos.

### Knowledge Transfer

The truest test of whether you understand a concept is to try to explain this concept to somebody else. You might be surprised about the areas that you need to gloss over because you dont have the knowledge you thought you had.

It should be obvious that this isn't a failing, in my experience is that it is quite common and just highlights the degree of our own understanding.  This in turn allows you to go back and focus on those areas in which you need to improve.

How many times have you watched an online tutorial or lecture, nodding along as various concepts are covered, and then realised after the event that you can't actually recall much of what you had supposedly learnt?  It happens to me quite a bit, so it is by going back and talking about what I had learnt that I gain a better understanding.

## Consistant style

To create the structure of this project I have chosen to split the resources that I am creating into modules, these modules means that my deployment is easier to write, debug and maintain.  By using modules, we can also choose to reuse our modules, which we will start to see in later sessions.

You will notice a consistent style within the project, the terraform code that is written for each module is grouped into multiple files, and these .tf files also appear in the root of the project.  Typically the files that exist are:

- main.tf
- variables.tf
- outputs.tf
- data.tf

### main.tf

In this file the terraform resources are described, unless you are looking in the root of the project structure in which case the main.tf file describes the modules used in the project.

Within a module I will define the resources that are logically related in the main.tf, this approach is recommended by HashiCorp, however is not always the chosen approach in reality.

### variables.tf

In this file the variables that are used by the project and the various modules can be defined, you can define the type of the variable, give it a description, and also declare a default value, making working with the project a little easier.

In later sessions we will make use of a *terraform.tfvars* file to define the value that we want to give to our variables.

### outputs.tf

In this file the output from the resources created are defined.  This can be useful if you want to print some output to the console when the deployment is completed, however you will most often use it to pass the output from one module to be used with another.

### data.tf

In this file is where I will define *data* resource blocks, therse can be used for different things including, getting information about existing AWS resources in order to utilise them with other resources.

## Disclaimer

Do not expect this to be complete with all industry best practices, however if you are new to working with Terraform then this could be a good set of sample projects to start with! 

My hope is that you will find some use in 'poking' this implementation to see how it works and changing it to see how it breaks. I will explain what some important sections of the code are doing so that you can start to develop and expand your own deployments.

## Lessons

Grouped and listed in a logical order, though this can be deviated from.

- [01_EC2_Example](https://github.com/matt-joe-hunt/01_EC2_Example)
- EC2_with_VPC_Example
- 
