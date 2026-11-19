---
title: Telemetry in ServiceNow Extensions for VS Code
description: ServiceNow Extensions for VS Code collects information on its various usage patterns such as the commands run with the help of Now Telemetry.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/application-development/telemtry-vscode.html
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [ServiceNow Extensions for Visual Studio Code, Building pro-code applications, Developing your application, Building applications]
---

# Telemetry in ServiceNow Extensions for VS Code

ServiceNow Extensions for VS Code collects information on its various usage patterns such as the commands run with the help of Now Telemetry.

Now Telemetry helps in the following

-   Debug issues
-   Analyse most used functions or features
-   Capture user actions
-   Improve the extension

**Note:** Telemetry collects anonymous information related to usage and does not capture any personal information such as name and email ID of the users. Data is accessible to ServiceNow only and is not shared with anyone

Telemetry is enabled by default for the ServiceNow extension. If you do not wish to send usage data, you can set the `now.telemetry.enableTelemetry` user setting to false. Alternatively, select **File** \(Windows\) or **Code** \(Mac\) and navigate to **Preferences** &gt; **Settings** &gt; **Extensions** &gt; **Now** and clear **Now Telemetry** check box to disable the feature.

\[Omitted image "telemetry-vscode.png"\] Alt text: Telemetry in VS code extension

**Note:** The usage data will be sent until you disable the setting. The extension abides by the global telemetry setting `telemetry.enableTelemetry`. If that is set to false, Now telemetry is disabled.

**Parent Topic:**[ServiceNow Extensions for Visual Studio Code](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/vs-code.md)

