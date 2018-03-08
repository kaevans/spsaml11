# Using Microsoft Azure Active Directory for Authentication with SharePoint Server 2016
This folder contains the sample scripts used with the article [Using Azure AD for SharePoint Server Authentication](https://docs.microsoft.com/en-us/office365/enterprise/using-azure-ad-for-sharepoint-server-authentication).

## Contents
The following files accompany the article:
- `MSGraphTokenLifetimePolicy.psm1` - Module containing functions to interact with Azure Active Directory Graph endpoint.
- `Initialize.ps1` - Script to initialize a PowerShell environment to use the sample module.

## Instructions
To use these modules, open an elevated PowerShell session. Import the module using the command:

````powershell
Import-Module <file path of Initialize.ps1>
````
You can now use the functions defined in the .psm1 module.

````powershell
Add-TokenIssuancePolicy -DisplayName "SharePointSAML1.1" -SigningAlgorithm "http://www.w3.org/2001/04/xmldsig-more#rsa-sha256" -TokenResponseSigningPolicy TokenOnly -SamlTokenVersion "1.1"
````