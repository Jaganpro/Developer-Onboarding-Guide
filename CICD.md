## Simplify Continuous Integration and Delivery Pipelines

![image](https://user-images.githubusercontent.com/2145211/64477543-de6dff00-d16a-11e9-8693-af2dc79f05a4.png)


* There are 2 types of development

![image](https://user-images.githubusercontent.com/2145211/64477563-08bfbc80-d16b-11e9-8280-f4406591a0d0.png)

* We are going to discuss about the Package based Development and what CI/CD looks like

![image](https://user-images.githubusercontent.com/2145211/64477782-a1efd280-d16d-11e9-9b80-a648bcb0de33.png)

* Advantages of CI/CD

![image](https://user-images.githubusercontent.com/2145211/64477801-d6638e80-d16d-11e9-9e64-fe0c95f41f22.png)

* CI/CD Workflow

![image](https://user-images.githubusercontent.com/2145211/64478240-9acbc300-d173-11e9-9031-bd4268c8c3a1.png)

![image](https://user-images.githubusercontent.com/2145211/64478274-13328400-d174-11e9-9915-1628268f4fc3.png)


### GitLab

![image](https://user-images.githubusercontent.com/2145211/64478292-568cf280-d174-11e9-8353-643269f2d95d.png)


### Demo

![image](https://user-images.githubusercontent.com/2145211/64478331-f480bd00-d174-11e9-8b6c-e51e428f1750.png)

* Step 1: Get the Salesforce Studio Project Checked out
* Step 2: Make sure we have the Salesforce Extension Pack using the Visual Studio Code
* Step 3: Now, lets make sure that we have our GitLab Signed-In

![image](https://user-images.githubusercontent.com/2145211/64478358-6bb65100-d175-11e9-8d52-fbbbc0b15668.png)

NOTE: Gitlab has created a special SFDX template

![image](https://user-images.githubusercontent.com/2145211/64478363-943e4b00-d175-11e9-97fd-3fdf8eca847a.png)

* Lets pick the "sfdx-project-template" (Available freely to Public) and clone the URL and create a new Project

![image](https://user-images.githubusercontent.com/2145211/64478397-cfd91500-d175-11e9-9e76-5b5023352f9d.png)

* Create a new Project

![image](https://user-images.githubusercontent.com/2145211/64478405-f1d29780-d175-11e9-9655-a8833c998ab8.png)

* There are several ways to create a Project such as importing an existing project

![image](https://user-images.githubusercontent.com/2145211/64478409-10d12980-d176-11e9-8b08-2929bcc12aae.png)

* Here in our example, we are using "Get Repo by URL"

![image](https://user-images.githubusercontent.com/2145211/64478499-50e4dc00-d177-11e9-978e-08539df62033.png)

* Now, once the project is created, it contains Gitlab CI YAML file to all the CI and CD automation

![image](https://user-images.githubusercontent.com/2145211/64478507-69ed8d00-d177-11e9-8ab4-885cec184513.png)

![image](https://user-images.githubusercontent.com/2145211/64478572-19c2fa80-d178-11e9-8a68-22706aa9e85e.png)

* Since we are using the Salesforce Template, we automatically get
   * Unit Testing
   * Review before deployment
   * Apex Testing
   * Static Application Security Testing
   * Deployment to both Sandbox and Production Orgs


* Now, we need to provide some configuration variables for this to work.
* This is because we want to know what Salesforce Orgs and DevHubs the CI is going to use. 

![image](https://user-images.githubusercontent.com/2145211/64478621-9eae1400-d178-11e9-8876-8a6682fba38e.png)

* NOTE: We have use the --verbose command in the SFDX to get the Auth URL for Production, DevHub etc..

![image](https://user-images.githubusercontent.com/2145211/64478670-7377f480-d179-11e9-8622-54e3d7af6efa.png)

* This is all we need for the piplines to Authenticate into Orgs

* Next, we want to add the name of the Package in sfdx-project.json

![image](https://user-images.githubusercontent.com/2145211/64478688-db2e3f80-d179-11e9-9677-c639cdbfa9b4.png)

* Now, lets say that we want to add a new feature, lets go to the Board

![image](https://user-images.githubusercontent.com/2145211/64478711-2a747000-d17a-11e9-8ee0-483908f3f5ac.png)

* Now, we are going to create the "Create Merge" request button

![image](https://user-images.githubusercontent.com/2145211/64478717-45df7b00-d17a-11e9-83ea-d2eafb80e918.png)

* What this does, is magic
  * It creates a new branch in git for that issue
  * It also creates a new merge request to track the work on that branch, to have a place for 
    * Code Review
    * Security Scan
    * Comments about this feature
    * Unit Testing, everything that is related to that feature
    
* Now, we want to go back to the Visual Studio Code and check out that Branch

![image](https://user-images.githubusercontent.com/2145211/64479042-3ca4dd00-d17f-11e9-9331-b85ae0acb41e.png)

* As soon as this is done, now, we will be working in that feature branch

![image](https://user-images.githubusercontent.com/2145211/64479047-4e868000-d17f-11e9-97f9-e495ecd9bab4.png)











