# Create Org Hierarchy for a Sample Bank and load data in Envizi via Excel Template

This blog explains about creating an organization hierarchy with Groups, Sub Groups, Locations, and Accounts in Envizi via the Excel Templae. 

#### Authors
 [Jeya Gandhi Rajan M](https://community.ibm.com/community/user/envirintel/people/jeya-gandhi-rajan-m1), [Indira Kalagara](https://community.ibm.com/community/user/envirintel/people/indira-kumari-kalagara1), [Mamatha Venkatesh](https://community.ibm.com/community/user/envirintel/network/members/profile?UserKey=813a3553-d5cc-4b76-9970-ed40f865cb31)

## 1. Objective

The objective of this article is to create an organization hierarchy in IBM Envizi. Assuming that we have understanding of the Organization Hierarchy and defined a view like the one represented in the below screenshot. 

Now, Lets  create the hierarchy defined for example Bank in IBM Envizi.

<img src="../1-create-and-load-data/images/INBank_OrgHierarchy.png">


We can create the hierarchy through template and UI. Here we will take the Template approach. 

Below is the sequence of steps to be followed.

1.	Create Groups/Subgroups 
2.	Create Locations 
3.	Create Accounts
4.	View Hierarch in Envizi 
5.	Load data
6.	View data

In this exercise, let’s call our Bank as - ‘IN Bank’ and use the same name as a prefix for all subgroups, locations, accounts, etc. 



## 1. Create Groups / Subgroups

Let’s create groups which are identified in our Bank hierarchy. 

### a.	Prepare Groups 

  Update the Groups template as shown below by adding the values in corresponding columns. 

    Action: Create
    Group Type: Classification
    Belongs To: DemoCropD1 
    Group Name: IN Bank

Note: Save this file with the below naming conventions 
 Sheet / tab name: ‘Setup’
 
 File name : ‘Envizi_SetupGroups_xxxxxxx’
 Ex: Envizi_SetupGroups_INBank


<img src="images/1.ParentGroup.png">


### b.	Prepare Subgroups 

As per our Bank hierarchy, we have identified 2 levels of subgroups. Using the same groups template, lets create the 1st level subgroups by updating values in the required columns.

    Action: Create
    Group Type: Classification
    Belongs To: DemoCropD1 
    Part of Name: [Name of the Parent group]
    Group Name: [Name of the Subgroup]


Note: Save this file with the below naming conventions 
    Sheet / tab name: ‘Setup’ 

    File name is ‘Envizi_SetupGroups_xxxxxxx’
    
    Ex : Envizi_SetupGroups_Sub_INBank

<img src="images/2.SubGroup_L1.png">

Similarly, create the 2nd level subgroups identified in the Bank hierarchy. Keeping the rest of the values same, update the sheet for the columns Part of Name and Group Name relevant for the subgroups.

Note: Save this file with the below naming conventions 
    Sheet / tab name: ‘Setup’ 
    File name is ‘Envizi_SetupGroups_xxxxxxx’
    Ex: Envizi_SetupGroups_Sub_Sub_INBank

<img src="images/3.SubGroup_L2.png">

### c.	Upload 

Upload the excel files prepared above by navigate to Envizi UI -> Manage -> Upload Files 

<img src="images/4.UploadFiles.png">

On the Files Uploaded page, click on Create New and select the File. Good to provide Name as it would help to search in Files Processed page to check the status / any errors.

<img src="images/5.Files Processed.png">

Once Uploaded, navigate to Envizi UI -> Manage -> Files Processed to check the status of the file.  In case the File Status is Error, then please check the Load / Parse errors, resolve the same and upload the file again. 

To check errors, select the file -> Actions button -> Show Load errors / Parse errors.


Follow the upload procedure for all the Groups / 1st level and 2nd level subgroups. Once created, verify the groups from Envizi UI -> Manage -> Groups. 

<img src="images/6.GroupsEnvizi.png">

## 2. Create Locations

Let’s create locations from where the actual data is going to be captured. For example, locations where the ATMs, branches or corporate offices located for the Bank.  

Update the location template with the values in corresponding columns. 

    Action: Create
    Associate: Demo Corp D1
    Location Type: [Type of the location ex: ATM, Bank, Offices, Other etc]
    Location Name: [Name of the location]
    Country: [Country of the given location]
    Region: [state / province / region]
    Group Name: [Provide the group to which this location should be associated with]
    Group Associate: Demo Corp D1


Note: Save this file with the below naming conventions 

Sheet / tab name: ‘Setup’ 

File name is ‘Envizi_ SetupLocations_xxxxxxx’
Ex: Envizi_SetupLocations_INBank.xlsx


An example locations file looks like below.
<img src="images/7.Locations.png">


Upload the file by following the steps from 1.c 

Once uploaded, verify the locations created in Envizi UI -> Manage -> Locations. 
<img src="images/8.LocationsEnvizi.png">

## 3.	Create Accounts

Now we have all the groups created and associated the same with locations, the next step is to create the account for each of the data type which needs to be captured from that location.  Lets have a look at the hierarchy diagram, which represents what needs to be captured from each location / site. This is just an example set of data, just to give an understanding. 

Another important step here before looking at the Account template is, identifying the corresponding Accoutn styles for each of the data types.  To check on the available Account Styles, extract the Account Style Report from Envizi.


Update the Accounts template:

    Action: Create
    Associate: Demo Corp D1
    Location Name: [Name of the location to associate the account with]
    Account Style: [Provide the Account style related to the data type to be captured]
    Account Number: [Provide a unique name]


Note: Save this file with the below naming conventions 

Sheet / tab name: ‘Setup’ 

File name is ‘Envizi_ SetupAccounts_xxxxxxx’
Ex: Envizi_SetupAccounts_INBank.xlsx

<img src="images/9.Accounts.png">

Upload the file by following the steps from 1.c 

Once uploaded, verify the accounts created in Envizi UI -> Manage -> Accounts.

<img src="images/10.AccountsEnvizi.png">


## 4.	View Organization Hierarchy in Envizi

To view the entire hierarchy created through the above steps, navigate to Envizi UI -> Demo Corp D1 -> Classification groups -> IN Bank 

<img src="images/11.OrgHierarchyEnvizi.png">

## 5.	Load data

Now that we have the sample organization hierarchy created for an example Bank called IN Bank, lets also look at how to capture the data using bulk load approach via template. 


Update the Records template:

    Oganization: Demo Corp D1
    Location: [Name of the location to associate the account with]
    Account Style Caption : [Account style associated with the account to which the data is being loaded ] 
    Account Number: [Provide Account number]
    Date Format : YYYY-MM-DD
    Start Date: [Provide Start date of the data]
    End Date: [Provide Start date of the data]
    Qunatity: [Provide the value based on the units defined for the data type] 
    Total Cost: [Optional]

Note: Save this file with the below naming conventions 

Sheet / tab name: ‘Records to load 

File name is ‘Envizi_Universal_Data_xxxx’
Ex: Envizi_Universal_Data_INBank.xlsx

<img src="images/12.RecordsToLoad.png">

Upload the file by following the steps from 1.c 
 
## 6.	View data

As we have uploaded the data successfully to the accounts, lets look at the same from Envizi UI.
Navigate to Manage -> Accounts -> Select an Account -> Click on Account number 

Here is an example screenshot of Account Summary page
<img src="images/13.AccountSummary.png">

You can view the Records loaded at the bottom.  If you observe, we have loaded one record each for the year 2022 and year 2023 till May.  Envizi normalizes the data in monthly data format and provide the view as you see in the Summary page. You can also navigate to Monthly Data summary from Review -> Monthly Data for Account Summary page.

Also, you can view the Performance at the Account level by navigating to Track -> Performance

Here is the Emissions performance of an account.  

<img src="images/14.AccountPerformance.png">

Looking at the above screen, we can gain insights on whether the emissions are increasing or decreasing with respect to that account.  

Lets also look at the Emissions of a particular Branch. 
<img src="images/15.BranchPerformance.png">


Similarly, look at the overall Bank performance.

<img src="images/16.BankPerformance.png">


## Conclusion:
In this article, we have tried to provide holistic view on organization hierarchy by taking an example Bank. For this example bank, we have identified groups /subgroups / locations / data to be captured and  created all of those using the excel templates . Also loaded data into the accounts and able to view the insights by looking emission performance dashboard starting at granular level like accounts, specific branch level and at overall bank. 

