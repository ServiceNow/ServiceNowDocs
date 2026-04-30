---
title: Add custom file types in Visual Studio Code
description: If you have work with file types other than the default types provided, you can add additional file types to your instance and edit them in ServiceNow extension for Visual Studio Code.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [ServiceNow Extensions for Visual Studio Code, Building pro-code applications, Developing your application, Building applications]
---

# Add custom file types in Visual Studio Code

If you have work with file types other than the default types provided, you can add additional file types to your instance and edit them in ServiceNow extension for Visual Studio Code.

## Before you begin

Role required: admin

## Procedure

1.  Create a new file type in your ServiceNow instance and inherit it from the application file.

2.  Add custom columns of the type **Script** and **String**, and enter some data.

3.  Navigate to **View** &gt; **Command Palette** in Visual Studio Code.

    You can also use a keyboard shortcut, Control+Shift+P on Windows or Command+Shift+P on MacOS, to open the command palette.

4.  Choose **Now: Add Custom File Types** from the command palette.

    The command fetches all the existing tables in the current application and opens the **Add new file type** wizard.

5.  Select the file type you created in your ServiceNow instance from the list.

6.  At the Select tags prompt, select the tags you created in the instance.

    All tags are selected by default. Click a tag's check box to deselect it.

    ![Select tags dialog box](../image/vscode-selecttags.png "Select tags dialog box")

    The new file type is successfully added to the `app.config.json` file. You can also add the desired file types manually to the `app.config.json` file under your project. See the example below.

7.  Absorb this new file type to the current project using the **Now: Configure File Types** command from the command palette.

8.  Select the file type you created from the list of file types and click **OK**.

    The selected file type is ready for editing in the ServiceNow Extensions for Visual Studio Code extension.


## Example

The following is an example for app.config.json

```
{
        "CustomFileTypes": {
        "sc_ic_aprvl_type_defn": {
            "superCoverName": "Miscellaneous",
            "coverName": "Approval Type Definition",
            "tags": {
                "approver_script": "js",
                "approver_html”: "html",
            }
        }
    }
}
```

-   superCoverName is a name of the super parent directory \(Should always pointtoMiscellaneous\).
-   coverName is a descriptive name of the table.
-   sc\_ic\_aprvl\_type\_defn is a table identifier.
-   tags represent the set of scriptable columns in the table
-   approver\_script is a name of the table column / xml tag
-   js is an extension of the file \(js \| html \| css \| json\)

**Parent Topic:**[ServiceNow Extensions for Visual Studio Code](../concept/vs-code.md)

