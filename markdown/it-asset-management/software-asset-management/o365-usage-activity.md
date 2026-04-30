---
title: Evaluating software usage activity for Microsoft 365 subscriptions
description: Evaluating software usage activity helps you discover active, inactive, and unassigned subscriptions among all subscriptions found on the Microsoft 365 portal.
locale: en-US
release: zurich
product: Software Asset Management
classification: software-asset-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 7
breadcrumb: [Integrating with Microsoft 365, Microsoft 365 integration, Software Asset Management publisher pack for Microsoft, Supported software publisher licenses, Software Asset Management, IT Asset Management]
---

# Evaluating software usage activity for Microsoft 365 subscriptions

Evaluating software usage activity helps you discover active, inactive, and unassigned subscriptions among all subscriptions found on the Microsoft 365 portal.

## Software usage activity for license optimization

Software usage activity refers to how software products are being used. By tracking this activity, you can monitor license usage and optimize your existing software subscriptions.

The following table lists the sources for collecting the software usage activity, the associated platform support, and the supported Microsoft 365 products.

|Sources of software usage activity collection|Platform support|Supported Microsoft Office 365 products|
|---------------------------------------------|----------------|---------------------------------------|
|Microsoft Graph APIs|Desktop, Web, Mobile|Outlook, Word, PowerPoint, Excel, OneNote, Teams, Exchange Online, SharePoint Online, Power BI|
|Microsoft SCCM or ACC-V|Desktop|Microsoft Office 365 apps for Enterprise|
|Jamf for macOS devices|Desktop|Microsoft Office 365 apps for Enterprise|
|Manual upload of the usage reports on the ServiceNow instance from the Microsoft Office 365 admin center|Desktop, Web, Mobile|Microsoft 365 Copilot, Visio Online, and Project Online|

**Note:** You can download the usage for Microsoft 365 Copilot, Visio Online, and Project Online from the Microsoft Office 365 admin center. For details, see [Upload the Microsoft 365 Copilot, Visio Online, and Project Online usage reports to your ServiceNow instance](../task/upload-usage-reports-copilot-visio-project.md).

After completing the [Microsoft 365 integration](integrate-with-microsoft.md), you can view the usage activity information using any of the following tables:

-   [Software Usages \[samp\_sw\_usage\]](../task/view-sw-usage-workspace.md)

    View the usage data for individual software products within the subscription in the Software Usages table. This table stores total usage and last activity retrieved from Microsoft APIs and other discovery solutions such as SCCM, Jamf, and ACC-V. For more details on software usage fields and their descriptions, see [View or create software usage](../task/view-sw-usage-workspace.md).

-   [Microsoft 365 Apps Usage Reports \[samp\_m365\_apps\_usage\_report\]](../reference/m365-apps-usage-report.md)

    View the last activity date for the Microsoft 365 products in the Microsoft 365 Apps Usage Reports table for each user. This table stores usage data for Microsoft 365 products in True or False retrieved from Microsoft APIs only. The last activity date helps you determine reclamation candidates more accurately for Microsoft 365 products, including Microsoft Outlook, Microsoft Word, Excel Microsoft PowerPoint, and OneNote. For more details on Microsoft 365 apps usage fields and their descriptions, see [Microsoft 365 Apps Usage Reports](../reference/m365-apps-usage-report.md).


These usage tables include the date when the software was last used and the type of the activities performed on the Desktop, Web, Mobile, or cumulative across platforms. The last activity data helps you select an optimized plan for individual products within your Microsoft 365 subscriptions. For related usage, the  **SAM - Collect Microsoft 365 Usage ** scheduled job collects the usage data daily.

Based on the software usage activity, Software Asset Management generates optimization recommendations for your software subscriptions.

## License optimization for Microsoft subscriptions

Software usage activity helps you with license optimization by discovering reclamation candidates from both the individual Microsoft products and the Microsoft 365 suite subscriptions. For more information, see [Publisher optimizations for Microsoft](../reference/pub-opt-microsoft.md). The  **SAM - Collect Microsoft 365 Usage ** scheduled job collects the usage data daily and the  **SAM - Create New Reclamation Candidates for Office 365 Integration**  generates the removal candidates weekly for low usage, downgrade, consolidated, and overlapping subscriptions. You can determine the reclamation candidates using both APIs and discovery solutions.

-   **Overlapping subscriptions**

    Overlapping Microsoft 365 integration subscriptions occur when a user or organization has several active subscriptions that provide the same or similar services at the same time. For example, both Microsoft 365 E3 and Office 365 E3 subscriptions exist, leading to unnecessary duplicate access to Office applications and additional services already included in Microsoft 365 E3. Software Asset Management recommends reclaiming the Office 365 E3 subscriptions and using the Microsoft 365 E3 subscriptions instead.

-   **Low usage subscriptions**

    Low usage Microsoft 365 or Microsoft Office 365 subscriptions are the subscriptions where the assigned licenses or services aren’t being fully used.

    -   Individual subscriptions such as Microsoft Teams, Microsoft SharePoint, or other single services.
    -   Subscription suites including Microsoft 365 and Microsoft Office 365.
    Software Asset Management recommends reclaiming the low usage subscriptions.

-   **Downgrade subscriptions**

    Downgrading Microsoft 365 or Microsoft Office 365 subscriptions means to switch from a higher-tier plan to a lower-tier plan. This approach usually involves moving from a plan with more features and services to one with fewer features and services, often at a reduced cost. The following table lists the downgrade subscriptions and conditions that result in downgrade recommendations.

<table id="table_nt1_1lg_xdc"><thead><tr><th>

Condition

</th><th>

Downgrade subscriptions

</th></tr></thead><tbody><tr><td>

No Power BI usage

</td><td>

-   Microsoft 365 Enterprise E5 to Microsoft 365 Enterprise E3
-   Microsoft 365 G5 USGOV GCCHIGH to Microsoft 365 E3 USGOV GCCHIGH
-   Microsoft 365 G5 for Government to Microsoft 365 G3 GCC
-   Microsoft 365 A5 for Students to Microsoft 365 A3 for Students
-   Microsoft 365 A5 for Faculty to Microsoft 365 A3 for Faculty


</td></tr><tr><td>

No desktop usage

</td><td>

-   Microsoft 365 E3 to Microsoft 365 F3
-   Microsoft Office 365 G3 GCC to Microsoft Office 365 G1 for Government
-   Microsoft 365 Enterprise E3 to Microsoft 365 Enterprise E1
-   Microsoft 365 A3 for Students to Microsoft 365 A1 for Students
-   Microsoft 365 A3 for Faculty to Microsoft 365 A1 for Faculty
 **Note:** For Microsoft 365 E3 to Microsoft 365 F3 downgrade, the user's mailbox and OneDrive size is also checked after checking the desktop usage.

</td></tr><tr><td>

User is a Shared Email Box

</td><td>

-   Microsoft 365 Enterprise E3 to Microsoft Exchange Online Plan 2
-   Microsoft 365 Enterprise E5 to Microsoft Exchange Online Plan 2
-   Microsoft Office 365 Enterprise E3 to Microsoft Exchange Online Plan 2
-   Microsoft Office 365 Enterprise E5 to Microsoft Exchange Online Plan 2
 **Note:** When the user is a shared email box, you can select the type of user as **Shared Email Box** in the **Non-person Account** field in the Discovered Users form.

</td></tr><tr><td>

Microsoft Exchange Online \(mailbox\) and Microsoft OneDrive size

</td><td>

Microsoft 365 E3 to Microsoft 365 F3If a user's mailbox size and OneDrive size is less than two gigabytes \(GB\), a downgrade recommendation is generated. The usage is retrieved from the Software storage usage \[saas\_sw\_storage\_usage\] table. For more information, see [Software storage usage fields](../reference/software-storage-usage.md).

</td></tr></tbody>
</table>    Additionally, you can view the Microsoft 365 and Office 365 downgrade candidates, including details about the source edition and the target edition in the [Subscription downgrade configuration \[saas\_downgrade\_configuration\]](../reference/saas-downgrade-configuration.md) table.

    You can view the conditions for downgrading the Microsoft 365 and Office 365 subscriptions in the [Subscription downgrade configuration condition \[saas\_downgrade\_config\_condition\]](../reference/saas-downgrade-config-conditions.md) table.

    **Note:** You can also determine usage for Microsoft Access and Publisher from additional discovery solutions, such as Microsoft SCCM or ACC-V for E3 to E1 optimization. Here, the frequency of downgrade candidate generation from E3 to E1 would be monthly instead of weekly.

-   **Consolidated subscriptions**

    Consolidating Microsoft 365 integration subscriptions means merging multiple separate subscriptions into one unified subscription. This approach brings all licenses and services under a single account which helps in saving cost, easier track usage, and license assignments. For example, if Office 365 Enterprise E5, Windows, and EMS subscriptions exist, Software Asset Management recommends using a single license such as Microsoft 365 Enterprise E5 to cover these multiple products at a lower cost.


Additionally, the subscription assignment date that is automatically populated from the Microsoft 365 portal helps in generating the reclamation candidates for individual subscriptions. Using the subscription assignment date instead of the record creation date on the ServiceNow AI Platform helps to create correct reclamation candidates based on the actual use from the Microsoft 365 portal.

**Related topics**  


[Integrating with Microsoft 365](integrate-with-microsoft.md)

[Publisher optimizations for Microsoft](../reference/pub-opt-microsoft.md)

[Reclamation rules for Microsoft 365 integration](../reference/m365-reclamation-rules.md)

[Scheduled jobs for Microsoft 365](../reference/m365-scheduled-jobs.md)

