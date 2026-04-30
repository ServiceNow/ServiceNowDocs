---
title: Headless Browser system properties
description: Below is a table of the properties you must have as you set up the ServiceNow Headless Browser for Automated Test Framework.
locale: en-US
release: xanadu
product: Automated Test Framework \(ATF\)
classification: automated-test-framework-atf
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Headless Browser for Automated Test Framework, Test your apps with the ATF, Testing and debugging applications, Building applications]
---

# Headless Browser system properties

Below is a table of the properties you must have as you set up the ServiceNow® Headless Browser for Automated Test Framework.

|Property name|Type|Default value|Purpose|
|-------------|----|-------------|-------|
|sn\_atf.headless.browser\_options|string|"--no-sandbox,--disable-gpu"|The CLI options are passed to the browser on startup|
|sn\_atf.headless.default\_browser|string|Chrome|Default browser used when starting up headless requests|
|sn\_atf.headless.default\_os|string|Linux|Operating system of host machine|
|sn\_atf.headless.docker\_image\_name|string| |Name:tag of the Docker image on the host machine|
|sn\_atf.headless.docker\_window\_seconds|int|60|If the Docker container fails to start up twice in this amount of time, the service will not attempt to restart|
|sn\_atf.headless.enabled|true/false|false|Determines whether the instance attempts to create headless client test runners for scheduled UI test runs|
|sn\_atf.headless.heartbeat\_enabled|true/false|true|When property is true, Docker container sends a REST API request every minute to the instance to check that the sys\_atf\_agent is still online, and stops the container if the record status is "offline" or the record no longer exists.|
|sn\_atf.headless.heartbeat\_uri|string|/api/now/atf\_agent/online|The URL of the heartbeat endpoint so container can verify browser is still responsive|
|sn\_atf.headless.images\_check.enabled|true/false|false|When this property is true, the instance verifies that the requested Docker image:tag is present on the host before test execution|
|sn\_atf.headless.login\_button\_id|string|sysverb\_login|The HTML ID of the login page Submit/Login button|
|sn\_atf.headless.login\_page|string|login.do|URL of login page that the browser navigates to|
|sn\_atf.headless.password\_field\_id|string|user\_password|The HTML ID of the input field for the password on the Login page|
|sn\_atf.headless.request\_timeout\_sec|int|200|Number of seconds that HTTP requests being sent to the Docker host have until timeout|
|sn\_atf.headless.retry\_count|int|10|Number of times the instance checks for agent coming online before cancelling the test run|
|sn\_atf.headless.runner\_banner\_id|string|test\_runner\_banner|The ID of the element verifying that client test runner page loaded correctly|
|sn\_atf.headless.runner\_url|string|atf\_test\_runner.do?sysparm\_nostack=true&amp;sysparm\_scheduled\_tests\_only=true&amp;sysparm\_headless=true|URL of the scheduled client test runner page and its query parameters|
|sn\_atf.headless.secret\_gid|string|1000|The GID of the Docker container default user|
|sn\_atf.headless.secret\_id|string| |The ID of the Docker secret on host machine|
|sn\_atf.headless.secret\_name|string| |Name of the Docker secret on host machine|
|sn\_atf.headless.secret\_path|string|/run/secrets/&lt;secret\_name&gt;|Path where Docker secret file exists: \(Learn more: https://docs.docker.com/engine/swarm/secrets/\#how-docker-manages-secrets\)|
|sn\_atf.headless.secret\_uid|string|1000|The UID of the Docker container default user|
|sn\_atf.headless.service\_clean\_exclude\_list|string| |Service ID exceptions that should NOT be deleted during the instance service cleanup job. This job runs every night and deletes any services that are on the host and past their expiration time.|
|sn\_atf.headless.service\_stop\_deletes|true/false|false|On completing of a test execution, if this property is true the instance will NOT send the service delete requests thus keeping the service and containers around on the host. Useful for debugging.|
|sn\_atf.headless.timeout\_mins|int|1440|Number of minutes before Docker service automatically shuts down|
|sn\_atf.headless.user\_field\_id|string|user\_name|The HTML ID of the input field for the username on the Login page|
|sn\_atf.headless.username|string| |Username of user who logs in to the instance|
|sn\_atf.headless.validation\_id|string|headless\_vp\_validation|The ID of the element confirming verification page has loaded|
|sn\_atf.headless.validation\_page|string|atf\_headless\_validation\_page|The URL of the validation page on the instance|
|sn\_atf.headless.vp\_has\_role\_id|string|headless\_vp\_has\_role|The ID of the element verifying that the user has correct roles|
|sn\_atf.headless.vp\_success\_id|string|headless\_vp\_success|The ID of the element signifying entire page loaded correctly|

**Parent Topic:**[Headless Browser for Automated Test Framework](../concept/atf-headless-browser.md)

**Related topics**  


[Headless Browser for Automated Test Framework](../concept/atf-headless-browser.md)

[Test your apps with the ATF](../concept/automated-test-framework.md)

