# IO.Swagger - the C# library for the Account Management REST API

The Account Management REST API can be used to manage user accounts, roles, and securables for applications on the Platform. The endpoints of this API allow you to perform the same the functionality of the Platform's Account Portal for your Tenant's applications.   For more information, see our documentation on the [Account Portal](/current/account).     ## Authentication    Before making a request, you must be authenticated. Follow these instuctions [to get authenticated](/restapi/accountmanagement/v1/authentication). ## Making a Request   ### Prerequisites    * Installed Platform of version 6.6.0 or later    * An active user account assigned to an active Tenant Account or Developer Team    * Authentication token   ### Request URL    All requests must use **https**.       The URL for every request you make is the URL of your Platform followed by \"/account\" and the path structure of the endpoint. For example, if your Platform URL is https://apps.apprenda.harp and you want to get a list of all user accounts for your Tenant, the request URL will be https://apps.apprenda.harp/account/api/v1/users.     For more information, see our documentation on [using api resources](/restapi/accountmanagement/v1/using-resources) and [finding your Cloud URI](/current/clouduri).    ### Request Headers  Your authenication token must be passed in the header of all requests using the key **ApprendaSessionToken** (not case sensitive).    

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
            
            var apiInstance = new ApplicationVersionsApi();
            var applicationVersionKey = applicationVersionKey_example;  // string | Required. Concatenation of application alias and version alias as 'AppAlias-VersionAlias'

            try
            {
                // Get a version of an application
                ApplicationVersion result = apiInstance.ApiV1ApplicationVersionsApplicationVersionKeyGet(applicationVersionKey);
                Debug.WriteLine(result);
            }
            catch (Exception e)
            {
                Debug.Print("Exception when calling ApplicationVersionsApi.ApiV1ApplicationVersionsApplicationVersionKeyGet: " + e.Message );
            }
        }
    }
}
```

<a name="documentation-for-api-endpoints"></a>
## Documentation for API Endpoints

All URIs are relative to *https://apps.apprenda.harp/account*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*ApplicationVersionsApi* | [**ApiV1ApplicationVersionsApplicationVersionKeyGet**](docs/ApplicationVersionsApi.md#apiv1applicationversionsapplicationversionkeyget) | **GET** /api/v1/applicationVersions/{applicationVersionKey} | Get a version of an application
*ApplicationVersionsApi* | [**ApiV1ApplicationVersionsGet**](docs/ApplicationVersionsApi.md#apiv1applicationversionsget) | **GET** /api/v1/applicationVersions | Get all applications
*PlansApi* | [**ApiV1ApplicationVersionsApplicationVersionKeyPlansGet**](docs/PlansApi.md#apiv1applicationversionsapplicationversionkeyplansget) | **GET** /api/v1/applicationVersions/{applicationVersionKey}/plans | Get all plans for an application version
*PlansApi* | [**ApiV1ApplicationVersionsApplicationVersionKeyPlansPlanIdGet**](docs/PlansApi.md#apiv1applicationversionsapplicationversionkeyplansplanidget) | **GET** /api/v1/applicationVersions/{applicationVersionKey}/plans/{planId} | Get a plan for an application version
*PlatformApi* | [**ApiV1PlatformUpgradestatusGet**](docs/PlatformApi.md#apiv1platformupgradestatusget) | **GET** /api/v1/platform/upgradestatus | Check if the Platform is upgrading
*RolesApi* | [**ApiV1ApplicationVersionsApplicationVersionKeySecurablesSecurableIdRolesDelete**](docs/RolesApi.md#apiv1applicationversionsapplicationversionkeysecurablessecurableidrolesdelete) | **DELETE** /api/v1/applicationVersions/{applicationVersionKey}/securables/{securableId}/roles | Remove role from a securable
*RolesApi* | [**ApiV1ApplicationVersionsApplicationVersionKeySecurablesSecurableIdRolesGet**](docs/RolesApi.md#apiv1applicationversionsapplicationversionkeysecurablessecurableidrolesget) | **GET** /api/v1/applicationVersions/{applicationVersionKey}/securables/{securableId}/roles | Get all roles using a securable
*RolesApi* | [**ApiV1ApplicationVersionsApplicationVersionKeySecurablesSecurableIdRolesPost**](docs/RolesApi.md#apiv1applicationversionsapplicationversionkeysecurablessecurableidrolespost) | **POST** /api/v1/applicationVersions/{applicationVersionKey}/securables/{securableId}/roles | Assign role(s) to a securable
*RolesApi* | [**ApiV1RolesGet**](docs/RolesApi.md#apiv1rolesget) | **GET** /api/v1/roles | Get all roles
*RolesApi* | [**ApiV1RolesPost**](docs/RolesApi.md#apiv1rolespost) | **POST** /api/v1/roles | Create role
*RolesApi* | [**ApiV1RolesRoleIdDelete**](docs/RolesApi.md#apiv1rolesroleiddelete) | **DELETE** /api/v1/roles/{roleId} | Remove role
*RolesApi* | [**ApiV1RolesRoleIdGet**](docs/RolesApi.md#apiv1rolesroleidget) | **GET** /api/v1/roles/{roleId} | Get role
*RolesApi* | [**ApiV1RolesRoleIdPut**](docs/RolesApi.md#apiv1rolesroleidput) | **PUT** /api/v1/roles/{roleId} | Update role
*RolesApi* | [**ApiV1RolesRoleIdRolesDelete**](docs/RolesApi.md#apiv1rolesroleidrolesdelete) | **DELETE** /api/v1/roles/{roleId}/roles | Remove a sub-role from a role
*RolesApi* | [**ApiV1RolesRoleIdRolesGet**](docs/RolesApi.md#apiv1rolesroleidrolesget) | **GET** /api/v1/roles/{roleId}/roles | Get all sub-roles assigned to a role
*RolesApi* | [**ApiV1RolesRoleIdRolesPost**](docs/RolesApi.md#apiv1rolesroleidrolespost) | **POST** /api/v1/roles/{roleId}/roles | Make role a sub-role of another role
*RolesApi* | [**ApiV1RolesRoleIdSecurablesGet**](docs/RolesApi.md#apiv1rolesroleidsecurablesget) | **GET** /api/v1/roles/{roleId}/securables | Get all securables for a role
*RolesApi* | [**ApiV1RolesRoleIdUsersDelete**](docs/RolesApi.md#apiv1rolesroleidusersdelete) | **DELETE** /api/v1/roles/{roleId}/users | Remove a user from role
*RolesApi* | [**ApiV1RolesRoleIdUsersGet**](docs/RolesApi.md#apiv1rolesroleidusersget) | **GET** /api/v1/roles/{roleId}/users | Get users of a role
*RolesApi* | [**ApiV1RolesRoleIdUsersPost**](docs/RolesApi.md#apiv1rolesroleiduserspost) | **POST** /api/v1/roles/{roleId}/users | Add users to a role
*RolesApi* | [**ApiV1UserRolesDelete**](docs/RolesApi.md#apiv1userrolesdelete) | **DELETE** /api/v1/userRoles | Remove a user from a role
*RolesApi* | [**ApiV1UserRolesGet**](docs/RolesApi.md#apiv1userrolesget) | **GET** /api/v1/userRoles | Get the roles of a user
*RolesApi* | [**ApiV1UserRolesPost**](docs/RolesApi.md#apiv1userrolespost) | **POST** /api/v1/userRoles | Assign a user to a role
*SecurablesApi* | [**ApiV1ApplicationVersionsApplicationVersionKeySecurablesGet**](docs/SecurablesApi.md#apiv1applicationversionsapplicationversionkeysecurablesget) | **GET** /api/v1/applicationVersions/{applicationVersionKey}/securables | Get all securables for an application version
*SecurablesApi* | [**ApiV1ApplicationVersionsApplicationVersionKeySecurablesSecurableIdGet**](docs/SecurablesApi.md#apiv1applicationversionsapplicationversionkeysecurablessecurableidget) | **GET** /api/v1/applicationVersions/{applicationVersionKey}/securables/{securableId} | Get a securable for an application version
*SecurablesApi* | [**ApiV1ApplicationVersionsApplicationVersionKeySecurablesSecurableIdRolesDelete**](docs/SecurablesApi.md#apiv1applicationversionsapplicationversionkeysecurablessecurableidrolesdelete) | **DELETE** /api/v1/applicationVersions/{applicationVersionKey}/securables/{securableId}/roles | Remove role from a securable
*SecurablesApi* | [**ApiV1ApplicationVersionsApplicationVersionKeySecurablesSecurableIdRolesGet**](docs/SecurablesApi.md#apiv1applicationversionsapplicationversionkeysecurablessecurableidrolesget) | **GET** /api/v1/applicationVersions/{applicationVersionKey}/securables/{securableId}/roles | Get all roles using a securable
*SecurablesApi* | [**ApiV1ApplicationVersionsApplicationVersionKeySecurablesSecurableIdRolesPost**](docs/SecurablesApi.md#apiv1applicationversionsapplicationversionkeysecurablessecurableidrolespost) | **POST** /api/v1/applicationVersions/{applicationVersionKey}/securables/{securableId}/roles | Assign role(s) to a securable
*SecurablesApi* | [**ApiV1RolesRoleIdSecurablesGet**](docs/SecurablesApi.md#apiv1rolesroleidsecurablesget) | **GET** /api/v1/roles/{roleId}/securables | Get all securables for a role
*SubscriptionsApi* | [**ApiV1ApplicationVersionsApplicationVersionKeySubscriptionsGet**](docs/SubscriptionsApi.md#apiv1applicationversionsapplicationversionkeysubscriptionsget) | **GET** /api/v1/applicationVersions/{applicationVersionKey}/subscriptions | Get all subscriptions of an application version
*SubscriptionsApi* | [**ApiV1ApplicationVersionsApplicationVersionKeySubscriptionsLocatorAssignedtoDelete**](docs/SubscriptionsApi.md#apiv1applicationversionsapplicationversionkeysubscriptionslocatorassignedtodelete) | **DELETE** /api/v1/applicationVersions/{applicationVersionKey}/subscriptions/{locator}/assignedto | Unsubscribe user from subscription
*SubscriptionsApi* | [**ApiV1ApplicationVersionsApplicationVersionKeySubscriptionsLocatorAssignedtoPost**](docs/SubscriptionsApi.md#apiv1applicationversionsapplicationversionkeysubscriptionslocatorassignedtopost) | **POST** /api/v1/applicationVersions/{applicationVersionKey}/subscriptions/{locator}/assignedto | Subscribe user
*SubscriptionsApi* | [**ApiV1ApplicationVersionsApplicationVersionKeySubscriptionsLocatorDelete**](docs/SubscriptionsApi.md#apiv1applicationversionsapplicationversionkeysubscriptionslocatordelete) | **DELETE** /api/v1/applicationVersions/{applicationVersionKey}/subscriptions/{locator} | Cancel a subscription
*SubscriptionsApi* | [**ApiV1ApplicationVersionsApplicationVersionKeySubscriptionsLocatorGet**](docs/SubscriptionsApi.md#apiv1applicationversionsapplicationversionkeysubscriptionslocatorget) | **GET** /api/v1/applicationVersions/{applicationVersionKey}/subscriptions/{locator} | Get a subscription for an application version
*SubscriptionsApi* | [**ApiV1ApplicationVersionsApplicationVersionKeySubscriptionsPost**](docs/SubscriptionsApi.md#apiv1applicationversionsapplicationversionkeysubscriptionspost) | **POST** /api/v1/applicationVersions/{applicationVersionKey}/subscriptions | Create a new subscription
*UpgradeStatusApi* | [**ApiV1PlatformUpgradestatusGet**](docs/UpgradeStatusApi.md#apiv1platformupgradestatusget) | **GET** /api/v1/platform/upgradestatus | Check if the Platform is upgrading
*UsersApi* | [**ApiV1ApplicationVersionsApplicationVersionKeySubscriptionsLocatorAssignedtoDelete**](docs/UsersApi.md#apiv1applicationversionsapplicationversionkeysubscriptionslocatorassignedtodelete) | **DELETE** /api/v1/applicationVersions/{applicationVersionKey}/subscriptions/{locator}/assignedto | Unsubscribe user from subscription
*UsersApi* | [**ApiV1ApplicationVersionsApplicationVersionKeySubscriptionsLocatorAssignedtoPost**](docs/UsersApi.md#apiv1applicationversionsapplicationversionkeysubscriptionslocatorassignedtopost) | **POST** /api/v1/applicationVersions/{applicationVersionKey}/subscriptions/{locator}/assignedto | Subscribe user
*UsersApi* | [**ApiV1RolesRoleIdUsersDelete**](docs/UsersApi.md#apiv1rolesroleidusersdelete) | **DELETE** /api/v1/roles/{roleId}/users | Remove a user from role
*UsersApi* | [**ApiV1RolesRoleIdUsersGet**](docs/UsersApi.md#apiv1rolesroleidusersget) | **GET** /api/v1/roles/{roleId}/users | Get users of a role
*UsersApi* | [**ApiV1RolesRoleIdUsersPost**](docs/UsersApi.md#apiv1rolesroleiduserspost) | **POST** /api/v1/roles/{roleId}/users | Add users to a role
*UsersApi* | [**ApiV1UserRolesDelete**](docs/UsersApi.md#apiv1userrolesdelete) | **DELETE** /api/v1/userRoles | Remove a user from a role
*UsersApi* | [**ApiV1UserRolesGet**](docs/UsersApi.md#apiv1userrolesget) | **GET** /api/v1/userRoles | Get the roles of a user
*UsersApi* | [**ApiV1UserRolesPost**](docs/UsersApi.md#apiv1userrolespost) | **POST** /api/v1/userRoles | Assign a user to a role
*UsersApi* | [**ApiV1UsersDelete**](docs/UsersApi.md#apiv1usersdelete) | **DELETE** /api/v1/users | Delete user
*UsersApi* | [**ApiV1UsersGet**](docs/UsersApi.md#apiv1usersget) | **GET** /api/v1/users | Get all users
*UsersApi* | [**ApiV1UsersPost**](docs/UsersApi.md#apiv1userspost) | **POST** /api/v1/users | Add a user
*UsersApi* | [**ApiV1UsersPut**](docs/UsersApi.md#apiv1usersput) | **PUT** /api/v1/users | Update a user


<a name="documentation-for-models"></a>
## Documentation for Models

 - [Model.ApplicationVersion](docs/ApplicationVersion.md)
 - [Model.PagedResourceBaseApplicationVersion](docs/PagedResourceBaseApplicationVersion.md)
 - [Model.PagedResourceBaseUser](docs/PagedResourceBaseUser.md)
 - [Model.Plan](docs/Plan.md)
 - [Model.PlanRequest](docs/PlanRequest.md)
 - [Model.ResourceBase](docs/ResourceBase.md)
 - [Model.Role](docs/Role.md)
 - [Model.Securable](docs/Securable.md)
 - [Model.Subscription](docs/Subscription.md)
 - [Model.SubscriptionRequest](docs/SubscriptionRequest.md)
 - [Model.UnpagedResourceBasePlan](docs/UnpagedResourceBasePlan.md)
 - [Model.UnpagedResourceBaseRole](docs/UnpagedResourceBaseRole.md)
 - [Model.UnpagedResourceBaseSecurable](docs/UnpagedResourceBaseSecurable.md)
 - [Model.UnpagedResourceBaseSubscription](docs/UnpagedResourceBaseSubscription.md)
 - [Model.UnpagedResourceBaseUser](docs/UnpagedResourceBaseUser.md)
 - [Model.UpgradeStatus](docs/UpgradeStatus.md)
 - [Model.User](docs/User.md)


<a name="documentation-for-authorization"></a>
## Documentation for Authorization

All endpoints do not require authorization.
