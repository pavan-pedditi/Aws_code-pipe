	Hi 👋, I'm pavan
 
 	Today i am here to demonstrate how i worked on AWS Continuous Integration & continous deployment. (Github, Aws-codebuild, Aws-codepipe, Aws-codedeploy)


![git](https://github.com/pavan-pedditi/Aws_code-pipe/assets/162891338/e1d824b9-af19-4180-9f5b-bb889b9127cb)

 	
 	Step-1:-
	Create an AWS CodePipeline:

	In this step, we'll create an AWS CodePipeline to automate the continuous integration process for our Python application. AWS CodePipeline 	will orchestrate the flow of changes from our 
        GitHub repository to the deployment of our application. Let's go ahead and set it up:

	1.Go to the AWS Management Console and navigate to the AWS CodePipeline service.
	2.Click on the "Create pipeline" button.
	3.Provide a name for your pipeline and click on the "Next" button.
	4.For the source stage, select "GitHub" as the source provider.
	5.Connect your GitHub account to AWS CodePipeline and select your repository.
	6.Choose the branch you want to use for your pipeline.
	7.In the build stage, select "AWS CodeBuild" as the build provider.
	8.Create a new CodeBuild project by clicking on the "Create project" button.
	9.Configure the CodeBuild project with the necessary settings for your Python application, such as the build environment, build commands, 	and artifacts.
	10.Save the CodeBuild project and go back to CodePipeline.
	
 
	Continue configuring the pipeline stages, such as deploying your application using AWS Elastic Beanstalk or any other suitable deployment 	option.
	.

 ![pipe-created](https://github.com/pavan-pedditi/Aws_code-pipe/assets/162891338/067e4125-4c61-4f0a-b66a-51ac1a6c9eb9)

	Review the pipeline configuration and click on the "Create pipeline" button to create your AWS CodePipeline.
	Awesome Let's move on to the next step to set up AWS CodeBuild
 
 	Step-2:-
	Configure AWS CodeBuild:

	In this step, we'll configure AWS CodeBuild to build our Python application based on the specifications we define. CodeBuild will take care 	of building and packaging our application for 	deployment. Follow these steps:

	1.In the AWS Management Console, navigate to the AWS CodeBuild service.
	2.Click on the "Create build project" button.
	3.Provide a name for your build project.
	4.For the source provider, choose "AWS CodePipeline."
	5.Select the pipeline you created in the previous step.
	6.Configure the build environment, such as the operating system, runtime, and compute resources required for your Python application.
	7.Specify the build commands, such as installing dependencies and running tests. Customize this based on your application's requirements.
	8.Set up the artifacts configuration to generate the build output required for deployment.
	9.Review the build project settings and click on the "Create build project" button to create your AWS CodeBuild project.
 	we're now ready to witness the magic of continuous integration in action.
  ![Build_sucess-pipe](https://github.com/pavan-pedditi/Aws_code-pipe/assets/162891338/2995bce2-fbbb-41aa-a2b8-b08840869e99)

 	Step-3:-
  	Make Ec2 as agent:
	
 	1.Create Ec2 instance
  	2.Add tag and change IAM Role
   	3.follow the steps provide https://docs.aws.amazon.com/codedeploy/latest/userguide/codedeploy-agent-operations-install-ubuntu.html 
    	4.After these steps you will create agent to deploy
     
   	Step-4:-
    	Configure AWS Codedeploy:
     	
       In this step, we'll configure AWS Codedeploy to deploy our Python application based on the specifications we define. Codedeploy will take care of deploying our app to ec2 instance. 
       Follow these steps

       1.In the AWS Management Console, navigate to the AWS CodeDeploy service
       2.Go to applications and create application by giving name and Ec2
       3.create deployment groups by giving application by giving deployment group name and slecting ec2
       4.create deployment by selecting deployment group
![deployment completed finally](https://github.com/pavan-pedditi/Aws_code-pipe/assets/162891338/256a46cf-1553-4959-9f35-fc9ef3b7932f)


       Trigger the CICD Process, In this final step, we'll trigger the CICD process by making a change to our GitHub repository.

	You should see the pipeline automatically kick off as soon as it detects the changes in your repository.
	Sit back and relax while AWS CodePipeline takes care of the rest. It will fetch the latest code, trigger the build process with AWS 		CodeBuild, and deploy the application configured in the deployment stage.
	
![Source and build succeded](https://github.com/pavan-pedditi/Aws_code-pipe/assets/162891338/c47962eb-8b76-4530-a021-01cfafa23de6)
![build and code-deploy suceeded](https://github.com/pavan-pedditi/Aws_code-pipe/assets/162891338/064eba52-6f3d-4516-b0c6-0038b24cdd43)

 	
