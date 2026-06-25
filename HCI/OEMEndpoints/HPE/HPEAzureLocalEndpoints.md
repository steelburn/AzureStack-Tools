# HPE required endpoints for Azure Local deployments

This page provides a comprehensive overview of the necessary endpoints for deploying Azure Local using HPE solutions. These URLs are maintained by the OEM hardware vendor. Please contact with your OEM provider if these URLs need to be updated.

Each hardware vendor provided [Solution Builder Extension (SBE)](https://learn.microsoft.com/en-us/azure/azure-local/update/solution-builder-extension) will require some minimal endpoints to allow for discovery and download of [SBE](https://learn.microsoft.com/en-us/azure/azure-local/update/solution-builder-extension) updates for your solution.

Refer to the table in the following document to determine if your solution supports an SBE as well is to review SBE release notes or and other documentation: https://learn.microsoft.com/en-us/azure/azure-local/update/solution-builder-extension?view=azloc-24113#identify-a-solution-builder-extension-update-for-your-hardware

In addition to [SBE](https://learn.microsoft.com/en-us/azure/azure-local/update/solution-builder-extension) endpoints, some OEM hardware vendors will require additional endpoints for there specific use cases as noted below.

**Last updated on June 25, 2026**

| Id | Endpoint Description | Endpoint URL                                                           | Port | Notes                                                    | Arc gateway support | Required for                 |
|----|---------------------|------------------------------------------------------------------------|------|----------------------------------------------------------|---------------------|------------------------------|
| 1  | SBE Manifest endpoint (primary)   | h41380.www4.hpe.com/hpe/microsoft/SBE_Discovery_HPE.xml  | 443  | Enables discovery and confirmation of validity for SBE updates from OEM. | No                  | Deployment & Post deployment |
| 2  | SBE Manifest endpoint (secondary)   | h41380.www4.hpe.com/hpe/SBE/SBE_Discovery_HPE.xml  | 443  | Enables discovery and confirmation of validity for SBE updates from OEM.  | No                  | Deployment & Post deployment |
| 3  | SBE Manifest redirection link (primary)     | aka.ms/AzureStackSBEUpdate/HPE                                   | 443  | Microsoft redirection to the explicit OEM SBE manifest endpoint. | No                 | Deployment & Post deployment |
| 4  | SBE Manifest redirection link (secondary)    | aka.ms/AzureStackSBEUpdate/HPE-ProLiant-Standard                                    | 443  | Microsoft redirection to the explicit OEM SBE manifest endpoint.  | No                 | Deployment & Post deployment |
| 5  | SBE Manifest download connector link   | h30302.www3.hpe.com/pub/*                        | 443  | Enables SBE download connector support.<br><br>The package and meta files of each SBE release are posted in the repository “h30302.www3.hpe.com/pub/” for download purpose. For example:<br><br>h30302.www3.hpe.com/pub/SBE_HPE_ProLiant-Standard_5.0.2604.21.zip?merchantId=PUB_DROPBOX<br><br>h30302.www3.hpe.com/pub/SBE_HPE_ProLiant-Standard_5.0.2604.21.xml?merchantId=PUB_DROPBOX | No                 | Download Connector
