---
title: Forms
description: The Forms components help you to trigger attended automations that are enabled with the Embedded Task Automation.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/workflow-data-fabric/forms\_sn\_rpa\_studio.html
release: australia
product: Workflow Data Fabric
classification: workflow-data-fabric
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [ServiceNow, Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Workflow Data Fabric]
---

# Forms

The Forms components help you to trigger attended automations that are enabled with the Embedded Task Automation.

Ensure you are familiar with Embedded Task Automation concepts. For more information, see [Embedded Task Automation \(ETA\) in RPA Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/workflow-data-fabric/embedded-task-auto-rpa.md).

-   **[Use the AttendedConfigurations component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/workflow-data-fabric/use-attended-configurations-forms.md)**  
When you use the AttendedConfigurations component, it shows a list of attended configurations associated to the selected same bot process. To select and give control out port for each configuration that routes the automation logic.
-   **[Use the GetProcessFieldParameters component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/workflow-data-fabric/use-get-process-field-param-forms.md)**  
Gets the values of the associated **Table** fields mapped to the process field parameter, that you had configured in an attended configuration record of a bot process. The component returns both the individual values of the parameters and all values as an object. This component reads the value of the associated **Table** field in the ServiceNow form record.
-   **[Use the GetRecordContextID component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/workflow-data-fabric/use-get-record-context-id-forms.md)**  
Get the Sys ID of the ServiceNow form record that is associated to an attended configuration with the GetRecordContextID component in the RPA Desktop Design Studio. Sys ID is the output of the component. For example, Sys ID is used to fetch the attachments in a record.
-   **[Use the SetProcessFieldParameters component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/workflow-data-fabric/use-set-process-field-param-forms.md)**  
Sets the values of the associated **Table** fields mapped to the process field parameter, that you had configured in an attended configuration record of a bot process. This component updates the values of the configured field parameters associated to the **Table** field in the ServiceNow form record.
-   **[Properties of the Forms components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/workflow-data-fabric/sn-forms-properties.md)**  
Learn about the properties of the Forms components in RPA Desktop Design Studio.

**Parent Topic:**[ServiceNow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/workflow-data-fabric/servicenow.md)

