---
title: Test an app locally
description: Testing a page locally with Vitest catches loader and rendering failures before you deploy. Separate unit tests cover your data-fetching logic, and separate render tests cover the HTML your component produces.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/application-development/test-an-app-locally.html
release: zurich
topic_type: task
last_updated: "2026-09-29"
reading_time_minutes: 3
keywords: [Test an app locally, Prerequisites, Steps, Other test types, Don't test the mock, Next steps]
breadcrumb: [Test and deploy a Lux app, Lux Development, Building pro-code applications, Developing your application, Building applications]
---

# Test an app locally

Testing a page locally with Vitest catches loader and rendering failures before you deploy. Separate unit tests cover your data-fetching logic, and separate render tests cover the HTML your component produces.

## Before you begin

-   A page with a `static async loader(ctx)` method and a `render()` method. To learn how a page declares both, see [Create a page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/create-a-page.md).
-   Vitest configured, which is present by default in an app scaffolded with `now-sdk init`.
-   Role required: admin

## About this task

Lux uses Vitest with a two-tier strategy: loader unit tests verify your data-fetching logic, and server-side rendering \(SSR\) render tests verify the HTML your component produces. They live in separate files; mixing them causes `vi.mock()` conflicts, because loader tests mock Lit entirely while render tests require real Lit and a DOM shim. To access the test runner's reference material, see the [Vitest documentation](https://vitest.dev/).

## Procedure

1.  Create the test files.

    ```
    my-app/
    ├── pages/
    │   └── risk/page.js
    └── test/
        ├── risk-page-loader.test.js   ← Tier 1: loader tests
        └── risk-page.test.js          ← Tier 2: SSR render tests
    ```

    Test files live in `test/` directories alongside `src/`.

2.  Write loader unit tests.

    Mock Lit and `fetch`, then assert on your loader's behavior, not on the mock.

    ```
    import {describe, it, expect, vi, beforeEach, afterEach} from 'vitest';
    
    vi.mock('lit', () => ({isServer: true}));
    vi.mock('lit/decorators.js', () => ({customElement: () => cls => cls}));
    
    const mockGetHeaders = vi.fn(() => ({'Content-Type': 'application/json'}));
    vi.mock('@servicenow/aiux-components-core', () => ({
      AIUXElement: class {},
      getHeaders: (...args) => mockGetHeaders(...args)
    }));
    
    const {default: MyPage} = await import('../pages/risk/page.js');
    
    describe('MyPage.loader', () => {
      it('calls the correct API endpoint', async () => {
        globalThis.fetch = vi.fn(async () => ({json: async () => ({result: []})}));
        await MyPage.loader(mockCtx);
        expect(globalThis.fetch).toHaveBeenCalledTimes(1);
      });
    });
    ```

    Assert on the fetch URL and method, that `getHeaders(ctx)` was forwarded, the return value's shape, error handling, and edge cases such as missing fields and empty arrays.

3.  Copy the SSR test helper.

    SSR render tests require real Lit and a DOM shim. Copy `test/ssr-utils.js` — about 50 lines — from the framework monorepo into your app's `test/` directory.

4.  Write SSR render tests, and render against mock loader data:

    ```
    import {html} from 'lit';
    import {setupLitSSR, renderToString, clean} from './helpers/ssr-utils.js';
    
    let render;
    beforeAll(async () => {
      ({render} = await setupLitSSR());
      await import('../pages/risk/page.js');
    });
    
    it('renders the risk list', async () => {
      globalThis.__COMPONENT_DATA__ = {risks: [{number: 'RSK0001'}], error: null};
      const result = render(html`<my-risk-page></my-risk-page>`);
      const output = clean(await renderToString(result));
      expect(output).toContain('RSK0001');
    });
    ```

    During real SSR, the framework sets `globalThis.__COMPONENT_DATA__` with your loader's return value before rendering, and `AIUXElement` reads it in its constructor. In tests, set it directly.

5.  Run the tests.

    Run everything, one package, one file, or one test by name.

    ```
    pnpm test                                                  # all tests
    pnpm exec vitest run test/risk-page-loader.test.js         # one file
    pnpm exec vitest run -t "calls the correct API endpoint"    # by test name
    pnpm exec vitest watch test/                               # watch mode
    pnpm test:coverage                                         # coverage report
    ```

    To run a single package's tests, change into its directory first and run `pnpm test` there.

6.  Run lint and type-check before you build.

    ```
    pnpm lint
    pnpm typecheck
    ```


## Other test types

The loader and SSR render tests described earlier are page-level tests running in Node. Two other test types support client-side verification. All three are provided in the following table.

|Type|File pattern|Command|Runs in|
|----|------------|-------|-------|
|Unit|`*.test.js`|`pnpm test`|Node environment|
|Browser-mode unit|`*.browser.js`|`pnpm test:browser`|Vitest browser mode|
|Smoke|`*.smoke.js`|`pnpm test:smoke`|Real Chromium, driven by Playwright — verifies a widget mounts and hydrates|

Add `pnpm test:smoke:headed` to run smoke tests with a visible browser window.

## Don't test the mock

A common mistake is mocking a call to return `X`, then asserting the result is `X`. That verifies the mock, not your code. Mock the dependency, which is the network call, and assert on the behavior, which is what your loader does with the response.

## What to do next

After your tests pass, move on to [Deploy to an instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/deploy-to-an-instance.md), `pnpm test` is the first item on that topic's ship checklist. For diagnosing a failure you can't explain from a test alone, see [https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/debug-an-experience.md](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/debug-an-experience.md). For the build-time and CI checks that run beyond what you can trigger locally, see [https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/validation-checks-and-when-they-run.md](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/validation-checks-and-when-they-run.md).

