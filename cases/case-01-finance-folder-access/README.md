# Case 01 — Finance Folder Access Issue

## 📌 Overview

A Finance user reported that they could log in to `FIN-PC01` but could not access the Finance shared folder.

This case was completed collaboratively by [Mr. Hari Krishnan R K](https://github.com/harikrishnan-rk), [Mr. Manu P Nair](https://github.com/manunair16), and [Mr. Varun M Nair](https://github.com/varunmnair95).

Each participant worked in an independent NorthBridge lab environment.

## 👤 My Role

**IT Support / Systems Administrator**

My responsibility was to investigate the access failure, identify the root cause, apply the appropriate remediation, and validate the result.

## 🔎 Investigation

### 1. Check User Group Membership

The affected user, Sara Mitchell, was checked in Active Directory.

Her account was a member of `GG_default`, but `GG_Finance` was not listed in her group membership.

**Evidence:**
[user-membership](evidence/investigation/01-user-membership.png)

The `GG_Finance` group was then checked to confirm that Sara was not currently a member.

**Evidence:**
[groups-members](evidence/investigation/02-groups-members.png)

### 2. Check Share Permissions

The Finance shared folder was checked to determine whether `GG_Finance` was part of the existing access model.

`GG_Finance` had:

* Read
* Change

share permissions.

**Evidence:**
[share-permission](evidence/permissions/03-share-permission.png)

### 3. Check NTFS Permissions

The Finance folder's NTFS permissions were also reviewed.

`GG_Finance` had **Modify** permission on the Finance folder.

**Evidence:**
[ntfs-share-permission](evidence/permissions/04-ntfs-share-permission.png)

## 🎯 Root Cause

The Finance user's expected membership in `GG_Finance` was missing.

The Finance share and NTFS permissions were already configured for `GG_Finance`.

Therefore, the user's authorization path was broken because the user was not receiving the permissions assigned through the Finance security group.

## 🛠️ Remediation

The affected user was added to:

`GG_Finance`

**Evidence:**
[user-added-to-group](evidence/remediation/05-user-added-to-group.png)

No direct permissions were added to the individual user, and the existing Share and NTFS permissions were not changed.

## ✅ Validation

After restoring the group membership, the user was able to access the Finance shared folder successfully.

**Evidence:**
[user-access-regained](evidence/remediation/06-user-access-regained.png)

## 🔐 Security Consideration

Restoring the user's existing security-group membership was preferred over granting individual permissions.

This maintains the existing centralized access-control model and avoids unnecessary direct permissions.

## 📸 Evidence

Technical investigation, permission review, remediation, and validation evidence are stored under:

`evidence/`

## 💡 Lesson Learned

Access problems should be investigated across the complete authorization path rather than changing permissions immediately.

In this case, the share and NTFS permissions were already correctly configured. The problem was the user's missing membership in the security group that provided the intended access.

## 🤝 Collaboration

* [Mr. Hari Krishnan R K](https://github.com/harikrishnan-rk)
* [Mr. Manu P Nair](https://github.com/manunair16)
* [Mr. Varun M Nair](https://github.com/varunmnair95)

Each participant maintained their own evidence, findings, and documentation.
