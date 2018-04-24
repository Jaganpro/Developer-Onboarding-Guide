# Developer-Onboarding-Guide

## IDEs and Plugins Setup for Salesforce Development 

### STEP 1: Installing Salesforce IDE
  * Go to https://code.visualstudio.com/Download to download Visual Studio Code IDE

  ![image](https://user-images.githubusercontent.com/2145211/39125629-9ae9a122-46cd-11e8-8592-6eb1ed00acd2.png)
  
### STEP 2: Search Extensions:MarketPlace for Salesforce Plugins
  * Once installed, Open Visual Studio code and navigate to "Extensions: MarketPlace" and search for "Salesforce"
  
  ![image](https://user-images.githubusercontent.com/2145211/39138227-7cd46d46-46ed-11e8-95f2-27b564a4c790.png)
  
### STEP 3: Install Salesforce Plugins
  * Install "Visual Studio Code Extension Pack for Salesforce DX"
  * Once Installed, we should be able to see the list of packages installed in Visual Studio
  
  ![image](https://user-images.githubusercontent.com/2145211/39137921-ca7de546-46ec-11e8-87de-d0ca74b995d2.png)

### STEP 4: Install Mavensmate Plugin (For Non-SFDX Projects)
  * Add VS Code to Path (Run Shell Command : Install code in PATH from command palette)
  * Install MavensMate Desktop Beta.6 (must be running in order for MavensMate for VS Code to function)
    * Install Link: https://github.com/joeferraro/MavensMate-Desktop/releases/tag/v0.0.11-beta.6
    * Once Installed, configure your workspace
      * "mm_workspace" : "/Users/YourUserName/Desktop/my-cool-project-name"
  * Search for "Mavensmate" and install the plugin in Visual Studio Code
  
  ![image](https://user-images.githubusercontent.com/2145211/39139406-d4f07144-46ef-11e8-86dd-1ab09a0bfba2.png)
  
### STEP 5: Install Node and NPM
  * Install NODE and NPM for your mac and Windows
  * Go to https://nodejs.org/en/ and click download. Please download the latest stable release.
  
  ![image](https://user-images.githubusercontent.com/2145211/39145523-fbc9ffbc-4701-11e8-9ec3-e2270a4fec27.png)
  
  * Once Installed, you should be able to see the following Messages
  
  ![image](https://user-images.githubusercontent.com/2145211/39145533-05808fe4-4702-11e8-8349-15880a0506bb.png)
  
### STEP 6: Install Salesforce CLI 
  * Go to https://developer.salesforce.com/tools/sfdxcli to Install Salesforce CLI
  
  ![image](https://user-images.githubusercontent.com/2145211/39145544-0e9313cc-4702-11e8-9863-6c9da9b2abcc.png)

### STEP 7: Tools Verification
  * Once Installed, Verify that you have NODE, NPM and Salesforce CLI Installed Correctly.
  
  ![image](https://user-images.githubusercontent.com/2145211/39145552-1827ca54-4702-11e8-83c9-61e5730708e8.png)

### STEP 8: Enable Developer Hub (One-Time Setup Only - By Admin) (Optional)
  * Enable Developer Hub in Production
  * Once Enabled, Developers needs to be a user in Production to create Scratch Orgs
  * The following Permission-Set features needs to be assigned for the users in Production:
    * Scratch Org Info
    * Active Scratch Org
    * NameSpace Registry
    
  ![image](https://user-images.githubusercontent.com/2145211/39145567-21b6dc7c-4702-11e8-9268-a999a0ef4b9b.png)

### Step 9: Configure Git
  * Make sure we configure git credentials in our System
    * Setup UserName
    * Setup Email Addresses
    
  ![image](https://user-images.githubusercontent.com/2145211/39145646-65ea7ee4-4702-11e8-8774-1011df8d7d49.png)
  
## Daily Cadence for Developers
  * <More Updates to follow>


  
