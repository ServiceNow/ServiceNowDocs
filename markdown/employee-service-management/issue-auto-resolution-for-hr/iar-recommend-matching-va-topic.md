---
title: Enhanced search results in IAR with Virtual Agent
description: The Issue Auto Resolution application for HR has enhanced its search results with the introduction of Virtual Agent to the IAR pipeline flow. The employee can now receive a matching Virtual Agent topic as a recommendation for a noncritical case, when the topic is available in the database, before the application performs a general AI search.
locale: en-US
release: australia
product: Issue Auto Resolution for HR
classification: issue-auto-resolution-for-hr
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Use, Issue Auto Resolution for HR, HR Service Delivery, Employee Service Management]
---

# Enhanced search results in IAR with Virtual Agent

The Issue Auto Resolution application for HR has enhanced its search results with the introduction of Virtual Agent to the IAR pipeline flow. The employee can now receive a matching Virtual Agent topic as a recommendation for a noncritical case, when the topic is available in the database, before the application performs a general AI search.

In the previous version of Issue Auto Resolution for HR, all the noncritical HR cases were sent recommendations that were based only on the AI search results. With this enhanced version, the IAR application first checks if a matching Virtual Agent topic is available for that particular HR case. If there’s a matching Virtual Agent topic, the IAR application recommends the identified Virtual Agent topic to the employee. If no matching Virtual Agent topic is found, the application performs an AI search, and the recommendations are sent to the employee based on the AI search results.

**Note:** To enable the Virtual Agent topic recommendation in the Issue Auto Resolution for HR, the administrator must set the sn\_iar\_hr.hr\_intent\_solution\_enable property to true. The ServiceNow® support team can update this feature to your Issue Auto Resolution flow.

## Virtual Agent topic flow

When an employee submits a human resource \(HR\) case via an email or portal, the Issue Auto Resolution first checks whether the **sn\_iar\_hr.hr\_intent\_solution\_enable** property value is set to **True**. If the property value is **True**, the Issue Auto Resolution checks if the corresponding intent for the topic map is active or not in the **Auto-resolution configuration** record. When the property value is **False**, then Issue Auto Resolution continues to perform the normal AI search.

The Virtual Agent process is as follows:

1.  An HR case is submitted by the employee through an email.
2.  The employee receives an email with the Virtual Agent topic recommendation in it.
3.  The employee selects **Go to portal** to access the details of the case on the portal.
4.  The employee accesses the Virtual Agent topic, by selecting the Virtual Agent chat icon ![VA chat icon.](../../universal-request/images/icon-chat-va.png) on the portal and selecting the case recommendation notification.

## Enhanced recommendations preview on email for AI search flow

The new recommendations section displays the titles of the knowledge articles and catalog items in the email. The ![IAR knowledge article icon.](../image/iar-knowledge-article.png) icon indicates that the recommendation title is a catalog item. The ![IAR catalog item icon.](../image/iar-catalog-item.png) icon indicates that the recommendation title is a knowledge article.

