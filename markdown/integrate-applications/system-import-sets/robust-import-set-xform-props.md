---
title: Robust import set transformer properties
description: Properties that define the types of updates that are permitted.
locale: en-US
release: zurich
product: System Import Sets
classification: system-import-sets
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Robust Import Set Transformers, Import sets, Imports, Workflow Data Fabric]
---

# Robust import set transformer properties

Properties that define the types of updates that are permitted.

## Properties for CI reclassification

To configure properties, navigate to **System Import Sets** &gt; **Administration** &gt; **Robust Import Set Transformers**.

The properties defined in the Robust Import Set Transformers form are at the IRE payload level and apply to all rows for the given import. If you define properties at the individual item level using IntegrationHub ETL, they take priority over properties defined at the IRE payload level. For more details about CI reclassification, see, [CI reclassification during IRE processing](https://www.servicenow.com/docs/access?context=c_CIReclassification&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US).

<table id="table_t2x_kth_krb"><thead><tr><th>

Name

</th><th>

Value

</th><th>

Description

</th></tr></thead><tbody><tr><td>

ire.input.items.settings.updateWithoutDowngrade

</td><td>

true/false

</td><td>

Valid values:

-   true: Update the item but don’t permit a downgrade.
-   false: Update the item and permit a downgrade.

 Default: false

</td></tr><tr><td>

ire.input.items.settings.updateWithoutUpgrade

</td><td>

true/false

</td><td>

Valid values:

-   true: Update the item but don’t permit an upgrade.
-   false: Update the item and permit an upgrade.

 Default: false

</td></tr><tr><td>

ire.input.items.settings.updateWithoutSwitch

</td><td>

true/false

</td><td>

Valid values:

-   true: Update the item but don’t permit class switching.
-   false: Update the item and permit class switching.

 Default: false

</td></tr><tr><td>

ire.input.items.classDowngrade

</td><td>

true/false

</td><td>

Valid values:

-   true: Update the CI class to a class that is higher in the class hierarchy, and the newly assigned class is a parent of the current class.
-   false: Update the item but don’t permit a class downgrade.

 Default: false

</td></tr><tr><td>

ire.input.items.classUpgrade

</td><td>

true/false

</td><td>

Valid values:

-   true: Update the CI class to a class that is higher in the class hierarchy, and the newly assigned class is a parent of the current class.
-   false: Update the item but do permit a class downgrade.

 Default: false

</td></tr><tr><td>

ire.input.items.classSwitch

</td><td>

true/false

</td><td>

Valid values:

-   true: Update the attribute. The newly assigned class is in a different branch in the class hierarchy and has a different set of attributes than the current class.
-   false: Update the attributes but don’tn’t permit a class switch.

 Default: false

</td></tr></tbody>
</table>