## Deployment using SFDX  

### Set up Salesforce CLI

1.	Download and install Salesforce CLI from https://developer.salesforce.com/tools/sfdxcli
2.	Set the PATH environment system variable as shown below

![image](https://user-images.githubusercontent.com/2145211/64368341-16006e00-cfe8-11e9-8a2d-3f97308e772b.png)

### Deployment to CLI

1.	Open Command Prompt
2.	Type “sfdx” to test if SFDX is properly installed

3.	Type the below command to authenticate the source and Destination Org

* sfdx force:auth:web:login -r https://test.salesforce.com -a <Name Of the Org>

* Example – if we are moving code from QA to UAT then the command would be 
* sfdx force:auth:web:login -r https://test.salesforce.com -a QA
* sfdx force:auth:web:login -r https://test.salesforce.com -a UAT

4.	Create 3 Folders to support the deployment
    a.	PackageXML
    b.	Retrieve
    c.	Deploy
5.	Place the package.xml in the PackageXML folder
6.	Use the below command to retrieve the components from Source ORG
* sfdx force:mdapi:retrieve -u QA -s -k ./PackageXML/Package.xml -r ./Retrieve

* Example –
* sfdx force:mdapi:retrieve -u QA -s -k  "C:\Users\jag\Desktop\Work\Software\SFDX\PACKAGEXML\Package.xml" -r "C:\Users\jag\Desktop\Work\Software\SFDX\Retrieve"

7.	Unzip the contents of the unpackaged.zip to the Deploy folder
8.	To validate the package (includes Run Local Tests)
* sfdx force:mdapi:deploy -u UAT -d ./Deploy -l RunLocalTests –c

* Example - 
* sfdx force:mdapi:deploy -u UAT -d 
* "C:\Users\jag\Desktop\Work\Software\SFDX\Deploy" -l RunLocalTests –c

9.	To deploy the package (includes Run Local Tests)

* sfdx force:mdapi:deploy -u UAT -d 
* "C:\Users\jag\Desktop\Work\Software\SFDX\Deploy" -l RunLocalTests

