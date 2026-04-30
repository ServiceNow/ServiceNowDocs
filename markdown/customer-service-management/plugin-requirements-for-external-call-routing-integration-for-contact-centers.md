---
title: Plugin requirements for external call routing integration with contact centers
description: For the Interaction Controls Component \(ICC\) call features to work, you must have a combination of plugins that can be downloaded from the ServiceNow Store and CCaaS providers.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-03-28"
reading_time_minutes: 1
keywords: [Plugins for CCaaS, contact center plugins for nvc, contact center plugins for icc]
breadcrumb: [Implement the Interaction Controls Component \(ICC\) for contact center integration, Enable communication channels, Configuring Customer Service Management, Customer Service Management]
---

# Plugin requirements for external call routing integration with contact centers

For the Interaction Controls Component \(ICC\) call features to work, you must have a combination of plugins that can be downloaded from the ServiceNow® Store and CCaaS providers.

The CCaaS providers must integrate with the ServiceNow platform . Additionally, they must submit their plugins for certification, to be made available for use from the ServiceNow® Store.

**Note:** Verify plugin dependencies against the store listing to ensure you're using the latest compatible versions.

The following plugins are required to deploy the call control integration with the contact center platform:

-   Advanced Work Assignment plugin
-   Customer Service Management \(CSM\)
-   IT Service Management \(ITSM\)
-   Agent Workspace, as well as any workspace that works with Agent Chat, Email Interaction, or Messages.
-   Plugin dependency: com.sn\_openframe
-   App dependency: sn\_openframe, sn\_timer, sn\_ct\_ctr\_it\_core
-   Products with [Contact Center Integration Core](https://store.servicenow.com/sn_appstore_store.do#!/store/application/31e69bd1934f4210d72e39797bba10ac/1.1.0?referer=%2Fstore%2Fsearch%3Flistingtype%3Dallintegrations%25253Bancillary_app%25253Bcertified_apps%25253Bcontent%25253Bindustry_solution%25253Boem%25253Butility%25253Btemplate%25253Bgenerative_ai%25253Bsnow_solution%26q%3Dcontact%2520center&sl=sh) Plugin
    -   [Application Spoke Selector](https://store.servicenow.com/sn_appstore_store.do#!/store/search?listingtype=allintegrations%253Bancillary_app%253Bcertified_apps%253Bcontent%253Bindustry_solution%253Boem%253Butility%253Btemplate%253Bgenerative_ai%253Bsnow_solution&q=application%20spoke%20selector)
    -   [External Agent Management Util Pack](https://store.servicenow.com/sn_appstore_store.do#!/store/application/9b13f51343083110bbf3b50afbb8f2f9/1.1.0?referer=%2Fstore%2Fsearch%3Flistingtype%3Dallintegrations%25253Bancillary_app%25253Bcertified_apps%25253Bcontent%25253Bindustry_solution%25253Boem%25253Butility%25253Btemplate%25253Bgenerative_ai%25253Bsnow_solution%26q%3DExternal%2520Agent%2520Mapping%2520Utility%2520Pack&sl=sh)
-   [OpenFrame](https://store.servicenow.com/sn_appstore_store.do#!/store/application/3d7925f9eb5002003e97afcef106fee6/26.10.2?referer=%2Fstore%2Fsearch%3Flistingtype%3Dallintegrations%25253Bancillary_app%25253Bcertified_apps%25253Bcontent%25253Bindustry_solution%25253Boem%25253Butility%25253Btemplate%25253Bgenerative_ai%25253Bsnow_solution%26q%3Dopenframe&sl=sh)
-   
