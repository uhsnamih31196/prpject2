# UKSC Azure Modules

This repository contains Bicep modules used to deploy the UK Supreme Court website to Azure.

## Modules

### CMS Module

The `cms.bicep` module is used to deploy the CMS for the UK Supreme Court website.

## Parameters

| Parameter | Description | Type | Default |
| --- | --- | --- | --- |
| `acrUseManagedIdentityCreds` | acrUseManagedIdentityCreds | bool |  |
| `alwaysOn` | alwaysOn | bool |  |
| `appServicePlanId` | Id of App service plan to use | string |  |
| `cmsContainerImage` | container image to use | string |  |
| `databaseName` | Name of database | string |  |
| `databasePassword` | password for SqlDB | string (secure) |  |
| `databaseUser` | database user for SqlDB | string |  |
| `detailedErrorLoggingEnabled` | detailedErrorLoggingEnabled | bool |  |
| `enabledForTemplateDeployment` | enabledForDeployment | string |  |
| `enablePurgeProtection` | enablePurgeProtection for KV | bool |  |
| `enableRbacAuthorization` | enable RbacAuthorization | bool |  |
| `enableSoftDelete` | enable SoftDelete | string |  |
| `existingManagedIdentityCms` | existingManagedIdentityCms | string |  |
| `existingPrivateDnsZoneDb` | existingPrivateDnsZoneDb | string |  |
| `existingPrivateDnsZoneKeyvault` | existingPrivateDnsZoneKeyvault | string |  |
| `existingVnet` | existingVnet | string |  |
| `frontDoorId` | Id of frontdoor | string |  |
| `ftpsState` | ftpsState | string |  |
| `http20Enabled` | http20Enabled | bool |  |
| `httpLoggingEnabled` | httpLoggingEnabled | bool |  |
| `httpsOnly` | httpsOnly | bool |  |
| `kvSku` | kvSku | string |  |
| `kvSkuFamily` | kvSkuFamily | string |  |
| `location` | The location of the resources. | string |  |
| `persistentResourceGroup` | The name of the resource group to deploy to. | string |  |
| `publicNetworkAccess` | publicNetworkAccess | string |  |
| `requestTracingEnabled` | requestTracingEnabled | bool |  |
| `resourcePrefix` | The prefix to use for all resources. | string |  |
| `sqlDbSku` | Sku for SqlDb | string |  |
| `sqlDbTier` | Tier for SqlDB | string |  |
| `tenantId` | The tenant ID of the Azure AD tenant used for authentication. | string |  |


#### Deployment

To deploy the CMS module, follow these steps:

1. Clone the repository and navigate to the `cms` directory.
2. Run the `bicep build` command to build the module.
3. Run the `az deployment group create` command to deploy the module to Azure.

For more information on deploying Bicep modules, see the [Bicep documentation](https://docs.microsoft.com/en-us/azure/azure-resource-manager/bicep/overview).

### Component Module

The `component.bicep` module is used to deploy the components for the UK Supreme Court website.

## Parameters

| Parameter | Description | Type | Default |
| --- | --- | --- | --- |
| `acrUseManagedIdentityCreds` | acrUseManagedIdentityCreds | bool |  |
| `alwaysOn` | alwaysOn | bool |  |
| `aspKind` | Update kind for App Service Plan it can be Windows or Linux | string |  |
| `aspSku` | Update SKU for App Service Plan | string |  |
| `aspTier` | Update Tier for App Service Plan | string |  |
| `cmsContainerImage` | cmsContainerImage | string |  |
| `databaseName` | databaseName | string |  |
| `databasePassword` | databasePassword | string |  |
| `databaseUser` | databaseUser | string |  |
| `dbPrivateEndpointsSubnetName` | db PrivateEndpoints SubnetName | string |  |
| `detailedErrorLoggingEnabled` | detailedErrorLoggingEnabled | bool |  |
| `enabledForTemplateDeployment` | enableForTemplateDeployment | string |  |
| `enablePurgeProtection` | enablePurgeProtection for KV | bool |  |
| `enableRbacAuthorization` | enableRbacAuthorization | bool |  |
| `enableSoftDelete` | enableSoftDelete | string |  |
| `existingManagedIdentityCms` | existingManagedIdentityCms | string |  |
| `existingManagedIdentitywebsite` | managed identity for Website app | string |  |
| `existingPrivateDnsZoneDb` | existingPrivateDnsZoneDb | string |  |
| `existingPrivateDnsZoneKeyvault` | existingPrivateDnsZoneKeyvault | string |  |
| `existingVnet` | existingVnet | string |  |
| `frontDoorSku` | Update SKU for FrontDoor | string |  |
| `ftpsState` | ftpsState | string |  |
| `http20Enabled` | http20Enabled | bool |  |
| `httpLoggingEnabled` | httpLoggingEnabled | bool |  |
| `httpsOnly` | httpsOnly | bool |  |
| `kvPrivateEndpointsSubnetName` | kv PrivateEndpoints SubnetName | string |  |
| `kvSku` | kvSku | string |  |
| `kvSkuFamily` | kvSkuFamily | string |  |
| `location` | Location | string |  |
| `persistentResourceGroup` | persistentResourceGroup | string |  |
| `publicNetworkAccess` | publicNetworkAccess | string |  |
| `requestTracingEnabled` | requestTracingEnabled | bool |  |
| `resourcePrefix` | Resource prefix | string | uniqueString(resourceGroup().id) |
| `sqlDbSku` | sqlDbSku | string |  |
| `sqlDbTier` | sqlDbTier | string |  |
| `tenantId` | tenantId | string |  |
| `websiteContainerImage` | websiteContainerImage | string |  |

#### Deployment

To deploy the component module, follow these steps:

1. Clone the repository and navigate to the `component` directory.
2. Run the `bicep build` command to build the module.
3. Run the `az deployment group create` command to deploy the module to Azure.

For more information on deploying Bicep modules, see the [Bicep documentation](https://docs.microsoft.com/en-us/azure/azure-resource-manager/bicep/overview).

### UKSC Website Module

The `uksc-website.bicep` module is used to deploy the UK Supreme Court website to Azure.

## Parameters

| Parameter | Description | Type | Default |
| --- | --- | --- | --- |
| `acrUseManagedIdentityCreds` | acrUseManagedIdentityCreds | bool |  |
| `alwaysOn` | alwaysOn | bool |  |
| `appServicePlanId` | appServicePlanId | string |  |
| `cmsHostName` | cmsHostName | string |  |
| `detailedErrorLoggingEnabled` | detailedErrorLoggingEnabled | bool |  |
| `enabledForTemplateDeployment` | enabledForDeployment | string |  |
| `enablePurgeProtection` | enablePurgeProtection for KV | bool |  |
| `enableRbacAuthorization` | enableRbacAuthorization | bool |  |
| `enableSoftDelete` | enableSoftDelete | string |  |
| `existingManagedIdentitywebsite` |  | string |  |
| `existingVnet` |  | string |  |
| `frontDoorId` | frontDoorId | string |  |
| `ftpsState` | ftpsState | string |  |
| `http20Enabled` | http20Enabled | bool |  |
| `httpLoggingEnabled` | httpLoggingEnabled | bool |  |
| `httpsOnly` | httpsOnly | bool |  |
| `kvSku` | kvSku | string |  |
| `kvSkuFamily` | kvSkuFamily | string |  |
| `location` | location | string | `resourceGroup().location` |
| `persistentResourceGroup` | persistentResourceGroup | string |  |
| `publicNetworkAccess` | publicNetworkAccess | string |  |
| `requestTracingEnabled` | requestTracingEnabled | bool |  |
| `resourcePrefix` | resourcePrefix | string | uniqueString(resourceGroup().id) |
| `tenantId` | tenantId | string | `subscription().tenantId` |
| `websiteContainerImage` | websiteContainerImage | string |  |


#### Deployment

To deploy the UKSC website module, follow these steps:

1. Clone the repository and navigate to the `uksc-website` directory.
2. Run the `bicep build` command to build the module.
3. Run the `az deployment group create` command to deploy the module to Azure.

For more information on deploying Bicep modules, see the [Bicep documentation](https://docs.microsoft.com/en-us/azure/azure-resource-manager/bicep/overview).
