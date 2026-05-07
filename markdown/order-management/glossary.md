---
title: Glossary
description: A list of terms used in CPQ
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [CPQ, Configure, price, quote, Reference, Sales Customer Relationship Management]
---

# Glossary

A list of terms used in CPQ

-   **Associated Picklist \(AP\)**

    CPQ functionality that allows a set to be generated with predetermined rows based on the selection of a picklist field.

-   **API \(Application Programming Interface\)**

    A way for two or more computer programs to communicate with each other. In the context of CPQ, APIs are categorized into runtime APIs \(create, update and save configurations\) and admin APIs \(works with blueprints, fields, rules, configurable products, managed tables, and various automation tasks\).

-   **Bill of materials \(BOM\)**

    A list of parts and components needed to manufacture a product.

-   **Blueprint**

    A collection of associated CPQ rules and fields utilizing a layout that defines a configuration experience. Identifying a product as a configurable product for a blueprint means it will launch the related configuration experience when selected.

-   **BOM type**

    A category in which products in the BOM will be organized under \(such as sales or manufacturing\).

-   **Buyside**

    Refers to the CPQ experience that the end user sees.

-   **Configurable product**

    A product that is associated with a blueprint that kicks off the CPQ configuration experience. The relationship to the blueprint differs whether CPQ is being used as a headless application or in Salesforce.

-   **Configuration Line Item \(CLI\)**

    Records that are generated from a configuration and associated with the Configuration Line Item object. A configuration ID lets related configuration line items be grouped together.

-   **CPQ \(Configure, Price, Quote\)**

    A category of sales software that lets users configure products and services, apply pricing, and generate price quotes.

-   **CRM \(Customer Relationship Management\)**

    Software that manages all your companyʼs relationships and interactions with customers and prospects. Some examples are Salesforce and Microsoft Dynamics, but there are many more.

-   **Enrichments**

    Scripts that run outside of the rules engine that affects configurations in CPQ. Enrichments can run on configure, on reconfigure, on BOM response, or via picklist extension pricing.

-   **Expert Services \(ES\)**

    Consulting hours purchased from the CPQ Expert Services team to receive design or implementation guidance, request build work to be done, etc.

-   **External Connections**

    Allows for data for a CPQ configuration to be retrieved from outside of CPQ. Called from in an enrichment.

-   **Field**

    Allows input to be gathered from the end user and stores data. There are several types of Fields that can be used to meet various needs, including: text, date, Boolean, number, and picklist.

-   **[Field grid](https://logikio.atlassian.net/wiki/spaces/CS/pages/1615134762)**

    A series of fields displayed as a matrixed layout.

-   **Flightpath**

    CPQ feature that allows administrators to record a configuration session tracks end-user inputs and how the CPQ rules engine responds.

-   **Go-Live**

    When your CPQ implementation is moved to a production environment and begins to be used by end users in some capacity.

-   **Headless application**

    An application where the backend \(data, logic, and functionality\) is decoupled from the frontend \(user interface\). CPQ is headless in the sense that customers can leverage its powerful functionality via APIs in their desired techstack.

-   **Layout**

    The visual experience that an end user sees when configuring a product in CPQ. Every blueprint in CPQ has a layout that can be customized by the Admin. Beginning at the lowest level, layouts contain fields, which are housed in columnsets. Finally, columnsets are situated in containers called tiers, which can be nested if desired.

-   **Matrix Loader**

    A feature in CPQ that enables the bulk upload of multiple types of data into CPQ, such as data in CSV files or entire CPQ blueprints.

-   **Migration**

    The act of moving your CPQ work from one environment to another. This could be from one test environment to another, or from a test environment to a production environment.

-   **Picklist extension \(PLE\)**

    CPQ feature for picklist field options that allows product info or additional info to be displayed, as well as filtering options.

-   **[Price Book Entry \(PBE\)](https://help.salesforce.com/s/articleView?id=sf.pricebooks_landing_page.htm&type=5)**

    Price books associate products with their prices in Salesforce.

-   **Product**

    A product can refer to many things, such as the companyʼs product itself, a configurable product \(e.g “Computer”\) or product part \(e.g. “Motherboard”\) in CPQ, and even an entry of the company product in a CRM like Salesforce.

-   **Product action**

    CPQ functionality used in tandem with a rule. The rule would specify the conditions that need to be met, and a product action can be defined to add a product to the BOM accordingly.

-   **Product ID**

    A unique identifier for a product, commonly used to refer to the unique IDs for products in Salesforce. An example of a Product ID is `01tHn00000VB38mIAD`.

-   **Product picker \(PP\)**

    This functionality allows you to display a number of options that represent products. When options are selected, the product will be added to the BOM. Additional columns of new or existing fields can also be appended to surface more metadata along with the ability to aggregate.

-   **Production environment**

    A CPQ Production environment represents your live and active environment currently being utilized, and is the most sensitive. Best practices are to do any implementation work in your test/sandbox CPQ environment, test it, and then migrate the work to your production environment along with some final testing.

-   **Quote Calculator Plugin \(QCP\)**

    A plugin for Salesforce CPQ that provides extra functionality in the quote line editor by means of custom JavaScript code.

-   **Quote Line Editor \(QLE\)**

    When using Salesforce CPQ, this interface allows you to add/remove products, apply discounts and markups, and calculate prices for the quote.

-   **Rule**

    Comprising conditions and actions, and associated with a blueprint, rules are the powerhouse that provides the ability to hide/show content, deliver recommendations and messages, add products to a BOM, and more.

-   **Rule action**

    Defined in a rule, rule actions are what will fire when a ruleʼs conditions are met. Action types consist of hiding/showing, excluding/including, Messages, adding products, Determination \(populating fields with metadata\), and more.

-   **Sandbox environment**

    A type of environment that should be used to build-out new implementations or features of CPQ according to best practices. Once built and tested, the work can be moved into a Production environment and tested again before use in an active workflow. Also known as a test environment.

-   **Service level agreement \(SLA\)**

    The level of service expected from a vendor. An example of a CPQ SLA could be how quickly customers can expect a support case to be acknowledged after being created.

-   **Set**

    A feature that groups fields so they can be multiply replicated in the end-userʼs UI in a matrix format. Sets reduce the number of fields and rules that need to be defined in scenarios where the same fields are being repeated. Analogous to Configuration Arrays in Oracle.

-   **Set repeater**

    Functionality that allows you to easily create new indices in a set.

-   **System Integration Testing \(SIT\)**

    A QA process to ensure the compatibility of two or more systems.

-   **Table**

    CPQ has tables \(relational databases\) that allow data to be stored, which can then be retrieved using able lookups.

-   **Table lookup**

    Utilizing a programming language called SQL \(Structured Query Language\), tables in CPQ can be queried using scripts to retrieve specific information.

-   **Test environment**

    See Sandbox environment.

-   **Twinning**

    The ability to automatically pull data from a Salesforce quote field into a CPQ field by creating a CPQ quote custom field using the format “&lt;fieldName&gt;LGK” in Salesforce, and a matching “&lt;fieldName&gt;” in CPQ.

-   **User acceptance testing \(UAT\)**

    Also known as end-user testing, this is a phase near the end of implementation and before going live. A small group of the end-users will run through various scenarios to validate the desired end-user experience and address any issues or bugs before the full launch.


**Parent Topic:**[CPQ reference](../reference/servicenow-cpq-reference.md)

