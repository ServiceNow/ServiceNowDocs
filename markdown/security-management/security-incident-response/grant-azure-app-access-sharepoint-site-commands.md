---
title: Commands to grant Azure application access to the Microsoft SharePoint site
description: Use one of the following three methods to grant your registered Azure application write access to the Microsoft SharePoint site at the site level, using the Microsoft Graph API.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/security-management/security-incident-response/grant-azure-app-access-sharepoint-site-commands.html
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: reference
last_updated: "2026-07-03"
reading_time_minutes: 3
breadcrumb: [Integrate Major Security Incident Management with Microsoft SharePoint, Integrate, Major Security Incident Management, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Commands to grant Azure application access to the Microsoft SharePoint site

Use one of the following three methods to grant your registered Azure application write access to the Microsoft SharePoint site at the site level, using the Microsoft Graph API.

**Note:** These commands are provided for reference only and are not sourced from an external tool vendor. Only one method is required — choose the method that best matches what the Azure administrator already has installed. All three methods achieve the same result.

|Placeholder|Example value|Where to find it|
|-----------|-------------|----------------|
|YOUR\_TENANT\_ID|xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx|Azure App Registration &gt; Overview &gt; Directory \(tenant\) ID|
|YOUR\_CLIENT\_ID|yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy|Azure App Registration &gt; Overview &gt; Application \(client\) ID|
|YOUR\_CLIENT\_SECRET|abc123XYZ~mySecretValue|Azure App Registration &gt; Certificates &amp; secrets &gt; Client secrets &gt; Value|
|YOUR\_TENANT / TENANT\_NAME|contoso|The Microsoft 365 tenant name — the subdomain before .sharepoint.com|
|YOUR\_SITE\_NAME / SITE\_NAME|MSIMSite|The Microsoft SharePoint site name — the relative path segment after /sites/|
|APP\_REGISTRATION\_DISPLAY\_NAME|Microsoft SharePoint Graph|The display name entered when registering the App|
|YOUR\_TOKEN\_FROM\_STEP1|eyJ0eXAiOiJKV1Qi...|Curl method only — the access\_token value from the Step 1 response|
|YOUR\_SITE\_ID\_FROM\_STEP\_2|contoso.sharepoint.com,abc123,def456|Curl method only — the id value from the Step 2 response|

## Method 1 — Curl

Replace all placeholders with values from the table above before executing. Copy the access\_token from Step 1 and the site id from Step 2 for use in Step 3.

```
# Step 1: Get OAuth Token for the Registered Azure Application
curl --location --request GET 'https://login.microsoftonline.com/YOUR_TENANT_ID/oauth2/v2.0/token' \
    --header 'accept: application/json' \
    --data-urlencode 'grant_type=client_credentials' \
    --data-urlencode 'client_id=YOUR_CLIENT_ID' \
    --data-urlencode 'client_secret=YOUR_CLIENT_SECRET' \
    --data-urlencode 'scope=https://graph.microsoft.com/.default'
# From the response JSON, copy the access_token value -- this becomes YOUR_TOKEN_FROM_STEP1

# Step 2: Retrieve SharePoint Site ID
curl --location 'https://graph.microsoft.com/v1.0/sites/YOUR_TENANT.sharepoint.com:/sites/YOUR_SITE_NAME' \
    --header 'Authorization: Bearer YOUR_TOKEN_FROM_STEP1'
# From the response JSON, copy the id value -- this becomes YOUR_SITE_ID_FROM_STEP_2

# Step 3: Grant Azure Application Permissions to the SharePoint Site
curl --location 'https://graph.microsoft.com/v1.0/sites/YOUR_SITE_ID_FROM_STEP_2/permissions' \
    --header 'Content-Type: application/json' \
    --header 'Authorization: Bearer YOUR_TOKEN_FROM_STEP1' \
    --data '{"roles": ["write"], "grantedToIdentities": [{"application": {"id": "YOUR_CLIENT_ID", "displayName": "APP_REGISTRATION_DISPLAY_NAME"}}]}'
```

## Method 2 — Azure CLI

Replace the placeholder variable values at the top of the script with your actual values, then execute the full script. Requires the Azure CLI. For installation, see [Install Azure CLI](https://learn.microsoft.com/en-us/cli/azure/install-azure-cli).

```
#!/bin/bash
# Replace placeholder values with your actual values
TENANT_ID="YOUR_TENANT_ID"
CLIENT_ID="YOUR_CLIENT_ID"
CLIENT_SECRET="YOUR_CLIENT_SECRET"
TENANT_NAME="YOUR_TENANT"  # e.g., contoso
SITE_NAME="YOUR_SITE_NAME"
APP_DISPLAY_NAME="APP_REGISTRATION_DISPLAY_NAME"

# Authenticate with Azure AD (without requiring a subscription)
az login --service-principal -u "$CLIENT_ID" -p "$CLIENT_SECRET" --tenant "$TENANT_ID" --allow-no-subscriptions

# Get access token for Microsoft Graph API
ACCESS_TOKEN=$(az account get-access-token --resource https://graph.microsoft.com --query accessToken --output tsv)
if [ -z "$ACCESS_TOKEN" ]; then echo "Failed to retrieve access token." >&2; exit 1; fi

# Fetch SharePoint Site ID
SITE_ID=$(az rest --method GET --uri "https://graph.microsoft.com/v1.0/sites/$TENANT_NAME.sharepoint.com:/sites/$SITE_NAME" --headers "Authorization=Bearer $ACCESS_TOKEN" --query "id" --output tsv)
if [ -z "$SITE_ID" ]; then echo "Failed to retrieve SharePoint Site ID." >&2; exit 1; fi

# Grant App Permissions to SharePoint Site
az rest --method POST --uri "https://graph.microsoft.com/v1.0/sites/$SITE_ID/permissions" \
    --headers "Authorization=Bearer $ACCESS_TOKEN" "Content-Type=application/json" \
    --body "{\"roles\": [\"write\"], \"grantedToIdentities\": [{\"application\": {\"id\": \"$CLIENT_ID\", \"displayName\": \"$APP_DISPLAY_NAME\"}}]}"
```

## Method 3 — PowerShell

Replace the placeholder variable values at the top of the script with your actual values, then execute the full script. For installation, see [Install PowerShell](https://learn.microsoft.com/en-us/powershell/scripting/install/installing-powershell).

```
# Define Variables -- Replace placeholder values with actual values
$tenantId = "YOUR_TENANT_ID"
$clientId = "YOUR_CLIENT_ID"
$clientSecret = "YOUR_CLIENT_SECRET"
$tenantName = "YOUR_TENANT"
$siteName = "SITE_NAME"
$appDisplayName = "APP_REGISTRATION_DISPLAY_NAME"

try {
    # Step 1: Get Access Token
    $tokenResponse = Invoke-RestMethod -Method Post -Uri "https://login.microsoftonline.com/$tenantId/oauth2/v2.0/token" -Body @{ grant_type = "client_credentials"; client_id = $clientId; client_secret = $clientSecret; scope = "https://graph.microsoft.com/.default" } -ContentType "application/x-www-form-urlencoded"
    $accessToken = $tokenResponse.access_token
    if (-not $accessToken) { throw "Failed to retrieve access token." }

    # Step 2: Get SharePoint Site ID
    $siteResponse = Invoke-RestMethod -Uri "https://graph.microsoft.com/v1.0/sites/$tenantName.sharepoint.com:/sites/$siteName" -Method Get -Headers @{ "Authorization" = "Bearer $accessToken" }
    $siteId = $siteResponse.id
    if (-not $siteId) { throw "Failed to retrieve SharePoint Site ID." }

    # Step 3: Grant App Permissions
    $body = @{ roles = @("write"); grantedToIdentities = @(@{ application = @{ id = $clientId; displayName = $appDisplayName } }); displayName = "$appDisplayName" } | ConvertTo-Json -Depth 10
    Invoke-RestMethod -Uri "https://graph.microsoft.com/v1.0/sites/$siteId/permissions" -Method Post -Headers @{ "Authorization" = "Bearer $accessToken"; "Content-Type" = "application/json" } -Body $body
} catch { Write-Host "Error: $_" -ForegroundColor Red; exit 1 }
```

## External references

These references are external to ServiceNow® and are provided for tooling installation and API reference only. The commands above are sourced from the Major Security Incident Management Workspace UI, not from these external links.

-   [Microsoft Graph API — Site Permissions reference](https://learn.microsoft.com/en-us/graph/api/site-post-permissions)
-   [Microsoft Entra ID App Registration reference](https://learn.microsoft.com/en-us/entra/identity-platform/quickstart-register-app)

**Parent Topic:**[Integrate Major Security Incident Management with Microsoft SharePoint](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-incident-response/integrate-msim-sharepoint.md)

