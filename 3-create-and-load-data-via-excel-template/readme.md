# Create Org Hierarchy and load data in Envizi via Excel Template

This article explains about creating Org Hierarchy with Groups, Sub Groups, Locations, and Accounts in Envizi via the Excel Templae. 

#### Authors
 [Jeya Gandhi Rajan M](https://community.ibm.com/community/user/envirintel/people/jeya-gandhi-rajan-m1), [Indira Kalagara](https://community.ibm.com/community/user/envirintel/people/indira-kumari-kalagara1), [Mamatha Venkatesh](https://community.ibm.com/community/user/envirintel/network/members/profile?UserKey=813a3553-d5cc-4b76-9970-ed40f865cb31)

## 1. Objective

The objective of this blog is to create an Org Hierarchy as like the below with a group, sub groups, locations and accounts through Excel template upload. Then load some sample data into the accounts and view the Account Summary.

<img src="images/09-target.png">

## 2. Excel Data 

Here is the structure of the various excel template available in Envizi to upload files.

#### Group

Here is the excel template to create `Group`.

1. The below columns needs to be filled in.
- Action : It can be `Create` or `Update` based on whether you create a new Group or updating the existing group.
- Group Type: `Classification`
- Belongs To: The Organization name of this group.
- Group Name: Name of the group that we are going to create.

2. The name of the sheet should be `Setup`

3. File name of the excel should be `Envizi_SetupGroups_XXXXXX.xlsx`

<img src="images/10-excel-1.png">

#### SubGroup

Here is the excel template to create `Sub Group`.

1. The below columns needs to be filled in.
- Action : `Create` or `Update`.
- Group Type : `Classification`
- Belongs To : The Organization name of this group.
- Part of Name : The parent group name.
- Group Name : Name of the subgroup that is going to be created.

2. The name of the sheet should be `Setup`

3. File name of the excel should be `Envizi_SetupGroups_XXXXXX.xlsx`

<img src="images/10-excel-2.png">

#### Location

Here is the excel template to create `Location`.

1. The below columns needs to be filled in.
- Action : `Create` or `Update`.
- Associate : The Organization name of this location.
- Location Name : Name of the location that is going to be created.
- Country: Country where the location belongs to.
- Region: Region where the location belongs to.
- Group Name : Name of the group/subgroup under which the location is going to get created.
- Group Associate : The Organization name of this Group.

2. The name of the sheet should be `Setup`

3. File name of the excel should be `Envizi_SetupLocations_XXXXXX.xlsx`


<img src="images/10-excel-3.png">

#### Account

Here is the excel template to create `Account`.

1. The below columns needs to be filled in.
- Action : `Create` or `Update`.
- Associate : Name of the subgroup that is going to be created.
- Location Name : Name of the location under which this account is going to get created.
- Account Style : `Account Style Name` from  `Account Style Extract` report. Or the `Account Style Name` from  `Universal Data Template`  given in the below section.
- Account Number : Name of the account that is going to be created.

2. The name of the sheet should be `Setup`

3. File name of the excel should be `Envizi_SetupAccounts_XXXXXX.xlsx`

<img src="images/10-excel-4.png">

#### Account Style

The below picture shows the Account Style extact as part of the `Universal Data Template`.

Here the `Account Style Name` and `Account Style Caption` and other columns values are taken from the `Account Style Extract` report.

This will be used during the `Data` loading.

<img src="images/10-excel-4.png">

<img src="images/10-excel-5.png">

#### Data

Here is the excel template to load `Data`.

1. The below columns needs to be filled in.
- Organization : The Organization name of this data.
- Location : Name of the location under which the account is available.
- Account Style Caption : `Account Style Caption` from `Supported account style` sheet of this `Universal Data Template`. This should be equivalent to the  `Account Style Name` of the Account.
- Account Number : Name of the account to which the data is going to loaded.
- Start Date : Start date of the data
- End Date : End date of the data
- Qty : Qty of the data
- Total Cost : Total cost of the data

2. The name of the sheet should be `Records to load`

3. File name of the excel should be `Envizi_Universal_Data_XXXXXX.xlsx`

<img src="images/10-excel-6.png">

#### Sample Template

Sample excel Template is available based on the request.

## 3. Create Group

Let us create a Group

### Upload excel

1. Click on `Manage > Upload files`

<img src="images/11-group-11.png">

2. Click on `Create new file upload`

<img src="images/11-group-12.png">

3. Enter some values for `Name` and `Description`

4. Upload the `Envizi_SetupGroups_XXXXXX.xlsx` file created above.

5. Click on `Save`

<img src="images/11-group-13.png">

Files get uploaded.

<img src="images/11-group-14.png">

6. Click on `Manage > Files Processed - Accounts & Setup`

<img src="images/11-group-15.png">

Files get processed.

<img src="images/11-group-16.png">

### View Group

1. Click on `Manage > Groups`

<img src="images/11-group-17.png">

2. Type `G7` in Name search. 

You can view the created Group.

<img src="images/11-group-18.png">

## 4. Create Sub Group

Let us create Sub Groups

### Upload excel

1. Upload the file as like the above.

<img src="images/12-subgroup-1.png">

<img src="images/12-subgroup-2.png">

<img src="images/12-subgroup-3.png">

### View Group

1. View the created groups as like the above.

<img src="images/12-subgroup-4.png">

## 5. Create Location

Let us create locations.

### Upload excel

1. Upload the file as like the above.

<img src="images/13-location-1.png">

<img src="images/13-location-2.png">

<img src="images/13-location-3.png">

### View Location

1. View the created locations as like the above.

<img src="images/13-location-4.png">

<img src="images/13-location-5.png">

### View Location in Org Hierarchy

1. View the Location in the Org Hiearchy. 

Before associating the location with the group the Group and SubGroups are not visible in the Hierarchy.

<img src="images/13-location-6.png">

## 6. Create Account

Let us create accounts.

### Upload excel

1. Upload the file as like the above.

<img src="images/14-account-1.png">

<img src="images/14-account-2.png">

### View Account

1. View the created accounts as like the above.

<img src="images/14-account-3.png">

<img src="images/14-account-4.png">

### View Account in Org Hierarchy

1. View the Account in the Org Hiearchy. 

<img src="images/14-account-5.png">

## 7. Load Data

Let us load data.

### Upload excel

1. Upload the file as like the above.

<img src="images/15-data-1.png">

<img src="images/15-data-2.png">

### View Data

1. Goto the Org Hiearchy and click on the account

<img src="images/15-data-3.png">

Account summary page get displayed.

This account summary page shows the data type as `Electricity`.

<img src="images/15-data-4.png">
<img src="images/15-data-5.png">

This account summary page shows the data type as `Water`.

<img src="images/15-data-6.png">
<img src="images/15-data-7.png">


## 7. Troubleshooting

You can troubleshoot the error during the file upload.

### View the Parser Error or Load Error

1. Click on `Manage > Files Processed - Accounts & Setup`

2. Select a record

3. Click on `Actions > Show Load Errors`

<img src="images/16-error-1.png">

4. Click on `Actions > Show Parse Errors`

<img src="images/16-error-2.png">
