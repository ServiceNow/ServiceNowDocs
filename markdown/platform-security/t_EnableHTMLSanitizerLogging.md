---
title: Enabling HTML Sanitizer logging
description: When the HTML sanitizer removes elements or attributes, they are added to the system log.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Enabling HTML sanitizer, HTML sanitizer]
---

# Enabling HTML Sanitizer logging

When the HTML sanitizer removes elements or attributes, they are added to the system log.

## Before you begin

Role required: admin

## About this task

You can review these sanitized elements by adding /syslog\_list.do?sysparm\_query=source%3DHTMLSanitizer to your instance URL.

## Procedure

1.  To review these sanitized elements add `/syslog_list.do?sysparm_query=source%3DHTMLSanitizer` to your instance URL.

2.  To enable or disable logging, add the `glide.html_sanitize.discarded_log.enable` property to the system properties and set the value to **true** \(enabled\) or **false** \(disabled\).

    This property is **true** by default.


