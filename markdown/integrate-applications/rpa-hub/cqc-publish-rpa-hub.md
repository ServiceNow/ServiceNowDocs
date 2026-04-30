---
title: Code quality check compliance for RPA Hub
description: View a list of compliance rules that the Code Quality Check feature follows if a bot process is published from RPA Hub.
locale: en-US
release: zurich
product: RPA Hub
classification: rpa-hub
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Reference, RPA Hub, Robotic Process Automation \(RPA\) Hub, Workflow Data Fabric]
---

# Code quality check compliance for RPA Hub

View a list of compliance rules that the Code Quality Check feature follows if a bot process is published from RPA Hub.

|Code Quality Check status of the package version|Restriction on publishing \(Based on the system property **sn\_rpa\_fdn.restrict\_package\_by\_severity**\)|Publish of bot process created from package version|
|------------------------------------------------|-----------------------------------------------------------------------------------------------------------|---------------------------------------------------|
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


[Publish a bot process in RPA Hub](../task/publish-bot-process.md)

[Code quality check compliance for RPA Desktop Design Studio](cqc-publish-studio.md)

[Code quality check in RPA Hub](../concept/code-quality-check-rpa.md)

