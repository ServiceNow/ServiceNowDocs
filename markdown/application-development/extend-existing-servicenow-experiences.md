---
title: Extend existing ServiceNow experiences
description: Contribute a page to an experience owned by another scoped application, without changing the host application's repository. The contribution can be a net-new route or a replacement for one of the host's existing pages.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/application-development/extend-existing-servicenow-experiences.html
release: zurich
topic_type: task
last_updated: "2026-09-29"
reading_time_minutes: 4
keywords: [Extend existing ServiceNow experiences, Prerequisites, Steps, Two extensions targeting the same route]
breadcrumb: [Extend experiences, Lux Development, Building pro-code applications, Developing your application, Building applications]
---

# Extend existing ServiceNow experiences

Contribute a page to an experience owned by another scoped application, without changing the host application's repository. The contribution can be a net-new route or a replacement for one of the host's existing pages.

## Before you begin

-   Role required: admin
-   The Now SDK is installed and authenticated against a target instance.
-   Familiarity with scaffolding an application with `now-sdk init` \(see [Create your first Lux experience](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/create-your-first-experience.md)\).
-   The host application's `scope` and `basename` \(its `aiux.json` values\). If the host's manifest isn't visible - for example, a pre-existing experience whose scope wasn't derived through this convention - use the experience's sys\_id directly instead. For that explicit form, see [https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/supported-extension-points.md](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/supported-extension-points.md).

## About this task

For the same task through the ServiceNow® AI Experience Lab for VS Code instead of the CLI, see [Create an extension application with Lux Lab](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/create-an-extension-application-with-lux-lab.md).

## Procedure

1.  Scaffold the host application, if you're extending one you also own for this exercise \(skip this step against a real, already-deployed host\).

    ```
    mkdir host-app && cd host-app
    npx @servicenow/sdk@latest init --template javascript.aiux
    ```

    `now-sdk init` scaffolds into the current directory, prompting for the application name, package name, and scope if not passed as flags. Install dependencies, then build and deploy:

    ```
    pnpm install
    pnpm build
    pnpm run deploy
    ```

    Confirm that `https://<instance>/aiux/<basename>/home` renders the starter page before continuing.

2.  Scaffold the extending application, in a separate directory and terminal.

    ```
    mkdir extending-app && cd extending-app
    npx @servicenow/sdk@latest init --template javascript.aiux-extension
    ```

    Beyond the application name, package name, and scope, `init` also prompts for the host's scope and route ID \(its scope and basename from step 1\). Install dependencies:

    ```
    pnpm install
    ```

    The extending application's own `aiux.json` and `pages/` are unrelated to what it extends - an extension is declared separately, under `src/extensions/`. A project must not include both. If a project contains any src/extensions/ pages, its own pages/ are still processed. However, they get silently wired into the host's experience instead of its own, even with basename set. Keep an extension project extension-only \(pages under src/extensions/ only, no project-owned pages/\) A mixed project does carry one trap of its own around per-host lifecycle modules - see [https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/ownership-and-maintenance-considerations.md](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/ownership-and-maintenance-considerations.md).

3.  Add a net-new page, at a route the host doesn't already have, under the host's scope and basename.

    ```
    src/extensions/x_example_host/host/pages/reports/page.js
    ```

    ```
    import {html} from 'lit';
    import {customElement} from 'lit/decorators.js';
    import {AIUXElement} from '@servicenow/aiux-components-core';
    
    @customElement('ext-reports-page')
    export default class ExtReportsPage extends AIUXElement {
      render() {
        return html`<h1>Reports (contributed by extension-app)</h1>`;
      }
    }
    ```

4.  Add a dynamic-route page, if the net-new route takes a parameter.

    A bracket directory works the same way it does in an owned application:

    ```
    src/extensions/x_example_host/host/pages/sample/[sampleName]/page.js   # /sample/:sampleName
    ```

    The built `ssr` path for a bracket directory is mangled to `sample/_sampleName_/page.js`. Decorators are now extracted from the real source path, so `@roles([...])` and `@order()` survive the build. Confirm `sys_aix_page.roles` on the installed record if you're gating a dynamic-route page and the installed SDK predates that fix.

5.  Override an existing host page, at a route the host already owns.

    ```
    src/extensions/x_example_host/host/pages/home/page.js
    ```

    ```
    import {html} from 'lit';
    import {customElement} from 'lit/decorators.js';
    import {AIUXElement} from '@servicenow/aiux-components-core';
    
    @customElement('ext-home-override')
    export default class ExtHomeOverride extends AIUXElement {
      render() {
        return html`<h1>Home (overridden by extension-app)</h1>`;
      }
    }
    ```

6.  Build and deploy the extension.

    ```
    pnpm build
    pnpm run deploy
    ```

    `pnpm deploy` \(without `run`\) is pnpm's own reserved subcommand and fails with `ERR_PNPM_CANNOT_DEPLOY` - always use `pnpm run deploy`. No redeployment or reconfiguration of the host is needed. The host's experience acquires the contributed page only after the corresponding records exist and reference it.

7.  Verify.

    On an instance, open the host application. `/aiux/host/reports` renders the net-new page, and `/aiux/host/home` renders the override rather than the host's own starter page.

    `sys_aix_experience_page_rel`, filtered to the host experience, gains one membership row per contributed page. There is no `sys_aix_page_route_map` row for either, because extension routing doesn't use that table. The deploy auto-invalidates the host experience's cache, so the change is visible on the next request with no manual eviction step. For faster iteration, a dev server can render an extension straight from local source, with no deploy.

    **Important:**

    Don't verify a role-gated extension page as `admin`

    A session with the `admin` role passes `gs.hasRole()` for any role name, including one that has no `sys_user_role` record at all. So `admin` always sees the role-gated override and never triggers the fallback to the host's own page. This is standard ServiceNow behavior, not specific to extensions. To observe the fallback, use a session that genuinely has no roles. Either log in as a no-role user, or impersonate one. To impersonate, use **avatar menu** &gt; **Impersonate user** and pick a stock demo user with no roles. Navigate back to the route while impersonating, then stop impersonating to return to your own session.


## Two extensions targeting the same route

Scaffolding a second extending application that overrides the same host route is a supported scenario, though the tooling doesn't resolve it for you. For the ordering rules, see [https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/ownership-and-maintenance-considerations.md](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/ownership-and-maintenance-considerations.md).

