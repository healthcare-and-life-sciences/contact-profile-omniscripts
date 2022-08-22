<h1>A-HLS Profile Card Omniscript Documentation</h1>

<h2>Overview</h2>

The objective of the Profile Card Omniscripts is to enable customers to rapidly deploy a Contact Profile Card for various types of Accounts.  The solution includes integration with Google Maps.  This Accelerator provides a ‘starting point’ for customers to configure according to their needs. It also includes an OmniScript widget framework with various record view/edit/update capabilities and Google Maps API integration that customers can customize to their business needs. 

This package consists of three Omniscripts that can be used as part of a Contact Profile Card:

1. CreateCase - This Omniscript creates a Case record for the current Person Account
2. UpdateContactMethods - This Omniscript displays the current Contact Methods for the Person Account.  It then provides the ability to update the Contact Methods
3. MemberChangeAddress - This Omniscript integrates with Google Maps and displays the current Address associated to the Person Account and provides the ability to update the Contact Methods


<h2>Business Objective</h2>

The objective of the Profile Card Omniscripts is to enable your organization to more quickly provide users with access to editable contact information as well as the creation of a Case.

<h3>Business Value and Benefit</h3>

* Reduce development time and IT costs
* Increase speed to market for users
* Reduce time required to make edits 
* Improve user experience


<h2>Industry Focus and Workflow</h2>

<h3>Primary Industry:</h3>

This solution is intended for multiple industries

<h3>Primary User Persona:</h3>

* Contact Center Agents
* Self-Service web sites

<h3>User Workflow:</h3>

* Display and/or edit Contact data
* Create Case


<h2>Package Includes:</h2>

*OmniScripts (3)*

* MemberServices/UpdateContactMethods 
* contactProfile/CreateCase 
* sfihsePatientEngagement/CreateCase 

*DataRaptors (3)*

* GetAddressAndContactData
* hinsCards_GetContactData_ForOs
* CreateComplaintCase

Flexcards (1)

* contactProfileFC


<h2>Configuration Requirements</h2>

<h3>Pre-Install Configuration Steps:</h3>

1. None

<h3>Installation Steps:</h3>

1. The Data Pack folder in the following GitHub repository contains the accelerator assets listed above. Please download the Data Pack(s) and save them to your desktop: healthcare-and-life-sciences (https://github.com/healthcare-and-life-sciences/contact-profile-omniscripts)
2. Then, complete the following steps to import them into your Salesforce org.
    1. To Import, in your destination Salesforce org, Click on *App Launcher* → Search for '*OmniStudio DataPacks*' and click on it.
    2. Click on '*Installed*' and on the right side click on '*Import from*'.
    3. Select '*From File*' - When the window opens, select the Data Pack file that you downloaded and stored on your machine. Click '*Install*'.
    4. After install, choose *‘Activate Now’*. This will activate all components. 
    5. The Data Pack is: ContactProfile Multipack 

<h3>Post-Install Configuration Steps:</h3>

1. In order to activate the Google Maps integration, please follow the below steps:
    1. Obtain a Google Maps API Key at the following URL: 
        1. https://developers.google.com/maps/documentation/javascript/get-api-key
        2. Create a Remote Site Settings record:
        3. [Image: image.png]
2. De-activate and re-activate the omniscripts:
3. [Image: image.png]
4. [Image: image.png]


Preview each Omniscript to verify functionality:

1. Retrieve the Id of a Person Account
2. Preview the Omniscript and enter the Person Account Id in the Context Id field:
3. [Image: image.png]
4. After previewing the OS, verify outcome:
    1. For the CreateCase Omniscript, navigate to Cases and verify the Case was created:
    2. [Image: image.png]
5. Preview the MemberChangeAddress Omniscript, enter the Person Account Id in the Context Id field:
    1. [Image: image.png]
    2. Verify Current Address fields retrieve the appropriate data
    3. Enter a new address (verify Type-Ahead works) and verify the new address is shown in the Google Map

<h2>Assumptions</h2>

1. A customer has licenses for Health Cloud, and the HINS Managed Package with OmniStudio. These solutions have all been installed and are functional.
2. A customer is assuming Salesforce Lightning Experience — not Classic.
3. Data Model elements that are part of the HINS (Vlocity) Managed package and Health Cloud are all available.
4. The Accelerator uses the Lightning Design System standards and look. Customers may want to apply their own branding which can be achieved.


<h2>Revision History</h2>

* *Revision Short Description (Month Day, Year)*

    * August 16, 2022 - Initial commit

