---
title: Code quality check compliance for RPA Desktop Design Studio
description: View a list of compliance rules that the Code Quality Check feature follows if a package is published from RPA Desktop Design Studio.
locale: en-US
release: xanadu
product: RPA Hub
classification: rpa-hub
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [RPA Hub reference, RPA Hub, Robotic Process Automation \(RPA\) Hub, Creating integrations with applications]
---

# Code quality check compliance for RPA Desktop Design Studio

View a list of compliance rules that the Code Quality Check feature follows if a package is published from RPA Desktop Design Studio.

|Code Quality Check status of the automation project|Restriction on publishing \(Based on the system property **sn\_rpa\_fdn.restrict\_package\_by\_severity**\)|Publish of package to connected instance|
|---------------------------------------------------|-----------------------------------------------------------------------------------------------------------|----------------------------------------|
|Error|Error|Error to publish|
|Error|Error or Warning|Error to publish|
|Error|No restriction|Success|
|Warning|Error|Success|
|Warning|Error or Warning|Error to publish|
|Warning|No restriction|Success|
|Pass|Error|Success|
|Pass|Error or Warning|Success|
|Pass|No restriction|Success|

**Parent Topic:**[RPA Hub reference](rpa-hub-reference.md)

**Related topics**  


[Publish an automation project in RPA Desktop Design Studio](../../rpa-studio/task/publish-automation-project.md)

[Code quality check in RPA Desktop Design Studio](../../rpa-studio/concept/code-quality-check-studio.md)

[Code quality check compliance for RPA Hub](cqc-publish-rpa-hub.md)

[Code quality check in RPA Hub](../concept/code-quality-check-rpa.md)

