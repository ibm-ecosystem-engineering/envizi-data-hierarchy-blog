# Create Org Hierarchy and load data in Envizi via UI

This blog explains about creating Org Hierarchy with Groups, Sub Groups, Locations, and Accounts in Envizi via the UI console. Also it explains about loading data into the accounts and view the emissions details.

## Contents

- [1. Create Group and SubGroup](#1-Create-Group-and-SubGroup)
- [2. Create Location](#2-Create-Location)
- [3. Create Account ](#3-Create-Account)
- [4. Group Summary Before loading Data ](#4-Group-Summary-Before-loading-Data)
- [5. Location Details ](#5-Location-Details)
- [6. Load Account data ](#6-Load-Account-data)
- [7. Location Performance ](#7-Location-Performance)
- [8. Account Summary ](#8-Account-Summary)
- [9. Load Account data 2 ](#9-Load-Account-data-2)
- [10. Load Account data 3 ](#10-Load-Account-data-3)


## Objective

The objective of this blog is to create an Org Hierarchy as like the below with a group, 2 sub groups, 4 locations and 6 accounts through the Envizi console UI. Then load some sample data into the accounts and view the Account Summary and emissions details.

<img src="images/00-org-hiearchy.png">

## 1. Create Group and SubGroup

### 1.1 Create Group

1. Click on `Manage > Groups` 
<img src="images/01-group1.png">

It shows the Groups page.

2. Click on `Create New Group` button.

<img src="images/01-group2.png">

3. Fill in the details as below. 

- Group Type :  `Classification`
- Belongs To : The Org name of the account. Here `Demo Corp D1`
- Name :  Give any name for the Group. Ex: `G1-Telco`
- Report Percent :  100

4. Click on `Save` button.
<img src="images/01-group3.png">

A new Group called `G1-Telco` got created.
<img src="images/01-group4.png">

### 1.2 Create Sub Group 1

Here are we are going to create a new SubGroup called `G1-Telco-CellTowers` under the group `G1-Telco`

1. Fill in the details as below. 

- Group Type :  `Classification`
- Belongs To : The Org name of the account. Here `Demo Corp D1`
- Part Of :  `G1-Telco` (the parent group)
- Name :  Give any name for the Group. Ex: `G1-Telco-CellTowers`
- Report Percent :  100

2. Click on `Save` button.

<img src="images/01-group5.png">

A new Sub Group called `G1-Telco-CellTowers` got created.

<img src="images/01-group6.png">

### 1.3 Create Sub Group 2

Here are we are going to create a new SubGroup called `G1-Telco-DataCentres` under the group `G1-Telco`

1. Fill in the details as below. 

- Part Of :  `G1-Telco` (the parent group)
- Name :  Give any name for the Group. Ex: `G1-Telco-DataCentres`

<img src="images/01-group7.png">

A new Sub Group called `G1-Telco-DataCentres` got created.

<img src="images/01-group8.png">

## 2. Create Location

We are going to create 4 locations.

### 2.1 Create Location 1

1. Click on `Manage > Locations` 
<img src="images/02-location11.png">

It shows the Locations page.

2. Click on `Create New Location` button.

<img src="images/02-location12.png">

3. Fill in the details as below. 

- Location Type :  `Cell Tower`
- Name :  Give any name for the Location. Ex: `G1-Tower-2000`
- Country :  `United States`
- Region :  `illinois : state United States`
- Group :  Choose the sub group created before. Ex:  `G1-Telco-CellTowers`

4. Click on `Save` button.

<img src="images/02-location13.png">
<img src="images/02-location14.png">

A new Location called `G1-Towers-2000` got created.
<img src="images/02-location15.png">

### 2.2 Create Location 2

Similarly create a new location called `G1-Tower-2001` under the group  `G1-Telco-CellTowers`

<img src="images/02-location16.png">
<img src="images/02-location17.png">

### 2.3 Create Location 3

Similarly create a new location called `G1-DC-2000` under the group  `G1-Telco-DataCenters`

<img src="images/02-location18.png">
<img src="images/02-location19.png">

### 2.3 Create Location 4

Similarly create a new location called `G1-DC-2001` under the group  `G1-Telco-DataCenters`

<img src="images/02-location21.png">
<img src="images/02-location22.png">

### 2.4 Location List

All the above crated Locations got listed here.

<img src="images/02-location23.png">

## 3. Create Account

We are going to create 6 Accounts.

### 3.1 Create Account 1

1. Click on `Manage > Account` 
<img src="images/03-account11.png">

It shows the Account page.

2. Click on `Create New Account` button.

<img src="images/03-account12.png">

3. Fill in the details as below. 

- Location : Choose the above created location. Ex: `G1-Tower-2000`
- Account Style :  Choose an electricy type : `Electricity - Total kWh and Cost`
- Name :  Give any name for the Group. Ex: `G1-Tower-2000-Elec-01`

4. Click on `Save` button.

<img src="images/03-account13.png">

A new Account called `Electricity - Total kWh and Cost` got created under the location `G1-Tower-2000`
<img src="images/03-account14.png">

The newly created account looks like this in the Org Hiearchy section

<img src="images/03-account15.png">

### 3.2 Create Account 2

1. Fill in the details as below. 

- Location : Choose the above created location. Ex: `G1-Tower-2001`
- Account Style :  Choose an electricy type : `Electricity - Total kWh and Cost`
- Name :  Give any name for the Group. Ex: `G1-Tower-2001-Elec-01`

<img src="images/03-account16.png">

2. Click on `Save` button.

### 3.3 Create Account 3

1. Fill in the details as below. 

- Location : Choose the above created location. Ex: `G1-DC-2000`
- Account Style :  Choose an electricy type : `Electricity - Total kWh and Cost`
- Name :  Give any name for the Group. Ex: `G1-DC-2000-Elec-01`

<img src="images/03-account17.png">

2. Click on `Save` button.

### 3.4 Create Account 4

1. Fill in the details as below. 

- Location : Choose the above created location. Ex: `G1-DC-2001`
- Account Style :  Choose an electricy type : `Electricity - Total kWh and Cost`
- Name :  Give any name for the Group. Ex: `G1-DC-2001-Elec-01`

<img src="images/03-account18.png">

2. Click on `Save` button.


### 3.5 Create Account 5

1. Fill in the details as below. 

- Location : Choose the above created location. Ex: `G1-DC-2000`
- Account Style :  Choose an electricy type : `Diesel Transport - miles`
- Name :  Give any name for the Group. Ex: `G1-DC-2000-Diesel-01`

<img src="images/03-account19.png">

2. Click on `Save` button.


### 3.6 Create Account 6

1. Fill in the details as below. 

- Location : Choose the above created location. Ex: `G1-DC-2001`
- Account Style :  Choose an electricy type : `Diesel Transport - miles`
- Name :  Give any name for the Group. Ex: `G1-DC-2001-Diesel-01`

<img src="images/03-account20.png">

2. Click on `Save` button.


### 3.7 Account List

All the above created Accounts got listed here..

<img src="images/03-account21.png">


#### 3.8 Org Hiearchy 

Here is the Org hiearchy showing the above created accounts under the corresponding locations.

<img src="images/03-account22.png">


## 4. Group Summary Before loading Data

Here is the group summary of the above created group `G1-Telco`. before loading the data.

<img src="images/04-group-summary.png">

## 5. Location Details

Here is the location details of the above created location `G1-DC-2000` that shows emissions data as empty. 

<img src="images/05-location-detail1.png">
<img src="images/05-location-detail2.png">
<img src="images/05-location-detail3.png">
<img src="images/05-location-detail4.png">
<img src="images/05-location-detail5.png">

## 6. Load Account data

1. Select the account from the left panel. 

<img src="images/06-load-account-data11.png">

Account summary get displayed as below.

2. Click on `Track > Records` 

<img src="images/06-load-account-data12.png">

3. Click on `Capture > Data` 

<img src="images/06-load-account-data13.png">

4. Fill in the details as below. 
- Start Period : Enter the starting period of the data
- End Period : Enter the ending period of the data
- Total Electricity :  Enter the total electricity
- Total Cost :  Enter the total cost

The total value would split across each month available in between the given period.

5. Click on `Save` button.

<img src="images/06-load-account-data14.png">

The record saved successfuly as below.

6. Click on `Monthly Data` button.

<img src="images/06-load-account-data15.png">

The total value split across each month is shown here.

<img src="images/06-load-account-data16.png">
<img src="images/06-load-account-data17.png">

## 7. Location Performance

1. Open the location `G1-DC-2000` from the Org Hierarchy.

2. Click on the `Performance` menu.

<img src="images/07-location-performance1.png">

The location performance details is displayed.
<img src="images/07-location-performance2.png">
<img src="images/07-location-performance3.png">
</details>

## 8. Account Summary

1. Open the Account `G1-DC-2000-Elec-01` from the Org Hierarchy.

<img src="images/08-account-summary1.png">

The `Account Summary` page is displayed.

<img src="images/08-account-summary2.png">
<img src="images/08-account-summary3.png">

## 9. Load Account data 2

1. Open the Account from the Org Hierarchy.

<img src="images/09-load-account-data11.png">

2. Click on the `Actions > Capture Data` menu.

<img src="images/09-load-account-data12.png">

3. Fill in the details as below. 
- Start Period : Enter the starting period of the data
- End Period : Enter the ending period of the data
- Distance Travelled :  Enter the distance travelled
- Total Cost :  Enter the total cost

4. Click on `Save` button.

<img src="images/09-load-account-data13.png">

The data is saved and here is the `Account Summary` details.

5. Click on `Records` button.

<img src="images/09-load-account-data14.png">
<img src="images/09-load-account-data15.png">

The `Records` list is displayed.
<img src="images/09-load-account-data16.png">

6. Click on `Monthly Data` button.

The `Monthly Data` list is displayed.

<img src="images/09-load-account-data17.png">
<img src="images/09-load-account-data18.png">

## 10. Load Account data 3

1. Open the Account from the Org Hierarchy.

<img src="images/10-load-account-data11.png">

2. Click on the `Actions > Capture Data` menu.

<img src="images/10-load-account-data12.png">

3. Fill in the details as below. 
- Start Period : Enter the starting period of the data
- End Period : Enter the ending period of the data
- Total Electricity :  Enter the total electricity value
- Total Cost :  Enter the total cost

4. Click on `Save` button.

<img src="images/10-load-account-data13.png">

The data is saved and here is the `Account Summary` details.

5. Click on `Records` button.

<img src="images/10-load-account-data14.png">
<img src="images/10-load-account-data15.png">

The `Records` list is displayed.

<img src="images/10-load-account-data16.png">

6. Click on `Monthly Data` button.

The `Monthly Data` list is displayed.

<img src="images/10-load-account-data17.png">
<img src="images/10-load-account-data18.png">