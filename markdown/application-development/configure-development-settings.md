---
title: Configure development settings
description: Set the instance origin, proxy, and development server options for a component project.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/application-development/configure-development-settings.html
release: australia
topic_type: task
last_updated: "2026-10-26"
reading_time_minutes: 1
breadcrumb: [Configure, UI component CLI extension, Building pro-code applications, Developing your application, Classic app development, Building applications]
---

# Configure development settings

Set the instance origin, proxy, and development server options for a component project.

## Before you begin

-   The ui-component extension must be installed. See [Install the UI component CLI extension](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/install-ui-component-cli-extension.md).
-   The Next Experience UI component project must exist.

Role required: admin

## Procedure

1.  Open the now-cli.json file at the root of the component project.

2.  Locate the development object and add the properties you need.

<table id="table_nkt_swm_1lc"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

development.origin

</td><td>

Host of the instance that the proxy server opens with, such as your instance address.Run the `snc configure profile set` command to connect to the instance that it specifies.

</td></tr><tr><td>

development.proxy.proxies

</td><td>

URL glob patterns that the proxy server passes through.

</td></tr><tr><td>

development.proxy.headers

</td><td>

Headers to append to the proxied request.

</td></tr><tr><td>

development.devServer.port

</td><td>

Port that the local development server listens on.

</td></tr><tr><td>

development.devServer.client.overlay

</td><td>

Setting that shows a full-screen browser overlay when the compiler reports errors or warnings. Default is false.

</td></tr></tbody>
</table>    **Important:**

    Don't include your credentials in the now-cli.json file. Configuration files are sometimes pushed to repositories by mistake, and exposed credentials can reveal your username and password on the public internet. Store credentials in the default profile that you set with the `snc configure profile set` command.

3.  Save the now-cli.json file.


## Result

The development server uses the new settings the next time you run `snc ui-component develop`.

## Development settings

```
{
                        "development": {
                        "origin": "https://<instance-name>.service-now.com",
                        "proxy": {
                        "proxies": ["/api"]
                        },
                        "devServer": {
                        "client": {
                        "overlay": false
                        }
                        }
                        }
                        }
```

