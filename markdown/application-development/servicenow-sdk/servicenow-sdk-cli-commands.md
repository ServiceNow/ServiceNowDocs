---
title: ServiceNow SDK CLI
description: Use the ServiceNow SDK command-line interface \(CLI\) to manage changes between a local application and the application on an instance.Authenticate to an instance and store, update, or view user credentials for accessing an instance on your system.Create an application or convert an existing application to support development in source code. The application is added in the current directory.Compile source files and output build artifacts. Third-party library dependencies are converted into XML files that can be installed with the application.Package the build artifacts and install or update an application on an instance. Before using the install command, you must use the build command to generate an installable package.Download application dependencies and TypeScript definitions from an instance to enable IntelliSense and code validation for an application.Download application metadata \(XML\) from the instance and transform the metadata into ServiceNow Fluent source code to synchronize the application changes on the instance into your local application.Transform application metadata \(XML\) in the global scope from an instance into ServiceNow Fluent source code in a local global application.Download all application metadata \(XML\) from an application on an instance to compare with the metadata in your local application.Remove the build artifacts that were output with the previous build.Package the build artifacts that were output with the previous build into an installable ZIP file.View documentation and examples for a ServiceNow Fluent API.
locale: en-US
release: australia
product: ServiceNow SDK
classification: servicenow-sdk
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 15
breadcrumb: [Reference, ServiceNow SDK, Building applications in source code, Building pro-code applications, Developing your application, Building applications]
---

# ServiceNow SDK CLI

Use the ServiceNow SDK command-line interface \(CLI\) to manage changes between a local application and the application on an instance.

From the command-line tool on your system, enter `now-sdk` to start the CLI and return a list of available commands or `now-sdk [command]` to begin using the ServiceNow SDK.

**Note:** If you use `npx` to install the ServiceNow SDK in application rather than globally, you must use `npx @servicenow/sdk [command]` rather than `now-sdk [command]` with the ServiceNow SDK CLI.

The CLI includes the following commands and global options:

|Option|Description|
|------|-----------|
|--version, -v|Return the version of the CLI.|
|--help, -h|Return information about commands, sub-commands, and parameters.|
|--debug, -d|Return the debug logs generated with a command.|

**Parent Topic:**[ServiceNow SDK reference](../concept/servicenow-sdk-reference.md)

## auth

Authenticate to an instance and store, update, or view user credentials for accessing an instance on your system.

The `auth` command has parameters for adding credentials, deleting credentials, listing credentials, and setting credentials to use by default.

For more information, see [Authenticating to a ServiceNow instance with the ServiceNow SDK](../concept/authenticate-instance-now-sdk.md).

### add

Store credentials in the device keychain or credential manager on your system.

The `auth` command has the following structure with the `--add` parameter:

```cmd
npx @servicenow/sdk auth [--add <instance url>] [--type <auth method>] [--alias <alias>]
```

**Note:** Using the `npx` command installs the ServiceNow SDK in your application directory instead of globally.

|Parameter|Type|Description|Default value|
|---------|----|-----------|-------------|
|--add|String|The URL of the target instance to access and to which you install applications. The instance must be on the Washington DC release or later.|—|

<table id="table_erc_hwb_l2c"><thead><tr><th>

Parameter

</th><th>

Type

</th><th>

Description

</th><th>

Default value

</th></tr></thead><tbody><tr><td>

--type

</td><td>

String

</td><td>

The method to use to authenticate with the target instance. Specify `basic` for basic authentication or `oauth` for OAuth 2.0 authentication.

</td><td>

basic

</td></tr><tr><td>

--alias

</td><td>

String

</td><td>

The alias for the instance and user credentials.The alias can be used for authentication with the `init`, `transform`, `dependencies`, and `install` commands.

</td><td>

—

</td></tr></tbody>
</table>For example:

```cmd
npx @servicenow/sdk auth --add https://myinstance.service-now.com --type oauth --alias devuser1
```

### delete

Remove credentials in the device keychain or credential manager on your system.

The `auth` command has the following structure with the `--delete` parameter:

```cmd
now-sdk auth [--delete <alias or all>]
```

<table id="table_jbw_rxb_l2c"><thead><tr><th>

Parameter

</th><th>

Type

</th><th>

Description

</th><th>

Default value

</th></tr></thead><tbody><tr><td>

--delete

</td><td>

String

</td><td>

The alias for the instance and user credentials.

 To delete all credentials, set this parameter to `--delete all`.

</td><td>

—

</td></tr></tbody>
</table>For example:

```cmd
now-sdk auth --delete devuser1
```

### list

View credentials saved in the device keychain or credential manager on your system. Passwords and authentication codesaren't returned.

The `auth` command has the following structure with the `--list` parameter:

```cmd
now-sdk auth [--list]
```

|Parameter|Type|Description|Default value|
|---------|----|-----------|-------------|
|--list|String|Lists all available authentication credentials.|—|

For example:

```cmd
now-sdk auth --list
```

### use

Set the credentials to be used by commands by default.

The `auth` command has the following structure with the `--use` parameter:

```cmd
now-sdk auth [--use <alias>]
```

|Parameter|Type|Description|Default value|
|---------|----|-----------|-------------|
|--use|String|The alias for the instance and user credentials.|—|

For example:

```cmd
now-sdk auth --use devuser1
```

## init

Create an application or convert an existing application to support development in source code. The application is added in the current directory.

To create an application with your default credentials, you can run the `init` command without any optional parameters. For example, `now-sdk init`. To convert an existing application, you must include the `--from` parameter to provide the sys\_id of an application on an instance or a path to a local directory that contains an application.

After initializing an application, you must install the required third-party dependencies using your preferred package manager before building the application. For example, if you use Node Package Manager \(npm\), run `npm install`.

The `init` command has the following structure:

```cmd
npx @servicenow/sdk init [--from <sys_id or path>] [--appName <name>] [--packageName <name>] [--scopeName <name>] [--auth <alias>] [--template <template>]
```

**Note:** Using the `npx` command installs the ServiceNow SDK in your application directory instead of globally.

<table id="table_bny_zfc_l2c"><thead><tr><th>

Parameter

</th><th>

Type

</th><th>

Description

</th><th>

Default value

</th></tr></thead><tbody><tr><td>

--from

</td><td>

String

</td><td>

A sys\_id of an application on the instance or a path to a local directory that contains an application to convert to support development in source code.Converting an application adds the necessary files and directories for using the ServiceNow SDK locally and downloads the application metadata. The application isn't changed on the instance until you build and install it on the instance. After installing a converted application, the **Package JSON** field of the custom application record \[sys\_app\] contains the path to the `package.json` file for the application.

</td><td>

—

</td></tr><tr><td>

--appName

</td><td>

String

</td><td>

A name for the application.

</td><td>

—

</td></tr><tr><td>

--packageName

</td><td>

String

</td><td>

A name for the application package used in the `package.json` file. The package name must adhere to Node Package Manager \(npm\) package naming standards.

</td><td>

—

</td></tr><tr><td>

--scopeName

</td><td>

String

</td><td>

The scope of the application. The scope name must be unique on the instance, begin with x\_&lt;prefix&gt;, and be 18 characters or fewer. For more information, see [Namespace identifier](../../applications/concept/c_NamespaceIdentifier.md).

</td><td>

—

</td></tr><tr><td>

--auth, -a

</td><td>

String

</td><td>

An alias for the credentials to use to authenticate to the instance.

</td><td>

If set, the default alias.

</td></tr><tr><td>

--template

</td><td>

String

</td><td>

A template for the default structure of the application.-   base: An application with only the basic structure necessary for development in source code.
-   javascript.basic: An application configured for development in ServiceNow Fluent and JavaScript.
-   javascript.react: An application configured for development in ServiceNow Fluent, JavaScript, and React.
-   typescript.basic: An application configured for development in ServiceNow Fluent and TypeScript. TypeScript source files in the `src/server` directory are transpiled into JavaScript modules.
-   typescript.react: An application configured for development in ServiceNow Fluent, TypeScript, and React. TypeScript source files in the `src/server` directory are transpiled into JavaScript modules.
-   partial.javascript.react: Adds template files and directories to an existing application for development in ServiceNow Fluent, JavaScript, and React.
-   partial.typescript.react: Adds template files and directories to an existing application for development in ServiceNow Fluent, TypeScript, and React.

</td><td>

—

</td></tr></tbody>
</table>For example:

```cmd
npx @servicenow/sdk init --from dbce0f6a3b3fda107b45b5d355e45af6 --appName Example App --packageName example-app --scopeName x_snc_example --auth devuser1 --template base
```

For more information, see [Create an application with the ServiceNow SDK](../task/create-application-now-sdk.md) or [Convert an application with the ServiceNow SDK](../task/convert-application-now-sdk.md).

## build

Compile source files and output build artifacts. Third-party library dependencies are converted into XML files that can be installed with the application.

The `build` command has the following structure:

```cmd
now-sdk build <source> [--frozenKeys <flag>]
```

<table id="table_vx2_vvr_rzb"><thead><tr><th>

Parameter

</th><th>

Type

</th><th>

Description

</th><th>

Default value

</th></tr></thead><tbody><tr><td>

source

</td><td>

String

</td><td>

The path to the directory that contains the `package.json` file for your application. The `package.json` should be in the base directory of your application.

</td><td>

Current working directory

</td></tr><tr><td>

--frozenKeys

</td><td>

Boolean

</td><td>

An option to validate that the `keys.ts` file is up to date for continuous integration \(CI\) builds. If true and changes were made to the application's ServiceNow Fluent code, the `keys.ts` file isn't updated and the build fails.The `keys.ts` file is automatically generated in the `src/fluent/generated` directory.

</td><td>

false

</td></tr><tr><td>

--errorOnConflict

</td><td>

Boolean

</td><td>

An option to treat sys\_id conflicts between ServiceNow Fluent code and metadata XML as errors instead of warnings.

</td><td>

false

</td></tr></tbody>
</table>For example:

```cmd
now-sdk build /path/to/package --frozenKeys true
```

For more information, see [Build and install an application with the ServiceNow SDK](../task/build-deploy-application-now-sdk.md).

## install

Package the build artifacts and install or update an application on an instance. Before using the `install` command, you must use the `build` command to generate an installable package.

The `install` command has the following structure:

```cmd
now-sdk install [--source <package path>] [--reinstall <flag>] [--auth <alias>] [--open-browser <flag>] [--info <flag>]
```

<table id="table_fwn_q5d_m2c"><thead><tr><th>

Parameter

</th><th>

Type

</th><th>

Description

</th><th>

Default value

</th></tr></thead><tbody><tr><td>

--source

</td><td>

String

</td><td>

The path to the directory that contains the `package.json` file for your application. The `package.json` should be in the base directory of your application.

</td><td>

Current working directory

</td></tr><tr><td>

--reinstall, -r

</td><td>

Boolean

</td><td>

An option to uninstall and reinstall the application on the instance to ensure that the metadata on the instance matches the metadata in the installation package. **Warning:** Metadata that is on the instance but not in your local application is removed.

If you have previous versions of modules in the EcmaScript Module \[sys\_module\] table that aren't needed, re-installing an application removes previous versions of the application’s modules from the table.

</td><td>

false

</td></tr><tr><td>

--auth, -a

</td><td>

String

</td><td>

An alias for the credentials to use to authenticate to the instance.**Note:** For CI/CD pipelines, you can set the following environment variables to authenticate with an instance at runtime using basic authentication:

-   SN\_SDK\_INSTANCE\_URL: The URL of the target instance to access and to which you install applications.
-   SN\_SDK\_USER: A username for the instance.
-   SN\_SDK\_USER\_PWD: The password associated with the user.
-   SN\_SDK\_NODE\_ENV: Set to SN\_SDK\_CI\_INSTALL to enable CI server support.

</td><td>

If set, the default alias.

</td></tr><tr><td>

--open-browser, -b

</td><td>

Boolean

</td><td>

An option to open the application record in your default browser after successfully installing the application.

</td><td>

false

</td></tr><tr><td>

--info, -i

</td><td>

Boolean

</td><td>

An option to return details about the most recent installation of this application, such as the status and records updated. When this parameter is used, the application isn’t installed.

</td><td>

false

</td></tr><tr><td>

--demoData

</td><td>

Boolean

</td><td>

An option to install demo data with an application.

</td><td>

true

</td></tr><tr><td>

--skip-flow-activation

</td><td>

Boolean

</td><td>

An option to skip activating, or publishing, flows when installing an application. By default, flows are activated on the instance when an application is installed.**Note:** ServiceNow IDE version 4.1.1 or later must be installed to activate flows with this command.

</td><td>

false

</td></tr></tbody>
</table>For example:

```cmd
now-sdk install --source /path/to/package --reinstall false --auth devuser1 --open-browser true --info true
```

For more information, see [Build and install an application with the ServiceNow SDK](../task/build-deploy-application-now-sdk.md).

## dependencies

Download application dependencies and TypeScript definitions from an instance to enable IntelliSense and code validation for an application.

The `dependencies` command downloads dependencies and TypeScript definitions for scripts and ServiceNow Fluent code:

-   For scripts, this command downloads TypeScript definitions for all Glide APIs and scans the modules and scripts in your application and generates type definitions for the script includes that they use. Type definitions are added in the `@types/servicenow` directory. After downloading script dependencies, you must update your `tsconfig.json` file to include the type definitions.
-   For ServiceNow Fluent, this command downloads the dependencies listed in an application's `now.config.json` file and generates TypeScript definitions for them in the `@types/servicenow/fluent` directory.

To download all script and ServiceNow Fluent dependencies for an application, you can use the `dependencies` command with no parameters. If needed, provide the application directory and authentication alias too.

The `dependencies` command has the following structure:

```cmd
now-sdk dependencies [--directory <package path>] [--auth <alias>]\[--type-defs-only &lt;flag&gt;\] \[--fluent-only &lt;flag&gt;\] \[--add &lt;table&gt; &lt;sys\_ids or names&gt;\] \[--scope &lt;name&gt;\]
```

<table id="table_fwn_q5d_m2c"><thead><tr><th>

Parameter

</th><th>

Type

</th><th>

Description

</th><th>

Default value

</th></tr></thead><tbody><tr><td>

--directory

</td><td>

String

</td><td>

The path to the directory that contains the `package.json` file for your application. The `package.json` should be in the base directory of your application.

</td><td>

Current working directory

</td></tr><tr><td>

--auth, -a

</td><td>

String

</td><td>

An alias for the credentials to use to authenticate to the instance.

</td><td>

If set, the default alias.

</td></tr><tr><td>

--type-defs-only

</td><td>

Boolean

</td><td>

An option to download TypeScript definitions for only script dependencies.Script types are downloaded in the `@types/servicenow` directory.

</td><td>

false

</td></tr><tr><td>

--fluent-only

</td><td>

Boolean

</td><td>

An option to download dependencies and TypeScript definitions for only ServiceNow Fluent dependencies from other application scopes. You must list an application’s dependencies in its `now.config.json` file.ServiceNow Fluent types are generated in the `@types/servicenow/fluent` directory.

</td><td>

false

</td></tr><tr><td>

--add

</td><td>

String

</td><td>

Adds the dependencies that you want to download to the application's `now.config.json` file. You must specify the type of dependencies to add using the table name and then the names or sys\_ids of each item to add, separated by spaces.```cmd
--add <table_name> <sys_id1> <sys_id2> <sys_id3>
```

-   To add table dependencies, you can use the `table` alias and names of tables instead of the sys\_ids. For example:

    ```cmd
--add tables incident problem change_request
    ```

-   To add role dependencies, you can use the `role` alias and names of roles instead of the sys\_ids. For example:

    ```cmd
--add roles admin user itil
    ```


Use a wildcard \(`*`\) to add all items from a specified table and scope. For example:

```cmd
--add sys_security_acl "*"
```

</td><td>

—

</td></tr><tr><td>

sysIds

</td><td>

Array

</td><td>

A list of sys\_ids of dependencies to download and generate TypeScript definitions from. This parameter only applies if you use the `--add` parameter.

</td><td>

—

</td></tr><tr><td>

--scope

</td><td>

String

</td><td>

The application scope from which to download dependencies. This parameter is required if you use the `--add` parameter.

</td><td>

—

</td></tr></tbody>
</table>For example:

```cmd
now-sdk dependencies --directory /path/to/package --auth devuser1 --add sys\_ui\_view fa776f6d97700100f309124eda2975bc --scope global
```

For more information, see [Downloading dependencies with the ServiceNow SDK](../concept/downloading-dependencies-now-sdk.md#).

## transform

Download application metadata \(XML\) from the instance and transform the metadata into ServiceNow Fluent source code to synchronize the application changes on the instance into your local application.

After initializing an application, you can run the `transform` command without any parameters to transform new application metadata from the instance into source code in the `src/fluent/generated` directory and synchronize changes to metadata into source code in the `src/fluent` directory. To transform metadata that existed when the application was initialized into source code, use the `--from` parameter to provide the path to a local directory or file that contains XML. If metadata exists in the local application as both XML and source code, the XML version takes precedence when installed on the instance.

The `transform` command has the following structure:

```cmd
now-sdk transform [--from <path>] [--directory <package path>] [--preview <flag>] [--auth <alias>] [--format <flag>]
```

<table id="table_bny_zfc_l2c"><thead><tr><th>

Parameter

</th><th>

Type

</th><th>

Description

</th><th>

Default value

</th></tr></thead><tbody><tr><td>

--from

</td><td>

String

</td><td>

A path to a local directory or file that contains metadata XML to transform into ServiceNow Fluent code.

</td><td>

—

</td></tr><tr><td>

--directory

</td><td>

String

</td><td>

The path to the directory that contains the `package.json` file for your application. The `package.json` should be in the base directory of your application.

</td><td>

Current working directory

</td></tr><tr><td>

--preview

</td><td>

Boolean

</td><td>

An option to preview the transformed ServiceNow Fluent code from the command line without saving the changes.

</td><td>

false

</td></tr><tr><td>

--auth, -a

</td><td>

String

</td><td>

An alias for the credentials to use to authenticate to the instance.

</td><td>

If set, the default alias.

</td></tr><tr><td>

--format, -f

</td><td>

Boolean

</td><td>

An option to format new and updated ServiceNow Fluent source code when it's transformed.

</td><td>

true

</td></tr></tbody>
</table>For example:

```cmd
now-sdk transform --from metadata/update --directory /path/to/package --preview true --auth devuser1 --format true
```

For more information, see [Convert an application with the ServiceNow SDK](../task/convert-application-now-sdk.md) or [Build and install an application with the ServiceNow SDK](../task/build-deploy-application-now-sdk.md).

## move

Transform application metadata \(XML\) in the global scope from an instance into ServiceNow Fluent source code in a local global application.

To customize the global metadata, the global application in which you want to move metadata must already be installed on the instance.

The `move` command has the following structure:

```cmd
now-sdk move [--ids <sys_ids>] [--source <package path>] [--auth <alias>]
```

<table id="table_qp2_2j1_l2c"><thead><tr><th>

Parameter

</th><th>

Type

</th><th>

Description

</th><th>

Default value

</th></tr></thead><tbody><tr><td>

--ids

</td><td>

Array

</td><td>

A list of sys\_ids of global application metadata to move into the local global application and transform into ServiceNow Fluent code.

</td><td>

—

</td></tr></tbody>
</table><table id="table_bny_zfc_l2c"><thead><tr><th>

Parameter

</th><th>

Type

</th><th>

Description

</th><th>

Default value

</th></tr></thead><tbody><tr><td>

--source

</td><td>

String

</td><td>

The path to the directory that contains the `package.json` file for your application. The `package.json` should be in the base directory of your application.

</td><td>

Current working directory

</td></tr><tr><td>

--auth, -a

</td><td>

String

</td><td>

An alias for the credentials to use to authenticate to the instance.

</td><td>

If set, the default alias.

</td></tr></tbody>
</table>For example:

```cmd
now-sdk move --ids 9f4e7402317d470da09ac34c0693d02d,c4e34f348b1843899ca5efb2a31666f0,5057309fccef409cb30692c86a9aaac6 --auth devuser1
```

## download

Download all application metadata \(XML\) from an application on an instance to compare with the metadata in your local application.

Updates to JavaScript modules aren't included when downloading application metadata from your instance.​

The `download` command has the following structure:

```cmd
now-sdk download <directory> [--source <package path>] [--incremental <flag>]
```

<table id="table_fwd_rcf_m2c"><thead><tr><th>

Parameter

</th><th>

Type

</th><th>

Description

</th><th>

Default value

</th></tr></thead><tbody><tr><td>

directory

</td><td>

String

</td><td>

A path to any directory in which to download the metadata.**Note:** This directory should be a different directory from the `metadata` directory in your application.

</td><td>

—

</td></tr></tbody>
</table><table id="table_sbb_xds_rzb"><thead><tr><th>

Parameter

</th><th>

Type

</th><th>

Description

</th><th>

Default value

</th></tr></thead><tbody><tr><td>

--source

</td><td>

String

</td><td>

The path to the directory that contains the `package.json` file for your application. The `package.json` should be in the base directory of your application.

</td><td>

Current working directory

</td></tr><tr><td>

--incremental

</td><td>

Boolean

</td><td>

An option to download only changes to application metadata made on the instance and recorded in the Customer Updates \[sys\_update\_xml\] table.

</td><td>

false

</td></tr></tbody>
</table>For example:

```cmd
now-sdk download /path/to/directory --source /path/to/package --incremental true
```

## clean

Remove the build artifacts that were output with the previous build.

The `clean` command has the following structure:

```cmd
now-sdk clean <source>
```

<table id="table_vx2_vvr_rzb"><thead><tr><th>

Parameter

</th><th>

Type

</th><th>

Description

</th><th>

Default value

</th></tr></thead><tbody><tr><td>

source

</td><td>

String

</td><td>

The path to the directory that contains the `package.json` file for your application. The `package.json` should be in the base directory of your application.

</td><td>

Current working directory

</td></tr></tbody>
</table>For example:

```cmd
now-sdk clean /path/to/package
```

## pack

Package the build artifacts that were output with the previous build into an installable ZIP file.

The `pack` command has the following structure:

```cmd
now-sdk pack <source>
```

<table id="table_vx2_vvr_rzb"><thead><tr><th>

Parameter

</th><th>

Type

</th><th>

Description

</th><th>

Default value

</th></tr></thead><tbody><tr><td>

source

</td><td>

String

</td><td>

The path to the directory that contains the `package.json` file for your application. The `package.json` should be in the base directory of your application.

</td><td>

Current working directory

</td></tr></tbody>
</table>For example:

```cmd
now-sdk pack /path/to/package
```

## explain

View documentation and examples for a ServiceNow Fluent API.

The `explain` command has the following structure:

```cmd
now-sdk explain <topic> [--list <keyword>] [--format <output type>] [--peek <flag>]
```

|Parameter|Type|Description|Default value|
|---------|----|-----------|-------------|
|topic|String|A keyword or topic name to search for to view related ServiceNow Fluent API, guide, or skill documentation, such as `table-api` or `table-guide`. To get a list of available topics, use the `--list` parameter.|—|

|Parameter|Type|Description|Default value|
|---------|----|-----------|-------------|
|--list, -l|Boolean|An option to view a list of available topics, which you can filter by providing a topic name or keyword, such as `now-sdk explain flow --list`. The list returned includes matches that contain the keyword and possibly related matches.|—|
|--format|Boolean|An option to format the output for the terminal \(`pretty`\) or as Markdown \(`raw`\).|pretty|
|--peek, -p|Boolean|An option to display a short description of a topic instead of the complete topic content. You can use this parameter with the `--list` parameter to display summaries of the listed topics.|—|

For example:

```cmd
now-sdk explain uipage-api --format raw
```

