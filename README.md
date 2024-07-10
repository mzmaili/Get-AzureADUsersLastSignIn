# Azure AD Users Last Sign-in Report
Coming from the fact that we have a challenge when it comes to getting last sign-in details for Azure AD users as this attribute is not available either in AzureAD or MSOnline modules, Get-AzureADUsersLastSignIn.ps1 PowerShell script resolves this challenge as it retrieves Azure AD users with their last sign in dates.

## Script requirements
- You need to sign-in using a Global Admin (GA) account.
- Tenant should have an Azure Active Directory Premium license.

## How to run the script
Download and run the `Get-AzureADUsersLastSignIn.ps1` script from [this](https://github.com/mzmaili/Get-AzureADUsersLastSignIn) GitHub repo. 

## Why is this script useful?
- To retrieve Azure AD users with their last sign-in details.
- To generate a CSV report with the result.

## User experience
PowerShell console output:  
![Alt text](https://github.com/mzmaili/Get-AzureADUsersLastSignIn/blob/main/media/PS.png "PowerShell Output")  

CSV output:  
![Alt text](https://github.com/mzmaili/Get-AzureADUsersLastSignIn/blob/main/media/CSV.png "CSV Output")  

# Frequently asked questions
## Does this script change anything?
No. It just retrieves data.

## Should tenant have a specific Azure AD license?
Yes, tenant should have an Azure AD Premium license.

## What data does this script retrieves?
Get-AzureADUsersLastSignIn script retrieves the following details for each user in the tenant:  
`Object ID, Display Name, User Principal Name, Account Enabled, onPremisesSyncEnabled, Created DateTime (UTC), Last Non-Interactive Signin (UTC), Last Interactive Signin (UTC), Last Success Signin (UTC)
`

## Can I get users last sign-in details through Get-Azureaduser command?
No.

## Does this script require any PowerShell module to be installed?
No, the script does not require any PowerShell module.

## What does "N/A" value in "Last Success Signin (UTC)" / "Last Interactive Signin (UTC)" / "Last Success Signin (UTC)" field mean?
If 'Last Success Signin (UTC)' value is 'N/A', this could be due to one of the following two reasons:
- The last successful sign-in of a user took place before April 2020.
- The affected user account was never used for a successful sign-in.


## What is the meaning of "Last Success Signin (UTC)" / "Last Interactive Signin (UTC)" / "Last Success Signin (UTC)"?
Detail Definition of the date columns can be found here: https://learn.microsoft.com/en-us/graph/api/resources/signinactivity?view=graph-rest-1.0