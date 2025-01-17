# openapi-java-client

PostPuma - OpenAPI 3.0
- API version: 1.0.0
  - Build date: 2024-10-24T16:39:28.677807+02:00[Europe/Berlin]
  - Generator version: 7.9.0

PostPuma API specifications


*Automatically generated by the [OpenAPI Generator](https://openapi-generator.tech)*


## Requirements

Building the API client library requires:
1. Java 1.8+
2. Maven (3.8.3+)/Gradle (7.2+)

## Installation

To install the API client library to your local Maven repository, simply execute:

```shell
mvn clean install
```

To deploy it to a remote Maven repository instead, configure the settings of the repository and execute:

```shell
mvn clean deploy
```

Refer to the [OSSRH Guide](http://central.sonatype.org/pages/ossrh-guide.html) for more information.

### Maven users

Add this dependency to your project's POM:

```xml
<dependency>
  <groupId>org.openapitools</groupId>
  <artifactId>openapi-java-client</artifactId>
  <version>1.0.0</version>
  <scope>compile</scope>
</dependency>
```

### Gradle users

Add this dependency to your project's build file:

```groovy
  repositories {
    mavenCentral()     // Needed if the 'openapi-java-client' jar has been published to maven central.
    mavenLocal()       // Needed if the 'openapi-java-client' jar has been published to the local maven repo.
  }

  dependencies {
     implementation "org.openapitools:openapi-java-client:1.0.0"
  }
```

### Others

At first generate the JAR by executing:

```shell
mvn clean package
```

Then manually install the following JARs:

* `target/openapi-java-client-1.0.0.jar`
* `target/lib/*.jar`

## Getting Started

Please follow the [installation](#installation) instruction and execute the following Java code:

```java

// Import classes:
import PostPuma.ApiClient;
import PostPuma.ApiException;
import PostPuma.Configuration;
import PostPuma.auth.*;
import org.openapitools.client.model.*;
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

## Documentation for API Endpoints

All URIs are relative to *https://app.postpuma.com/app/5afgg2-1egj4n-7612ng-g313ie*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*AccountsApi* | [**getAccount**](docs/AccountsApi.md#getAccount) | **GET** /accounts/{accountUuid} | Get account
*AccountsApi* | [**listAccounts**](docs/AccountsApi.md#listAccounts) | **GET** /accounts | List accounts
*MediaApi* | [**deleteMediaFiles**](docs/MediaApi.md#deleteMediaFiles) | **DELETE** /media | Delete media files
*MediaApi* | [**getMediaFile**](docs/MediaApi.md#getMediaFile) | **GET** /media/{mediaUuid} | Get media file
*MediaApi* | [**listMediaFiles**](docs/MediaApi.md#listMediaFiles) | **GET** /media | List media files
*MediaApi* | [**uploadMediaFile**](docs/MediaApi.md#uploadMediaFile) | **POST** /media | Upload media file
*PostsApi* | [**createPost**](docs/PostsApi.md#createPost) | **POST** /posts | Create post
*PostsApi* | [**deletePost**](docs/PostsApi.md#deletePost) | **DELETE** /posts/{postUuid} | Delete post
*PostsApi* | [**deletePosts**](docs/PostsApi.md#deletePosts) | **DELETE** /posts | Delete posts
*PostsApi* | [**getPost**](docs/PostsApi.md#getPost) | **GET** /posts/{postUuid} | Get post
*PostsApi* | [**listPosts**](docs/PostsApi.md#listPosts) | **GET** /posts | List posts
*PostsApi* | [**queuePost**](docs/PostsApi.md#queuePost) | **POST** /posts/add-to-queue/{postUuid} | Queue post
*PostsApi* | [**schedulePost**](docs/PostsApi.md#schedulePost) | **POST** /posts/schedule/{postUuid} | Schedule post
*PostsApi* | [**updatePost**](docs/PostsApi.md#updatePost) | **PUT** /posts/{postUuid} | Update post
*TagsApi* | [**createTag**](docs/TagsApi.md#createTag) | **POST** /tags | Create tag
*TagsApi* | [**deleteTag**](docs/TagsApi.md#deleteTag) | **DELETE** /tags/{tagUuid} | Delete tag
*TagsApi* | [**getTag**](docs/TagsApi.md#getTag) | **GET** /tags/{tagUuid} | Get tag
*TagsApi* | [**listTags**](docs/TagsApi.md#listTags) | **GET** /tags | List tags
*TagsApi* | [**updateTag**](docs/TagsApi.md#updateTag) | **PUT** /tags/{tagUuid} | Update tag


## Documentation for Models

 - [Account](docs/Account.md)
 - [AccountData](docs/AccountData.md)
 - [CreatePostRequest](docs/CreatePostRequest.md)
 - [CreateTagRequest](docs/CreateTagRequest.md)
 - [DeleteMediaFiles200Response](docs/DeleteMediaFiles200Response.md)
 - [DeleteMediaFilesRequest](docs/DeleteMediaFilesRequest.md)
 - [DeletePostRequest](docs/DeletePostRequest.md)
 - [DeletePosts200Response](docs/DeletePosts200Response.md)
 - [DeletePosts200ResponseOneOf](docs/DeletePosts200ResponseOneOf.md)
 - [DeletePosts200ResponseOneOf1](docs/DeletePosts200ResponseOneOf1.md)
 - [DeletePostsRequest](docs/DeletePostsRequest.md)
 - [ListAccounts200Response](docs/ListAccounts200Response.md)
 - [ListMediaFiles200Response](docs/ListMediaFiles200Response.md)
 - [ListPosts200Response](docs/ListPosts200Response.md)
 - [ListTags200Response](docs/ListTags200Response.md)
 - [MediaFile](docs/MediaFile.md)
 - [Post](docs/Post.md)
 - [PostUser](docs/PostUser.md)
 - [QueuePost200Response](docs/QueuePost200Response.md)
 - [SchedulePostRequest](docs/SchedulePostRequest.md)
 - [Tag](docs/Tag.md)
 - [UpdatePostRequest](docs/UpdatePostRequest.md)
 - [UpdateTagRequest](docs/UpdateTagRequest.md)
 - [Version](docs/Version.md)
 - [VersionContent](docs/VersionContent.md)
 - [VersionOptions](docs/VersionOptions.md)
 - [VersionOptionsInstagram](docs/VersionOptionsInstagram.md)
 - [VersionOptionsLinkedin](docs/VersionOptionsLinkedin.md)
 - [VersionOptionsMastodon](docs/VersionOptionsMastodon.md)
 - [VersionOptionsPinterest](docs/VersionOptionsPinterest.md)
 - [VersionOptionsPinterestBoards](docs/VersionOptionsPinterestBoards.md)
 - [VersionOptionsTiktok](docs/VersionOptionsTiktok.md)
 - [VersionOptionsTiktokPrivacyLevel](docs/VersionOptionsTiktokPrivacyLevel.md)
 - [VersionOptionsYoutube](docs/VersionOptionsYoutube.md)


<a id="documentation-for-authorization"></a>
## Documentation for Authorization


Authentication schemes defined for the API:
<a id="bearerAuth"></a>
### bearerAuth

- **Type**: HTTP Bearer Token authentication


## Recommendation

It's recommended to create an instance of `ApiClient` per thread in a multithreaded environment to avoid any potential issues.

## Author

support@postpuma.com

