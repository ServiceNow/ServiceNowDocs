---
title: Deploy to an instance
description: Getting a change onto a ServiceNow instance is a three-step pipeline: build the app, deploy its records, then verify the service and the app. The same pipeline runs from the command line, from Lux Lab, or ServiceNow Lux Lab for VS Code.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/application-development/deploy-to-an-instance.html
release: australia
topic_type: task
last_updated: "2026-09-29"
reading_time_minutes: 3
keywords: [Deploy to an instance, Prerequisites, Steps, What gets installed where, Release and promotion, Roll back a deploy, Promote between instances, Install through an update set, Deploying from Lux Lab, Deploying from ServiceNow IDE, Deploying through Maven, Diagnose a failed deploy, Ship checklist, Next steps]
breadcrumb: [Test and deploy a Lux app, Lux Development, Building pro-code applications, Developing your application, Building applications]
---

# Deploy to an instance

Getting a change onto a ServiceNow instance is a three-step pipeline: build the app, deploy its records, then verify the service and the app. The same pipeline runs from the command line, from Lux Lab, or ServiceNow Lux Lab for VS Code.

## Before you begin

-   Role required: admin, on the target instance.
-   `now-sdk` installed.
-   Tests and lint passing. For the local checks, see [Test an app locally](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/test-an-app-locally.md).

## About this task

```
Source code  →  pnpm build  →  pnpm deploy  →  ServiceNow instance
                  (aiux build)    (now-sdk install)
```

## Procedure

1.  Register credentials for your target instance, if not already registered.

    ```
    npx now-sdk auth --add local --type basic
    ```

    The command prompts for the host, user name, and password. Confirm it was saved.

    ```
    npx now-sdk auth --list
    ```

    This writes `~/.snc/credentials`, which `now-sdk` reads for the instance URL and authentication on every subsequent command. The SDK stores credentials in the OS keychain under the alias you choose.

2.  Set `scope` and `scopeId` in `now.config.json`.

    Without both, the build produces browser bundles but no installable records.

    ```
    {
      "scope": "x_myco_my_app",
      "scopeId": "<32-char-scope-sys-id>",
      "name": "My App",
      "appOutputDir": "dist-metadata/app"
    }
    ```

    `scope` is the application's scope name on the instance; `scopeId` is its sys\_id.

3.  Build the app.

    This emits the metadata and the deployable zip under `target/`.

    ```
    pnpm build
    ```

    The build compiles your pages and components into versioned bundles under `dist/vN/`, generates a route manifest, and produces `dist-metadata/`, the ServiceNow record XML that gets installed. Don't commit `dist/`, `dist-metadata/`, or `target/`; apps scaffolded with `now-sdk init` gitignore all three.

    |Output|Contents|
    |------|--------|
    |`dist/vN/`|Per-page browser and SSR bundles, a `manifest.json` mapping routes to bundles, shared chunks, and pre-compressed `.br` and `.gz` assets|
    |`dist-metadata/app/`|ServiceNow record XML, one scope record plus the `update/` records for widgets, pages, layouts, and dependencies, and `sys_aix_*` metadata|
    |`target/<app>_<version>.zip`|The deployable scoped-app archive that the ServiceNow SDK installs onto an instance|

    To clear all caches and force a full rebuild, use `pnpm build:force`; add `-v` or `--verbose` for detailed output.

4.  Deploy.

    **Note:** `now-sdk init` doesn't generate a `deploy` script by default, add one to `package.json`: `"deploy": "now-sdk install"`.

    ```
    npx now-sdk install --auth local
    ```

    In most apps this is also wired to `pnpm deploy`. The SDK reads `dist-metadata/`, REST-pushes the records to the instance, and prints a rollback URL: save it, because visiting it undoes the install. The first deploy creates the app's `sys_scope` record; later deploys update existing records in place, so re-running it is safe.

    To re-run a deploy from a scaffolded app's own scripts, `pnpm run deploy:reinstall` wraps `now-sdk install --reinstall`.

    **Warning:** `--reinstall` removes any application metadata on the instance that isn't present in your local build, including metadata other developers added. Run `now-sdk transform --auth <alias>` first to sync down what's already there.

5.  Verify the service.

    If `/aiux/health` doesn't answer, nothing you deployed will render and the problem is the instance, not your code:

    ```
    curl https://<instance>/aiux/health
    ```

    A minimal `{"status": "UP", "service": "aiux-service"}` is the healthy answer for an ordinary caller.

6.  Verify the app.

    Open `https://<instance>/aiux/<basename>/<landing>` and confirm the app loads. Check server-side rendering \(SSR\) output through **DevTools** &gt; **Network** &gt; **Preview**, and check the real-time log viewer at `https://<instance>/aiux/<basename>/logs` for server-side loader or SSR failures.

    For the SSR check in detail, see [Ways to preview a Lux experience](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/ways-to-preview-an-experience.md). For the `/aiux/ready` route and the other checks that run before and during a deploy, see .


## What gets installed where

|Source|ServiceNow table|Record|
|------|----------------|------|
|`aiux.json`|`sys_aix_experience`|One record \(the app itself\)|
|`pages/<route>/page.js`|`sys_aix_page` + `sys_aix_widget`|One page record and one widget record per page|
|`pages/layout.js`|`sys_aix_layout`|One record \(the app's layout\)|
|`widgets/<name>/index.js`|`sys_aix_widget`|One record per discoverable widget|
|Page dependencies and shared widgets|`sys_aix_dependency`|One record per dependency|
|`src/fluent/tables/*.now.ts`|`sys_db_object` + columns|Tables and dictionary entries|
|`src/fluent/security/*.now.ts`|`sys_user_role` + ACLs|Roles and access controls|
|Static assets|`sys_attachment`|Bundled into the scope|

A real app produces hundreds of these records; a large app can emit well over a thousand, that volume is normal.

