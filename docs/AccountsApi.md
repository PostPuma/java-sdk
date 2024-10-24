# AccountsApi

All URIs are relative to *https://app.postpuma.com/app/5afgg2-1egj4n-7612ng-g313ie*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**getAccount**](AccountsApi.md#getAccount) | **GET** /accounts/{accountUuid} | Get account |
| [**listAccounts**](AccountsApi.md#listAccounts) | **GET** /accounts | List accounts |


<a id="getAccount"></a>
# **getAccount**
> Account getAccount(accountUuid)

Get account

Get account

### Example
```java
// Import classes:
import PostPuma.ApiClient;
import PostPuma.ApiException;
import PostPuma.Configuration;
import PostPuma.auth.*;
import PostPuma.models.*;
import PostPuma.AccountsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://app.postpuma.com/app/5afgg2-1egj4n-7612ng-g313ie");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    AccountsApi apiInstance = new AccountsApi(defaultClient);
    String accountUuid = "accountUuid_example"; // String | Account UUID
    try {
      Account result = apiInstance.getAccount(accountUuid);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling AccountsApi#getAccount");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **accountUuid** | **String**| Account UUID | |

### Return type

[**Account**](Account.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful operation |  -  |
| **401** | Unauthenticated. |  -  |
| **403** | Access forbidden. |  -  |
| **404** | Workspace not found. |  -  |

<a id="listAccounts"></a>
# **listAccounts**
> ListAccounts200Response listAccounts()

List accounts

List accounts

### Example
```java
// Import classes:
import PostPuma.ApiClient;
import PostPuma.ApiException;
import PostPuma.Configuration;
import PostPuma.auth.*;
import PostPuma.models.*;
import PostPuma.AccountsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://app.postpuma.com/app/5afgg2-1egj4n-7612ng-g313ie");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    AccountsApi apiInstance = new AccountsApi(defaultClient);
    try {
      ListAccounts200Response result = apiInstance.listAccounts();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling AccountsApi#listAccounts");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**ListAccounts200Response**](ListAccounts200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful operation |  -  |
| **401** | Unauthenticated. |  -  |
| **403** | Access forbidden. |  -  |
| **404** | Workspace not found. |  -  |

