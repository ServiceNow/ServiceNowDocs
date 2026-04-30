---
title: Parametrized list screens
description: Learn how to use parameters to pass information into a list screen.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [List screen, Mobile screen types, Mobile screens, Mobile app components, Building mobile apps, Mobile Platform]
---

# Parametrized list screens

Learn how to use parameters to pass information into a list screen.

Use parameters to pass information into a list screen. For example, a user views a grouped list showing records grouped by priority. When a user selects a priority, a list containing records matching that priority displays. This second list needs to know which priority the user selected to display the appropriate records. The system accomplishes this task by passing a parameter. The first list stores the selected priority value in a parameter. The second list uses the information in that parameter to display the appropriate records.

|Incidents grouped by Priority|Incident list with a high priority selected|
|-----------------------------|-------------------------------------------|
|![Grouped list applet with items from the incident table grouped by priority](../image/GroupedListApplet.png)|![Grouped list applet with records from a specific priority selected](../image/GroupedListApplet2.png)|

