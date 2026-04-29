---
title: General guidelines
description: Practice the following general guidelines for an enhanced Now Assist for Setup experience.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-16"
reading_time_minutes: 2
breadcrumb: [Reference, Now Assist for Setup, Get started, Administer the ServiceNow AI Platform]
---

# General guidelines

Practice the following general guidelines for an enhanced Now Assist for Setup experience.

## Instance specific configurations

The following configurations are excluded from the update set and must be re-configured directly on the production instance:

-   Single Sign-On \(SSO\)
-   LDAP directory integration
-   Notification templates and settings

## Validation checks

If you encounter an error immediately after uploading the update set XML file, perform the following validation checks:

-   Confirm that you are uploading the XML file downloaded from the non-production instance.
-   Verify that the file has not been modified, renamed, or corrupted after download.
-   If the issue persists, repackage the batch update set in the non-production instance, download the XML file again, and retry the upload.

## Preview errors

Preview errors indicate conflicts or unresolved dependencies in the update set. Resolve each error on the Update Set Preview page before you can commit the update set. For each preview problem record, there is an Available Actions dropdown. The following resolution options are available:

<table id="table_vh3_trw_p3c"><thead><tr><th>

Available Actions

</th><th>

Description

</th><th>

When to use

</th></tr></thead><tbody><tr><td>

Compare with local

</td><td>

Opens a side-by-side comparison view of the incoming update set version against the version currently on the production instance.

</td><td>

Use this action prior to selecting Accept or Skip in order to review the specific differences between the two versions and make an informed resolution decision.

</td></tr><tr><td>

Accept remote update

</td><td>

Overwrites the existing record on the production instance with the version contained in the update set.

</td><td>

Select this option when the incoming configuration from the update set is the correct and intended state of the record, and the local version on production should be replaced.**Note:** It is recommended to use the Compare with local action before selecting Accept remote update or Skip remote update for any conflict. Accepting a remote update will overwrite the existing production record and cannot be undone through the update set process.

</td></tr><tr><td>

Skip remote update

</td><td>

Discards the conflicting change from the update set and retains the existing record on the production instance.

</td><td>

Select this option when the local version on the production instance is the correct state, or when the incoming change is not applicable to the target environment.

</td></tr><tr><td>

Show local record

</td><td>

Shows the local version of the update set version available on the production instance.

</td><td>

Select this option to view the local version of the current update set version on the production instance.

</td></tr><tr><td>

Show local update

</td><td>

Shows the local update of the update set version available on the production instance.

</td><td>

Select this option to view the update made to the current update set version on the production instance.

</td></tr></tbody>
</table>**Parent Topic:**[Now Assist for Setup references](../reference/ia-reference.md)

