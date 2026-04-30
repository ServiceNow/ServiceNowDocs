---
title: Custom license metric example script
description: The following is an example of a custom license metric script.
locale: en-US
release: zurich
product: Software Asset Management
classification: software-asset-management
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Add a custom license metric, Software Asset Management administration, Software Asset Management, IT Asset Management]
---

# Custom license metric example script

The following is an example of a custom license metric script.

**Note:** This example is for demo purposes only and is not meant to be used for actual compliance scenarios.

```
<script><![CDATA[getRightsForDevice();
function getRightsForDevice(){
var rightsForDevice = -1;
	var deviceRecord = new GlideRecord('cmdb_ci_computer');
	if(deviceRecord.get(entity)){
		rightsForDevice = deviceRecord.getValue('disk_space');
	}
	return rightsForDevice;
}]]></script>
```

**Parent Topic:**[Add a custom license metric](../task/add-custom-license-metric.md)

