---
title: Module access policy visualization
description: Use module access policy visualization to view all relevant cryptographic module information on a single UI page.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/platform-encryption/map-vis-concept.html
release: australia
product: Platform Encryption
classification: platform-encryption
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Key Management Framework Reference, Key Management Framework, Encryption]
---

# Module access policy visualization

Use module access policy visualization to view all relevant cryptographic module information on a single UI page.

\[Omitted image "map-vis-ui-page.png"\] Alt text: Module access policy visualization UI page

Key Management Framework admins and cryptographic managers can use the module access policy UI page to view all access control mechanisms related to a single cryptographic module. Use the information collected on this UI page to determine who has access to encrypted information on your instance.

Users with the **sn\_kmf.admin** or **sn\_kmf.cryptographic\_manager** roles can access the module access policy visualization UI page by navigating to **All** &gt; **Key Management** &gt; **Cryptographic Modules** &gt; **All**.

## Results Labels

Module access policies contain a **Result** field, which determines whether to grant access to the selected cryptographic module. The UI page displays a label on elements on the UI page based on the value of that field.

|UI label|Result field value|Definition|
|--------|------------------|----------|
|\[Omitted image "map-vis-track.png"\] Alt text: Track label|**Track** or **Allow**|Access is granted to all users, including scripts.|
|\[Omitted image "map-vis-reject.png"\] Alt text: Reject label|**Reject**|Access is denied unless a track module access policy is found.|
|\[Omitted image "map-vis-strictreject.png"\] Alt text: StrictReject label|**StrictReject**|Access is denied.|
|\[Omitted image "map-vis-absent.png"\] Alt text: Absent label|**N/A**|The module access policy doesn’t exist on the instance. Access is denied to all.|

## Global policies

<table id="table_hqc_p54_qxb"><tbody><tr><td>

Use the **Global policies** section to review the module access policies that control platform-level access.

 Select the **Manage** button below any of the policies to navigate to that policy record. If the policy doesn't exist, an **Add** button appears below that entry. Select the **Add** button to navigate to a new policy record where you can define the policy.

</td><td>

\[Omitted image "map-vis-global-section.png"\] Alt text: Global policies section

</td></tr></tbody>
</table>|Policy|Definition|
|------|----------|
|Default rule|The default rule policy defines the behavior when no existing rule matches an access request.|
|Platform backend|The platform backend policy governs internal platform code access to cryptographic keys.|
|Script engine|The script engine policy governs whether the script engine is permitted to access cryptographic keys.|
|System user|The system user policy governs whether the system user is permitted to access cryptographic keys.|

## Helpful resources

<table id="table_hn2_gr4_qxb"><tbody><tr><td>

Use the **Helpful resources** section to find links to product documentation, relevant knowledge articles, and a brief description on how module access policies are evaluated on the platform. For a deeper look into how module access policies are evaluated, see [Module access policy debugger](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/platform-encryption/map-debugger.md).

</td><td>

\[Omitted image "map-vis-help.png"\] Alt text: Helpful resources section

</td></tr></tbody>
</table>## Granular policies

<table id="table_j5n_js4_qxb"><tbody><tr><td>

Use the **Granular policies** section to view lists of module access policies, separated by policy type. Use the tabs above the list to select a policy category to display.

 -   Role
-   Scope
-   Scope and Domain \(if Domain Separation is active\)
-   Script
-   Resource exchange \(if the cryptographic module is a Password2 or Field Encryption submodule\)
-   Identity \(if Secrets Management Enterprise is active\)

 By default, the each list displays only active policies. Use the filter icon to change the default filter for the list.

</td><td>

\[Omitted image "map-vis-granular.png"\] Alt text: Granular policies section

</td></tr></tbody>
</table>## Users with access

<table id="table_btv_b54_qxb"><tbody><tr><td>

Use the **Users with access** section to see a list of all users that have access to the selected cryptographic module. The list is grouped by user, as single users can posses multiple roles that grant access to a cryptographic module.

</td><td>

\[Omitted image "map-vis-users.png"\] Alt text: Users with access section

</td></tr></tbody>
</table>**Parent Topic:**[Key Management Framework Reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/platform-encryption/understanding-kmf.md)

**Related topics**  


[Key Management Framework key life-cycle states]()

[Roles installed with Key Management Framework]()

[Module access policy debugger]()

[Encryption and Key Management subscription bundle]()

