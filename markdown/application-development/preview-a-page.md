---
title: Preview a page
description: Preview a page from within Lux Lab to test that it appears and functions as intended. The preview updates automatically as you save source files, without a full page reload.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/application-development/preview-a-page.html
release: zurich
topic_type: task
last_updated: "2026-09-30"
reading_time_minutes: 1
keywords: [Preview a page]
breadcrumb: [Using Lux Lab, Lux Lab, Building pro-code applications, Developing your application, Building applications]
---

# Preview a page

Preview a page from within Lux Lab to test that it appears and functions as intended. The preview updates automatically as you save source files, without a full page reload.

## Before you begin

Role required: admin

Your machine meets the minimum system requirements in [Configuring Lux Lab](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/configuring-lux-lab.md).

## About this task

You can also start the development server by selecting **Run** or **Preview** in the title bar, which opens the running application in the Preview panel.

## Procedure

1.  Open a Lux Lab project.

2.  In the Explorer panel, navigate to the `/pages` folder.

3.  Hover over the file of the page to preview, or over its parent folder, to reveal the inline **View** icon \(an eye\).

4.  Select the **View** icon.


## Result

A preview of your page opens as an embedded browser tab. The preview toolbar has the controls in the following table.

|Control|Description|
|-------|-----------|
|URL bar|Path or URL editor that navigates when you press Enter|
|Refresh|Preview page reload button|
|Open in browser|Button that opens the current URL in your default system browser|
|Device presets|Viewport size selector for Mobile, Tablet, and Desktop presets|
|Screenshot|Screenshot tool that captures the current preview and sends it to the Agent Chat panel|

Saving a source file triggers Hot Module Replacement \(HMR\), which updates the preview automatically without a full page reload.

