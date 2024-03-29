# IO.Swagger - the C# library for the Apprenda.DeveloperPortal.Web

No description provided (generated by Swagger Codegen https://github.com/swagger-api/swagger-codegen)

This C# SDK is automatically generated by the [Swagger Codegen](https://github.com/swagger-api/swagger-codegen) project:

- API version: v1
- SDK version: 1.0.0
- Build package: io.swagger.codegen.languages.CSharpClientCodegen

<a name="frameworks-supported"></a>
## Frameworks supported
- .NET 4.0 or later
- Windows Phone 7.1 (Mango)

<a name="dependencies"></a>
## Dependencies
- [RestSharp](https://www.nuget.org/packages/RestSharp) - 105.1.0 or later
- [Json.NET](https://www.nuget.org/packages/Newtonsoft.Json/) - 7.0.0 or later

The DLLs included in the package may not be the latest version. We recommend using [NuGet] (https://docs.nuget.org/consume/installing-nuget) to obtain the latest version of the packages:
```
Install-Package RestSharp
Install-Package Newtonsoft.Json
```

NOTE: RestSharp versions greater than 105.1.0 have a bug which causes file uploads to fail. See [RestSharp#742](https://github.com/restsharp/RestSharp/issues/742)

<a name="installation"></a>
## Installation
Run the following command to generate the DLL
- [Mac/Linux] `/bin/sh build.sh`
- [Windows] `build.bat`

Then include the DLL (under the `bin` folder) in the C# project, and use the namespaces:
```csharp
using IO.Swagger.Api;
using IO.Swagger.Client;
using IO.Swagger.Model;
```

<a name="packaging"></a>
## Packaging

A `.nuspec` is included with the project. You can follow the Nuget quickstart to [create](https://docs.microsoft.com/en-us/nuget/quickstart/create-and-publish-a-package#create-the-package) and [publish](https://docs.microsoft.com/en-us/nuget/quickstart/create-and-publish-a-package#publish-the-package) packages.

This `.nuspec` uses placeholders from the `.csproj`, so build the `.csproj` directly:

```
nuget pack -Build -OutputDirectory out IO.Swagger.csproj
```

Then, publish to a [local feed](https://docs.microsoft.com/en-us/nuget/hosting-packages/local-feeds) or [other host](https://docs.microsoft.com/en-us/nuget/hosting-packages/overview) and consume the new package via Nuget as usual.

<a name="getting-started"></a>
## Getting Started

```csharp
using System;
using System.Diagnostics;
using IO.Swagger.Api;
using IO.Swagger.Client;
using IO.Swagger.Model;

namespace Example
{
    public class Example
    {
        public void main()
        {
            
            var apiInstance = new AddOnsApi();
            var alias = alias_example;  // string | 
            var subAlias = subAlias_example;  // string | 

            try
            {
                apiInstance.AddOnsDelete(alias, subAlias);
            }
            catch (Exception e)
            {
                Debug.Print("Exception when calling AddOnsApi.AddOnsDelete: " + e.Message );
            }
        }
    }
}
```

<a name="documentation-for-api-endpoints"></a>
## Documentation for API Endpoints

All URIs are relative to *https://apps.apprenda.msterling/developer*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*AddOnsApi* | [**AddOnsDelete**](docs/AddOnsApi.md#addonsdelete) | **DELETE** /api/v1/AddOns | 
*AddOnsApi* | [**AddOnsDeleteByAlias**](docs/AddOnsApi.md#addonsdeletebyalias) | **DELETE** /api/v1/AddOns/{alias}/{subAlias} | 
*AddOnsApi* | [**AddOnsGet**](docs/AddOnsApi.md#addonsget) | **GET** /api/v1/AddOns | 
*AddOnsApi* | [**AddOnsGetByAlias**](docs/AddOnsApi.md#addonsgetbyalias) | **GET** /api/v1/AddOns/{id} | 
*AddOnsApi* | [**AddOnsGetBySubAlias**](docs/AddOnsApi.md#addonsgetbysubalias) | **GET** /api/v1/AddOns/{alias}/{subAlias} | 
*AddOnsApi* | [**AddOnsPost**](docs/AddOnsApi.md#addonspost) | **POST** /api/v1/AddOns/{id} | 
*AddOnsApi* | [**AddOnsPostToSubAlias**](docs/AddOnsApi.md#addonsposttosubalias) | **POST** /api/v1/AddOns/{alias}/{subAlias} | 
*AppsApi* | [**AppsDelete**](docs/AppsApi.md#appsdelete) | **DELETE** /api/v1/Apps/{id} | 
*AppsApi* | [**AppsDeleteBySubAlias**](docs/AppsApi.md#appsdeletebysubalias) | **DELETE** /api/v1/Apps/{alias}/{subAlias} | 
*AppsApi* | [**AppsGet**](docs/AppsApi.md#appsget) | **GET** /api/v1/Apps/{id} | 
*AppsApi* | [**AppsGetBySubAlias**](docs/AppsApi.md#appsgetbysubalias) | **GET** /api/v1/Apps/{alias}/{subAlias} | 
*AppsApi* | [**AppsPost**](docs/AppsApi.md#appspost) | **POST** /api/v1/Apps/{alias}/{subAlias} | 
*AppsApi* | [**AppsPut**](docs/AppsApi.md#appsput) | **PUT** /api/v1/Apps/{id} | 
*AppsApi* | [**AppsPutBySubAlias**](docs/AppsApi.md#appsputbysubalias) | **PUT** /api/v1/Apps/{alias}/{subAlias} | 
*CacheNodesApi* | [**CacheNodesGet**](docs/CacheNodesApi.md#cachenodesget) | **GET** /api/v1/CacheNodes/{id} | 
*CacheNodesApi* | [**CacheNodesGetBySubAlias**](docs/CacheNodesApi.md#cachenodesgetbysubalias) | **GET** /api/v1/CacheNodes/{alias}/{subAlias} | 
*CloudsApi* | [**CloudsGet**](docs/CloudsApi.md#cloudsget) | **GET** /api/v1/Clouds | 
*CloudsApi* | [**CloudsGetById**](docs/CloudsApi.md#cloudsgetbyid) | **GET** /api/v1/Clouds/{id} | 
*CloudsApi* | [**CloudsGetBySubAlias**](docs/CloudsApi.md#cloudsgetbysubalias) | **GET** /api/v1/Clouds/{alias}/{subAlias} | 
*ComponentsApi* | [**ComponentsDeleteCertificate**](docs/ComponentsApi.md#componentsdeletecertificate) | **DELETE** /api/v1/components/{appAlias}/{versionAlias}/{componentAlias}/certificates/{fileName} | 
*ComponentsApi* | [**ComponentsGet**](docs/ComponentsApi.md#componentsget) | **GET** /api/v1/Components | 
*ComponentsApi* | [**ComponentsGetByIDentifier**](docs/ComponentsApi.md#componentsgetbyidentifier) | **GET** /api/v1/Components/{alias}/{subAlias}/{identifier} | 
*ComponentsApi* | [**ComponentsGetBySubAlias**](docs/ComponentsApi.md#componentsgetbysubalias) | **GET** /api/v1/Components/{alias}/{subAlias} | 
*ComponentsApi* | [**ComponentsGetCertificate**](docs/ComponentsApi.md#componentsgetcertificate) | **GET** /api/v1/components/{appAlias}/{versionAlias}/{componentAlias}/certificates/{fileName} | 
*ComponentsApi* | [**ComponentsGetFiles**](docs/ComponentsApi.md#componentsgetfiles) | **GET** /api/v1/components/{appAlias}/{versionAlias}/{componentAlias}/files | 
*ComponentsApi* | [**ComponentsGetScaleByAlias**](docs/ComponentsApi.md#componentsgetscalebyalias) | **GET** /api/v1/Components/{appAlias}/{versionAlias}/{componentAlias}/scale/{count} | 
*ComponentsApi* | [**ComponentsPost**](docs/ComponentsApi.md#componentspost) | **POST** /api/v1/Components | 
*ComponentsApi* | [**ComponentsPostActionByIdentifier**](docs/ComponentsApi.md#componentspostactionbyidentifier) | **POST** /api/v1/Components/{alias}/{subAlias}/{identifier} | 
*ComponentsApi* | [**ComponentsPostCertificate**](docs/ComponentsApi.md#componentspostcertificate) | **POST** /api/v1/components/{appAlias}/{versionAlias}/{componentAlias}/certificates | 
*ComponentsApi* | [**ComponentsPostScaleByIdentifier**](docs/ComponentsApi.md#componentspostscalebyidentifier) | **POST** /api/v1/Components/{appAlias}/{versionAlias}/{componentAlias}/scale/{count} | 
*ComponentsApi* | [**ComponentsPut**](docs/ComponentsApi.md#componentsput) | **PUT** /api/v1/Components | 
*ComponentsApi* | [**ComponentsPutByAlias**](docs/ComponentsApi.md#componentsputbyalias) | **PUT** /api/v1/Components/{alias}/{subAlias}/{identifier} | 
*ComponentsApi* | [**ComponentsPutCountByIdentifier**](docs/ComponentsApi.md#componentsputcountbyidentifier) | **PUT** /api/v1/Components/{appAlias}/{versionAlias}/{componentAlias}/scale/{count} | 
*ContextApi* | [**ContextGet**](docs/ContextApi.md#contextget) | **GET** /api/v1/Context | 
*ContextApi* | [**ContextGetBySubAlias**](docs/ContextApi.md#contextgetbysubalias) | **GET** /api/v1/Context/{alias}/{subAlias} | 
*CustomPropertiesApi* | [**CustomPropertiesDelete**](docs/CustomPropertiesApi.md#custompropertiesdelete) | **DELETE** /api/v1/CustomProperties | 
*CustomPropertiesApi* | [**CustomPropertiesDeleteByIdentifier**](docs/CustomPropertiesApi.md#custompropertiesdeletebyidentifier) | **DELETE** /api/v1/CustomProperties/{alias}/{subAlias}/{identifier} | 
*CustomPropertiesApi* | [**CustomPropertiesDeleteBySubAlias**](docs/CustomPropertiesApi.md#custompropertiesdeletebysubalias) | **DELETE** /api/v1/CustomProperties/{alias}/{subAlias} | 
*CustomPropertiesApi* | [**CustomPropertiesGet**](docs/CustomPropertiesApi.md#custompropertiesget) | **GET** /api/v1/CustomProperties | 
*CustomPropertiesApi* | [**CustomPropertiesGetByIdentifier**](docs/CustomPropertiesApi.md#custompropertiesgetbyidentifier) | **GET** /api/v1/CustomProperties/{alias}/{subAlias}/{identifier} | 
*CustomPropertiesApi* | [**CustomPropertiesGetBySubAlias**](docs/CustomPropertiesApi.md#custompropertiesgetbysubalias) | **GET** /api/v1/CustomProperties/{alias}/{subAlias} | 
*CustomPropertiesApi* | [**CustomPropertiesGetModel**](docs/CustomPropertiesApi.md#custompropertiesgetmodel) | **GET** /api/v1/custompropertymodels/{modelName} | 
*CustomPropertiesApi* | [**CustomPropertiesPut**](docs/CustomPropertiesApi.md#custompropertiesput) | **PUT** /api/v1/CustomProperties | 
*CustomPropertiesApi* | [**CustomPropertiesPutByIdentifier**](docs/CustomPropertiesApi.md#custompropertiesputbyidentifier) | **PUT** /api/v1/CustomProperties/{alias}/{subAlias}/{identifier} | 
*CustomPropertiesApi* | [**CustomPropertiesPutBySubAlias**](docs/CustomPropertiesApi.md#custompropertiesputbysubalias) | **PUT** /api/v1/CustomProperties/{alias}/{subAlias} | 
*CustomUrlCertificateApi* | [**CustomUrlCertificateDelete**](docs/CustomUrlCertificateApi.md#customurlcertificatedelete) | **DELETE** /api/v1/apps/{appAlias}/customUrlCertificate | 
*CustomUrlCertificateApi* | [**CustomUrlCertificateGet**](docs/CustomUrlCertificateApi.md#customurlcertificateget) | **GET** /api/v1/apps/{appAlias}/customUrlCertificate | 
*CustomUrlCertificateApi* | [**CustomUrlCertificatePost**](docs/CustomUrlCertificateApi.md#customurlcertificatepost) | **POST** /api/v1/apps/{appAlias}/customUrlCertificate | 
*CustomUrlCertificateApi* | [**CustomUrlCertificatePut**](docs/CustomUrlCertificateApi.md#customurlcertificateput) | **PUT** /api/v1/apps/{appAlias}/customUrlCertificate | 
*JavaContainerApi* | [**JavaContainerGet**](docs/JavaContainerApi.md#javacontainerget) | **GET** /api/v1/JavaContainer | 
*JavaContainerApi* | [**JavaContainerGetBySubAlias**](docs/JavaContainerApi.md#javacontainergetbysubalias) | **GET** /api/v1/JavaContainer/{alias}/{subAlias} | 
*JavaRuntimeApi* | [**JavaRuntimeGet**](docs/JavaRuntimeApi.md#javaruntimeget) | **GET** /api/v1/JavaRuntime | 
*JavaRuntimeApi* | [**JavaRuntimeGetBySubAlias**](docs/JavaRuntimeApi.md#javaruntimegetbysubalias) | **GET** /api/v1/JavaRuntime/{alias}/{subAlias} | 
*LogOverridesApi* | [**LogOverridesDelete**](docs/LogOverridesApi.md#logoverridesdelete) | **DELETE** /api/v1/LogOverrides/{id} | 
*LogOverridesApi* | [**LogOverridesDeleteById**](docs/LogOverridesApi.md#logoverridesdeletebyid) | **DELETE** /api/v1/LogOverrides/{alias}/{subAlias} | 
*LogOverridesApi* | [**LogOverridesGet**](docs/LogOverridesApi.md#logoverridesget) | **GET** /api/v1/LogOverrides | 
*LogOverridesApi* | [**LogOverridesGetById**](docs/LogOverridesApi.md#logoverridesgetbyid) | **GET** /api/v1/LogOverrides/{id} | 
*LogOverridesApi* | [**LogOverridesGetBySubAlias**](docs/LogOverridesApi.md#logoverridesgetbysubalias) | **GET** /api/v1/LogOverrides/{alias}/{subAlias} | 
*LogOverridesApi* | [**LogOverridesPost**](docs/LogOverridesApi.md#logoverridespost) | **POST** /api/v1/LogOverrides | 
*LogOverridesApi* | [**LogOverridesPostBySubAlias**](docs/LogOverridesApi.md#logoverridespostbysubalias) | **POST** /api/v1/LogOverrides/{alias}/{subAlias} | 
*LogSummaryApi* | [**LogSummaryGet**](docs/LogSummaryApi.md#logsummaryget) | **GET** /api/v1/LogSummary | 
*LogSummaryApi* | [**LogSummaryGetById**](docs/LogSummaryApi.md#logsummarygetbyid) | **GET** /api/v1/LogSummary/{id} | 
*LogSummaryApi* | [**LogSummaryGetBySubAlias**](docs/LogSummaryApi.md#logsummarygetbysubalias) | **GET** /api/v1/LogSummary/{alias}/{subAlias} | 
*MonitoringSubscriptionsApi* | [**MonitoringSubscriptionsDelete**](docs/MonitoringSubscriptionsApi.md#monitoringsubscriptionsdelete) | **DELETE** /api/v1/monitoringsubscriptions/{appAlias}/{versionAlias}/{componentAlias}/{locator} | 
*MonitoringSubscriptionsApi* | [**MonitoringSubscriptionsGet**](docs/MonitoringSubscriptionsApi.md#monitoringsubscriptionsget) | **GET** /api/v1/monitoringsubscriptions/{appAlias}/{versionAlias} | 
*MonitoringSubscriptionsApi* | [**MonitoringSubscriptionsGetByComponent**](docs/MonitoringSubscriptionsApi.md#monitoringsubscriptionsgetbycomponent) | **GET** /api/v1/monitoringsubscriptions/{appAlias}/{versionAlias}/{componentAlias} | 
*MonitoringSubscriptionsApi* | [**MonitoringSubscriptionsGetByLocator**](docs/MonitoringSubscriptionsApi.md#monitoringsubscriptionsgetbylocator) | **GET** /api/v1/monitoringsubscriptions/{appAlias}/{versionAlias}/{componentAlias}/{locator} | 
*MonitoringSubscriptionsApi* | [**MonitoringSubscriptionsPost**](docs/MonitoringSubscriptionsApi.md#monitoringsubscriptionspost) | **POST** /api/v1/monitoringsubscriptions/{appAlias}/{versionAlias}/{componentAlias} | 
*MonitoringSubscriptionsApi* | [**MonitoringSubscriptionsPut**](docs/MonitoringSubscriptionsApi.md#monitoringsubscriptionsput) | **PUT** /api/v1/monitoringsubscriptions/{appAlias}/{versionAlias}/{componentAlias}/{locator} | 
*PlatformApi* | [**PlatformGetUpgradingStatus**](docs/PlatformApi.md#platformgetupgradingstatus) | **GET** /api/v1/platform/upgradeStatus | 
*PoliciesApi* | [**PoliciesGet**](docs/PoliciesApi.md#policiesget) | **GET** /api/v1/Policies | 
*PoliciesApi* | [**PoliciesGetById**](docs/PoliciesApi.md#policiesgetbyid) | **GET** /api/v1/Policies/{id} | 
*PoliciesApi* | [**PoliciesGetBySubAlias**](docs/PoliciesApi.md#policiesgetbysubalias) | **GET** /api/v1/Policies/{alias}/{subAlias} | 
*QuotasApi* | [**QuotasGet**](docs/QuotasApi.md#quotasget) | **GET** /api/v1/Quotas | 
*QuotasApi* | [**QuotasGetById**](docs/QuotasApi.md#quotasgetbyid) | **GET** /api/v1/Quotas/{id} | 
*QuotasApi* | [**QuotasGetBySubAlias**](docs/QuotasApi.md#quotasgetbysubalias) | **GET** /api/v1/Quotas/{alias}/{subAlias} | 
*RegistryApi* | [**RegistryGet**](docs/RegistryApi.md#registryget) | **GET** /api/v1/Registry | 
*RegistryApi* | [**RegistryGetByAlias**](docs/RegistryApi.md#registrygetbyalias) | **GET** /api/v1/Registry/{alias}/{subAlias} | 
*RegistryApi* | [**RegistryGetById**](docs/RegistryApi.md#registrygetbyid) | **GET** /api/v1/Registry/{id} | 
*SecurablesApi* | [**SecurablesGet**](docs/SecurablesApi.md#securablesget) | **GET** /api/v1/Securables | 
*SecurablesApi* | [**SecurablesGetById**](docs/SecurablesApi.md#securablesgetbyid) | **GET** /api/v1/Securables/{id} | 
*SecurablesApi* | [**SecurablesGetBySubAlias**](docs/SecurablesApi.md#securablesgetbysubalias) | **GET** /api/v1/Securables/{alias}/{subAlias} | 
*TenantsApi* | [**TenantsGet**](docs/TenantsApi.md#tenantsget) | **GET** /api/v1/Tenants | 
*TenantsApi* | [**TenantsGetByIdentifier**](docs/TenantsApi.md#tenantsgetbyidentifier) | **GET** /api/v1/Tenants/{alias}/{subAlias}/{identifier} | 
*TenantsApi* | [**TenantsGetBySubAlias**](docs/TenantsApi.md#tenantsgetbysubalias) | **GET** /api/v1/Tenants/{alias}/{subAlias} | 
*UtilizationApi* | [**UtilizationGet**](docs/UtilizationApi.md#utilizationget) | **GET** /api/v1/Utilization/{id} | 
*UtilizationApi* | [**UtilizationGetSubAlias**](docs/UtilizationApi.md#utilizationgetsubalias) | **GET** /api/v1/Utilization/{alias}/{subAlias} | 
*VersionReportCardsApi* | [**VersionReportCardsGet**](docs/VersionReportCardsApi.md#versionreportcardsget) | **GET** /api/v1/versions/{appAlias}/{versionAlias}/reportCards | 
*VersionReportCardsApi* | [**VersionReportCardsGetLatest**](docs/VersionReportCardsApi.md#versionreportcardsgetlatest) | **GET** /api/v1/versions/{appAlias}/{versionAlias}/reportCards/latest | 
*VersionsApi* | [**VersionsDelete**](docs/VersionsApi.md#versionsdelete) | **DELETE** /api/v1/Versions | 
*VersionsApi* | [**VersionsDeleteByAlias**](docs/VersionsApi.md#versionsdeletebyalias) | **DELETE** /api/v1/Versions/{alias}/{subAlias} | 
*VersionsApi* | [**VersionsGet**](docs/VersionsApi.md#versionsget) | **GET** /api/v1/Versions/{id} | 
*VersionsApi* | [**VersionsGetAll**](docs/VersionsApi.md#versionsgetall) | **GET** /api/v1/Versions | 
*VersionsApi* | [**VersionsGetByAlias**](docs/VersionsApi.md#versionsgetbyalias) | **GET** /api/v1/Versions/{alias}/{subAlias} | 
*VersionsApi* | [**VersionsGetByIdentifier**](docs/VersionsApi.md#versionsgetbyidentifier) | **GET** /api/v1/Versions/{alias}/{subAlias}/{identifier} | 
*VersionsApi* | [**VersionsPost**](docs/VersionsApi.md#versionspost) | **POST** /api/v1/Versions/{id} | 
*VersionsApi* | [**VersionsPostById**](docs/VersionsApi.md#versionspostbyid) | **POST** /api/v1/Versions/{alias}/{subAlias} | 
*VersionsApi* | [**VersionsPostBySubAlias**](docs/VersionsApi.md#versionspostbysubalias) | **POST** /api/v1/Versions | 
*VersionsApi* | [**VersionsPut**](docs/VersionsApi.md#versionsput) | **PUT** /api/v1/Versions | 
*VersionsApi* | [**VersionsPutIntoAlias**](docs/VersionsApi.md#versionsputintoalias) | **PUT** /api/v1/Versions/{alias}/{subAlias} | 
*WorkloadsApi* | [**WorkloadsGet**](docs/WorkloadsApi.md#workloadsget) | **GET** /api/v1/Workloads | 
*WorkloadsApi* | [**WorkloadsGetById**](docs/WorkloadsApi.md#workloadsgetbyid) | **GET** /api/v1/Workloads/{id} | 
*WorkloadsApi* | [**WorkloadsGetByIdentifier**](docs/WorkloadsApi.md#workloadsgetbyidentifier) | **GET** /api/v1/Workloads/{alias}/{subAlias}/{identifier} | 
*WorkloadsApi* | [**WorkloadsGetBySubAlias**](docs/WorkloadsApi.md#workloadsgetbysubalias) | **GET** /api/v1/Workloads/{alias}/{subAlias} | 
*WorkloadsApi* | [**WorkloadsPost**](docs/WorkloadsApi.md#workloadspost) | **POST** /api/v1/Workloads/{alias}/{subAlias} | 
*WorkloadsApi* | [**WorkloadsPostById**](docs/WorkloadsApi.md#workloadspostbyid) | **POST** /api/v1/Workloads/{id} | 


<a name="documentation-for-models"></a>
## Documentation for Models

 - [Model.AddOn](docs/AddOn.md)
 - [Model.AddOnContainer](docs/AddOnContainer.md)
 - [Model.AddOnInstancesContainer](docs/AddOnInstancesContainer.md)
 - [Model.AddOnParameter](docs/AddOnParameter.md)
 - [Model.AddOnParameterDefinition](docs/AddOnParameterDefinition.md)
 - [Model.AggregateApplicationAllocationDTO](docs/AggregateApplicationAllocationDTO.md)
 - [Model.AggregateLogData](docs/AggregateLogData.md)
 - [Model.Application](docs/Application.md)
 - [Model.ByteArrayContent](docs/ByteArrayContent.md)
 - [Model.CacheNode](docs/CacheNode.md)
 - [Model.Certificate](docs/Certificate.md)
 - [Model.Cloud](docs/Cloud.md)
 - [Model.CloudReference](docs/CloudReference.md)
 - [Model.Component](docs/Component.md)
 - [Model.ComponentInstanceHolder](docs/ComponentInstanceHolder.md)
 - [Model.ComponentReference](docs/ComponentReference.md)
 - [Model.ComponentResource](docs/ComponentResource.md)
 - [Model.Context](docs/Context.md)
 - [Model.CustomProperty](docs/CustomProperty.md)
 - [Model.CustomPropertyModel](docs/CustomPropertyModel.md)
 - [Model.CustomUrlCertificate](docs/CustomUrlCertificate.md)
 - [Model.DebugConnection](docs/DebugConnection.md)
 - [Model.DeployedAddOn](docs/DeployedAddOn.md)
 - [Model.DeployedAddOnReference](docs/DeployedAddOnReference.md)
 - [Model.EnhancedAddOn](docs/EnhancedAddOn.md)
 - [Model.EnrichedApplication](docs/EnrichedApplication.md)
 - [Model.EnrichedComponent](docs/EnrichedComponent.md)
 - [Model.EnrichedComponentModel](docs/EnrichedComponentModel.md)
 - [Model.EnrichedResourceAllocationPolicy](docs/EnrichedResourceAllocationPolicy.md)
 - [Model.EnrichedStorageQuota](docs/EnrichedStorageQuota.md)
 - [Model.EnrichedVersion](docs/EnrichedVersion.md)
 - [Model.JMXConnection](docs/JMXConnection.md)
 - [Model.JavaContainerDTO](docs/JavaContainerDTO.md)
 - [Model.JavaRuntimeReturn](docs/JavaRuntimeReturn.md)
 - [Model.KeyValuePairStringIEnumerableString](docs/KeyValuePairStringIEnumerableString.md)
 - [Model.LogOverride](docs/LogOverride.md)
 - [Model.LogOverrideDTO](docs/LogOverrideDTO.md)
 - [Model.LogOverrideEmailRecipientDTO](docs/LogOverrideEmailRecipientDTO.md)
 - [Model.LogOverrideRepeatAggregationSettings](docs/LogOverrideRepeatAggregationSettings.md)
 - [Model.LogOverrideSubscriber](docs/LogOverrideSubscriber.md)
 - [Model.LogOverrideUser](docs/LogOverrideUser.md)
 - [Model.MinimalCustomUrlCertificate](docs/MinimalCustomUrlCertificate.md)
 - [Model.MonitoringConnectionDetailsDTO](docs/MonitoringConnectionDetailsDTO.md)
 - [Model.MonitoringSubscription](docs/MonitoringSubscription.md)
 - [Model.NameValuePair](docs/NameValuePair.md)
 - [Model.OverrideTenantInfoDTO](docs/OverrideTenantInfoDTO.md)
 - [Model.OverrideUserInfoDTO](docs/OverrideUserInfoDTO.md)
 - [Model.PagedResourceBaseSubscribedTenant](docs/PagedResourceBaseSubscribedTenant.md)
 - [Model.PagedResourceBaseSubscribedUser](docs/PagedResourceBaseSubscribedUser.md)
 - [Model.PlatformLogOverrideDTO](docs/PlatformLogOverrideDTO.md)
 - [Model.ProvisionAddOnOptions](docs/ProvisionAddOnOptions.md)
 - [Model.RegistrySettingBase](docs/RegistrySettingBase.md)
 - [Model.ReportCard](docs/ReportCard.md)
 - [Model.ReportCardMessage](docs/ReportCardMessage.md)
 - [Model.ReportCardSection](docs/ReportCardSection.md)
 - [Model.ResourceAllocationPolicy](docs/ResourceAllocationPolicy.md)
 - [Model.ResourceAllocationPolicyReference](docs/ResourceAllocationPolicyReference.md)
 - [Model.ResourceBase](docs/ResourceBase.md)
 - [Model.ScheduledScalingEvent](docs/ScheduledScalingEvent.md)
 - [Model.SecurableAccess](docs/SecurableAccess.md)
 - [Model.StorageQuota](docs/StorageQuota.md)
 - [Model.StorageQuotaReference](docs/StorageQuotaReference.md)
 - [Model.SubscribedTenant](docs/SubscribedTenant.md)
 - [Model.SubscribedUser](docs/SubscribedUser.md)
 - [Model.UpgradeStatus](docs/UpgradeStatus.md)
 - [Model.UtilizationAggregate](docs/UtilizationAggregate.md)
 - [Model.Version](docs/Version.md)
 - [Model.Workload](docs/Workload.md)


<a name="documentation-for-authorization"></a>
## Documentation for Authorization

All endpoints do not require authorization.
