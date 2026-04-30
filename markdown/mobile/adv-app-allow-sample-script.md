---
title: Advanced app allowance example script
description: Users with the admin role can use the example JSON script to configure a scripted extension point. Admins can use these scripted extension points to limit which mobile apps can log in to ServiceNow instances. These scripts can also be used to specify a redirect link to authorized mobile apps.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configure advanced app allowance with links to permitted apps, Control specific app usage, Configuring the Mobile Platform, Mobile Platform]
---

# Advanced app allowance example script

Users with the admin role can use the example JSON script to configure a scripted extension point. Admins can use these scripted extension points to limit which mobile apps can log in to ServiceNow instances. These scripts can also be used to specify a redirect link to authorized mobile apps.

## Example script

The following example script blocks all apps except the Mobile Agent app and the Now Mobile app.

All other apps are restricted. This script also uses the **blocked\_mobile\_apps\_redirect** property. When an end user attempts to log in with an unauthorized app, an error message appears with a redirect button. That button redirects the end user to log in to a mobile app that is authorized to connect to the ServiceNow instance.

```
var CustomPreAuthProperties = Class.create(); 
CustomPreAuthProperties.prototype = { 
    initialize: function() {}, 

    /** 
     * Returns a JSON object keyed by the custom property names. 
     */ 
    getProperties: function(input) { 
        var customProperties = {}; 
        if (input.clientType == "agent") { 
            customProperties['allowed_mobile_apps'] = 'com.servicenow.fulfiller'; 
            if (input.deviceType == 'android') { 
                customProperties['blocked_mobile_apps_redirect'] =  
				'https://play.google.com/store/apps/details?id=com.servicenow.fulfiller&hl=en_US&gl=US'; 
            } else { 
                customProperties['blocked_mobile_apps_redirect'] =  
				'https://apps.apple.com/us/app/servicenow-agent/id1446951408'; 
            } 
        } else if (input.clientType == 'request') { 
            customProperties['allowed_mobile_apps'] = 'com.servicenow.requestor'; 
            if (input.deviceType == 'android') { 
                customProperties['blocked_mobile_apps_redirect'] =  
				'https://play.google.com/store/apps/details?id=com.servicenow.requestor&hl=en_US&gl=US'; 
            } else { 
                customProperties['blocked_mobile_apps_redirect'] =  
				'https://apps.apple.com/us/app/now-mobile/id1469616608'; 
            } 
        } 

        return customProperties; 
    }, 

    type: 'CustomPreAuthProperties' 
};
```

This sample script uses the following JSON objects:

-   `input.clientType` which determines the mobile app type.
-   `input.deviceType` which determines the operating system type.

