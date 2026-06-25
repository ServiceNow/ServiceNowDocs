---
title: Return to Workplace campaigns
description: Use campaigns to deliver important messages and information to your employees that are going through the Return to Workplace process.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/employee-service-management/safe-workplace/return-workplace-campaigns.html
release: yokohama
product: Safe Workplace
classification: safe-workplace
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Enterprise Employee Experience Pack, Safe Workplace, Health and Safety, Employee Service Management]
---

# Return to Workplace campaigns

Use campaigns to deliver important messages and information to your employees that are going through the Return to Workplace process.

For employees that have communicated that they are ready to return to the workplace, you can target them with specific emails or content in the Employee Center Pro portal.

Campaigns are comprised of content are created in Content Publishing and assembled in Content Experiences. For more information on Content Experiences, see [Creating campaigns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/employee-service-management/employee-experience-foundation/ecpro-campaigns.md).

## Campaign structure

Campaign structure looks like a pyramid with the campaign at the top. A campaign contains campaign bundles. Each campaign bundle contains the content that you want to present to your employees.

\[Omitted image "return-workplace-campaign.png"\] Alt text: Return to Workplace - Campaign structure

The following campaign is part of this application:

## Return to Workplace

The Return to Workplace campaign helps keep your employees informed during the return to work planning process.

The target audiences for this campaign are the employees with information on their HR profiles indicating they're ready to return to work and have a specific return date. For more information, see [Add or modify an HR profile](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/employee-service-management/hr-service-delivery/t_CreateOrModifyAUserProfile.md).

The Return to Workplace campaign contains the following bundles and content:

-   Announce and Plan Return
    -   Return to Workplace - Get Ready to Return Banner: Provides a banner on the Service Portal or Employee Service Center that links to the Return to Workplace Company Updates \(KB0088880\) knowledge base \(KB\) article. You can find this KB article by navigating to **Knowledge** &gt; **Articles** &gt; **All** and searching for KB0088880. The link to the KB article is configured in **Link Content** under Content Delivery. For more information, see [Add or modify links to other content sources](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/employee-service-management/employee-experience-foundation/ecpro-manage-link-content.md).
    -   Return to Workplace sample Notification: Sends an email with a sample message on returning to the workplace. The email uses notification content created in Content Delivery. For more information, see [Create email, SMS, or push notification content](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/employee-service-management/employee-experience-foundation/ecpro-manage-notification-content.md).

        The Announce and Plan Return campaign bundle triggers dynamically based on a trigger table and fields. For more information, see [Create campaign bundles/stages](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/employee-service-management/employee-experience-foundation/ecpro-manage-campaign-bundles.md).

-   Welcome back to the workplace
    -   Return to Workplace - Welcome Back Notification: Provides a sample email communicating information about plans to reopen the office. The link in the email points to the Workplace Health and Safety Policy FAQ knowledge article \(KB0088882\). You can find the KB article by navigating to **Knowledge** &gt; **Articles** &gt; **All** and searching for KB0088882. The link to the KB article is configured in **Link Content** under Content Publishing. For more information, see [Add or modify links to other content sources](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/employee-service-management/employee-experience-foundation/ecpro-manage-link-content.md).
    -   Return to Workplace Welcome Back: Provides a banner on the ESC with a link to the Social distancing and safety tips for common workspaces FAQ \(KB0088883\) article. You can find the KB article by navigating to **Knowledge** &gt; **Articles** &gt; **All** and searching for KB0088883. The link to the KB article is configured in **Link Content** under Content Publishing. For more information, see [Add or modify links to other content sources](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/employee-service-management/employee-experience-foundation/ecpro-manage-link-content.md).

        The Welcome back to the workplace bundle triggers dynamically based on a trigger table and fields. For more information, see [Campaign bundle triggers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/employee-service-management/employee-experience-foundation/ecpro-triggers.md).


-   **[Accessing the Return to Workplace campaign](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/employee-service-management/safe-workplace/access-campaigns.md)**  
View and edit the campaign content and campaign bundles in the Return to Workplace campaign.

**Parent Topic:**[Enterprise Employee Experience Pack](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/employee-service-management/safe-workplace/return-workplace-employee-exp-pack.md)

