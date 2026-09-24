---
title: Workload Identity Federation for outbound OAuth
description: Authenticate outbound OAuth calls to Microsoft Azure and Google Cloud using a signed JWT that the cloud provider validates through the instance's public JWKS endpoint, so that no client secret needs to be stored on the instance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/authentication/workload-identity-federation.html
release: brazil
product: Authentication
classification: authentication
topic_type: concept
last_updated: "2026-09-24"
reading_time_minutes: 1
keywords: [Workload Identity Federation, WIF, outbound OAuth, JWKS, Key Management Framework, KMF]
breadcrumb: [OAuth Outbound, OAuth authentication, Authentication, Access Management]
---

# Workload Identity Federation for outbound OAuth

Authenticate outbound OAuth calls to Microsoft Azure and Google Cloud using a signed JWT that the cloud provider validates through the instance's public JWKS endpoint, so that no client secret needs to be stored on the instance.

## How Workload Identity Federation works

With traditional client-secret authentication, the instance sends a `client_id` and `client_secret` to the cloud provider. The provider validates the secret and issues an access token. That approach requires storing, rotating, and protecting the secret.

With Workload Identity Federation \(WIF\), the instance sends a JWT signed by a private key held in the Key Management Framework \(KMF\). The cloud provider fetches the corresponding public key from the instance's JWKS endpoint, validates the JWT signature, and issues an access token. No shared secret is stored on the instance, and the private key never leaves KMF.

WIF is supported for two cloud providers in this release:

-   **Microsoft Azure** — using the OAuth client credentials grant with a JWT assertion \(`client_assertion`\).
-   **Google Cloud** — using the OAuth 2.0 token exchange grant \(`urn:ietf:params:oauth:grant-type:token-exchange`\).

## What you need on the instance

-   A KMF Cryptographic Module that holds the private key used to sign the outbound JWT.
-   A JWT signing key \(`jwt_keystore_aliases` record\) with Key Source set to KMF Cryptographic Module and the KMF Module set to the module.
-   A JWT provider that references the signing key.
-   An OAuth entity and OAuth entity profile configured for the target provider — either directly or through the fast-configuration UI.

## What the cloud provider needs to know about the instance

-   The issuer URL — served by the instance at `/.well-known/openid-configuration`.
-   The JWKS endpoint URL — the public-key set served by the instance for signature validation.

**Note:** Once WIF is configured, the `client_secret` is not sent to the cloud provider. The existing OAuth entities that use a stored `client_secret` continue to work unchanged — WIF is an additive capability, not a replacement for other outbound authentication methods.

