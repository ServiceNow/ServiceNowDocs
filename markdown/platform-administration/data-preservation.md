---
title: Preserving data from target instances during clones
description: Use data preservers to protect data on the target instance from being overwritten. If you have custom applications, you must also manually preserve unpublished application content.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Manage, Instance Clone, Configure core features, Administer]
---

# Preserving data from target instances during clones

Use data preservers to protect data on the target instance from being overwritten. If you have custom applications, you must also manually preserve unpublished application content.

## Data preservers

Sometimes, it’s necessary to preserve some data on an instance targeted for cloning. For example, if the target is a MID Server, you must not overwrite the MID Server \[ecc\_agent\] table. Preserved data is reapplied to the target instance after exclusions are completed.

**Warning:** You must define data preservers on the source instance. Defining them on the target instance doesn't preserve the data.

Data preservers typically preserve system settings and themes, such as:

-   Instance-specific authentication settings
-   Bookmark \[sys\_ui\_bookmark\]
-   Recent Selection \[sys\_ui\_recent\_selection\]
-   User Preference \[sys\_user\_preference\]

## Data preservers for Multi-SSO

The system automatically creates the necessary data preservers for cloning when you activate Multiple Provider Single Sign-On integration.

<table><thead><tr><th>

Name

</th><th>

Table

</th><th>

Conditions

</th></tr></thead><tbody><tr><td>

Certificate

</td><td>

X.509 Certificates \[sys\_certificate\]

</td><td>

None

</td></tr><tr><td>

Core Instance Properties

</td><td>

System Property \[sys\_properties\]

</td><td>

-   \[OR\] \[Name\] \[is one of\] \[glide.authenticate.external, glide.authenticate.external.logout\_redirect\]
-   \[OR\] \[Name\] \[starts with\] \[com.snc.integration.saml\_esig\]
-   \[OR\] \[Name\] \[is one of\] \[glide.smtp.port, glide.smtp.auth, glide.smtp.encryption\]
-   \[OR\] \[Name\] \[starts with\] \[glide.authenticate.multisso\]
-   \[OR\] \[Name\] \[is\] \[glide.authenticate.sso.redirect.idp\]

 **Note:** The properties **glide.smtp.port**, **glide.smtp.auth**, and **glide.smtp.encryption** are deprecated.

</td></tr><tr><td>

Digest Properties

</td><td>

Digest Properties \[digest\_properties\]

</td><td>

None

</td></tr><tr><td>

Identity Providers

</td><td>

Identity Providers \[sso\_properties\]

</td><td>

None

</td></tr><tr><td>

SAML2 Update1 Properties

</td><td>

SAML2 Update1 Properties \[saml2\_update1\_properties\]

</td><td>

None

</td></tr></tbody>
</table>**Note:** Although you can modify these data preservers, it’s good practice not to. The Digest Properties \[digest\_properties\], Identity Providers \[sso\_properties\], and SAML2 Update1 Properties \[saml2\_update1\_properties\] tables are required for multiple sources, single sign-on \(SSO\) to function properly. If multiple sources, single sign-on is turned off on the target instance, you can safely remove all three data preservers. Remove all tables simultaneously, as attempting to clone while preserving a table results in a system error and termination of the clone process.

## Preservation of unpublished applications

You can't use data preservers to save unpublished applications. Instead, application developers must choose how they want to preserve unpublished applications.

The cloning process doesn’t preserve version differences for applications in development. Instead, the system clone only copies the application version installed on the source instance onto the target instance. If the target instance had a development version of the same application, the application is editable after the clone. The target instance maintains the same version that is installed on the source instance. If the application was missing from the source instance, the cloning process deletes the application from the target instance.

**Parent Topic:**[Managing Instance Clone](../task/using-instance-clone.md)

