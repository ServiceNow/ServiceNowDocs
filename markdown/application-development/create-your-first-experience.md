---
title: Create your first Lux experience
description: Install the ServiceNow SDK toolchain, scaffold a new Lux application, and deploy your first app to your ServiceNow instance. This foundational workflow guides you through environment setup, local development, and deployment.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/application-development/create-your-first-experience.html
release: zurich
topic_type: task
last_updated: "2026-09-29"
reading_time_minutes: 4
keywords: [Create your first experience, Prerequisites]
breadcrumb: [Exploring Lux, Lux Development, Building pro-code applications, Developing your application, Building applications]
---

# Create your first Lux experience

Install the ServiceNow SDK toolchain, scaffold a new Lux application, and deploy your first app to your ServiceNow instance. This foundational workflow guides you through environment setup, local development, and deployment.

## About this task

If you'd rather use Lux Lab or the VS Code extension, which wrap these same steps in a UI, see [Development tooling](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/development-tooling.md).

## Before you begin

-   Role required: admin
-   Node.js 24 or later and `pnpm` 10 or later
-   A ServiceNow instance you can deploy to
-   `@servicenow/sdk` installed globally: `npm install -g @servicenow/sdk@latest`

## Procedure

1.  Check your prerequisites

    Verify that you have the right version of Node.js.

    ```
    node --version
    ```

    Verify that you have the right version of pnpm.

    ```
    pnpm --version
    ```

    Verify that you have the right version of the ServiceNow SDK.

    ```
    now-sdk --version
    ```

    If your version does not match the listed requirements, install or update your packages as necessary.

2.  Connect the ServiceNow SDK to your instance

    Run the following command to authenticate the now-sdk with your ServiceNow instance:

    ```
    now-sdk auth --add https://your-instance.service-now.com --type basic --alias dev
    ```

    Replace `your-instance` with your actual instance name. You will be prompted to enter your ServiceNow username and password.

    For more information on instance setup or other authentication methods, see the [ServiceNow SDK authentication documentation](https://www.servicenow.com/docs/r/application-development/servicenow-sdk/authenticate-instance-now-sdk.html).

3.  Scaffold the application

    Run the following command to create a local directory for your first experience and initialize a new ServiceNow application project. This scaffolds the project for Lux development with a boilerplate structure including configuration files, build scripts, and server-side logic.

    ```
    mkdir my-app && cd my-app
    npx @servicenow/sdk@latest init --template javascript.aiux
    ```

    You will see prompts for an app name, package name \(also used as the URL basename\), and scope name. To skip the prompts:

    ```
    npx @servicenow/sdk@latest init --template javascript.aiux --appName my-app --scopeName x_aix_myapp --packageName my-app
    ```

    The scope name must start with your vendor prefix and be 18 characters or fewer. Don't change it after the first install. Changing it without uninstalling the old scope from the instance creates a duplicate.

    **Note:** For more information about application scope naming, refer to: [application scope naming documentation](https://www.servicenow.com/docs/r/application-development/c_NamespaceIdentifier.html).

    |Flag|Purpose|
    |----|-------|
    |`--instance=<url>`|ServiceNow instance URL|
    |`--scope=<scope>`|App scope for scoped applications|
    |`--template=<name>`|Starter template \(default: default\)|
    |`--env`|Create .env file interactively|

    The scaffold generates the following project structure.

    ```
    my-app/
    ├── aiux.json              # Lux app manifest — app name, URL basename, landing route
    ├── now.config.json        # ServiceNow scope manifest — scope, scopeId, install settings
    ├── package.json           # Depends on the Lux runtime + @servicenow/sdk
    ├── application.js         # App-level lifecycle hooks (setup, navigate, teardown)
    ├── theme.js               # App theme tokens (colors, radii)
    ├── tailwind.app.css       # Tailwind configuration
    ├── head.app.css           # App-level head styles
    ├── eslint.config.mjs      # ESLint flat config
    ├── pages/                 # File-based routing — one directory per route
    │   ├── home/
    │   │   ├── page.js        # The page (default export)
    │   │   └── components/    # Components co-located with the page that uses them
    │   └── incidents/
    │       └── page.js        # A page with a static async loader(ctx)
    ├── widgets/               # Custom widgets (+ server scripts)
    │   └── aiux-hello-world/
    │       ├── index.js
    │       └── server-script.js
    ├── utils/                 # Shared utility modules
    ├── scripts/               # Postinstall helpers
    ├── dist/                  # Build output (generated — do not commit)
    └── dist-metadata/         # Build metadata (generated — do not commit)
    ```

    Add `dist/` and `dist-metadata/` to your `.gitignore`. The build generates both.

4.  Install dependencies

    Run the following command to install dependencies.

    ```
    pnpm install
    ```

5.  Run the example locally

    Use the following command to start at local dev server.

    ```
    pnpm run dev
    ```

    This spins up the full request pipeline on your machine with hot reload, so you can build against a real instance locally.

    To see your experience, Open `http://localhost/aiux/<basename>/<route>` in your browser.

    Example: if your app's `basename` is `my-app` and you want to access the `/home` route: `http://localhost/aiux/my-app/home`

    **Note:** The path after `/aiux/` is your app's basename \(from `aiux.json`\) followed by the page route:

    -   `/aiux/my-app/home` = basename `my-app` + route `/home`
    -   `/aiux/my-app/dashboard` = basename `my-app` + route `/dashboard`
    Editing a file under pages/ or components/ automatically recompiles and reloads the page in your browser. Build artifacts are written to .dev directories during development.

    You can try creating a page to add more to your experience: [Create a page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/create-a-page.md).

6.  Build

    ```
    pnpm run build
    ```

    This compiles your pages and widgets into an installable package, written to `dist/`. It also confirms that the toolchain and dependencies are in place.

    A clean build means that Node, pnpm, and the @servicenow/karuna package all resolved correctly.

7.  Deploy

    ```
    pnpm run deploy
    ```

    This installs the application on your ServiceNow instance. Open `https://<your-instance>/aiux/<basename>` to see it live.


## Result

The starter app ships two routes \(Home and Incidents\), an example component, and an example widget.

## What to do next

-   [Lux architecture](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/lux-architecture.md) for how these pieces fit together
-   [Create a page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/create-a-page.md) to add more routes
-   [Lux Widgets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/widgets.md) to build the widget the scaffold generated

