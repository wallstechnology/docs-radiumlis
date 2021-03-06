---
title: 'Getting Started (Lab Personnel)'
body_classes: 'title-center title-h1h2'
menu: 'Getting Started (Lab Personnel)'
recaptchacontact:
    enabled: false
toc: true
---

# Radium LIS User Guide
## For Lab Personnel
!!! This site should serve as a reference for common workflows and settings you will need to configure in order to get Radium LIS working for you!

[TOC]

### Section 1. Requirements & Logging In
Radium LIS will come pre-configured in most cases with crucial settings such as interfaces, a barcode printing
system, and some example providers.
In order to use Radium LIS, the first requirement is to have access to it.

A URL will be provided by the installation team.

#### Section 1.1. Requirements
The only requirement for end users to get started in Radium LIS is 
<a href="https://www.google.com/chrome" target="_blank">Google Chrome, click here to visit the download page.</a>

#### Section 1.2. Logging In
Your Radium LIS technician will provide you with a link and credentials to sign in to Radium LIS, 
follow that link and sign in using the credentials provided. You should see a login page like this:

[center]![](/images/tut-image-1-loginscreen.PNG?cropResize=600,400)[/center]

### Section 2. Basic Usage & Status Messages
In the next section we cover how to configure Radium LIS for your needs.
This section comes before as a reference because if you can understand this section, you may not need to read further.

#### Section 2.1. Basic Usage
In most cases, Radium LIS is designed to be intuitive. Simply following the instructions provided on the form will usually
result in a successful interaction with the LIS. From creating a patient, to placing an order, verifying results, viewing reports, 
these things were all designed to work within a typical clinical laboratory workflow. After basic training, 100% of our users have 
been successful in operating the LIS on a day to day basis.

#### Section 2.2. Status Messages
When configuring forms, performing actions, etc., status messages will be shown at the bottom of the page which 
indicate how your action was perceived by the LIS.
* **Successful** messages appear in green, and are a sign that whatever you did worked. Whether it was 
	creating a new test, a new provider, a new patient, approving an order, creating an order, etc., if you get a green message, it worked!
* **Warning** messages appear in yellow/orange and are an indication that the form submitted, but you may be missing some information. Usually
	these warnings can be ignored.
* **Failure** messages indicate that something went wrong, you were trying to do something not permitted, etc. For help with these messages 
	you may be able to solve them by correcting something in the form you were trying to submit. If you are unable to correct your message, 
    you can [contact support][support] to help resolve the issue.

### Section 3. Main Configuration
The settings menu can be found in the Radium LIS toolbar, it looks like some gears.
Radium LIS is highly customizable, so covering the settings is a crucial aspect of this guide.
You should go in order as some of the settings are dependent on others.
For example, you need a Lab to create a Practice. You need a Practice to create a Provider.
You need a Compound Method to create a Compound, and you need a Protocol to create a Plate Reader Test.
Interfaces are usually pre-configured by the support team when installing Radium LIS for your system, 
but settings are left open in case things change.

These are some examples that will give you an idea of the flexibility of the software. Enjoy!

#### Section 3.1. Labs
From the about page:
> Clinical Labs perform laboratory testing on patient samples. 
> Labs should be concerned with quality control and patient care, thus labs in Radium LIS are configured 
> to be streamlined with requisitions, automatic ordering, automatic result acquisition, and automatic reporting.
> Your lab should already be added but more labs may be added if necessary.

Labs in Radium LIS are used by [Practices][1]

##### Creating a Lab
``Permissions Required: Config Labs``

Navigate to Add Lab and enter the information for the lab.
Lab Name, Address, City, State, Zip, Phone, Email, CLIA #, Director, and Logo will all appear on every
report generated by the LIS.

The LCMS Report Disclaimer will appear on any report generated for LCMS compound testing.

##### Requisition Templates (Advanced)
``Permissions Required: Config Coordinates``
 
If you have the coordinates permission, you can upload a requisition template to your lab which will be used
when creating requisitions from orders.

* Required Fields:
	* Upload File - A PDF File containing the requisition on the first page. (Only the first page will be used)
	* Requisition Name - A friendly name that will appear in the Requisition Templates table.
	* Sample Type - Urine, Blood, Reference, Plate Reader. You can only have one sample type per requisition.
	* Make Default - Whether to make this the default requisition for the sample type you chose.

##### Requisition Coordinates (Advanced)
``Permissions Required: Config Coordinates``

This is where you configure the coordinates for the requisition templates you have uploaded for a lab.
You can use Paint or some other image processing software to find the X and Y coordinates for each point. 
Configuring coordinates usually takes trial and error but it is the main mechanism for creating an 
automatic electronic requisitioning system in Radium LIS.

#### Section 3.2. Practices & Providers
##### About Practices and Providers
From the Radium LIS about page:
> About Practices & Providers
> Clinical Practices are groups of providers. Practices can be configured in Radium LIS by importing them from the EMR, or by creating them. All a practice needs to get started is a name and an associated laboratory where testing is performed.
> Clinical Providers are physicians or non-physicians who assess and diagnose patients. Laboratory testing may be ordered for these patients using Radium LIS. Providers can be configured by importing them from the EMR, or by creating them. A provider needs a name, an external ID, an NPI, a specialty, and one or more practices. Practices should be configured before or at the same time as configuring providers so that a practice may be chosen for the provider you want to create.

##### Creating Practices
``Permissions Required: Config Providers``

* Required fields:
	* Practice ID - an integer number that you will associate with this practice
	* Practice Name - the actual name of the practice you are creating
	* Lab Selection - Any [lab][0] you have previously configured.

##### Creating Providers
``Permissions Required: Config Providers``

* Required fields:
	* ID - an integer used to refer to the provider. Must be unique within Radium LIS providers.
	* Title - the title of the provider (Dr., Mr., etc.)
	* Last Name - Last name of the provider
	* First Name - First name of the provider
	* NPI - The National Provider Identifier - must be unique within Radium LIS
	* Billing Type - Physician or Non-Physician Provider
	* Practice Selection - A previously configured [practice][1] must be chosen to add a provider.
* Optional fields:
	* Specialty - List the provider's specialty if they have one.

#### Section 3.3. Roles, Users & Clients
``Permissions required: Add/Edit Users``

! Note: If your setup does not allow for remote clients, you will not see the "Clients" part of this setting.
You will most likely already have access to everything if you are the main user for the LIS.
If you have access to Add and Edit Users, you will be able to create roles and users.
You will need the Add/Edit Clients permission in order to add and manage clients.

##### Roles and Permissions
``Permissions required: Add/Edit Users``

Permissions will appear on the "Roles" page under Roles, Users, & Clients Configuration.
These permissions are required for accessing different areas of Radium LIS. They will be referred to in this guide
as well.

We won't go into detail on each permission listed on the Roles page, as they will be covered instead by each section 
they refer to.

###### Adding a Role
To add a role, simply enter the Role Name, and select each permission you want that role to have.
The permissions are self explanatory with descriptions next to each one.

###### Deleting a Role
To delete a role, click the Delete button next to its list of permissions in the Roles table at the top of the page.

##### Creating a User
``Permissions required: Add/Edit Users``

To create a user, go to the "New User" page.

* Required fields:
	* Full Name - the user's full name will sometimes be used in the LIS to kindly point out their lack of privileges.
	* Username - the user will use this to login to the system.
	* Password - A temporary password to give to the user which will need to be changed after the first login.
	* [Role][P] - A role, previously configured in [Roles and Permissions][P]

##### Modifying User Permissions
``Permissions required: Add/Edit Users``

Users can be deleted and have their permissions changed from the User Permissions page.
Anyone with access to Add/Edit Users can change anyone else's access, besides users with the "Admin" role.

##### Managing Clients with the Client Manager
``Permissions required: Add/Edit Clients``
! Systems must have the Clients module enabled (System Admin Only) in order to manage clients.


Clients are accounts for use by [practices][pr]. Each client will be tied
to a practice and will only be able to perform a specific set of actions.

Namely, clients can Add/Edit patients, Add, Edit, and Approve orders for the patients they have added,
and Print Reports for the orders they have created.

###### Adding/Editing a Client
To add a client, fill in the required information on the client manager page.

* Required fields:
	* Client's Practice - the last field on the form, the Client's Practice is the practice that the client will be adding patients for.
	* Client's Full Name - Usually the Practice name, or the group that controls the Practice's patient testing
	* Username - a unique username that will be used by the client to login to the Provider Portal.
	* Password - use a temporary password that the client will change after they login the first time.
	* Address, City, State, & Zip - The main address of the client, for record keeping.
	* Contact - A contact person

* Optional fields:
	* Email, Phone #, & Fax # - contact details you may want to keep on record in case you need to interact with the client.
	* Active Client - you can deactivate clients by checking the "Active Client" box at the bottom of the form.

Editing a client is the same as adding, just click the edit icon from the client manager next to the client you
want to edit, and you can save or delete the client from there.

#### Section 3.4. Test & Panel Configuration
``Permissions required: Config Tests``

You can view tests from this menu, typically by choosing "View/Edit Tests" under the test type dropdown.
You will notice there are multiple test types supported, discussed below.

##### About Tests & Test Types
From the about page:
> Radium LIS can currently process 4 different types of instruments: Screening Analyzers,
  Complex Confirmatory Analyzers, Plate Readers, and Blood Analyzers. These instruments each have 
  unique methods of analyzing tests, and in order to organize them, Radium provides distinct categories 
  for these tests. These are Screen Tests, LCMS Compounds, Plate Reader Tests, and Blood Tests respectively.
  Radium LIS also provides the option of creating Reference Tests, which can be ordered but do not require
  results. Panels can contain any combination of these tests, including reference tests.


###### Screen Tests
Radium LIS was originally built to communicate with a Screening Instrument using HL7 messsages.
**Screen Tests** are the tests that interact with toxicology screening instruments and are typically used to report qualitative data.

The form to add or edit screen tests takes the following parameters.

_Add/Edit Tests_
* Basic (Required):
	* Test ID - The Unique ID of the test - unique across all tests, compounds, and panels.
	* Test Name - The name of the test as it should appear in the LIS and on reports.
	* Test Code - The test code is the code used by the analyzer. 
	* Active - Whether the test is actively being used and ran.
* Advanced (Optional):
	* Print Test Ranges - Check if you want to print the ranges for the test on reports.
	* Lower Positive, Lower Negative - the lowest possible value for a test to be considered positive, or negative, respectively.
	* Upper Positive, Upper Negative - the highest possible value for a test to be considered positive, or negative, respectively.
	! Upper Positive, Upper Negative, Lower Positive, and Lower Negative must not conflict with each other or the LIS
	! will produce an error.
	* Lower Limit - the lowest value to report, any values below the lower limit will be flagged as **< 0 ng/mL**, for example
	* Upper Limit - the highest value to report, values greater than will be flagged as **> 1000 ng/mL**, for example.
	* Result Units - units used by this test. Sometimes the instrument configuration will provide units, so this field is optional in that case.
	* Quantitative - Check this if you want to show the actual result for each test. Unchecking it will display **Positive** or **Negative** depending on:
		* Positive Text - replace **Positive** with a custom text field
		* Negative Text - replace **Negative** with a custom text field
		* _Abnormal values will be reported as **Abnormal**_

###### Configuring Compounds Methods
Compounds are managed in the same way as tests, except they require a Compound Method.

_Compound Methods_
* Required fields:
	* Interface - the interface/instrument this method will be associated with
    * Method Name - choose a friendly, letters and numbers only name
		This name will most likely be used when sending results to the interface
	* Method Filepath - Usually a filepath associated with the instrument, this may be used by the [Worklist Module][W]
	* Data Filepath - Usually a data path for storing the data on the interface, also used by the Worklist Module.


###### Compound Groups
Compound Groups are automatically managed and created by creating and managing compounds.
You can rename compound groups for an entire subset of compounds through the Compound Groups Menu, or
you can adjust compound group names through the View/Edit Compounds page.

###### Compounds
``Required permissions: Modify Tests``

Each compound has a compound group, discussed above. Compounds typically have a cutoff, an upper limit, and are associated
with LCMS machines.

_Add/Edit Compounds_
* Required Fields:
	* Compound ID: The unique ID for the compound. Must be a number between 1 and 99999 and must be unique across
		all tests in the LIS.
	* Compound Name: How the compound will appear on Reports as well as in the Results section and across the LIS.
    * LCMS Compound Name: Also referred to as the **Machine Name** or **Test Code**, this record may be overwritten by specific [interface settings][IS].
* Recommended fields:
	* Cutoff - values greater than or equal to the cutoff will be deemed **Positive**, values below will be **Negative**
    * Upper Limit - values greater than the upper limit will be flagged as **> 5000 ng/mL**, for example

###### Plate Reader Tests, Blood Tests, and Reference Tests
Further breaking your tests down into subcategories, we have plate reader tests, blood tests, and reference tests.
These test types use the same required and advanced options as [Screening Tests][st]

* **Plate reader tests** allow laboratory personnel the ability to create and interface tests for plate reader instruments.
* **Blood tests** Nothing special here. Blood tests interface with blood requisitions and blood machines.
* **Reference Tests** Reference tests work with Reference Lab interfaces to tell reference labs what tests are being requested.

###### Plate Reader Protocols
_Plate Reader Protocols_ are used to define protocols, also known as methods, for plate reader testing. These protocols are typically plate layouts and are designed for specific tests. Each plate reader test can have 1-N plate reader protocols. Protocols can not be shared between tests, but they can be duplicated for easy setup.

##### Panels
``Relevant permissions Add/Edit Panels, View Panels``
The permissions are the same standard as the rest, with Modify, View, and None. Users with the Panels:Modify permission are allowed to add or edit panels, users with the View Only permission are allowed to View them, and users with no permissions will not see the Panels pane.

###### Creating a Panel
``Required permissions: Modify Panels``

Required fields:
* Panel ID - A 4 digit ID that will be used to identify the panel in the LIS. This ID cannot be the same as any screen test, compound, blood test, plate reader test, reference test, etc.
* Panel Name - The name of the panel will appear on the [Order Form][o] and should describe the types of tests that will be selected.
* Active - Active panels will appear on the order form, whereas inactive panels will not. Active will be turned **on** by default.

Deprecated fields:
* Appears on Requisition/Requisition Sequence # - The [requisition coordinate system][rcs] is now responsible for if and where a box will be checked.

###### Test Selection
**Screen Tests** will appear at the top, followed by **LCMS Compounds**, **Plate Reader Tests**, **Blood Tests**, and **Reference Tests**
Each section will display a list of the tests which appear for that test type. Compounds will be sorted by their respective [Compound Groups][cg]

This same tests selection will appear on order forms, with the added section of Panels, which you can create by clicking the "Add Panel" button at the bottom
of the form.

#### Section 3.5. Barcodes
``Required permissions: Modify Barcodes``

Barcode settings are streamlined to allow lab users the option to change the number of labels to print, and to modify when in the process barcodes are printed.
Currently, barcodes are only created when orders are approved. This is planned to be changed to create barcodes when an order is created, since all of the information required for a barcode is presented at that time. Barcodes can also be printed on Requisitions using the [Requisition Coordinate System][rcs].

#### Section 3.6. Interfaces (Advanced)
<a id="interface-settings"></a>
``Required permissions: Config Interfaces``

! Note: Interface settings are crucial to the integration of LCMS machine results with Radium LIS, and should only be modified by experienced users.

Users with the Admin Role are in charge of configuring the interface to work with the system, however, Radium gives users the option to configure interface specific
settings, such as tests used, data types, data columns for CSV format result extraction, and data file labels and sheet information.

##### Section 3.6.1. LCMS Interface Settings
The following settings tabs will appear for LCMS interface settings.
!!! Note: For any section, you can _Save Changes or Cancel_ to save changes made or discard any changes made.
!!! All sections will be searched and saved simultaneously, so you will need to complete all settings before trying to Save, initially.

###### Compounds Used
LCMS machines come configured to use compounds, so from the Compounds Used page you can select which compounds are used on the interface.
These compounds can be used by multiple interfaces, however, a compound method cannot be used across multiple interfaces. Each interface must have its own compound methods. Radium tracks which compounds are used on the interface settings so that the user can specify the machine name for each instrument, if necessary.

###### Data Columns
Data Columns are the columns that appear in CSV or XLSX result exports.
Each column can be turned on or off in Radium LIS to support different template types.
Columns supported by Radium LIS are as follows:
* **Unique ID** A unique identifier such as an index for each unique compound + sample ID. If no Unique ID column is given, Radium will use the Sheet Row for the unique index.
* **Sample Name** and **Sample ID** Either the sample ID or the sample Name will be tied to the Order ID, depending on what you choose in the [Data Import][#data-import] section.
* **Component Name** This is the column which contains the _LCMS Compound Name_ that you specified in the Compounds Used settings section or in Compound Settings.
* **Calculated Concentration** The result value is usually the calculated concentration column. This is the result which will be used when results are given.
* **Used** Optional, has to do with whether the result will be used or not. _This is a relic of the [QCF][qcf] module and is not implemented for sample results as of yet._
* **Area Count**, **Retention Time**, **Notes** These are not used for results, see [QCForever Configuration Guide][qcf] on setting up QCF to use these settings.
* **Acquisition Time** Acquisition Time will default to the date supplied in the filename if there is not a column specified. We recommend exporting an Acquisition Time column so that you can know exactly _when_ your results were completed.

###### Data Import
Settings that have to do with the file you are importing into Radium LIS are found in this section.
They include:

* **Data File Label Start** and **Data File Label End** - import files must include a date so that the results can be referred to using that explicit date. Dates must be in YYMMDD format and must be a part of the filename. If a file is called 181220_Main.xlsx, for example, it should contain results from the "Main" method that were exported or found on December 20th, 2018. (The method name must also be a part of the file name).
* **Database: Overwrite data on import** - Enable this setting if you plan to re-import the same file but with different results, for example, or if there was something
wrong with the initial upload that you fixed and want to overwrite. Keep this disabled if you do not plan to be overwriting any results.
* **Select Highest Concentration** - Sometimes, multiple results come across for the same compound for a sample. Select this to ensure that the highest result will be used. If this is kept off and multiple results are found, the last result found will be used (which is often zero or undefined).
* **Use Sample Name Only**, **Use Sample ID Only**, and **Use Sample Name & Sample ID** are what they appear as. Select whichever one makes sense for your data.
* **Specify Data Sheet** - Sometimes results exports come with multiple sheets, often times these sheets are hidden. Select this option to automatically search for and use a data sheet with the **Data Sheet Name** setting, specified next.

##### Section 3.6.2. Screen Interface Settings
Screen Interface settings are set up on the backend by the system administrator.

##### Section 3.6.3. Plate Reader Interface Settings
This is where settings for plate reader interfaces can be configured. Each plate reader interface can allow [plate reader protocols][prp]

#### Section 3.7. QC Settings
##### QCForever: Settings
Radium comes with the ability to monitor the quality control of your LCMS machines using automatic chart creator software QCForever. 
**QCF Products** include:
* Levey-Jennings charts with standard deviation/acceptance criteria options
* Area Count and Retention Time charts

### Section 4. Results Export & Reporting
Different instruments and laboratories have different procedures for exporting results and viewing reports.
Results follow the same strategy for every instrument and laboratory, however, which is that results will be imported or inserted into the system, and once verified, a report will be generated for each test/instrument type.

Test types: **Screen, LCMS, Plate Reader, GCMS, Blood**
Each test type will have a separate section dedicated to reporting tests for that test type. 

#### Section 4.1. Clinical Toxicology Reporting
The clinical toxicology laboratory typically requires two distinct testing methods and consequently reports: **Screen** and **Confirmation.** Radium LIS automatically generates both of these reports when results are verified for each test type. Once all tests have been verified, an optional **Tox Analysis Report** will be generated, which is a combination report of both Screen and Confirmation tests, and also has the capability of including **Medications** that were prescribed for the sample. Further capabilities of the system include flagging whether those medications were **Consistent** or **Inconsistent.**

##### Section 4.1.1. Screening Instruments
Screening instruments typically have their results automatically transferred to the LIS using the built in results transfer methods provided by the instrument manufacturer. Alternatively, results can always be entered manually.

To enter results manually, simply go to the **Results -> Pending Results** page and find the order for which you want to modify the results.

##### Section 4.1.2. LCMS Instruments
LCMS Instruments typically have their results exported. The results export method is included in the shared drive accessible from your LCMS host computer. Radium LIS automatically checks this folder every few minutes and will automatically import any results it finds in the folder.

See [section 3.6. Interface Settings][IS] on making sure your import settings are correct.

Once results have been imported, they should show up under the **Results -> Pending Verification** page. If they are not there, check the **Results -> Pending All** page, some results may not have transferred, probably due to an error in configuration. Check your configuration and move the file back to the main results folder, where it can be re-imported with the correct settings. The file will be located in the **read/YYYY/M** folder.

#### Section 4.2. Other Laboratory Reporting
Other laboratories which simply wish to do testing and are not in the clinical toxicology realm will receive one general report for each test type, and a combination report when all tests have been completed. Rather than being called the "Tox Summary Report," it will be called the **Summary Report** or **Final Report,** depending on system configuration.

#### Section 4.3. Verifying Results
Once all results are accepted by your laboratory's discretion, they can be verified from the **Results -> Verified Results** menu. To verify results for a test type, click the tab corresponding to that test type, and scroll to the bottom of the results. After reviewing your results, click the **Verify** button. This will verify all results for that test type, and a report will be generated. You must verify results for all tests for a Final Report to be generated.

#### Section 4.4 Viewing Reports
Patient Reports can be found under the **Reports -> Reports** menu. This page is also visible to clients, who can see all reports for the samples they have sent in. Simply click **View Report** for each report you want to view next to a patient, and you can print or download the report from there.

[0]: #creating-a-lab "Configuring Labs"
[1]: #creating-practices "Configuring Practices"
[P]: #roles-and-permissions "Configuring Roles"
[pr]: #about-practices-and-providers "Practices and Providers"
[t]: #about-tests-and-test-types "About Tests & Test Types"
[W]: #about-worklists "The Worklist Module"
[IS]: #interface-settings "Interface Settings"
[st]: #screen-tests "Adding/Editing Screen Tests"
[o]: #order-form "The Order Form: Adding, Editing, Approving, and Viewing."
[rcs]: #requisition-coordinates-advanced "Using the Requisition Coordinate System"
[cg]: #compound-groups "About Compound Groups"
[support]: mailto:support@walls.solutions "Contact Support by Email"
[qcf]: #qcforever "Configuring and Using The QCForever Module"
[prp]: #plate-reader-protocols "About Plate Reader Protocols"
[qcfs]: #qcforever-settings "Configuring QCForever"
