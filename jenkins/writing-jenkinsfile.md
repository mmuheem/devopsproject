# Infrastructure as Code - jenkinsfile

## What is Infrastructure as code (jenkinsfile) in the context of Jenkins

Usually we have a sequence of tasks to run when we build a software packege. In other words, we create a pipeline of tasks to be executed. This pipeline is called a build pipeline or CICD pipeline. If we write a piece of code in some DSL (Domain Specific Language), which can be versioned in any SCM system such as Git, that when executed in Jenkins actually runs the pipeline tasks then this code is called **Infrastructure as Code**. In Jenkins this is achieved through a plug-in called pipeline plug-in. This allows us to define the pipeline written in some DSL, such as groovy, which can be pushed to Git and versioned and can be executed in Jenkins. This script file is specifically known as **jenkinsfile**.
<br>
Check-out a sample jenkins file present in the cicddemo repository or in the demowebapp repository in this account.
<br>

## Steps to create a jenkinsfile
1. Craete a pipeline project in Jenkins e.g. demopipeline
2. Pipeline script editor opens in Jenkins. Select the **Pipeline Script** option in the drop down. we need this to write or modify the script
3. In the script, **node** refers to the slave node where the task/s would run that follows it and the **stages** refer to the tasks that run inside the scope of the node. Scope is defines with aset of curly braces
4. Take help of **Pipeline syntax** link given in the page to write groovy syntax of commonly used tasks. Copy and paste the generated code in the scope of the task in the build script
5. Save and execute the script
6. If tested OK, then copy the script and save the content in a file named **jenkinsfile**. Push this file to your Git repository
7. Now, open the Pipeline configuration again in Jenkins. This time, select the option to **SCM** (change it from **Pipeline  Script** option and provide the repository and branch details where the jenkinsfile is present (containing your build pipeline written as code)
8. Execute the pipeline. Note that this time, Jenkins gets the file from Git SCM and does what is instructed there
<br>

## Sample jenkinsfile
https://github.com/trainingport/mycoolwebapp/blob/master/Jenkinsfile
