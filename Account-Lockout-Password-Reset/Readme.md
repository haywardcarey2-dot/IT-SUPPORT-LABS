# Lab 2: Windows Account Lockout and Password Reset

## Overview
Simulated a Windows account lockout, restored access using an administrator account, and documented the troubleshooting process in Spiceworks.

## Environment
- Windows 11 Pro virtual machine
- VMware Fusion
- Local test account: labuser
- Computer Management
- Local Security Policy
- Spiceworks Help Desk

## Issue
The user could not sign in after repeated incorrect password attempts. Windows displayed:
“The referenced account is currently locked out and may not be logged on to.”

## Investigation
1. Reviewed the account lockout policy in Local Security Policy.
2. Reproduced the lockout using the local test account.
3. Opened Computer Management → Local Users and Groups → Users.
4. Checked labuser Properties and confirmed “Account is locked out” was selected.

## Resolution
1. Cleared “Account is locked out” and applied the change.
2. Reset the account password using an administrator account.
3. Enabled “User must change password at next logon” to require the user to choose a new password.

## Verification
Successfully signed in to the labuser account and restored desktop access. Used the whoami command to verify the signed-in account.

## Skills Practiced
- Local user account administration
- Account lockout troubleshooting
- Administrator password resets
- Requiring a password change at next logon
- Verifying the signed-in user with whoami
- Help desk ticket documentation

## Scope
This lab used a local Windows account. It did not use Active Directory.
