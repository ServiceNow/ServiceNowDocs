---
title: Add and configure the Retail KPI widget
description: Display report data in card format on your portal. You can display the report data by adding and configuring the Retail KPI widget.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Set up Retail Portal, Configuring Retail, Retail]
---

# Add and configure the Retail KPI widget

Display report data in card format on your portal. You can display the report data by adding and configuring the Retail KPI widget.

## Before you begin

The Retail Core \[com.sn\_retail\_core\] plugin must be activated. For more information, see [Activate Retail Core](https://www.servicenow.com/docs/bundle/yokohama-retail-industry/page/product/rahi-retail/task/rahi-retail-operations-install.html).

The page to which you want to add the widget must exist. For more information, see  [Create a page for Configurable Portal widgets](https://www.servicenow.com/docs/bundle/xanadu-customer-service-management/page/product/customer-service-management/task/create-page-configurable-portal-widget.html).

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Service Portal** &gt; **Service Portal Configuration**.

2.  Select **Designer**.

3.  On the Service Portal Designer page, select a retail portal page.

4.  Select the **Widgets** tab.

5.  In the Layouts section, drag the Container layout onto the portal edit page.

6.  On the container, add a set of columns by selecting the plus button.

7.  On the Widgets pane, in the  **Filter Widget ** field, enter  **Retail KPI**.

8.  Drag the widget onto the container.

9.  In the Edit page, select the Portal Data List widget.

10. Select the Pencil icon\(![](../image/icon-pencil-ac.png)\).

11. On the instance options page, in the  **Data ** field, paste the following JSON code to configure the lists.

    ```
    [ 
        { 
            "title": "KPIs for area manager and regional manager", 
            "relatedPartyTypes": ["0598ebfd105a0e90f877992571046f22", "02a86f3510da0e90f877992571046f2e"], 
            "reports": [ 
                { 
                    "report_id": "7e80564b43561210ae0a620465b8f2fc", 
                    "link": "/rsp?id=rsp_cases&category=escalated%20cases" 
                }, 
                { 
                    "report_id": "8ec2120f43561210ae0a620465b8f253", 
                    "link": "/rsp?id=rsp_cases&category=action%20needed&sub_category=open%20p1%20cases" 
                }, 
                { 
                    "report_id": "e68538d743961210ae0a620465b8f2f2", 
                    "link": "/rsp?id=rsp_cases&category=action%20needed&sub_category=sla%20breached%20cases" 
                } 
            ], 
            "order": 10 
        }, 
        { 
            "title": "KPIs for store manager fulfiller", 
            "relatedPartyTypes": ["4c78677510de0e90f877992571046f17"], 
            "reports": [ 
                { 
                    "report_id": "8ec2120f43561210ae0a620465b8f253", 
                    "link": "/rsp?id=rsp_cases&category=action%20needed&sub_category=open%20p1%20cases" 
                }, 
                { 
                    "report_id": "f827385b43961210ae0a620465b8f2fe", 
                    "link": "/rsp?id=rsp_cases&category=cases&sub_category=unassigned" 
                }, 
                { 
                    "report_id": "b297b45b43961210ae0a620465b8f272", 
                    "link": "/rsp?id=rsp_cases&category=cases&sub_category=my%20assigned%20cases" 
                }, 
                { 
                    "report_id": "e68538d743961210ae0a620465b8f2f2", 
                    "link": "/rsp?id=rsp_cases&category=action%20needed&sub_category=sla%20breached%20cases" 
                } 
            ], 
            "order": 20 
        }, 
        { 
            "title": "KPIs for store manager contributor", 
            "relatedPartyTypes": ["36b4c8297701121080b68b457d5a9994"], 
            "reports": [ 
                { 
                    "report_id": "8ec2120f43561210ae0a620465b8f253", 
                    "link": "/rsp?id=rsp_cases&category=action%20needed&sub_category=open%20p1%20cases" 
                }, 
                { 
                    "report_id": "85f7389b43961210ae0a620465b8f247", 
                    "link": "/rsp?id=rsp_cases&category=cases&sub_category=requested%20by%20me" 
                }, 
                { 
                    "report_id": "f827385b43961210ae0a620465b8f2fe", 
                    "link": "/rsp?id=rsp_cases&category=cases&sub_category=unassigned" 
                }, 
                { 
                    "report_id": "e68538d743961210ae0a620465b8f2f2", 
                    "link": "/rsp?id=rsp_cases&category=action%20needed&sub_category=sla%20breached%20cases" 
                } 
            ], 
            "order": 30 
        }, 
        { 
            "title": "KPIs for store associate fulfiller", 
            "relatedPartyTypes": ["df267ece38f30210f8779c150ba3e504"], 
            "reports": [ 
                { 
                    "report_id": "b297b45b43961210ae0a620465b8f272", 
                    "link": "/rsp?id=rsp_cases&category=cases&sub_category=my%20assigned%20cases" 
                }, 
                { 
                    "report_id": "f827385b43961210ae0a620465b8f2fe", 
                    "link": "/rsp?id=rsp_cases&category=cases&sub_category=unassigned" 
                }, 
                { 
                    "report_id": "8ec2120f43561210ae0a620465b8f253", 
                    "link": "/rsp?id=rsp_cases&category=action%20needed&sub_category=open%20p1%20cases" 
                } 
            ], 
            "order": 40 
        }, 
        { 
            "title": "KPIs for store associate contributor", 
            "relatedPartyTypes": ["8d046b7d105a0e90f877992571046f3b"], 
            "reports": [ 
                { 
                    "report_id": "85f7389b43961210ae0a620465b8f247", 
                    "link": "/rsp?id=rsp_cases&category=cases&sub_category=requested%20by%20me" 
                }, 
                { 
                    "report_id": "ed3cfc9343d61210ae0a620465b8f294", 
                    "link": "/rsp?id=rsp_cases&category=action%20needed&sub_category=awaiting%20info%20cases" 
                }, 
                { 
                    "report_id": "8ec2120f43561210ae0a620465b8f253", 
                    "link": "/rsp?id=rsp_cases&category=action%20needed&sub_category=open%20p1%20cases" 
                } 
            ], 
            "order": 50 
        }, 
        { 
            "title": "KPIs for all users", 
            "reports": [ 
                { 
                    "report_id": "8ec2120f43561210ae0a620465b8f253", 
                    "link": "/rsp?id=rsp_cases&category=action%20needed&sub_category=open%20p1%20cases" 
                }, 
                { 
                    "report_id": "b297b45b43961210ae0a620465b8f272", 
                    "link": "/rsp?id=rsp_cases&category=cases&sub_category=my%20assigned%20cases" 
                }, 
                { 
                    "report_id": "85f7389b43961210ae0a620465b8f247", 
                    "link": "/rsp?id=rsp_cases&category=cases&sub_category=requested%20by%20me" 
                }, 
                { 
                    "report_id": "7e80564b43561210ae0a620465b8f2fc", 
                    "link": "/rsp?id=rsp_cases&category=escalated%20cases" 
                } 
            ], 
            "order": 60 
        } 
    ] 
    ```

    **Note:**

    For more information, see [Retail KPI JSON parameters](retail-kpi-json-parameters.md).

    Review sys\_report table records to validate configurations in use with the Retail KPI widget.

12. On the Instance form, fill in the fields.

13. Select **Save**.


