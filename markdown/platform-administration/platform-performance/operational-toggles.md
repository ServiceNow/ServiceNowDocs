---
title: Operational toggles
description: You can control how much bandwidth an application uses on your system by mapping system run levels to operational toggles. An excessive bandwidth could impact your system performance and your users' experience.
locale: en-US
release: zurich
product: Platform Performance
classification: platform-performance
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure, Platform performance, Maintain and monitor, Administer]
---

# Operational toggles

You can control how much bandwidth an application uses on your system by mapping system run levels to operational toggles. An excessive bandwidth could impact your system performance and your users' experience.

## Operational toggles overview

You can use system run levels to map descriptive names to operational toggle levels. System run levels define the operational state of your system based on the toggles and toggle levels you have configured. These levels help you manage the system's performance and resource allocation.

Operational toggles can be used to throttle application performance during high-use periods. By adjusting operational toggles, you can limit the number of events or jobs running within an application's scope to help prevent system overload.

You can also create operational toggles to enhance user experience. For example, a type-ahead search polling toggle might help users complete searches more quickly. You could add this toggle to enable users to perform type-ahead searches based on keystroke values, providing real-time search suggestions as they type.

## Operational toggle levels

You can create different levels of your desired toggle. For example, you might want to perform a type-ahead search every keystroke or every fifth keystroke. For more information about toggle levels, see [Create an operational toggle level](../task/create-operational-toggle-level.md).

## Run level toggle mapping

You can associate the system run level to the toggle level with toggle mapping. Depending on your instance health, the API returns the appropriate toggle level value and exception roles. For information about how to create run level toggle mapping, see. [Create run level toggle mapping](../task/create-run-level-toggle-mapping.md).

