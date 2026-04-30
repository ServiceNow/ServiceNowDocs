---
title: Troubleshoot domain separation errors
description: If you encounter domain separation issues, review this list of solutions.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Enable verbose domain logging and debug messages, Domain separation setup and administration, Domain separation for service providers, Access Management]
---

# Troubleshoot domain separation errors

If you encounter domain separation issues, review this list of solutions.

<table id="table_imr_4wm_v4"><thead><tr><th>

Error or symptom

</th><th>

Solution

</th></tr></thead><tbody><tr><td>

A domain sys\_id points to a non-existent domain

</td><td>

This error occurs when a data record, such as a user or task record, has a `sys_domain` column value whose `sys_id` does not exist in the current domain table. The domain `sys_id` could have been accidentally deleted or it could refer to a previous domain table if you changed the domain table. To fix the error, open a list for the table containing the error, filter on the invalid `sys_domain` value. Then, either manually enter the correct `sys_domain` value or remove it.

**Note:** You can have invalid domain `sys_ids` in any table that references the domain table. For example, invalid domain IDs can occur in the User Visibility Domain `[sys_user_visibility]`, Group Visibility Domain `[sys_user_group_visibility]`, and Contained Domain `[domain_contains]` tables.

</td></tr><tr><td>

A domain path or domain number sys\_id points to the wrong domain

</td><td>

This error occurs when a domain number or domain path query is out of sync with the actual domain name. This error can occur with domain numbers when adding domains requires renumbering or during the conversion from domain numbers to domain paths.To fix the error, check the results in the [Domain Separation Center](domain-separation-center.md). If the error persists, you can manually edit the value for the `sys_domain_path` or `sys_domain_number` columns to point to the proper domain.

</td></tr><tr><td>

The domain tree structure is corrupt

</td><td>

This error occurs if there is a series of domain contains relationships that create an infinite loop among domains. To fix the error, open a list for the domain table and manually edit the domain contains values to not form a loop.

</td></tr></tbody>
</table>