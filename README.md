# Group Chat Application

This is a group chat application developed in interest of showing port to port addressing while sending and receiving messages,
and i have also explained in detail how to deploy this application to AWS using Elastic Beanstalk.

## Getting Started

Following are the details you need to run the project

### Prerequisites

What things you need to install the software and how to install them

```

NodeJS
AWS Account for deployment
Github for using the code in pipeline

```

### Installing

A step by step series of examples that tell you how to get a development env running

```
cd letschat
npm install

```

and then run the server on localhost port 

```
npm start

```

## Deployment Stage

Go to AWS console, create an application in Elastic BeanStalk by giving it a name and choosing the rest of the settings

Create an web server environment with a default name as Node-env and proceed with default and recommended settings

The application will be deployed after some time.

### Pipeline integration

Choose CodePipeline option in the Developer tools.
Create Pipeline , give it a name.
Choose source provider and connect to it using your credentials and proceed with default settings.
Choose your project repository and branch (let it be 'master')
Build Provider -> AWS CodeBuild (leace the optional part)
Choose the Application name you made in Elastic BeanStalk and also the environment you created.
Review your settings and create the pipeline.

### Advantage of using CodePipeline

Whenever there is a change in the code , you don't need to re-deploy the application again and again .

```
You just make the changes in the locally stored code and commit that to the github repository and it will be updated
on the deployed application within a minute.

```

## Built With

* [NodeJS] - The web framework used
* [Express]- Express framework
* [AWS Elastic Beanstalk] - Used to Deploy the Project
* [Socket.io]- Socket interface for chat functions
 

## Authors

* **Ankit** - *Student, Developer* - [Ankit](https://github.com/akharb1192)



## Acknowledgments

* Youtube tutorial on sockets in NodeJS 
* Youtube tutorial on AWS Elastic Beanstalk
