---
title: Default data patterns
description: Review the default data patterns included in Data Discovery.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/data-discovery/default-data-patterns.html
release: brazil
product: Data Discovery
classification: data-discovery
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Configure patterns, Data Discovery jobs, Exploring Data Discovery \(Classic\), Data Discovery, Platform Privacy]
---

# Default data patterns

Review the default data patterns included in Data Discovery.

The following are the available default patterns for Data Discovery.

|Name|Regular Expression|
|----|------------------|
|Credit Card- Visa|\\b4\[0-9\]\{12\}\(?:\[0-9\]\{3\}\)?\\b|
|Credit Card- American Express|\\b3\[47\]\[0-9\]\{13\}\\b|
|Credit Card- Mastercard|\\b\(?:5\[1-5\]\[0-9\]\{2\}\|222\[1-9\]\|22\[3-9\]\[0-9\]\|2\[3-6\]\[0-9\]\{2\}\|27\[01\]\[0-9\]\|2720\)\[0-9\]\{12\}\\b|
|Credit Card- Diners Club|\\b3\(?:0\[0-5\]\|\[68\]\[0-9\]\)\[0-9\]\{11\}\\b|
|Credit Card- Discover|\\b6\(?:011\|5\[0-9\]\{2\}\)\[0-9\]\{12\}\\b|
|Social security number|\\b\(?!666\|000\|9\\d\{2\}\)\\d\{3\}-\(?!00\)\\d\{2\}-\(?!0\{4\}\)\\d\{4\}\\b|
|Email|\\b\[\\w!\#$%&amp;'\*+/=?\`\{\|\}~^-\]+\(?:\\.\[\\w!\#$%&amp;'\*+/=?\`\{\|\}~^-\]+\)\*@\(?:\[a-zA-Z0-9-\]+\\.\)+\[a-zA-Z\]\{2,6\}\\b|
|USA- Phone Number|\\b\\\(?\(\[0-9\]\{3\}\)\\\)?\[-. \]?\(\[0-9\]\{3\}\)\[-. \]?\(\[0-9\]\{4\}\)\\b|

