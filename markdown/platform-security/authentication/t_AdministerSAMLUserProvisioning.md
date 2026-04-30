---
title: Administer SAML user provisioning
description: Update the User table with the users in your IdP by first setting up field mapping and then enabling user provisioning through Multi-SSO IdP settings.
locale: en-US
release: xanadu
product: Authentication
classification: authentication
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [SAML user provisioning, SAML, Multi-Provider Single sign-on \(SSO\), Authentication, Access Management]
---

# Administer SAML user provisioning

Update the User table with the users in your IdP by first setting up field mapping and then enabling user provisioning through Multi-SSO IdP settings.

## Before you begin

Set up your IdP mapping to identify which fields in the IdP are mapped to the correct fields in the User table.

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Multi-Provider SSO** &gt; **Properties**.

2.  Select **Enable Auto Importing of users from all identity providers into the user table** \(**glide.authenticate.multisso.user.autoprovision**\) to activate this feature.

3.  Click **Save**.

4.  Navigate to **Multi-Provider SSO** &gt; **Identity Providers**.

5.  Open the Identity Provider record that you want to use.

6.  Create a record in the User table when the user does not already exist by selecting **Auto-provision Users**.

    If you upgraded to this release, you need to configure the form and add this field.

7.  Enable user records to be updated when users log in to the IdP and the information on the IdP is out of date with the information on the User table by selecting **Update User Record Upon Each Login**.

    If you upgraded to this release, you need to configure the form and add this field.

8.  Click **User Provisioning Transform Map** to see the map that the system automatically creates.

9.  Make changes to the map as needed.


## Result

When the first unknown users try to log in, the system creates the fields in the import set table from the metadata.xml file.

**Note:** You cannot map the fields from the IdP table until this first user logs in.

