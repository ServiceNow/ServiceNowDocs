---
title: Configure a template for OAuth JWT Bearer grant type
description: This example configuration template sets up Credential and Connection records using the JWT Bearer grant type to authenticate requests to Docusign.
locale: en-US
release: australia
product: Connections and Credentials
classification: connections-and-credentials
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Connection &amp; Credential configuration templates, Explore credentials, connections, and aliases, Connections and Credentials, Access Management]
---

# Configure a template for OAuth JWT Bearer grant type

This example configuration template sets up Credential and Connection records using the JWT Bearer grant type to authenticate requests to Docusign.

## Default data template

Each top-level item in the default data template creates an associated record. The template includes these sections:

-   `Credential`: Creates a record in the Credentials table.
-   `Connection`: Creates a record in the Connections \[sys\_connection\] table and any associated connection records.
-   `Additional`: Optionally creates records in a custom table. The post processing script tells the system what to do with these records.

The following example creates the records required for OAuth JWT Bearer grant type authentication.

```
{
  "credential": {
    "oauth_entity": {
      "oauth_entity_profile": [
        {
          "grant_type": "urn:ietf:params:oauth:grant-type:jwt-bearer",
          "name": "Docusign Profile",
          "default": true,
          "oauth_entity_profile_scope": [
            "users:read.email"
          ]
        }
      ],
      "code_challenge_method": "S256",
      "type": "consumer",
      "oauth_entity_scope": [
        {
          "oauth_entity_scope": "users:read.email",
          "name": "email"
        }
      ],
      "client_id": "<provider-client-id>",
      "use_mutual_auth": false,
      "revoke_token_url": "https://<provider-domain-name>.com/oauth2/revoke",
      "default_grant_type": "urn:ietf:params:oauth:grant-type:jwt-bearer",
      "public_client": false,
      "oauth_api_script": "3e3a3a11c333210016194ffe5bba8f70",
      "name": "Docusign Spoke OAuth",
      "client_secret": "<provider-client-secret>",
      "auth_url": "https://<provider-domain-name>.com/oauth2/auth",
      "token_url": "https://<provider-domain-name>.com/oauth2/token",
      "redirect_url": "https://<instance-name>.service-now.com/oauth_redirect.do"
    },
    "jwt_provider": {
      "jwt_keystore_aliases": {
        "kid": "<provider-key-id>",
        "name": "Docusign Spoke JWT Key",
        "signing_keystore": "<signing-keystore-sys-id>",
        "signing_algorithm": "rsa_256",
        "signing_key_password": "password"
      },
      "jwt_claim_validation" : [ {
        "name" : "iss",
        "is_standard" : true,
        "data_type" : "string",
        "value":"<docusign-iss-claim>"
      }, {
        "name" : "sub",
        "is_standard" : true,
        "data_type" : "string",
        "value":"<docusign-sub-claim>"
      }, {
        "name" : "aud",
        "is_standard" : true,
        "data_type" : "string",
        "value":"<docusign-aud-claim>"
      }, {
        "name" : "scope",
        "is_standard" : false,
        "data_type" : "string",
        "value" : "signature impersonation"
      } ],
      "name": "Docusign Spoke JWT Provider",
      "jwt_api_script": "9ef6af86ff10330001d3cd6bd53bf144"
    },
    "name": "Docusign Spoke Credential",
    "table": "oauth_2_0_credentials"
  },
  "connection": {
    "use_mid": false,
    "connection_url": "https://<provider-domain-name>.com",
    "name": "Docusign Spoke Connection",
    "table": "http_connection"
  },
"additional":{
    "docusign_account_name": "<docusign-account-name>",
    "docusign_account_email": "<docusign-account-email>"
}
}
```

## Dynamic data schema

The dynamic data schema defines what the user sees when they create a Connection &amp; Credential alias and collects their input. Use dot-walking syntax to map user input to fields created in the default data template. For example, `connection_fields` maps user input to the `connection_url` field in the `connection` object created by the default data template.

```
{
  "connection_fields": [
    {
      "name": "connection.connection_url",
      "label": "Connection URL",
      "type": "text",
      "defaultValue": "https://demo.docusign.net",
      "hint": "Connection URL for Docusign"
    }],
"additional_fields":[
    {
      "name": "additional.docusign_account_id",
      "label": "Docusign Account Number",
      "type": "text",
      "hint": "Docusign Account Number"
    },
    {
      "name": "additional.docusign_account_name",
      "label": "Docusign Account Name",
      "type": "text",
      "hint": "Name to identify the Docusign account"
    },
    {
      "name": "additional.docusign_account_email",
      "label": "Docusign Account Email",
      "type": "text",
      "hint": "Docusign Account Email"
    }
  ],
  "credential_fields": [
    {
      "name": "credential.oauth_entity.client_id",
      "label": "OAuth Client ID",
      "type": "text",
      "hint": "Client ID for Docusign"
    },
    {
      "name": "credential.oauth_entity.redirect_url",
      "label": "OAuth Redirect URL",
      "type": "text",
      "defaultValue": "https://<instance-name>.service-now.com/oauth_redirect.do",
      "hint": "Callback URL for Docusign"
    },
 {
      "name": "credential.jwt_provider.jwt_claim_validation[0].value",
      "label": "Issuer (iss) Claim value",
      "type": "text",
      "hint": "The integrator key (also known as client ID) of the application"
    },
 {
      "name": "credential.jwt_provider.jwt_claim_validation[1].value",
      "label": "Subject (sub) Claim value",
      "type": "text",
      "hint": "The user ID of the user to be impersonated"
    },
 {
      "name": "credential.jwt_provider.jwt_claim_validation[2].value",
      "label": "Audience (aud) Claim value",
      "type": "text",
      "defaultValue": "account-d.docusign.com",
      "hint": "The URI of the authentication service instance to be used e.g. account.docusign.com"
    },
    {
      "name": "credential.jwt_provider.jwt_keystore_aliases.kid",
      "label": "Key ID (kid)",
      "type": "text",
      "hint": "Indicates which key was used to secure the JWS"
    },
    {
      "name": "credential.jwt_provider.jwt_keystore_aliases.signing_keystore",
      "label": "Key Store",
      "type": "file"
    }
  ]
}
```

## Post processing script

The following post processing script maps user input to fields in the sn\_docusign\_spoke\_accounts table.

```
(function execute(aliasId, connectionSysId, jsonDefaultData, jsonDynamicData) {
	var jsonDynamicDataP = JSON.parse(jsonDynamicData);
	var accountGR = new GlideRecord("sn_docusign_spoke_accounts");
    accountGR.setValue("account_name", jsonDynamicDataP["additional.docusign_account_name"]);
    accountGR.setValue("alias", aliasId);
    accountGR.setValue("email", jsonDynamicDataP["additional.docusign_account_email"]);
    accountGR.setValue("id", jsonDynamicDataP["additional.docusign_account_id"]);
    accountGR.insert();
})(aliasId, connectionSysId, jsonDefaultData, jsonDynamicData);
```

## Resulting Docusign Connection and Credential configuration form

When the user navigates to the associated Docusign Connection &amp; Credential Alias and selects **Create New Connection &amp; Credential**, the following dialog appears.

![Docusign form requiring user input.](../image/docusign-template.png)

**Parent Topic:**[Connection &amp; Credential configuration templates](../concept/spoke-configuration-template.md)

