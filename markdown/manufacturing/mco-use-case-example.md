---
title: Manufacturing Commercial Operations Use Cases
description: In this example, the Manufacturing Commercial Operations application helps the fictitious Zenod manufacturing company \(the OEM\) use Service Exchange to manage their partnerships with Boxeo, a transportation company who uses their printers and services for shipping goods globally, and Office Mart, a channel retailer that sells many office brands and commercial tech supplies to retailers and consumers \(e.g., computers, monitors, printers, shipping supplies, etc.\)​.​
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Manufacturing Commercial Operations reference, Manufacturing]
---

# Manufacturing Commercial Operations Use Cases

In this example, the Manufacturing Commercial Operations application helps the fictitious Zenod manufacturing company \(the OEM\) use Service Exchange to manage their partnerships with Boxeo, a transportation company who uses their printers and services for shipping goods globally, and Office Mart, a channel retailer that sells many office brands and commercial tech supplies to retailers and consumers \(e.g., computers, monitors, printers, shipping supplies, etc.\)​.​

## Example scenario: Key personas and how they benefit

Zenod, a manufacturing company that manufactures and sells scanners, printers, and other multifunctional office systems, offers a shipping services package to its enterprise customers. A customer, Boxeo, has partnered with them to use Zenod printers, shipping supplies, and services for shipping goods globally.

The key personas \(manufacturer and customer\) can complete the following tasks in their respective Service Exchange instances:

**The manufacturer \(Zenod\) can**:

-   Publish a product or service catalog using remote catalog item and remote task definition
-   Receive requests in the agent workspace in real time
-   Relay resolutions to customers and any channel partners on the watchlist​​

**The customer \(Boxeo\) can**:

-   Request for repairs and tech support directly with Zenod using remote catalog
-   Synchronize using remote task​
-   View outages and service issues
-   View products they have purchased
-   Request services related to the products they have purchased

The scenario plays out in the following manner:

1.  Zenod publishes their product or service catalog using remote catalog item and remote task definition​.
2.  Boxeo's production printer goes down, and they raise a request for a repair and for tech support directly with Zenod using remote catalog​.
3.  While Boxeo's production printer is down, Boxeo's L1 is working on the incident, and needs to be able to relay that information and what they've done so far to Zenod. Boxeo's L1 and Zenod can synchronize workflows using remote task​.
4.  Zenod's tech support receives the request in their agent workspace in real time, meeting Boxeo where they are​, and proceeds with the resolution.

## Example Manufacturing Commercial Operations and Service Exchange use cases

Zenod manufactures scanners, printers, and other multifunctional office systems​, and sells them both B2B and to end consumers through wholesalers, SMBs, and retails channels. OfficeMart is a channel retailer that sells many office brands and commercial tech supplies to end consumers \(e.g., office furniture, computers, monitors, printers, shipping supplies, etc\)​.​​ Here is an example of how Zenod might use Manufacturing Commercial Operations with Service Exchange to communicate with their channel retailer, OfficeMart, and vice versa.

-   **Manufacturer \(OEM\) to Channel​**
    1.  Zenod creates a case that informs the channel retailer about a recall on a product​, and sets the channel and accounts to "Alert"​.
    2.  Office Mart receives a provider task on their instance, which appears in the portal as a task to be completed​.
    3.  Office Mart follows the pre-defined workflows for tasks surrounding the recall, such as how to notify customers that have purchased or licensed the product​ about the recall.
-   **Channel to​ Manufacturer \(OEM\)**
    1.  OfficeMart publishes a product or service catalog​.
    2.  An OfficeMart buyer makes a change request for their current order using the service catalog \(a remote catalog published by Zenod\) on their employee portal. They describe what they want to change and submit it to OfficeMart through their service catalog, where the system automatically creates a case task in their consumer instance that is synchronized to Zenod's Service Exchange for providers instance​.
    3.  The task is converted into a case. The Zenod order management agent receives the case directly in the agent workspace, and works to resolve it.​

