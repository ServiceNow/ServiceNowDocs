---
title: Logik.ai 2025/04/18 release notes
description: Logik.ai 2025/04/18 release notes include new enhancements and minor bug fixes.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/other-release-notes/oob-rn-logik-ai-2025-04-18.html
release: other
topic_type: reference
last_updated: "2025-11-25"
reading_time_minutes: 1
breadcrumb: [Logik.io available versions, OOB Other release notes]
---

# Logik.ai 2025/04/18 release notes

Logik.ai 2025/04/18 release notes include new enhancements and minor bug fixes.

## Schedule

|Sector|Upgrade|
|------|-------|
|Demo|Thursday, Apr 17, 2025, 8 pm CT|
|Test|Thursday, May 01, 2025, 8 pm CT|
|Prod|Friday, May 16, 2025, 8 pm CT|

Example: an environment with URL https://\[YourLogikURL\].prod.logik.io receives this build May 16, 2025.

## Release notes

This release version includes the following new enhancements and fixes.

## New Transaction Manager enhancement: sort product list results

New layout property in productList to define the sort parameters in the Product List in add lines to transaction flow.

## New Transaction Manager enhancement: product search and product configure button placement

Admin can determine if the Product Search and Configure Runtime UI buttons **Cancel**, **Add Line**, **Configure**, and **Done Configuring** are placed in the header, footer, or both.

## Bug fixes

<table id="table_gxv_hvs_l4b"><thead><tr><th>

Fix

</th><th>

Short description

</th></tr></thead><tbody><tr><td>

LGK-13677

</td><td>

Fixed an issue where rows from managed table API were not always properly paginated. Added new Revision to API from:```
/v1/managedTables/{tableName} // is deprecated in place. This is still supported and will work as previously designed
/v1/managedTables/{tableName}/{rowId} // gets record by rowId
/v1/managedTables/{tableName}/row // gets record by query param: like col1=value, col2=value2
/v2/managedTables/{tableName} // is advanced search for example ?search=rolex will search for all records containing rolex
/v2/managedTables/{tableName}/rows // has "filter" as paramater: like greaterThanEquals("age", 42)
```

</td></tr><tr><td>

LGK-16076

</td><td>

Fixed an issue where removing a child item in solution config was not properly reflected on BOM

</td></tr><tr><td>

LGK-16157, LGK-16159

</td><td>

Fixed differential behavior of rule execution between flightpath on and flightpath off

</td></tr><tr><td>

LGK-16357

</td><td>

Fixed an internal bug where a rule may not attach to a Blueprint

</td></tr><tr><td>

LGK-16368

</td><td>

Fixed a bug where fields remained hidden when corresponding hide rule stopped being true

</td></tr><tr><td>

LGK-16422

</td><td>

Fixed a bug where rapid repeated selection and deselection of an item in the UI may cause an error

</td></tr><tr><td>

LGK-16638

</td><td>

Hardened migration scripts for transition from very old versions to new versions of Logik

</td></tr></tbody>
</table>## Additional resources

-   Request new features or enhancements through the [Idea portal](https://support.servicenow.com/ideas) on [Now Support](https://support.servicenow.com/now).
-   Connect with other Logik.io users at [Now Community](https://www.servicenow.com/community/)

**Parent Topic:**[Logik.io available versions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/other/markdown/other-release-notes/oob-rn-logik-io.md)

