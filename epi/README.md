# ePI - electronic Product Information
Please find information about setting up the ePI-API [here](https://www.google.com)
and the openapi documentation with testing capabilites [here](https://www.google.com).

## API URL
After successfully setting up the ePI-API it is available through a link which follows the following structure:

```https://{serverPath}/mappingEngine/{epiDomain}/{companyVaultDomain}```

E.g.: https://epi-singapore-dev.535161841476.cloud.bayer.com/mappingEngine/epipoc/vault.my-company

*How to find link?*
*Always the same structure?*

## Verification and Authentication

In order to authenticate API-requests you need to use a valid token. This token will be sent with the API requests.

Tokens are generated in the enterprise wallet specific for each user. After logging in you can find the token under the tab "User as Holder" called "Wallet Identifier". The access rights can be permitted to a specific user in the demiurge wallet.

When sending API-requests the token needs to be added in the header of the request. The name of the header variable is "token" and the value is the wallet identifier.

*Authentication with OAuth?*

## Single Sign On (SSO) with OAuth
ePI allows the integration of SSO with OAuth. OAuth (Open Authorization) is an open standard for access delegation, commonly used as a way for Internet users to grant websites or applications access to their information on other websites but without giving them the passwords.

Please find details about the integration process of OAuth [here.](https://upm365.sharepoint.com/:w:/r/sites/PharmaLedger/_layouts/15/doc2.aspx?sourcedoc=%7B58261221-3903-4080-81BC-B3CBEA78451E%7D&file=ePI%20-%20Enterprise%20Wallet%20SSO%20authentication%20methodology.docx&action=default&mobileredirect=true&DefaultItemOpen=1&params=eyJBcHBOYW1lIjoiVGVhbXMtRGVza3RvcCIsIkFwcFZlcnNpb24iOiIyNy8yMjAzMDcwMTYxMCJ9&cid=8e0c4949-c9e1-4b9a-9c64-0032c2959199)

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
