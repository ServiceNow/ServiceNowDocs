---
title: Use case: Embed ServiceNow CPQ UI in a Lightning Web Component
description: Learn how to embed ServiceNow CPQ in a LWC in a Salesforce org.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/order-management/use\_case\_embed\_logik\_in\_a\_lightning\_web\_component.html
release: zurich
topic_type: concept
last_updated: "2025-10-08"
reading_time_minutes: 1
breadcrumb: [Use cases, Using ServiceNow CPQ, Configure, price, quote apps, Use, Sales Customer Relationship Management]
---

# Use case: Embed ServiceNow CPQ UI in a Lightning Web Component

Learn how to embed ServiceNow CPQ in a LWC in a Salesforce org.

You can embed ServiceNow CPQ in a Lightning Web Component \(LWC\) in a Salesforce org. This eliminates the need to directly navigate to ServiceNow CPQ through a particular product or the ServiceNow CPQ custom URL.

## Steps for Embedding

1.  Download the base LWC package [here](https://drive.google.com/file/d/1MLtv1xUCzXwk-kbDvr9tWTMR4Xuky4Rn/view?usp=sharing), and unzip.
2.  Within an integrated development environment \(IDE—in this example, VSCode\), or on the command line:
    1.  Connect to your Salesforce org using the Salesforce CLI or Salesforce Extensions for the IDE.

        \[Omitted image "cpq-embed-logik-lightning-code.png"\] Alt text: Lightening code

    2.  Open the folder and publish to org using Salesforce CLI or the extensions in your IDE. In VSCode, this means right- clicking the folder in the VSCode explorer and clicking Deploy Source to Org.

        **Note:** To complete this step, you must be connected to the org.

        \[Omitted image "cpq-embed-logik-lightning-code-deploy.png"\] Alt text: Menu

3.  Go into the Salesforce page where you want to embed ServiceNow CPQ.
4.  On the Setup menu, click Edit Page.

    \[Omitted image "cpq-embed-logik-lightning-edit-page.png"\] Alt text: User interface

5.  Drag the Logik LWC from the menu at the bottom left into the page layout where you want to embed ServiceNow CPQ.

    \[Omitted image "cpq-embed-logik-lightning-drag.png"\] Alt text: Menu bar

6.  Add the configuration URL.

    \[Omitted image "cpq-embed-logik-lightning-config-url.png"\] Alt text: Config url

    If you are passing the configuration URL as a parameter, include a Runtime Token in the URL \(for example,`?rt=xxxxxxxxxxxx`\)


**Parent Topic:**[Use cases](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/order-management/use-cases.md)

