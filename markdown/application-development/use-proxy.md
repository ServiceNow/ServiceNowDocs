---
title: Use a proxy server with ui-component extension
description: Use a proxy server with the Now CLI to define a separate data source for your component. When using a proxy server, the instance forwards Now CLI requests to the proxy server.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Create custom components using ServiceNow CLI, Builder library, Developing your application, Building applications]
---

# Use a proxy server with ui-component extension

Use a proxy server with the Now CLI to define a separate data source for your component. When using a proxy server, the instance forwards Now CLI requests to the proxy server.

## Before you begin

[Set up your environment](set-up-environment.md).

## Procedure

1.  In your component directory, open the `now-cli.json` file.

2.  Update the `proxy` object.

    ```
    {
    	development: {		
    		proxy: {
    			headers: {
    				Authorization: "Basic <username:password>"
    			},
    			origin: "http://myinstance.servicenow.com",
    			port: 3000,
    			proxies: []
    		}
    	}
    }
    
    ```

    Update the following parameters with your proxy information.

    |Parameter|Description|
    |---------|-----------|
    |development.proxy.headers|Headers to append to your proxied request.|
    |development.proxy.headers.Authorization|Authentication header to add to the proxied request. Enter your Base 64-encoded username:password here.|
    |development.proxy.origin|Host to open a proxy with \(your instance host address\).|
    |development.proxy.port|The port the proxy runs on.|
    |development.proxy.proxies|URL glob patterns to pass to the proxy server.|

3.  Save the file.


## What to do next

[Develop a component](develop-component.md).

**Parent Topic:**[Create custom components using ServiceNow CLI](../concept/custom-components.md)

**Related topics**  


[Create custom components using ServiceNow CLI](../concept/custom-components.md)

