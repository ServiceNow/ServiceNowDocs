---
title: Plugin requirements
description: For the Interaction Controls Component \(ICC\) call features to work, you must have a combination of plugins that can be downloaded from the ServiceNow Store and CCaaS providers.
locale: en-US
release: australia
product: Agent Workspace for HR Case Management
classification: agent-workspace-for-hr-case-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Integration with Contact Center as a Service \(CCaaS\), Using Agent Workspace for HR Case Management, Agent Workspace, HR Service Delivery, Employee Service Management]
---

# Plugin requirements

For the Interaction Controls Component \(ICC\) call features to work, you must have a combination of plugins that can be downloaded from the ServiceNow® Store and CCaaS providers.

The CCaaS providers must integrate with the ServiceNow platform. Additionally, they must submit their plugin for certification, to be made available for use from the ServiceNow® Store.

The following plugins are required to deploy the call control integration with the contact center platform:

-   Interaction Controls Component \(ICC\) \(sn\_int\_control\)

    The following plugin and app dependencies are installed as part of the ICC plugin:

    Plugin dependency:

    -   Glide Conversation Server \(com.glide.cs\)
    -   Glide Conversation Server Custom Adapter \(com.glide.cs.custom.adapter\)
    -   Appointment Booking \(com.snc.appointment\_booking\) is required for callback integrations.
    -   Openframe \(com.sn\_openframe\)
    App dependency:

    -   [External Agent Management Util Pack](https://store.servicenow.com/store/app/b1a9af221b246a50a85b16db234bcbf9) \(sn\_external\_agent\)
    -   [Contact Center Integration Core](https://store.servicenow.com/sn_appstore_store.do#!/store/application/31e69bd1934f4210d72e39797bba10ac/1.1.0?referer=%2Fstore%2Fsearch%3Flistingtype%3Dallintegrations%25253Bancillary_app%25253Bcertified_apps%25253Bcontent%25253Bindustry_solution%25253Boem%25253Butility%25253Btemplate%25253Bgenerative_ai%25253Bsnow_solution%26q%3Dcontact%2520center&sl=sh) \(sn\_ct\_ctr\_it\_core\)
    -   [Omnichannel Callback](https://store.servicenow.com/store/app/b1a9af221b246a50a85b16db234bcbf9)\(sn\_omni\_callback\)
    -   [OpenFrame](https://store.servicenow.com/sn_appstore_store.do#!/store/application/3d7925f9eb5002003e97afcef106fee6/26.10.2?referer=%2Fstore%2Fsearch%3Flistingtype%3Dallintegrations%25253Bancillary_app%25253Bcertified_apps%25253Bcontent%25253Bindustry_solution%25253Boem%25253Butility%25253Btemplate%25253Bgenerative_ai%25253Bsnow_solution%26q%3Dopenframe&sl=sh) \(sn\_openframe\)
-   Advanced Work Assignment

    The [External Routing Support](https://www.servicenow.com/docs/access?context=enable-awa-external-routing&version=australia&pubname=australia-conversational-interfaces&ft:locale=en-US) plugin is required for callback integration with contact centers.

-   Agent Workspace, as well as any workspace that works with Agent Chat, Email Interaction, or Messages.
-   Products with [Contact Center Integration Core](https://store.servicenow.com/sn_appstore_store.do#!/store/application/31e69bd1934f4210d72e39797bba10ac/1.1.0?referer=%2Fstore%2Fsearch%3Flistingtype%3Dallintegrations%25253Bancillary_app%25253Bcertified_apps%25253Bcontent%25253Bindustry_solution%25253Boem%25253Butility%25253Btemplate%25253Bgenerative_ai%25253Bsnow_solution%26q%3Dcontact%2520center&sl=sh) Plugin

    -   [Application Spoke Selector](https://store.servicenow.com/sn_appstore_store.do#!/store/search?listingtype=allintegrations%253Bancillary_app%253Bcertified_apps%253Bcontent%253Bindustry_solution%253Boem%253Butility%253Btemplate%253Bgenerative_ai%253Bsnow_solution&q=application%20spoke%20selector)
    -   [External Agent Management Util Pack](https://store.servicenow.com/sn_appstore_store.do#!/store/application/9b13f51343083110bbf3b50afbb8f2f9/1.1.0?referer=%2Fstore%2Fsearch%3Flistingtype%3Dallintegrations%25253Bancillary_app%25253Bcertified_apps%25253Bcontent%25253Bindustry_solution%25253Boem%25253Butility%25253Btemplate%25253Bgenerative_ai%25253Bsnow_solution%26q%3DExternal%2520Agent%2520Mapping%2520Utility%2520Pack&sl=sh)
    **Note:** Address the Contact Center Integration Core plugin dependencies prior to downloading the plugin.


