# PetApi

All URIs are relative to *http://petstore.swagger.io/v2*

Method | HTTP request | Description
------------- | ------------- | -------------
[**addPet**](PetApi.md#addPet) | **POST** /pet | Add a new pet to the store
[**deletePet**](PetApi.md#deletePet) | **DELETE** /pet/{petId} | Deletes a pet
[**findPetsByStatus**](PetApi.md#findPetsByStatus) | **GET** /pet/findByStatus | Finds Pets by status
[**findPetsByTags**](PetApi.md#findPetsByTags) | **GET** /pet/findByTags | Finds Pets by tags
[**getPetById**](PetApi.md#getPetById) | **GET** /pet/{petId} | Find pet by ID
[**updatePet**](PetApi.md#updatePet) | **PUT** /pet | Update an existing pet
[**updatePetWithForm**](PetApi.md#updatePetWithForm) | **POST** /pet/{petId} | Updates a pet in the store with form data
[**uploadFile**](PetApi.md#uploadFile) | **POST** /pet/{petId}/uploadImage | uploads an image


<a name="addPet"></a>
# **addPet**
> Void addPet(body)

Add a new pet to the store



### Example
```java
// Import classes:
//import com.prokarma.pkmst.controller.ApiClient;
//import com.prokarma.pkmst.controller.ApiException;
//import com.prokarma.pkmst.controller.Configuration;
//import com.prokarma.pkmst.controller.auth.*;
//import com.prokarma.pkmst.controller.PetApi;

ApiClient defaultClient = Configuration.getDefaultApiClient();

// Configure OAuth2 access token for authorization: petstore_auth
OAuth petstore_auth = (OAuth) defaultClient.getAuthentication("petstore_auth");
petstore_auth.setAccessToken("YOUR ACCESS TOKEN");

PetApi apiInstance = new PetApi();
Pet body = ; // Pet | Pet object that needs to be added to the store
try {
    Void result = apiInstance.addPet(body);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling PetApi#addPet");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**Pet**](Pet.md)| Pet object that needs to be added to the store |

### Return type

[**Void**](.md)

### Authorization

[petstore_auth](../README.md#petstore_auth)

### HTTP request headers

 - **Content-Type**: application/json, application/xml
 - **Accept**: application/xml, application/json

<a name="deletePet"></a>
# **deletePet**
> Void deletePet(petId, apiKey)

Deletes a pet



### Example
```java
// Import classes:
//import com.prokarma.pkmst.controller.ApiClient;
//import com.prokarma.pkmst.controller.ApiException;
//import com.prokarma.pkmst.controller.Configuration;
//import com.prokarma.pkmst.controller.auth.*;
//import com.prokarma.pkmst.controller.PetApi;

ApiClient defaultClient = Configuration.getDefaultApiClient();

// Configure OAuth2 access token for authorization: petstore_auth
OAuth petstore_auth = (OAuth) defaultClient.getAuthentication("petstore_auth");
petstore_auth.setAccessToken("YOUR ACCESS TOKEN");

PetApi apiInstance = new PetApi();
Long petId = 789; // Long | Pet id to delete
String apiKey = apiKey_example; // String | 
try {
    Void result = apiInstance.deletePet(petId, apiKey);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling PetApi#deletePet");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **petId** | **Long**| Pet id to delete |
 **apiKey** | **String**|  | [optional]

### Return type

[**Void**](.md)

### Authorization

[petstore_auth](../README.md#petstore_auth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/xml, application/json

<a name="findPetsByStatus"></a>
# **findPetsByStatus**
> Pet findPetsByStatus(status)

Finds Pets by status

Multiple status values can be provided with comma separated strings

### Example
```java
// Import classes:
//import com.prokarma.pkmst.controller.ApiClient;
//import com.prokarma.pkmst.controller.ApiException;
//import com.prokarma.pkmst.controller.Configuration;
//import com.prokarma.pkmst.controller.auth.*;
//import com.prokarma.pkmst.controller.PetApi;

ApiClient defaultClient = Configuration.getDefaultApiClient();

// Configure OAuth2 access token for authorization: petstore_auth
OAuth petstore_auth = (OAuth) defaultClient.getAuthentication("petstore_auth");
petstore_auth.setAccessToken("YOUR ACCESS TOKEN");

PetApi apiInstance = new PetApi();
List<String> status = ; // List<String> | Status values that need to be considered for filter
try {
    Pet result = apiInstance.findPetsByStatus(status);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling PetApi#findPetsByStatus");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **status** | [**List&lt;String&gt;**](String.md)| Status values that need to be considered for filter | [enum: available, pending, sold]

### Return type

[**Pet**](Pet.md)

### Authorization

[petstore_auth](../README.md#petstore_auth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/xml, application/json

<a name="findPetsByTags"></a>
# **findPetsByTags**
> Pet findPetsByTags(tags)

Finds Pets by tags

Muliple tags can be provided with comma separated strings. Use         tag1, tag2, tag3 for testing.

### Example
```java
// Import classes:
//import com.prokarma.pkmst.controller.ApiClient;
//import com.prokarma.pkmst.controller.ApiException;
//import com.prokarma.pkmst.controller.Configuration;
//import com.prokarma.pkmst.controller.auth.*;
//import com.prokarma.pkmst.controller.PetApi;

ApiClient defaultClient = Configuration.getDefaultApiClient();

// Configure OAuth2 access token for authorization: petstore_auth
OAuth petstore_auth = (OAuth) defaultClient.getAuthentication("petstore_auth");
petstore_auth.setAccessToken("YOUR ACCESS TOKEN");

PetApi apiInstance = new PetApi();
List<String> tags = ; // List<String> | Tags to filter by
try {
    Pet result = apiInstance.findPetsByTags(tags);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling PetApi#findPetsByTags");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **tags** | [**List&lt;String&gt;**](String.md)| Tags to filter by |

### Return type

[**Pet**](Pet.md)

### Authorization

[petstore_auth](../README.md#petstore_auth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/xml, application/json

<a name="getPetById"></a>
# **getPetById**
> Pet getPetById(petId)

Find pet by ID

Returns a single pet

### Example
```java
// Import classes:
//import com.prokarma.pkmst.controller.ApiClient;
//import com.prokarma.pkmst.controller.ApiException;
//import com.prokarma.pkmst.controller.Configuration;
//import com.prokarma.pkmst.controller.auth.*;
//import com.prokarma.pkmst.controller.PetApi;

ApiClient defaultClient = Configuration.getDefaultApiClient();

// Configure API key authorization: api_key
ApiKeyAuth api_key = (ApiKeyAuth) defaultClient.getAuthentication("api_key");
api_key.setApiKey("YOUR API KEY");
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//api_key.setApiKeyPrefix("Token");

PetApi apiInstance = new PetApi();
Long petId = 789; // Long | ID of pet to return
try {
    Pet result = apiInstance.getPetById(petId);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling PetApi#getPetById");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **petId** | **Long**| ID of pet to return |

### Return type

[**Pet**](Pet.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/xml, application/json

<a name="updatePet"></a>
# **updatePet**
> Void updatePet(body)

Update an existing pet



### Example
```java
// Import classes:
//import com.prokarma.pkmst.controller.ApiClient;
//import com.prokarma.pkmst.controller.ApiException;
//import com.prokarma.pkmst.controller.Configuration;
//import com.prokarma.pkmst.controller.auth.*;
//import com.prokarma.pkmst.controller.PetApi;

ApiClient defaultClient = Configuration.getDefaultApiClient();

// Configure OAuth2 access token for authorization: petstore_auth
OAuth petstore_auth = (OAuth) defaultClient.getAuthentication("petstore_auth");
petstore_auth.setAccessToken("YOUR ACCESS TOKEN");

PetApi apiInstance = new PetApi();
Pet body = ; // Pet | Pet object that needs to be added to the store
try {
    Void result = apiInstance.updatePet(body);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling PetApi#updatePet");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**Pet**](Pet.md)| Pet object that needs to be added to the store |

### Return type

[**Void**](.md)

### Authorization

[petstore_auth](../README.md#petstore_auth)

### HTTP request headers

 - **Content-Type**: application/json, application/xml
 - **Accept**: application/xml, application/json

<a name="updatePetWithForm"></a>
# **updatePetWithForm**
> Void updatePetWithForm(petId, name, status)

Updates a pet in the store with form data



### Example
```java
// Import classes:
//import com.prokarma.pkmst.controller.ApiClient;
//import com.prokarma.pkmst.controller.ApiException;
//import com.prokarma.pkmst.controller.Configuration;
//import com.prokarma.pkmst.controller.auth.*;
//import com.prokarma.pkmst.controller.PetApi;

ApiClient defaultClient = Configuration.getDefaultApiClient();

// Configure OAuth2 access token for authorization: petstore_auth
OAuth petstore_auth = (OAuth) defaultClient.getAuthentication("petstore_auth");
petstore_auth.setAccessToken("YOUR ACCESS TOKEN");

PetApi apiInstance = new PetApi();
Long petId = 789; // Long | ID of pet that needs to be updated
String name = name_example; // String | Updated name of the pet
String status = status_example; // String | Updated status of the pet
try {
    Void result = apiInstance.updatePetWithForm(petId, name, status);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling PetApi#updatePetWithForm");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **petId** | **Long**| ID of pet that needs to be updated |
 **name** | **String**| Updated name of the pet | [optional]
 **status** | **String**| Updated status of the pet | [optional]

### Return type

[**Void**](.md)

### Authorization

[petstore_auth](../README.md#petstore_auth)

### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/xml, application/json

<a name="uploadFile"></a>
# **uploadFile**
> ModelApiResponse uploadFile(petId, additionalMetadata, file)

uploads an image



### Example
```java
// Import classes:
//import com.prokarma.pkmst.controller.ApiClient;
//import com.prokarma.pkmst.controller.ApiException;
//import com.prokarma.pkmst.controller.Configuration;
//import com.prokarma.pkmst.controller.auth.*;
//import com.prokarma.pkmst.controller.PetApi;

ApiClient defaultClient = Configuration.getDefaultApiClient();

// Configure OAuth2 access token for authorization: petstore_auth
OAuth petstore_auth = (OAuth) defaultClient.getAuthentication("petstore_auth");
petstore_auth.setAccessToken("YOUR ACCESS TOKEN");

PetApi apiInstance = new PetApi();
Long petId = 789; // Long | ID of pet to update
String additionalMetadata = additionalMetadata_example; // String | Additional data to pass to server
File file = new org.springframework.core.io.FileSystemResource(new java.io.File("/path/to/file.txt")); // File | file to upload
try {
    ModelApiResponse result = apiInstance.uploadFile(petId, additionalMetadata, file);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling PetApi#uploadFile");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **petId** | **Long**| ID of pet to update |
 **additionalMetadata** | **String**| Additional data to pass to server | [optional]
 **file** | **File**| file to upload | [optional]

### Return type

[**ModelApiResponse**](ModelApiResponse.md)

### Authorization

[petstore_auth](../README.md#petstore_auth)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: application/json

