# SFDX for Non-Scratch Orgs


### Scratch Org Based Development

If we are starting a new Project, then the recommendation is to use the "Scratch Org based Development" Model . [or] Small projects which can be easily converted into DX Format.

![image](https://user-images.githubusercontent.com/2145211/48164153-b47c4f80-e2af-11e8-91bd-c74b9c009198.png)

- Let's say we have code in the GIT Repository (For Existing Org based Development)
- Convert the existing code in the GIT Repository to SFDX Format (This can be done using the CLI)
- Understand the Features we are using to create correct Org Shape (For Scratch Orgs)
- Understanding and Scripting all the features or additional customization so that those can be applied to scratch orgs.
- Scripting sample data which needed to be pushed to scratch orgs for development
- CLI Provides commands such as "force:source:pull" and "force:source:push"

### Change-Set Based Development

![image](https://user-images.githubusercontent.com/2145211/48164994-3b322c00-e2b2-11e8-878c-31cbe6c847d7.png)

- Each Dev Org can be assigned to each developer. Easy to refresh from Production.
- Most common defined model.


### Using SFDX CLI for Change-set Based Development

### Difference between SFDX Format from Traditional Format

- Static Resources are uncompressed in DX, so that we can edit it
- Lightning Bundles and components must reside in a directory named "Aura"
- Documents organized inside its folder directory
- Object Metadata is further organized into sub-directories
  - businessProcess
  - compactLayouts
  - fields
  - fieldSets
  - listViews
  - recordTypes
  - sharingReasons
  - ValidationRules
  - webLinks

![image](https://user-images.githubusercontent.com/2145211/48174775-5a8f8000-e2d7-11e8-9212-ff90cf564151.png)

### Winter '19 Salesforce Source Commands (Retrieve, Deploy and Delete)

### Retrieve Commands

```
sfdx force:source:retrieve -x path/to/package.xml
sfdx force:source:retrieve -m CustomObject,ApexClass
```

### Deploy Commands

```
sfdx force:source:deploy -x path/to/package.xml
sfdx force:source:deploy -m ApexClass:MyApexClass
```
















