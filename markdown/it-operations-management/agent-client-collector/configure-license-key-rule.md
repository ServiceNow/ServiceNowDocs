---
title: Configure a license key discovery rule and write a parser script
description: Enable license key discovery to verify the legitimacy of your software installation. Set up support for a new vendor's license file format by creating a parser script and defining a matching rule.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-operations-management/agent-client-collector/configure-license-key-rule.html
release: zurich
product: Agent Client Collector
classification: agent-client-collector
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 3
keywords: [license key discovery, parser script, file-based discovery, configuration]
breadcrumb: [Discovering a license key in a file-based discovery framework, Agent Client Collector File-Based Discovery, ACC deployment - endpoints, Agent Client Collector, IT Operations Management]
---

# Configure a license key discovery rule and write a parser script

Enable license key discovery to verify the legitimacy of your software installation. Set up support for a new vendor's license file format by creating a parser script and defining a matching rule.

## Before you begin

Role required: agent\_client\_collector\_admin or discovery\_admin

## About this task

To discover license keys from a vendor's license file format, you must create the following complementary configuration records:

-   A parser script that knows how to extract license information from the specified file format.
-   A file-matching rule that tells the framework when to invoke that parser.

The parser is created first because the file-matching rule references it.

## Procedure

1.  Write the parser script on the **License Parsers** page.

    1.  Enter **sn\_acc\_vis\_content\_license\_parser.list** into the navigation menu.

    2.  Select **New**.

    3.  Enter a name into the **Parser Name** field.

    The parser is a small piece of server-side JavaScript that receives the raw text content of a matched file and extracts license information from it.

    The script must extract the following information where available:

    -   Product name
    -   Vendor name
    -   License key
    -   Expiry date \(if present in the file\)
    The script must set a variable called `answer` to an array of result objects. Create one object per license entry found in the file — a single file can contain multiple products' licenses. If the script fails to set `answer` as an array, the parser is treated as invalid.

    Example structure of a result object:

    ```
    {
      product_name: "Product Name",
      vendor: "Vendor Name",
      license_key: "ABC123DEF456",
      expiry_date: "2026-12-31"
    }
    ```

2.  Validate the parser script before using it on real data.

    Every License Parser record includes a **Test Parser** link in the **Related Links** section. To validate your script, do the following on the License Parser record page:

    1.  Fill in the **sample\_input** field with representative file content.
    2.  Fill in the **sample\_output** field with the exact result you expect the parser to produce.
    3.  Select **Test Parser**.
    The Test Parser executes your script against the sample input using the exact same code path used during a real scan. It reports whether the actual result matches the expected sample output, catching mistakes before the parser processes real license files.

3.  Create a License File Configuration record to define the matching rule.

    With the validated parser in place, create a License File Configuration record that describes which file to look for. Enter **sn\_acc\_vis\_content\_license\_file\_config.list** in the navigation menu and specify the following:

    -   **display\_name** — A unique name identifying the rule
    -   **file\_name** — The file name or partial name to match \(for example, "ProductLicense"\)
    -   **file\_name\_condition** — How to match the file name: `exact_match` \(default\), `starts_with`, `ends_with`, or `contains`
    -   **file\_extension** — Optional file extension to narrow the match further \(do not include a leading dot before the extension\)
    -   **platform** — The operating system\(s\) the rule applies to: `all` \(default\), `windows`, `linux`, or `mac`
    -   **parser** — Reference to the parser created in the previous steps
    -   **order** — Priority when multiple rules could match the same file \(default 100; lower values win\)
    -   **active** — Indicates whether the rule is currently in use \(default = true\)
4.  Enable license key discovery in the system.

    Ensure that the following components are active:

    -   System property `sn_acc_vis_content.enable_license_key_discovery` — Set to **true**
    -   Policy `File Based Discovery Policy - License Key` — **Active**
    -   Check definition `File Based Discovery - License Key` — **Active**
    After enabling these components, the agent will begin scanning for files matching your License File Configuration rule during its regular file-scanning activity.


## Result

Your new rule is active and the agent will automatically discover license keys from files matching your configuration. The discovered licenses appear in the appropriate tables when they are successfully matched in the software catalog.

