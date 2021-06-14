# Get-AzureADUsersLastSignIn
Get-AzureADUsersLastSignIn.ps1 is a PowerShell script retrieves Azure AD users with their last sign in date.

## Script requirements
- You need to sign-in using a Global Admin (GA) account.
- Tenant should have an Azure Active Directory Premium license.

## How to run the script
Download and run the `Get-AzureADUsersLastSignIn.ps1` script from [this](https://github.com/mzmaili/Get-AzureADUsersLastSignIn) GitHub repo. 

## Why is this script useful?
- To retrieve Azure AD users with their last sign-in details.
- To generate a CSV report with the result.

# Frequently asked questions
## Does this script change anything?
No. It just retrieves data.

## Should tenant have a specific Azure AD license?
Yes, tenant should have an Azure AD Premium license.

## Can I get users last sign-in details through Get-Azureaduser command?
No.

## Does this script require any PowerShell module to be installed?
No, the script does not require any PowerShell module.

## What does "N/A" value in "Last Success Signin (UTC)" field mean?
If 'Last Success Signin (UTC)' value is 'N/A', this could be due to one of the following two reasons:
- The last successful sign-in of a user took place before April 2020.
- The affected user account was never used for a successful sign-in.
