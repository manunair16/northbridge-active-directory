# Technical Findings — Case 01

## Ticket Reference

**Incident:** NB-INC-001

**Issue:** Finance user unable to access \\SRV-DC01\Finance

**Role:** IT Support / Systems Administrator

## Problem

Sara Mitchell could authenticate to the domain and log into `FIN-PC01`, but access to:

`\\SRV-DC01\Finance`

was denied.

## Investigation

The user's Active Directory membership was reviewed.

Sara was not a member of:

`GG_Finance`

The `GG_Finance` group was then reviewed and confirmed not to contain Sara.

The Finance share permissions were checked and showed that `GG_Finance` had **Read** and **Change** permissions.

The Finance folder's NTFS permissions showed that `GG_Finance` had **Modify** permission.

## Root Cause

The user's expected membership in `GG_Finance` was missing.

The permission configuration itself did not require modification. The authorization path depended on membership in `GG_Finance`, which the affected user did not have.

## Remediation

Sara Mitchell was added to:

`GG_Finance`

No direct user permissions were added.

No changes were made to the existing Share or NTFS permissions.

## Validation

After the group membership was restored and the user's session was refreshed, access to the Finance shared folder was successfully restored.

## Security Reasoning

The remediation followed the existing security-group-based access model.

Adding the user directly to the folder permissions would have solved the immediate problem but would create an unnecessary individual permission entry and weaken centralized access management.

## Conclusion

The Finance access failure was caused by incorrect Active Directory group membership rather than an incorrect Share or NTFS permission configuration.
