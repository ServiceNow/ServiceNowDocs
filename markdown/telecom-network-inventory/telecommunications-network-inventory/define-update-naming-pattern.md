---
title: Define or update a naming pattern for a related template
description: Define a JavaScript expression that names the configuration item \(CI\) you create from a related template within an inventory template. The naming pattern can include literal text, variables from the token library, conditionals, and string transformations.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/telecom-network-inventory/telecommunications-network-inventory/define-update-naming-pattern.html
release: australia
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: task
last_updated: "2026-06-25"
reading_time_minutes: 4
breadcrumb: [Create inventory template for network asset instantiation, Use, Telecommunications Network Inventory]
---

# Define or update a naming pattern for a related template

Define a JavaScript expression that names the configuration item \(CI\) you create from a related template within an inventory template. The naming pattern can include literal text, variables from the token library, conditionals, and string transformations.

## Before you begin

Role required: Inventory Template Manager.

## Procedure

1.  Navigate to the SOW workspace or the Network Inventory workspace.

    Go to **List** &gt; **Network Inventory Templates** &gt; **Inventory Templates** and select the inventory template that contains the related template you want to update.

2.  Open the related template record.

    From the inventory template, select the **Related Templates** tab. Locate the related template you want to update and select its name to open the record.

    Alternatively, select the **Overview** tab, select the related template's node in the tree, and select **View details** in the top-right of the Overview to open the related template record in a new tab.

3.  Open the Define name pattern modal.

    On the related template record's form, locate the **Name Pattern** field. Select the **Define name pattern** button at the right edge of the field.

    The Define name pattern modal opens. The modal shows the current pattern, if one exists, in the **Name pattern** input.

    **Note:** The **Define name pattern** button is visible only to users with the Inventory Template Manager role. Users without this role see the Name Pattern field as read-only.

4.  Edit the pattern in the **Name pattern** input.

    Enter or update the JavaScript expression that produces the CI name. The pattern can combine literal text, variables, string methods such as `.replace()`, and conditional logic using the ternary operator.

    For the full pattern syntax, see [How inventory template names are generated](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/how-inventory-template-names-are-generated.md).

5.  Insert a variable from the token library.

    Place the cursor in the **Name pattern** input. The list of available variables opens automatically. Select a variable from the list to insert it into the pattern at your cursor position.

6.  Review the inline pattern feedback.

    As you edit the pattern, the modal displays inline feedback below the **Name pattern** input:

    -   **Pattern valid.** A green message appears: `Valid name pattern. Preview: <resolved name>`. The name shown after `Preview:` is a sample of what your pattern produces, using sample values for the pattern's variables.

    -   **Pattern invalid or empty result.** A red message appears: `Name pattern results in empty name. Please try again.` The **Apply** action is blocked. The same message appears whether the pattern has invalid JavaScript, references a variable that is not in the token library, or evaluates to an empty string.

7.  Select **Preview** to refresh the inline feedback.

    Selecting **Preview** re-runs the pattern and updates the sample name shown in the green message.

8.  Select **Apply** to add the pattern to the Name Pattern field.

    The modal closes, the **Name Pattern** field shows the new pattern, and the record form indicates you have unsaved changes.

    **Note:** **Apply** does not save the record. The pattern stays in the form until you save the record.

9.  Save the related template record.


## What to do next

To verify the new pattern produces the expected resolved name across the template hierarchy:

1.  Open the parent inventory template.
2.  Select the **Overview** tab.
3.  Select **Refresh** in the top-right of the Overview tab. Refreshing the Overview updates the resolved names in the tree.
4.  Locate the related template you updated. Confirm that the tree node label shows the resolved name you expected.

**Parent Topic:**[Create inventory template for network asset instantiation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/preparing-inv-templates-network-asset-generation.md)

**Related topics**  


[Naming patterns in inventory templates](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/naming-patterns-in-inventory-templates.md)

[Models and templates name definition](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/how-models-and-templates-define-names.md)

[How inventory template names are generated](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/how-inventory-template-names-are-generated.md)

[The Inventory Template Overview tab](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/inventory-template-overview-tab.md)

[Extension point for custom naming validation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/extension-point-custom-naming-validation.md)

[Naming pattern validation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/naming-pattern-validation.md)

