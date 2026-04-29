---
title: Add custom software products in workspace
description: Add a custom software product for any publicly available software product that does not exist in the Software Asset Management Content Library. Custom software products enable you to normalize and account for software products that aren’t part of the Software Asset Management Content Library yet.
locale: en-US
release: australia
product: Software Asset Management
classification: software-asset-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Using Software Asset Workspace, Software Asset Management, IT Asset Management]
---

# Add custom software products in workspace

Add a custom software product for any publicly available software product that does not exist in the Software Asset Management Content Library. Custom software products enable you to normalize and account for software products that aren’t part of the Software Asset Management Content Library yet.

## Before you begin

If you want to enable the Software Asset Management application to submit content requests for your custom software products, opt in to the Software Asset Management Content Service and then enable the Custom Software Products KPI. See [Enable sharing information with Software Asset Management content service](t_EnableSAMContentService.md) for detailed instructions.

Role required: sam\_admin

## Procedure

1.  Navigate to **Workspaces** &gt; **Software Asset Workspace**.

2.  From the Software Asset Workspace, open the License operations view.

3.  From the navigation menu of the License operations view, navigate to **Content** &gt; **Custom software products**.

4.  Select **New**.

5.  On the form, fill in the fields.

<table id="table_pwn_5yv_2bc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Publisher

</td><td>

Publisher of the custom software product.

</td></tr><tr><td>

Product

</td><td>

Name of the custom software product.

</td></tr><tr><td>

Subscription software

</td><td>

Option to indicate if the custom software product has a subscription.

</td></tr><tr><td>

Product type

</td><td>

Type of software product. Select one of the following options:-   **Child**: A component of a main software product. This software product type isn’t licensable.
-   **Driver**: A software product that controls a device.
-   **Licensable**: A software product that is licensable.
-   **Not Licensable**: A software product that is not licensable.
-   **Patch**: A software product that updates, fixes, or improves an existing computer program.
-   **Unknown**: A software product that is unknown.


</td></tr><tr><td>

Product classification

</td><td>

United Nations Standard Products and Services Code® \(UNSPSC®\) classification for the custom software product.

</td></tr><tr><td>

Active

</td><td>

Option to indicate if the custom software product is active.

</td></tr><tr><td>

Exclude from content service

</td><td>

Option to prevent the custom software product from being shared with the Software Asset Management Content Service.

</td></tr></tbody>
</table>6.  Select **Submit**.


## Result

The custom software product is immediately available to use in your downstream processes, such as normalization and reconciliation. Depending on whether you enabled or turned off the **Exclude from content service** option, the Software Asset Management application can either continue using the custom software product or begin using the corresponding software product in the Software Asset Management Content Library.

-   If you enabled the **Exclude from content service** option, the Software Asset Management application continues to use the custom software product in your downstream processes.
-   If you turned off the **Exclude from content service** option, the Software Asset Management application proceeds as follows:
    1.  The Software Asset Management application automatically creates and sends a corresponding content request to the Content Service team.
    2.  After the Content Service team reviews and approves the request, the software product is added to the Software Asset Management Content Library.
    3.  During the next scheduled content update, the new software product in the Content Library is pushed to your ServiceNow instance and then mapped to the custom software product.
    4.  The Software Asset Management application automatically generates a product suggestion that enables you to consolidate the custom software product with the software product in the Content Library. This consolidation updates all references to the custom software product with references to the software product in the Content Library. You can choose to accept or reject the suggestion.

        -   If you accept the suggestion, the Software Asset Management application begins using the software product in the Content Library for your downstream processes.
        -   If you reject the suggestion, the Software Asset Management application continues to use the custom software product in your downstream processes.
        For more information on product suggestions, see [View custom software product suggestions in workspace](view-custom-software-product-suggestions-workspace.md).


**Parent Topic:**[Using Software Asset Workspace](../concept/using-sam-workspace.md)

