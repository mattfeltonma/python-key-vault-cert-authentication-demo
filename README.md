# Azure Key Vault and client certificates demo in Python
This solution demonstrates how a client certificate stored in [Azure's Key Vault](https://docs.microsoft.com/en-us/azure/key-vault/) can be retrieved using an [Azure Managed Identity](https://docs.microsoft.com/en-us/azure/active-directory/managed-identities-azure-resources/overview) and then be used to query the Azure Resource Manager API.

It is written in Python 3 and uses the [Microsft Azure Python SDKs](https://docs.microsoft.com/en-us/azure/developer/python/azure-sdk-overview) and the [Microsoft Authentication Library (MSAL).](https://docs.microsoft.com/en-us/azure/active-directory/develop/msal-overview)

## What problem does this solve?
Secure credential management remains a challenge in the public cloud.  Azure Key Vault addresses this challenge by providing secure storage for keys, secrets, and certificates which can then be made programmatically available to applications.  The certificate capability creates an opportunity to shift from using passwords and secrets to a higher assurance credential in the form of a certificate.  

## Requirements

### Resources
* A managed identity assigned to a resource running in Azure
* An instance of Azure Key Vault where managed identity has been granted the [GetSecret permission](https://docs.microsoft.com/en-us/azure/key-vault/general/secure-your-key-vault)
* A client certificate that has been [imported](https://docs.microsoft.com/en-us/azure/key-vault/certificates/tutorial-import-certificate) or created in Azure Key Vault and has been configured with a content type of PEM

## Setup

1. Use pip to install the required libraries.
2. Modify __init__.py to provide the required variables.
3. Run the solution.
