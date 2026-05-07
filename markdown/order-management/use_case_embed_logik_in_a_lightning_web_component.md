---
title: Use case: Embed CPQ UI in a Lightning Web Component
description: Learn how to embed CPQ in a LWC in a Salesforce org.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Use cases, Using CPQ, Configure, price, quote apps, Use, Sales Customer Relationship Management]
---

# Use case: Embed CPQ UI in a Lightning Web Component

Learn how to embed CPQ in a LWC in a Salesforce org.

You can embed CPQ in a Lightning Web Component \(LWC\) in a Salesforce org. This eliminates the need to directly navigate to CPQ through a particular product or the CPQ custom URL.

## Steps for Embedding

1.  Download the base LWC package [here](https://drive.google.com/file/d/1MLtv1xUCzXwk-kbDvr9tWTMR4Xuky4Rn/view?usp=sharing), and unzip.
2.  Within an integrated development environment \(IDE—in this example, VSCode\), or on the command line:
    1.  Connect to your Salesforce org using the Salesforce CLI or Salesforce Extensions for the IDE.

        ![Lightening code](../images/cpq-embed-logik-lightning-code.png)

    2.  Open the folder and publish to org using Salesforce CLI or the extensions in your IDE. In VSCode, this means right- clicking the folder in the VSCode explorer and clicking Deploy Source to Org.

        **Note:** To complete this step, you must be connected to the org.

        ![Menu](../images/cpq-embed-logik-lightning-code-deploy.png)

3.  Go into the Salesforce page where you want to embed CPQ.
4.  On the Setup menu, click Edit Page.

    ![User interface](../images/cpq-embed-logik-lightning-edit-page.png)

5.  Drag the Logik LWC from the menu at the bottom left into the page layout where you want to embed CPQ.

    ![Menu bar](../images/cpq-embed-logik-lightning-drag.png)

6.  Add the configuration URL.

    ![Config url](../images/cpq-embed-logik-lightning-config-url.png)

    If you are passing the configuration URL as a parameter, include a Runtime Token in the URL \(for example,`?rt=xxxxxxxxxxxx`\)


**Parent Topic:**[Use cases](use-cases.md)

