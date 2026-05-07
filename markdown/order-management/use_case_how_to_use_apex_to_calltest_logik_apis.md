---
title: Use case: Using Apex to call or test CPQ APIs
description: Learn how to use Apex to call or to test CPQ APIs.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Use cases, Using CPQ, Configure, price, quote apps, Use, Sales Customer Relationship Management]
---

# Use case: Using Apex to call or test CPQ APIs

Learn how to use Apex to call or to test CPQ APIs.

The easiest way to test Apex code for use of CPQ is through the developer console in SFDC.

![User interface](../images/cpq-using-apex-developer-console.png)

To test the script from in the console, the code must be wrapped in a larger class with the “exec” function. For example:

```
public class testGetConfig { public static void exec() {
```

Save the code, and then in the Debug menu, click Execute Anonymous Window.

![Debug menu](../images/cpq-using-apex-anonymous-window.png)

In the execute anonymous window, execute the code `functionName.exec();`

## Example Apex code to call a CPQ API

The following code is an example of an Apex class that will get information about a potential configuration:

```
1 public class testGetConfig {
2 	public static void exec(){
3
4 		HttpRequest httpRequest = new HttpRequest();
httpRequest.setEndpoint('https://tenant.sector.logik.io/api/[config id here]');
httpRequest.setTimeout(5000);
5
6 		httpRequest.setMethod('GET'); httpRequest.setHeader('Content-Type', 'application/json');
7
8 		httpRequest.setHeader('Authorization', 'Bearer [INSERT TOKEN HERE]');
httpRequest.setHeader('Origin', 'https://tenant.sector.logik.io/');
9
10 		Http http = new Http(); HttpResponse httpResponse;
11
12 		httpResponse = http.send(httpRequest);
13
14 	}
15 }
```

This code would be executed as `testGetConfig.exec();`.

**Parent Topic:**[Use cases](use-cases.md)

