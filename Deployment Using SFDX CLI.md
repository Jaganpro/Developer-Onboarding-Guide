## Deployment Steps

### Install Salesforce CLI
  * For detailed steps, please refer the link below:
  * https://github.com/Jaganpro/Developer-Onboarding-Guide/blob/master/README.md
  
### Authenticate all Sandbox and Production Orgs
  * For Brevity, lets assume that we are moving code from Dev Sandbox to UAT Sandbox
      * Dev Sandbox - Dev (Source)
      * UAT Sandbox - UAT (Destination)
  * Here in this scenario, we are assuming that both the orgs are authenticated in SFDX CLI.
  
### Folder Creation
  * Lets create the following folders to support deployment
      * PackageXML
      * Retrieve
      * Deploy
      
### Retrieve Components from Source Org
  * `sfdx force:mdapi:retrieve -u Dev -s -k ./PackageXML/Package.xml -r ./Retrieve`
    * -s --> Single Package
    * -k --> Location of Package.xml
    * -r --> Location where we want `unpackaged.zip` file needs to be saved
    
### Unzip Contents and Move it to Deploy Folder
  * `unzip ./Retrieve/unpackaged.zip -d ./Deploy`
    * -d --> Destination Directory
    
### Deploy to Destination Org
  * `sfdx force:mdapi:deploy -u UAT -d ./Deploy -l NoTestRun -c`
    * -u --> Org Name
    * -d --> Root of directory tree of files to deploy 
    * -c --> Check Only (Use this flag to Validate the deployment) 
    * -l --> testLevel (NoTestRun, RunSpecifiedTests, RunLocalTests, RunAllTestsInOrg)
    
### Check Deployment Status
  * `sfdx force:mdapi:deploy:report -i <JobID>`
    * -i --> Job ID reference we get from Salesforce when we try to deploy
    
