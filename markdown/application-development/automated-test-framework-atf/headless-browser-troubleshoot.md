---
title: Headless Browser troubleshooting
description: These tips can help you troubleshoot your Linux or Microsoft Windows setup of the ServiceNow Headless Browser for Automated Test Framework.
locale: en-US
release: xanadu
product: Automated Test Framework \(ATF\)
classification: automated-test-framework-atf
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Headless Browser for Automated Test Framework, Test your apps with the ATF, Testing and debugging applications, Building applications]
---

# Headless Browser troubleshooting

These tips can help you troubleshoot your Linux or Microsoft Windows setup of the ServiceNow® Headless Browser for Automated Test Framework.

There are three basic areas to examine when troubleshooting your Headless Browser setup.

## Docker container

Error logs: When the headless test completes, if there are errors they are generated in the Docker container. Whether the operation fails or succeeds, the container's **stdout/stderr** logs are placed in the **sn\_atf\_docker\_service** table.

**Headless client test runner did not start in the time allotted** message: This message generally means an error occurred in the Docker container while it was initializing or starting up. This may indicate something is incorrect in your Docker container setup. Navigate to the **sn\_atf\_docker\_service** table to read the logs and see the error message.

## Instance

**Error caught running Docker flow** when starting the ATF tests messages: Follow the URL address to find the flow context, which contains the error logs. For example, the above error message can display when the instance can't access the Docker host.

## Network errors

Firewalls: Make sure your firewalls are set up so that the instance can access the host and port and the server can access the instance.

## Headless Browser action flow diagram

![Workflow of headless browser](../image/headless-browser-workflow-diagram.png "Example flow diagram")

**Parent Topic:**[Headless Browser for Automated Test Framework](atf-headless-browser.md)

