---
title: Configure HR Service Delivery Advanced Integration with Workday
description: Configure HR Service Delivery Advanced Integration with Workday.
locale: en-US
release: australia
product: HR Service Delivery
classification: hr-service-delivery
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [HR Service Delivery Advanced Integration with Workday, Integration of HR Service Delivery with third-party systems, HR Service Delivery, Employee Service Management]
---

# Configure HR Service Delivery Advanced Integration with Workday

Configure HR Service Delivery Advanced Integration with Workday.

## Application setup

First, you must activate the HR Service Delivery Advanced Integration with Workday application from ServiceNow Store, which automatically activates the Workday HR Spoke. Next, set up Workday HR Spoke Workday HR Spoke , and install the following applications:

-   Glide Virtual Agent plugin \[com.glide.cs.chatbot\]
-   Human Resources Scoped App: NLU Model\[com.sn\_hr\_nlu\_model\]
-   Human Resources Scoped App: Core \[com.sn\_hr\_core\]

**Important:**

-   The HR Service Delivery Advanced Integration with Workday application is built on Workday web service version 33.2. The application may not be compatible with the previous or later versions of Workday web service version 33.2.
-   For the application to work with the ServiceNow Standard Ticket page, you must install these [update sets](https://store.servicenow.com/sn_appstore_store.do#!/store/application/1575864a1b8de41050d621b5ec4bcbe1/1.0.1?referer=%2Fstore%2Fsearch%3Flistingtype%3Dallintegrations%25253Bancillary_app%25253Bcertified_apps%25253Bcontent%25253Bindustry_solution%25253Boem%25253Butility%25253Btemplate%26q%3DHR%2520Service%2520Delivery%2520advanced%2520Integration%2520with%2520Workday&sl=sh): **standard\_ticket\_rca**
-   For the application to work with Human Resource: Core, you must install these [update sets](https://store.servicenow.com/sn_appstore_store.do#!/store/application/1575864a1b8de41050d621b5ec4bcbe1/1.0.1?referer=%2Fstore%2Fsearch%3Flistingtype%3Dallintegrations%25253Bancillary_app%25253Bcertified_apps%25253Bcontent%25253Bindustry_solution%25253Boem%25253Butility%25253Btemplate%26q%3DHR%2520Service%2520Delivery%2520advanced%2520Integration%2520with%2520Workday&sl=sh): **human\_resources\_core\_rca**
-   For the application to work with Human Resources: Service Portal, you must install these [update sets](https://store.servicenow.com/sn_appstore_store.do#!/store/application/1575864a1b8de41050d621b5ec4bcbe1/1.0.1?referer=%2Fstore%2Fsearch%3Flistingtype%3Dallintegrations%25253Bancillary_app%25253Bcertified_apps%25253Bcontent%25253Bindustry_solution%25253Boem%25253Butility%25253Btemplate%26q%3DHR%2520Service%2520Delivery%2520advanced%2520Integration%2520with%2520Workday&sl=sh): **human\_resources\_portal\_rca**

