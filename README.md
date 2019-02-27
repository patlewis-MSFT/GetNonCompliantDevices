# GetNonCompliantDevices
Uses Intune Graph APIs to show non Compliant devices for each policy

Version 1.0.0

The GetNonCompliantDevices.ps1 script searches for devices that are non compliant for each compliant policy. 

Also if a device is not compliant and is does not fail the compliance check for a policy it could mean the device does not have a policy assigned. These devices will also be displayed

## More Intune Samples
This utilizes one or more parts from the Powershell Intune samples here: 
https://github.com/microsoftgraph/powershell-intune-samples

## Prerequisites
* The logged on user must have the appropriate Graph permissions setup in Intune prior to running the script: https://docs.microsoft.com/en-us/intune/intune-graph-apis#intune-permission-scopes
* Install the AzureAD PowerShell module by running 'Install-Module AzureAD' or 'Install-Module AzureADPreview' from an elevated PowerShell prompt
* An Intune tenant which supports the Azure Portal with a production or trial license (https://docs.microsoft.com/en-us/intune-azure/introduction/what-is-microsoft-intune)
* Using the Microsoft Graph APIs to configure Intune controls and policies requires an Intune license.
* An account with permissions to administer the Intune Service
* PowerShell v5.0 on Windows 10 x64 (PowerShell v4.0 is a minimum requirement for the scripts to function correctly)
Note: For PowerShell 4.0 you will require the PowershellGet Module for PS 4.0 to enable the usage of the Install-Module functionality
First time usage of these scripts requires a Global Administrator of the Tenant to accept the permissions of the application
* If you receive an error that scripts are disabled on your machine, you will need to allow the script to run by running the Set-ExecutionPolicy cmdlet. For more information: https://docs.microsoft.com/en-us/powershell/module/microsoft.powershell.security/set-executionpolicy?view=powershell-6

## Getting Started
After the prerequisites are installed or met, perform the following steps to use the script:
1. Download the GetNonCompliantDevices.ps1 to your local Windows machine
1. Run PowerShell from an elevated Administrator account
1. Browse to the directory where you copied GetNonCompliantDevices.ps1
   * Type: **.\GetNonCompliantDevices.ps1**
1. Follow the prompts for authentication and for the UPN of the owner or previous owner's device
