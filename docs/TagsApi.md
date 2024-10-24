# TagsApi

All URIs are relative to *https://app.postpuma.com/app/5afgg2-1egj4n-7612ng-g313ie*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**createTag**](TagsApi.md#createTag) | **POST** /tags | Create tag |
| [**deleteTag**](TagsApi.md#deleteTag) | **DELETE** /tags/{tagUuid} | Delete tag |
| [**getTag**](TagsApi.md#getTag) | **GET** /tags/{tagUuid} | Get tag |
| [**listTags**](TagsApi.md#listTags) | **GET** /tags | List tags |
| [**updateTag**](TagsApi.md#updateTag) | **PUT** /tags/{tagUuid} | Update tag |


<a id="createTag"></a>
# **createTag**
> Tag createTag(createTagRequest)

Create tag

Create tag

### Example
```java
// Import classes:
import PostPuma.ApiClient;
import PostPuma.ApiException;
import PostPuma.Configuration;
import PostPuma.auth.*;
import PostPuma.models.*;
import PostPuma.TagsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://app.postpuma.com/app/5afgg2-1egj4n-7612ng-g313ie");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    TagsApi apiInstance = new TagsApi(defaultClient);
    CreateTagRequest createTagRequest = new CreateTagRequest(); // CreateTagRequest | 
    try {
      Tag result = apiInstance.createTag(createTagRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling TagsApi#createTag");
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
| **createTagRequest** | [**CreateTagRequest**](CreateTagRequest.md)|  | [optional] |

### Return type

[**Tag**](Tag.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful operation |  -  |
| **401** | Unauthenticated. |  -  |
| **403** | Access forbidden. |  -  |
| **404** | Workspace not found. |  -  |
| **422** | Validation errors. |  -  |

<a id="deleteTag"></a>
# **deleteTag**
> DeleteMediaFiles200Response deleteTag(tagUuid)

Delete tag

Delete tag

### Example
```java
// Import classes:
import PostPuma.ApiClient;
import PostPuma.ApiException;
import PostPuma.Configuration;
import PostPuma.auth.*;
import PostPuma.models.*;
import PostPuma.TagsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://app.postpuma.com/app/5afgg2-1egj4n-7612ng-g313ie");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    TagsApi apiInstance = new TagsApi(defaultClient);
    String tagUuid = "tagUuid_example"; // String | Tag UUID
    try {
      DeleteMediaFiles200Response result = apiInstance.deleteTag(tagUuid);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling TagsApi#deleteTag");
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
| **tagUuid** | **String**| Tag UUID | |

### Return type

[**DeleteMediaFiles200Response**](DeleteMediaFiles200Response.md)

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

<a id="getTag"></a>
# **getTag**
> Tag getTag(tagUuid)

Get tag

Get tag

### Example
```java
// Import classes:
import PostPuma.ApiClient;
import PostPuma.ApiException;
import PostPuma.Configuration;
import PostPuma.auth.*;
import PostPuma.models.*;
import PostPuma.TagsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://app.postpuma.com/app/5afgg2-1egj4n-7612ng-g313ie");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    TagsApi apiInstance = new TagsApi(defaultClient);
    String tagUuid = "tagUuid_example"; // String | Tag UUID
    try {
      Tag result = apiInstance.getTag(tagUuid);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling TagsApi#getTag");
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
| **tagUuid** | **String**| Tag UUID | |

### Return type

[**Tag**](Tag.md)

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

<a id="listTags"></a>
# **listTags**
> ListTags200Response listTags()

List tags

List tags

### Example
```java
// Import classes:
import PostPuma.ApiClient;
import PostPuma.ApiException;
import PostPuma.Configuration;
import PostPuma.auth.*;
import PostPuma.models.*;
import PostPuma.TagsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://app.postpuma.com/app/5afgg2-1egj4n-7612ng-g313ie");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    TagsApi apiInstance = new TagsApi(defaultClient);
    try {
      ListTags200Response result = apiInstance.listTags();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling TagsApi#listTags");
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

[**ListTags200Response**](ListTags200Response.md)

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

<a id="updateTag"></a>
# **updateTag**
> DeleteMediaFiles200Response updateTag(tagUuid, updateTagRequest)

Update tag

Update tag

### Example
```java
// Import classes:
import PostPuma.ApiClient;
import PostPuma.ApiException;
import PostPuma.Configuration;
import PostPuma.auth.*;
import PostPuma.models.*;
import PostPuma.TagsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://app.postpuma.com/app/5afgg2-1egj4n-7612ng-g313ie");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    TagsApi apiInstance = new TagsApi(defaultClient);
    String tagUuid = "tagUuid_example"; // String | Tag UUID
    UpdateTagRequest updateTagRequest = new UpdateTagRequest(); // UpdateTagRequest | 
    try {
      DeleteMediaFiles200Response result = apiInstance.updateTag(tagUuid, updateTagRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling TagsApi#updateTag");
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
| **tagUuid** | **String**| Tag UUID | |
| **updateTagRequest** | [**UpdateTagRequest**](UpdateTagRequest.md)|  | [optional] |

### Return type

[**DeleteMediaFiles200Response**](DeleteMediaFiles200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful operation |  -  |
| **401** | Unauthenticated. |  -  |
| **403** | Access forbidden. |  -  |
| **404** | Workspace not found. |  -  |
| **422** | Validation errors. |  -  |

