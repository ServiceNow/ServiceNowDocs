---
title: Enable e-signature for Service Portal
description: You can configure e-signature in Service Portal to require re-authentication from approving users.Open a new window for SSO authentication when using e-Signature for approvals.Paste the spEsignatureCustom script in the sys\_ui\_script.list script field.Paste the spAuthCustom script in the sys\_ui\_script.list script field.
locale: en-US
release: yokohama
product: Service Portal
classification: service-portal
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 5
breadcrumb: [Managing portal access, Configuring Service Portal, Service Portal, Configure UIs and portals, Configure user experiences]
---

# Enable e-signature for Service Portal

You can configure e-signature in Service Portal to require re-authentication from approving users.

## Before you begin

The **com.snc.integration.esig.window** system property is supported to enable SSO login in a new window.

Role required: admin

## Procedure

1.  Activate the Approvals with e-Signature \[com.glide.e\_signature\_approvals\] plugin.

2.  Navigate to **System Definition** &gt; **e-Signature Registry**.

3.  Add any tables you want to require an e-signature for to the list.


## Result

With e-signature enabled, approvers are required to provide a password to approve or reject any requests. Authentication with touch ID works in the mobile app. On the mobile web, approvers are still required to enter a password. For more information on configuring e-signature, see [Approval with e-signature](https://www.servicenow.com/docs/access?context=approval-with-e-signature&version=yokohama&pubname=yokohama-build-workflows&ft:locale=en-US).

**Parent Topic:**[Managing portal access](../concept/portal-security.md)

## Enable SSO login in a new window

Open a new window for SSO authentication when using e-Signature for approvals.

### Before you begin

Security Assertion Markup Language \(SAML\) login is only supported on the desktop Service Portal.

For additional information, see the [e-signature SSO login KB article](https://support.servicenow.com/kb?id=kb_article_view&sys_kb_id=2dca1fe8db49a010190b1ea668961999).

Role required: admin

### Procedure

1.  Enter the spEsignatureCustom script.

    1.  Enter `sys_ui_script.list` in the Filter navigator.

    2.  Select **New**, and create a new UI script.

    3.  On the UI Script form, enter `spEsignatureCustom` in the API Name field.

    4.  In the UI Type field, select **Mobile/Service Portal**.

    5.  Paste the [spEsignatureCustom script](enable-esignature-sp.md#) in the **Script** field.

    6.  Select **Submit**.

2.  Enter the spAuthCustom script.

    1.  In the same `sys_ui_script.list` table, create another new UI script by selecting **New**.

    2.  On the UI Script form, enter `spAuthCustom` in the API Name field.

    3.  In the UI Type field, select **Mobile/Service Portal**.

    4.  Paste the [spAuthCustom script](enable-esignature-sp.md#) in the **Script** field.

    5.  Select **Submit**.

3.  Associate the UI scripts to the JS Include record.

    1.  Navigate to **Service Portal** &gt; **Portals**.

    2.  Identify the Service Portal you want to apply the esignature support to and select the Theme.

    3.  In the related lists, select **JS Includes**.

    4.  Select **New**.

    5.  On the form, fill in the fields.

        |Field|Description|
        |-----|-----------|
        |Display name|Name for your JS Include. Enter `spEsignatureCustom` and associate the record with the spEsignatureCustom UI script you created, or enter `spAuthCustom` and associate the record with spAuthCustom you created.|
        |Source|Source for your JS Include record. Select **UI Script**.|
        |UI script|UI script source for your JS Include record. Select either spEsignatureCustom or spAuthCustom depending on the record you're creating.|
        |Application|Application for your JS Include record. The default application is **Global**.|
        |Updated|Field displaying when the record was last updated.|
        |Package|Field that establishes the JS Include package.|

    6.  Select **Submit**.


### Result

A new window opens when you use E-Signature for approvals.

## spEsignatureCustom script

Paste the spEsignatureCustom script in the sys\_ui\_script.list script field.

```
angular.module('sn.$sp').provider('spEsignature', function() {
	'use strict';

	this.$get = function spEsignature($q, $http, $window, urlTools, xmlUtil) {
		var w = window;
		var esignOW;
		var windowWidth;
		var windowHeight;
		var redirectURL;

		function isWindowChosen() {
			var postParams = {
				sysparm_scope: 'global',
				sysparm_processor: 'ESignatureAuthUtils',
				sysparm_name: 'isWindowChosen'
			};
			return $http({
				method: 'POST',
				url: '/xmlhttp.do',
				data: urlTools.encodeURIParameters(postParams),
				headers: {
					'Content-Type': 'application/x-www-form-urlencoded'
				},
				transformResponse: function(response) {
					return xmlUtil.getDataFromXml(response);
				}
			}).then(
				function(response) {
					var data = response.data ? response.data[0] : {};
					return data.answer ===  'true'
				},
				function(response) {
					// Handling failure case.
					switch (response.status) {
						default:
						case 404:
							return false;
					}
				});
		}

		function initiateEsignature() {
			var postParams = {
				sysparm_scope: 'global',
				sysparm_processor: 'ESignatureAuthUtils',
				sysparm_name: 'fetchAuthDetails'
			}
			return $http({
				method: 'POST',
				url: '/xmlhttp.do',
				data: urlTools.encodeURIParameters(postParams),
				headers: {
					'Content-Type': 'application/x-www-form-urlencoded'
				},
				transformResponse: function(response) {
					return xmlUtil.getDataFromXml(response, 'result');
				}
			}).then(
				function(response) {
					var data = response.data ? response.data[0] : {};
					process(data);
				});
		}

		function process(data) {
			var shouldLogoutFirst = data.logoutFirst === 'true';
			w['windowHeight'] = data.popup_window_height;
			w['windowWidth'] = data.popup_window_width;
			w['redirectURL'] = data.loginURL;
			if (shouldLogoutFirst)
				openEsignatureWindow(data.logoutURL);
			else
				authenticate();
		}

		function openEsignatureWindow(url) {
			w['esignOW'] = window.open(url, 'esignatureAuthentication',
				'height='+w['windowHeight']+',width='+w['windowWidth']+',top=100,left=100,toolbar=0,location=0,menubar=0');
		}

		w['authenticate'] = function(){
			if(w['redirectURL']){
				if(w['esignOW']) //when we signed out previously, a window is already opened. reuse it.
					w['esignOW'].location.href = w['redirectURL'];
				else
					openEsignatureWindow(w['redirectURL']);
			}
		};

		w['evaluateRedirect'] = function(msg) {
			w['esignOW'].close();
			if (msg == "saml2 login complete") {
				$window.onReauthenticationComplete(msg);
			}
		};

		return {
			isWindowChosen: isWindowChosen,
			initiateEsignature: initiateEsignature
		};

	};
});

```

## spAuthCustom script

Paste the spAuthCustom script in the sys\_ui\_script.list script field.

```
angular.module('sn.$sp').factory('spAuthModal', function($q, spModal, i18n, $http, spAuthentication, glideUserSession, cabrillo, $cookies, $window, spUtil, $uibModal, spEsignature) {
	"use strict";

	function _showAuthenticationModal(requestParams, username, userSysId) {
		var currentUser;
		var deferred = $q.defer();
		glideUserSession.loadCurrentUser({reload: true}).then(function(user) {
			if (!user) {
				deferred.reject({
					error: {
						status: 'ANONYMOUS',
						message: i18n.getMessage('Not logged in')
					}
				});
				return;
			}
			currentUser = user;
			var serializedUser = {
				sysId: currentUser.userID,
				userName: currentUser.userName,
				firstName: currentUser.firstName,
				lastName: currentUser.lastName
			};

			// hand off to native clients
			if (cabrillo.isNative()) {
				cabrillo.auth.reauthenticate(currentUser).then(function() {
					deferred.resolve(serializedUser);
				}, function(error) {
					if (error && error.status) {
						deferred.reject({
							error: error
						});
					}
					//TODO: Handle rejection a little more gracefully
					deferred.reject();
				});
				return;
			}

			var loginMethod = currentUser.$private.loginMethod;
			if (!loginMethod) {
				// As we were unable to determine the login method via the HTTP session, trying to get glide_sso_id cookie which is set in case of multisso login
				var providerSysId = $cookies.get('glide_sso_id');
				loginMethod = providerSysId ? 'multisso' : 'db';
			}

			if (loginMethod === 'saml' || loginMethod === 'oidc' || loginMethod === 'multisso') {
				spEsignature.isWindowChosen().then(function(result) {
					var modal;
					if (!spUtil.isMobile() && loginMethod !== 'oidc' && result === true) {
						// If enabled, Opening a new window for desktop saml login
						spEsignature.initiateEsignature();
					} else {
						glideUserSession.getSsoReauthenticationUrl().then(function(url) {
							requestParams.externalLoginURL = url;
							openExternalAuthModal(requestParams).then(function(m) {
								modal = m;
							});
						});
					}
					$window.onReauthenticationComplete = function(result) {
						deferred.resolve(serializedUser);
						if (modal)
							modal.close();
					};
				});
			} else {
				spModal.open({
					title:i18n.getMessage("Approver authentication"),
					message:i18n.getMessage("Additional authentication is required, enter your usename and password to continue."),
					footerStyle: {border: 'none', 'padding-top': 0},
					widget: 'simpleloginui',
					widgetInput: {},
					shared: requestParams,
					onSubmit: function() {
						return onLoginModalSubmit(requestParams, username);
					}
				}).then(function(confirm) {
					if (confirm.label == i18n.getMessage("OK")) {
						deferred.resolve(serializedUser);
					} else {
						deferred.reject();
					}
				});
			}
		});

		return deferred.promise;
	}

	function onLoginModalSubmit(requestParams, username) {
		//(1) call login service to verify auth
		//(2) verify same user
		return $q(function(resolve, reject) {
			var errorMessage = null;

			if(!requestParams.username || requestParams.username.trim() === "" ||
					!requestParams.password || requestParams.password.trim() === "") {
				errorMessage = i18n.getMessage("User name or password invalid");
			} else if(requestParams.username !== username) {
				errorMessage = i18n.getMessage("Attempted to authenticate as a different user");
			}

			if(!errorMessage || errorMessage === "") {
				spAuthentication.validateCreds(requestParams.username, requestParams.password).then(function(res) {
					resolve({status: res.success, errorMessage: res.message});
				});
			} else {
				resolve({status: !errorMessage || errorMessage === "", errorMessage: errorMessage});
			}
		});

	}

	function openExternalAuthModal(requestParams) {
		var deferred = $q.defer();

		var options = {
			title: i18n.getMessage("Approver authentication"),
			message: '',
			messageOnly: false,
			errorMessage: '',
			input: false,
			label: '',
			size: 'lg',
			value: '',
			required: false,
			footerStyle: {border: 'none', 'padding-top': 0},
			values: false,
			onSubmit: null,
			widget: 'simpleloginui',
			widgetInput: {},
			shared: requestParams,
			buttons: [{label: i18n.getMessage('Cancel'), cancel:true}]
		};

		var widgetURL = spUtil.getWidgetURL(options.widget);
		$http.post(widgetURL, options.widgetInput).success(function(response) {
			options.widget = response.result;
			options.widget.options.shared = options.shared;
			var modal = $uibModal.open({
				templateUrl:'sp-modal.html',
				controller: spModalCtrl,
				size: options.size,
				resolve: {
					options: function() {
						return options;
					}
				}
			});

			deferred.resolve(modal);
		});
		
		return deferred.promise;
	}

	function spModalCtrl($scope, options) {
		$scope.options = options;
		$scope.form = {};

		$scope.buttonClicked = function(button){
			if (button.cancel) {
				$scope.$dismiss();
				return;
			}
		}
	}

	return {
		prompt: _showAuthenticationModal
	}
}).decorator("spAuthModal", function($delegate) { return( $delegate );});

```

