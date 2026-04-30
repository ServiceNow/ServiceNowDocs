---
title: Location hierarchy and child locations
description: The list of impacted people is populated based on the selected location and includes individuals from any child locations in the Location \[cmn\_location\] table hierarchy.
locale: en-US
release: zurich
product: Critical Event Management
classification: critical-event-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure, Critical Event Management, Health and Safety, Employee Service Management]
---

# Location hierarchy and child locations

The list of impacted people is populated based on the selected location and includes individuals from any child locations in the Location \[cmn\_location\] table hierarchy.

The Location table supports a hierarchical parent-child structure, so child locations are nested under primary parent locations. Each child location can also have its own child locations.

When a critical event is assigned to a parent location, the system automatically includes all individuals associated with that location and any child locations. For example, selecting USA as the parent location \(Location1\) would include child locations such as California \(Location2\).

To configure, see [Define a location hierarchy](https://www.servicenow.com/docs/access?context=define-tni-locations&version=zurich&pubname=zurich-telecom-network-inventory&ft:locale=en-US)

