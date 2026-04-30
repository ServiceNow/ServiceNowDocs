---
title: Limitations of Robotic Process Automation \(RPA\) bot generation skill
description: The limitations of the RPA bot generation skill are as follows.
locale: en-US
release: yokohama
product: RPA Hub
classification: rpa-hub
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 3
keywords: [Now Assist, generative AI]
breadcrumb: [Now Assist for RPA Hub reference, Now Assist for RPA Hub, Robotic Process Automation \(RPA\) Hub, Data and Automation]
---

# Limitations of Robotic Process Automation \(RPA\) bot generation skill

The limitations of the RPA bot generation skill are as follows.

-   **AI Search and LLM timeout**

    The RPA bot generation skill relies on AI Search and large language models \(LLM\) to understand the user instructions and flow creation. The timeout limits and rate-limiting behavior of these APIs collectively apply to the RPA bot generation skill. For more information about AI search system properties, see [AI Search system properties](https://www.servicenow.com/docs/access?context=system-properties-ais&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US). For more information about API rate limits, see [Inbound REST API rate limiting](https://www.servicenow.com/docs/access?context=inbound-REST-API-rate-limiting&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US). For more information about configuring rate limiting for providers, see [Configure rate limiting for providers](https://www.servicenow.com/docs/access?context=configure-rate-limit&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US).

-   **Component scope in Yokohama release**

    The initial version supports few components. Components outside this scope don't appear in the generated automation workflow. For example, if you provide an instruction, such as `Capture a screen shot and save it in the location at 'C:\Users\Screens'`, the generated automation workflow might not contain the Capture component because it isn’t included in the initial version components list. For more information about the list of supported components, see [Supported components and connectors for Now Assist for RPA Hub in Yokohama release](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1808191).

-   **Plugin version compatibility**

    The feature uses Yokohama version plugins. If the large language model \(LLM\) returns a method that doesn’t exist in the loaded plugin version, then such methods are displayed as unknown components in the generated automation workflow. For example, if you’re using Washington DC version plugins within an existing automation project and provide an instruction to set or get values from an application, then the SetValue, GetValue, or Click methods of the Universal App connector are displayed as unknown components in the generated automation workflow.

    In the following example, to get the weather information, data reader components are required. Since they are not available in the current scope, they appear as UNKNOWN components in the automation preview.

    ![Automation preview section displays UNKNOWN components.](../image/weather-data-reader-uc-narh.png "Unknown components in the Automation preview")

    If you select **Next** in the previous screen, the automation appears as follows on the Design surface.

    ![Design surface displays UNKNOWN components.](../image/unknown-comp-rpa-na-t2b.png "Unknown components on the Design surface")

-   **Usage of existing connectors in new activity using Now Assist or build automation context menu options**

    During the automation workflow creation, if a method, such as the AddNewWorksheet method of Microsoft Excel connector is created, RPA Desktop Design Studio checks for an existing global object of the same connector type and uses the most recent one. In the following example, the Badging Data Microsoft Excel connector is used.

    ![Project Explorer section displays Microsoft Excel connectors in the Global Objects. Badging Data Microsoft Excel connector is selected.](../image/global-obj-recent.png "Microsoft Excel connectors in Global Objects")

-   **Dynamic configuration**

    Dynamic configuration for supported components isn’t available in the Yokohama release. You can configure components manually. For example, you must give inputs in the configuration window for the Microsoft Excel connector's SetCellValues method. Select the settings icon \(![Settings icon.](../image/component-settings-icon.png)\) to view the configuration window.

    Data in the parameter values might not be populated in the large language model \(LLM\) generated components.

    ![Configuration window for the SetCellValues method is displayed.](../image/dynamic-config-limitation.png "Configuration window for SetCellValues method")

-   **Automation for Windows, Java, or browser applications**

    For automating Windows, Java, or browser-based applications, RPA Desktop Design Studio suggests generic UI actions such as SetValue, GetValue, or Click. These actions are a part of the Universal app connector. You must configure these actions manually, including capturing screens and adding elements via the field window. For more information about these methods, see [Universal app connector](../concept/universal-app-connector.md).

-   **Expression-based components**

    For components that require expressions, such as Decision or Expression, and so on, expressions in these components aren’t automatically populated in the Yokohama release.

-   **Hallucinated components**

    If the large language model \(LLM\) returns a method that doesn’t exist in the RPA Desktop Design Studio, then such methods are displayed as unknown components in the generated automation workflow.


**Parent Topic:**[Now Assist for RPA Hub reference](../concept/now-assist-rpa-hub-reference.md)

