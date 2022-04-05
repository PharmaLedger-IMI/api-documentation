# ePI - electronic Product Information
Please find information about setting up the ePI-API [here](https://www.google.com)
and the openapi documentation with testing capabilites [here](https://www.google.com).

## API URL
After successfully setting up the ePI-API it is available through a link which follows the following structure:

```
https://{serverPath}/mappingEngine/{epiDomain}/{companyVaultDomain}
E.g.: https://epi-singapore-dev.535161841476.cloud.bayer.com/mappingEngine/epipoc/vault.my-company
```
## Verification and Authentication

In order to authenticate API-requests you need to use a valid token. This token will be sent with the API requests.
Tokens are generated in the enterprise wallet specific for each user. After logging in you can find the token under the tab "User as Holder" called "Wallet Identifier". The access rights can be permitted to a specific user in the demiurge wallet.
When sending API-requests the token needs to be added in the header of the request. The name of the header variable is "token" and the value is the wallet identifier.

## Single Sign On (SSO) with OAuth

### Overview

Single Sign On (SSO) services protocol used is oAuth for connection.  Federation SSO uses a trust model where the application trusts a message signed by the SSO server.  This removes the application from having to directly validate the user's ID & password against LDAP/Active Directory.

Authentication vs. Authorization:
Authentication and authorization are the security measures taken in -order to protect data and systems.  Authentication is the process of verifying the person’s identity who is attempting to access the system.  Authorization is the responsibility of the application owner and is a crucial part of checking the privileges or access list for which the person is authorized.
An overview of High-level flow is provided below:
**insert ascii chart**

### Prerequisite
-	Access to Identity Provider such as Azure LDAP
-	Epi-workspace 

To enable SSO in application, application need to have tenant-client ID and modify epi-workspace source code as explained in below two steps. This document is prepared assuming that Azure being used for ePI application registration for tenant and client ID:

#### 1. Getting tenant and client ID for ePI application

| Step  | Location |
| ------------- | ------------- |
| 1. Refer to the two links below for registering your ePI in Azure Active Directory:<br>[How to get Azure api credentials](https://www.inkoop.io/blog/how-to-get-azure-api-credentials/)<br>[How to find tenant](https://docs.microsoft.com/en-us/azure/active-directory/fundamentals/active-directory-how-to-find-tenant)| As per your organization  |
| 2. Put custom scope as explained in the following link:<br>[Quickstart app expose web apis](https://docs.microsoft.com/en-us/azure/active-directory/develop/quickstart-configure-app-expose-web-apis) | As per your organization  |
| 3. Call back URL value in Azure registration must match with:<br>3.1 ‘redirectPath’ value in apihub.json  ‘http://localhost:8080/?root=true’<br>3.2 ‘postLogoutRedirectUrl’ value in apihub.json  ‘http://localhost:8080/?logout=true’ | Common for all and as defined in apihub.json  |

#### 2. Source code modification



## Fields and Data Types
There are three different types of requests: batch, product, leaflet (split into basis and images).

Please find the request documentation [here]()

and the detailed fields and data type specification [here](https://github.com/PharmaLedger-IMI/api-documentation/blob/6895ba69a1065dfdbb81a982dc7418a73f7dca42/fgt/schema/product_create.json).

## Callback URL

How is it defined?

## Buffering

Is there buffering in place? What is the maximum capacity?

## Try it out

### Swagger
Swagger is a collection of open source tools to design, build, document, and use HTTP web services (also called HTTP API or REST-like API).

Find the current openapi documentation in Swagger and ready for testing [here](https://www.google.com).

### Postman
Postman is an API platform for building and using APIs. 

You can install Postman from their website [here](https://www.postman.com/downloads/).
After opening Postman you can [click on import](https://learning.postman.com/docs/integrations/available-integrations/working-with-openAPI/) and select the openapi documentation.

For further details refer to the [Postman Docs](https://learning.postman.com/docs/getting-started/introduction/):
- [Navigating Postman](https://learning.postman.com/docs/getting-started/navigating-postman/)
- [Send your first request](https://learning.postman.com/docs/getting-started/sending-the-first-request/)
- [more](https://learning.postman.com/docs/getting-started/introduction/)
