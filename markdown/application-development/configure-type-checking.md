---
title: Configure type checking
description: Configure type checking for a component and JavaScript-only project.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/application-development/configure-type-checking.html
release: australia
topic_type: task
last_updated: "2026-10-26"
reading_time_minutes: 1
breadcrumb: [Configure, UI component CLI extension, Building pro-code applications, Developing your application, Classic app development, Building applications]
---

# Configure type checking

Configure type checking for a component and JavaScript-only project.

## Before you begin

-   The ui-component extension must be installed. See [Install the UI component CLI extension](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/install-ui-component-cli-extension.md).
-   The Next Experience UI component project must exist.

Role required: admin

## About this task

Type checking is enabled by default for projects that use both TypeScript and JavaScript. For a JavaScript-only project, type checking requires a tsconfig.json file with type checking enabled.

## Procedure

1.  Set the type checking property in the now-cli.json file at the root of the project.

    **Note:**

    If you provide both the CLI option and typescript.typeCheck, the CLI option takes precedence.

    ```
    {
                            "typescript": {
                            "typeCheck": true
                            }
                            }
    ```

2.  Create a tsconfig.json file for a JavaScript-only project.

3.  Insert the file at the root of the project or monorepo with the following compiler options.

    **Note:**

    The extension provides a default tsconfig.json file. A tsconfig.json file that you define overrides the default.

    ```
    {
                            "compilerOptions": {
                            "allowJs": true,
                            "checkJs": true
                            }
                            }
    ```


## Result

The extension type checks the project files according to the settings that you configured.

