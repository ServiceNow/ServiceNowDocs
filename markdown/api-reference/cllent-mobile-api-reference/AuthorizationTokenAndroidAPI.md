---
title: AuthorizationToken class - Android
description: The AuthorizationToken class provides the authorization token provided by the host application. Used by the NowSDK to authorize access to a specified ServiceNow instance for the currently logged in user.Returns the authorization token provided by the host application.
locale: en-US
release: xanadu
product: Cllent Mobile API Reference
classification: cllent-mobile-api-reference
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Mobile SDK API reference - Android, Mobile SDK API reference, API reference, API implementation and reference]
---

# AuthorizationToken class - Android

The AuthorizationToken class provides the authorization token provided by the host application. Used by the NowSDK to authorize access to a specified ServiceNow instance for the currently logged in user.

<table id="table_vx2_klw_5pb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

token

</td><td>

String

</td><td>

Value of the authorization token.

</td></tr><tr><td>

type

</td><td>

String

</td><td>

Type of authorization token.Valid values \(case-sensitive\):

-   JWT
-   OAuthAccess
-   OAuthRefresh

</td></tr></tbody>
</table>**Parent Topic:**[Mobile SDK API reference - Android](../../concept/MobileSDKAndroidAPI.md)

## AuthorizatonToken - AuthorizationToken\(type: AuthorizationTokenType, token: String\)

Returns the authorization token provided by the host application.

<table id="table_orr_1gn_cqb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

type

</td><td>

String

</td><td>

Type of authorization token.Valid values \(case-sensitive\):

-   JWT
-   OAuthAccess
-   OAuthRefresh

</td></tr><tr><td>

token

</td><td>

String

</td><td>

Value of the authorization token.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

```
class SDKManager @Inject constructor(
  private val settings: Provider<NowSDKSettings>,
  private val jwtService: JWTService
) : NowSDKAuthorizationProviding,
  DevicePermissionDelegate {

  override fun requestAuthorization(
    instanceURL: URL,
    callback: Consumer<List<AuthorizationToken>?>
  ) {
      GlobalScope.launch(Dispatchers.IO) {
        try {
          val token = jwtService.getJWT(settings.get().user, settings.get().clientId).token
          callback.accept(
            listOf(
              AuthorizationToken(
                AuthorizationTokenType.JWT,
                token
              )
            )
          )
        } catch (ex : Exception) {
           Log.e("JWT", "Failed to get jwt", ex)
           return@launch callback.accept(null)
        }
      }
    }
```

