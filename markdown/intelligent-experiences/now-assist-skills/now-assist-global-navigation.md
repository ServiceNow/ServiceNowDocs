---
title: Navigation
description: Use the navigation skill in Now Assist to take you where you want to go on the ServiceNow AI Platform.
locale: en-US
release: zurich
product: Now Assist Skills
classification: now-assist-skills
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
keywords: [now, assist, global, navigation, skills, LLM, Generative AI, Gen AI]
breadcrumb: [Skills in the Platform workflow, Now Assist skills, Now Assist AI assets, Enable AI experiences]
---

# Navigation

Use the navigation skill in Now Assist to take you where you want to go on the ServiceNow AI Platform.

## Overview of navigation

Navigation is a skill in the Now Assist panel that handles record search requests during a chat. When you ask for records or tables in plain language Now Assist shows you links in the chat to take you to the best match to your request. For example, you could enter `Show me incident records`.

In the following figure, the user entered `navigate me to incidents` in the Now Assist panel. Now Assist responds with a link to the Incidents table.

![When the user types, "navigate me to incidents," Now Assist responds with a link to the records in the Incidents table.](../../virtual-agent/images/na-global-nav-2.png "Navigation query and response in the Now Assist panel")

When you click the link, the list of all records in the Incidents table displays.

![Selecting the link in the chat takes you to the requested area.](../../virtual-agent/images/na-global-nav-3.png "Navigating to the Incidents table from the Now Assist panel")

## Refining your results

You can refine your results further by using more detailed requests. If you enter `Show me all incident records whose status is Complete`, Now Assist shows you only the records in the table with a Complete status.

In the following example, the user asks for all P1 incidents that are in the New state.

![You can include multiple specific terms to refine your search, such as Priority 1 or State is New.](../../virtual-agent/images/na-global-nav-4.png "A refined query of the Incidents table")

The number of results is based on how many potential results Now Assist finds in response to your request. If Now Assist finds more than 10 results, the list is paginated. In the following example, Now Assist finds two possible tables: the Catalog Item table and the Catalog table.

![If Now Assist finds multiple possible results, it presents them for you to select your choice.](../../virtual-agent/images/na-global-nav-5.png "Multiple table results in the Now Assist panel")

If Now Assist does not understand your request, you receive an error message asking you to rephrase your request. You can also choose to navigate to a "best guess" based on your previous request.

![If Now Assist receives an unclear request, you are prompted to rephrase your request.](../../virtual-agent/images/na-global-nav-6.png "Rephrase request message in the Now Assist panel")

**Parent Topic:**[Now Assist skills in the Platform workflow](now-assist-on-now-platform.md)

