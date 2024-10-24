# PostsApi

All URIs are relative to *https://app.postpuma.com/app/5afgg2-1egj4n-7612ng-g313ie*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**createPost**](PostsApi.md#createPost) | **POST** /posts | Create post |
| [**deletePost**](PostsApi.md#deletePost) | **DELETE** /posts/{postUuid} | Delete post |
| [**deletePosts**](PostsApi.md#deletePosts) | **DELETE** /posts | Delete posts |
| [**getPost**](PostsApi.md#getPost) | **GET** /posts/{postUuid} | Get post |
| [**listPosts**](PostsApi.md#listPosts) | **GET** /posts | List posts |
| [**queuePost**](PostsApi.md#queuePost) | **POST** /posts/add-to-queue/{postUuid} | Queue post |
| [**schedulePost**](PostsApi.md#schedulePost) | **POST** /posts/schedule/{postUuid} | Schedule post |
| [**updatePost**](PostsApi.md#updatePost) | **PUT** /posts/{postUuid} | Update post |


<a id="createPost"></a>
# **createPost**
> Post createPost(createPostRequest)

Create post

Create post

### Example
```java
// Import classes:
import PostPuma.ApiClient;
import PostPuma.ApiException;
import PostPuma.Configuration;
import PostPuma.auth.*;
import PostPuma.models.*;
import PostPuma.PostsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://app.postpuma.com/app/5afgg2-1egj4n-7612ng-g313ie");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    PostsApi apiInstance = new PostsApi(defaultClient);
    CreatePostRequest createPostRequest = new CreatePostRequest(); // CreatePostRequest | 
    try {
      Post result = apiInstance.createPost(createPostRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling PostsApi#createPost");
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
| **createPostRequest** | [**CreatePostRequest**](CreatePostRequest.md)|  | [optional] |

### Return type

[**Post**](Post.md)

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

<a id="deletePost"></a>
# **deletePost**
> DeletePosts200Response deletePost(postUuid, deletePostRequest)

Delete post

Delete post

### Example
```java
// Import classes:
import PostPuma.ApiClient;
import PostPuma.ApiException;
import PostPuma.Configuration;
import PostPuma.auth.*;
import PostPuma.models.*;
import PostPuma.PostsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://app.postpuma.com/app/5afgg2-1egj4n-7612ng-g313ie");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    PostsApi apiInstance = new PostsApi(defaultClient);
    String postUuid = "postUuid_example"; // String | Post UUID
    DeletePostRequest deletePostRequest = new DeletePostRequest(); // DeletePostRequest | 
    try {
      DeletePosts200Response result = apiInstance.deletePost(postUuid, deletePostRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling PostsApi#deletePost");
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
| **postUuid** | **String**| Post UUID | |
| **deletePostRequest** | [**DeletePostRequest**](DeletePostRequest.md)|  | [optional] |

### Return type

[**DeletePosts200Response**](DeletePosts200Response.md)

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

<a id="deletePosts"></a>
# **deletePosts**
> DeletePosts200Response deletePosts(deletePostsRequest)

Delete posts

Delete posts

### Example
```java
// Import classes:
import PostPuma.ApiClient;
import PostPuma.ApiException;
import PostPuma.Configuration;
import PostPuma.auth.*;
import PostPuma.models.*;
import PostPuma.PostsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://app.postpuma.com/app/5afgg2-1egj4n-7612ng-g313ie");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    PostsApi apiInstance = new PostsApi(defaultClient);
    DeletePostsRequest deletePostsRequest = new DeletePostsRequest(); // DeletePostsRequest | 
    try {
      DeletePosts200Response result = apiInstance.deletePosts(deletePostsRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling PostsApi#deletePosts");
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
| **deletePostsRequest** | [**DeletePostsRequest**](DeletePostsRequest.md)|  | [optional] |

### Return type

[**DeletePosts200Response**](DeletePosts200Response.md)

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

<a id="getPost"></a>
# **getPost**
> Post getPost(postUuid)

Get post

Get post

### Example
```java
// Import classes:
import PostPuma.ApiClient;
import PostPuma.ApiException;
import PostPuma.Configuration;
import PostPuma.auth.*;
import PostPuma.models.*;
import PostPuma.PostsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://app.postpuma.com/app/5afgg2-1egj4n-7612ng-g313ie");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    PostsApi apiInstance = new PostsApi(defaultClient);
    String postUuid = "postUuid_example"; // String | Post UUID
    try {
      Post result = apiInstance.getPost(postUuid);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling PostsApi#getPost");
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
| **postUuid** | **String**| Post UUID | |

### Return type

[**Post**](Post.md)

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

<a id="listPosts"></a>
# **listPosts**
> ListPosts200Response listPosts(page)

List posts

List posts

### Example
```java
// Import classes:
import PostPuma.ApiClient;
import PostPuma.ApiException;
import PostPuma.Configuration;
import PostPuma.auth.*;
import PostPuma.models.*;
import PostPuma.PostsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://app.postpuma.com/app/5afgg2-1egj4n-7612ng-g313ie");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    PostsApi apiInstance = new PostsApi(defaultClient);
    Integer page = 56; // Integer | Page
    try {
      ListPosts200Response result = apiInstance.listPosts(page);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling PostsApi#listPosts");
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
| **page** | **Integer**| Page | [optional] |

### Return type

[**ListPosts200Response**](ListPosts200Response.md)

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

<a id="queuePost"></a>
# **queuePost**
> QueuePost200Response queuePost(postUuid)

Queue post

Queue post

### Example
```java
// Import classes:
import PostPuma.ApiClient;
import PostPuma.ApiException;
import PostPuma.Configuration;
import PostPuma.auth.*;
import PostPuma.models.*;
import PostPuma.PostsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://app.postpuma.com/app/5afgg2-1egj4n-7612ng-g313ie");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    PostsApi apiInstance = new PostsApi(defaultClient);
    String postUuid = "postUuid_example"; // String | Post UUID
    try {
      QueuePost200Response result = apiInstance.queuePost(postUuid);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling PostsApi#queuePost");
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
| **postUuid** | **String**| Post UUID | |

### Return type

[**QueuePost200Response**](QueuePost200Response.md)

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
| **422** | Validation errors |  -  |

<a id="schedulePost"></a>
# **schedulePost**
> QueuePost200Response schedulePost(postUuid, schedulePostRequest)

Schedule post

Schedule post

### Example
```java
// Import classes:
import PostPuma.ApiClient;
import PostPuma.ApiException;
import PostPuma.Configuration;
import PostPuma.auth.*;
import PostPuma.models.*;
import PostPuma.PostsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://app.postpuma.com/app/5afgg2-1egj4n-7612ng-g313ie");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    PostsApi apiInstance = new PostsApi(defaultClient);
    String postUuid = "postUuid_example"; // String | Post UUID
    SchedulePostRequest schedulePostRequest = new SchedulePostRequest(); // SchedulePostRequest | 
    try {
      QueuePost200Response result = apiInstance.schedulePost(postUuid, schedulePostRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling PostsApi#schedulePost");
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
| **postUuid** | **String**| Post UUID | |
| **schedulePostRequest** | [**SchedulePostRequest**](SchedulePostRequest.md)|  | [optional] |

### Return type

[**QueuePost200Response**](QueuePost200Response.md)

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

<a id="updatePost"></a>
# **updatePost**
> DeleteMediaFiles200Response updatePost(postUuid, updatePostRequest)

Update post

Update post

### Example
```java
// Import classes:
import PostPuma.ApiClient;
import PostPuma.ApiException;
import PostPuma.Configuration;
import PostPuma.auth.*;
import PostPuma.models.*;
import PostPuma.PostsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://app.postpuma.com/app/5afgg2-1egj4n-7612ng-g313ie");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    PostsApi apiInstance = new PostsApi(defaultClient);
    String postUuid = "postUuid_example"; // String | Post UUID
    UpdatePostRequest updatePostRequest = new UpdatePostRequest(); // UpdatePostRequest | 
    try {
      DeleteMediaFiles200Response result = apiInstance.updatePost(postUuid, updatePostRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling PostsApi#updatePost");
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
| **postUuid** | **String**| Post UUID | |
| **updatePostRequest** | [**UpdatePostRequest**](UpdatePostRequest.md)|  | [optional] |

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

