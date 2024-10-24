# MediaApi

All URIs are relative to *https://app.postpuma.com/app/5afgg2-1egj4n-7612ng-g313ie*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**deleteMediaFiles**](MediaApi.md#deleteMediaFiles) | **DELETE** /media | Delete media files |
| [**getMediaFile**](MediaApi.md#getMediaFile) | **GET** /media/{mediaUuid} | Get media file |
| [**listMediaFiles**](MediaApi.md#listMediaFiles) | **GET** /media | List media files |
| [**uploadMediaFile**](MediaApi.md#uploadMediaFile) | **POST** /media | Upload media file |


<a id="deleteMediaFiles"></a>
# **deleteMediaFiles**
> DeleteMediaFiles200Response deleteMediaFiles(deleteMediaFilesRequest)

Delete media files

Delete media files

### Example
```java
// Import classes:
import PostPuma.ApiClient;
import PostPuma.ApiException;
import PostPuma.Configuration;
import PostPuma.auth.*;
import PostPuma.models.*;
import PostPuma.MediaApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://app.postpuma.com/app/5afgg2-1egj4n-7612ng-g313ie");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    MediaApi apiInstance = new MediaApi(defaultClient);
    DeleteMediaFilesRequest deleteMediaFilesRequest = new DeleteMediaFilesRequest(); // DeleteMediaFilesRequest | 
    try {
      DeleteMediaFiles200Response result = apiInstance.deleteMediaFiles(deleteMediaFilesRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling MediaApi#deleteMediaFiles");
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
| **deleteMediaFilesRequest** | [**DeleteMediaFilesRequest**](DeleteMediaFilesRequest.md)|  | [optional] |

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
| **422** | Validation errors |  -  |

<a id="getMediaFile"></a>
# **getMediaFile**
> MediaFile getMediaFile(mediaUuid)

Get media file

Get media file

### Example
```java
// Import classes:
import PostPuma.ApiClient;
import PostPuma.ApiException;
import PostPuma.Configuration;
import PostPuma.auth.*;
import PostPuma.models.*;
import PostPuma.MediaApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://app.postpuma.com/app/5afgg2-1egj4n-7612ng-g313ie");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    MediaApi apiInstance = new MediaApi(defaultClient);
    String mediaUuid = "mediaUuid_example"; // String | Media UUID
    try {
      MediaFile result = apiInstance.getMediaFile(mediaUuid);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling MediaApi#getMediaFile");
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
| **mediaUuid** | **String**| Media UUID | |

### Return type

[**MediaFile**](MediaFile.md)

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

<a id="listMediaFiles"></a>
# **listMediaFiles**
> ListMediaFiles200Response listMediaFiles(page)

List media files

List media files

### Example
```java
// Import classes:
import PostPuma.ApiClient;
import PostPuma.ApiException;
import PostPuma.Configuration;
import PostPuma.auth.*;
import PostPuma.models.*;
import PostPuma.MediaApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://app.postpuma.com/app/5afgg2-1egj4n-7612ng-g313ie");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    MediaApi apiInstance = new MediaApi(defaultClient);
    Integer page = 56; // Integer | Page number
    try {
      ListMediaFiles200Response result = apiInstance.listMediaFiles(page);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling MediaApi#listMediaFiles");
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
| **page** | **Integer**| Page number | [optional] |

### Return type

[**ListMediaFiles200Response**](ListMediaFiles200Response.md)

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

<a id="uploadMediaFile"></a>
# **uploadMediaFile**
> MediaFile uploadMediaFile(_file)

Upload media file

Upload media file

### Example
```java
// Import classes:
import PostPuma.ApiClient;
import PostPuma.ApiException;
import PostPuma.Configuration;
import PostPuma.auth.*;
import PostPuma.models.*;
import PostPuma.MediaApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://app.postpuma.com/app/5afgg2-1egj4n-7612ng-g313ie");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    MediaApi apiInstance = new MediaApi(defaultClient);
    File _file = new File("/path/to/file"); // File | 
    try {
      MediaFile result = apiInstance.uploadMediaFile(_file);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling MediaApi#uploadMediaFile");
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
| **_file** | **File**|  | [optional] |

### Return type

[**MediaFile**](MediaFile.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful operation |  -  |
| **401** | Unauthenticated. |  -  |
| **403** | Access forbidden. |  -  |
| **404** | Workspace not found. |  -  |

