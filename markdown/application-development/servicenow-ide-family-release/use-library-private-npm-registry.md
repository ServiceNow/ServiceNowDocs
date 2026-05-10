---
title: Install an npm package from a private registry with the ServiceNow IDE
description: Install Node Package Manager \(npm\) packages from a private registry as dependencies in your application to use them as third-party libraries.
locale: en-US
release: australia
product: ServiceNow IDE \(Family Release\)
classification: servicenow-ide-family-release
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Use third-party libraries, Develop applications, ServiceNow IDE, Building applications in source code, Building pro-code applications, Developing your application, Building applications]
---

# Install an npm package from a private registry with the ServiceNow IDE

Install Node Package Manager \(npm\) packages from a private registry as dependencies in your application to use them as third-party libraries.

## Before you begin

Role required: admin

## About this task

To install packages from private registries, you must configure your Package Manager user settings in the ServiceNow IDE. Then you can choose in which applications to install packages.

ServiceNow IDE uses the public npm registry \(`https://registry.npmjs.org`\) as its default package source. If your network blocks access to this registry, you must have access to an alternate registry to download packages and build applications in the ServiceNow IDE. If access to the public npm registry is blocked on your system, you must configure a private npm registry in your Package Manager user settings in the ServiceNow IDE.

**Note:** To install packages from a private registry, the registry must respond with the HTTP `Access-Control-Allow-Origin` header.

## Procedure

1.  Navigate to **All** &gt; **App Development** &gt; **ServiceNow IDE**.

2.  Open a workspace.

3.  Use one of the following keyboard shortcuts to open the command palette:

    -   Windows: Ctrl-Shift-P
    -   Mac: Cmd-Shift-P
4.  Enter `Preferences: Open User Settings (JSON)` and press Enter.

5.  Specify a private registry as the default registry or a scoped registryfrom which you can install packages.

<table id="choicetable_mnm_z32_42c"><thead><tr><th align="left" id="d152827e146">

Option

</th><th align="left" id="d152827e149">

Example

</th></tr></thead><tbody><tr><td id="d152827e155">

**Default registry**

</td><td>

```json
"package-manager.defaultRegistry": "<private-registry-url>",
```

</td></tr><tr><td id="d152827e167">

**Scoped registry**

</td><td>

```json
"package-manager.scopedRegistries": [
        {
            "scope": "@<scope>",
            "registry": "<private-registry-url>"
        },
        ...
]

```

</td></tr></tbody>
</table>    **Note:** To install packages from public registries, you can specify a public registry as the default registry or a scoped registry in addition to any private registries.

6.  Provide your credentials for accessing the private registry.

<table id="choicetable_qmx_xht_ydc"><tbody><tr><td id="d152827e195">

**Basic authentication**

</td><td>

Provide a user name and password to access the default registry that you specified.```json
"package-manager.basicAuth": [
    {
        "registry": "<private-registry-url>",
        "user": "<user-name>",
        "pass": "<password>"
    },
    ...
]
```

</td></tr><tr><td id="d152827e206">

**Legacy authentication**

</td><td>

Provide a legacy token to access the default registry that you specified. Legacy tokens are basic authentication credentials encoded in Base64 format.```json
"package-manager.legacyAuth": [
    {
        "registry": "<private-registry-url>",
        "token": "<legacy-token>"
    },
    ...
] 
```

</td></tr><tr><td id="d152827e217">

**Token authentication**

</td><td>

Provide a bearer token to access the default registry that you specified.```json
"package-manager.tokenAuth": [
    {
        "registry": "<private-registry-url>",
        "token": "<token>"
    },
    ...
] 
```

</td></tr></tbody>
</table>7.  Save your changes to the `settings.json` file.

8.  Install packages from the configured registries.

    1.  Use one of the following keyboard shortcuts to open the command palette:

        -   Windows: Ctrl-Shift-P
        -   Mac: Cmd-Shift-P
    2.  Enter `Package Manager: Install Dependencies` and press Enter.

    3.  Select an application to install packages in as dependencies.

    Packages are installed in the `node_modules` directory.


## User settings for private registry access

In the following example, a user configured access to a private registry using basic authentication. The user also configured their settings to install packages from a public registry with the `@example` scope.

```json
{
    "files.autoSave": "off",
    "package-manager.defaultRegistry": "<private-registry-url>",
    "package-manager.basicAuth": [
        {
        "registry": "<private-registry-url>",
            "user": "<user-name>",
            "pass": "<password>"
        }
    ],
    "package-manager.scopedRegistries": [
        {
            "scope": "@example",
            "registry": "<public-registry-url>"
        }
    ]
}

```

## What to do next

Use the packages that you installed as third-party libraries in your application. For more information, see [Use third-party libraries in applications in the ServiceNow IDE](use-third-party-libraries-ide.md).

**Parent Topic:**[Use third-party libraries in applications in the ServiceNow IDE](use-third-party-libraries-ide.md)

