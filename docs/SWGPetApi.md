# \SWGPetApi

All URIs are relative to *http://petstore.swagger.io/v2*

Method | HTTP request | Description
------------- | ------------- | -------------
[**addPet**](SWGPetApi.md#addPet) | **POST** /pet | Add a new pet to the store
[**addPetUsingByteArray**](SWGPetApi.md#addPetUsingByteArray) | **POST** /pet?testing_byte_array=true | Fake endpoint to test byte array in body parameter for adding a new pet to the store
[**deletePet**](SWGPetApi.md#deletePet) | **DELETE** /pet/{petId} | Deletes a pet
[**findPetsByStatus**](SWGPetApi.md#findPetsByStatus) | **GET** /pet/findByStatus | Finds Pets by status
[**findPetsByTags**](SWGPetApi.md#findPetsByTags) | **GET** /pet/findByTags | Finds Pets by tags
[**getPetById**](SWGPetApi.md#getPetById) | **GET** /pet/{petId} | Find pet by ID
[**getPetByIdInObject**](SWGPetApi.md#getPetByIdInObject) | **GET** /pet/{petId}?response=inline_arbitrary_object | Fake endpoint to test inline arbitrary object return by &#39;Find pet by ID&#39;
[**petPetIdtestingByteArraytrueGet**](SWGPetApi.md#petPetIdtestingByteArraytrueGet) | **GET** /pet/{petId}?testing_byte_array=true | Fake endpoint to test byte array return by &#39;Find pet by ID&#39;
[**updatePet**](SWGPetApi.md#updatePet) | **PUT** /pet | Update an existing pet
[**updatePetWithForm**](SWGPetApi.md#updatePetWithForm) | **POST** /pet/{petId} | Updates a pet in the store with form data
[**uploadFile**](SWGPetApi.md#uploadFile) | **POST** /pet/{petId}/uploadImage | uploads an image


# **addPet**
> addPet($body)

Add a new pet to the store



### Example 
```objc

SWGConfiguration *apiConfig = [SWGConfiguration sharedConfig];

// Configure OAuth2 access token for authorization: (authentication scheme: petstore_auth)
[apiConfig setAccessToken:@"YOUR_ACCESS_TOKEN"];


SWGPet* *body = SwaggerClient.SWGPet*(); // SWGPet* | Pet object that needs to be added to the store

@try
{ 
    SWGSWGPetApi *apiInstance = [[SWGPetApi alloc] init];

    // Add a new pet to the store
    [apiInstance addPetWithBody:body
              completionHandler: ^(NSError* error)) {
                            if (error) {
                                NSLog(@"Error: %@", error);
                            }
                        }];
}
@catch (NSException *exception)
{
    NSLog(@"Exception when calling SWGPetApi->addPet: %@ ", exception.name);
    NSLog(@"Reason: %@ ", exception.reason);
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**SWGPet***](SWGPet*.md)| Pet object that needs to be added to the store | [optional] 

### Return type

void (empty response body)

### Authorization

[petstore_auth](../README.md#petstore_auth)

### HTTP reuqest headers

 - **Content-Type**: application/json, application/xml
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **addPetUsingByteArray**
> addPetUsingByteArray($body)

Fake endpoint to test byte array in body parameter for adding a new pet to the store



### Example 
```objc

SWGConfiguration *apiConfig = [SWGConfiguration sharedConfig];

// Configure OAuth2 access token for authorization: (authentication scheme: petstore_auth)
[apiConfig setAccessToken:@"YOUR_ACCESS_TOKEN"];


NSString* *body = B; // NSString* | Pet object in the form of byte array

@try
{ 
    SWGSWGPetApi *apiInstance = [[SWGPetApi alloc] init];

    // Fake endpoint to test byte array in body parameter for adding a new pet to the store
    [apiInstance addPetUsingByteArrayWithBody:body
              completionHandler: ^(NSError* error)) {
                            if (error) {
                                NSLog(@"Error: %@", error);
                            }
                        }];
}
@catch (NSException *exception)
{
    NSLog(@"Exception when calling SWGPetApi->addPetUsingByteArray: %@ ", exception.name);
    NSLog(@"Reason: %@ ", exception.reason);
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | **NSString***| Pet object in the form of byte array | [optional] 

### Return type

void (empty response body)

### Authorization

[petstore_auth](../README.md#petstore_auth)

### HTTP reuqest headers

 - **Content-Type**: application/json, application/xml
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **deletePet**
> deletePet($petId, $apiKey)

Deletes a pet



### Example 
```objc

SWGConfiguration *apiConfig = [SWGConfiguration sharedConfig];

// Configure OAuth2 access token for authorization: (authentication scheme: petstore_auth)
[apiConfig setAccessToken:@"YOUR_ACCESS_TOKEN"];


NSNumber* *petId = @789; // NSNumber* | Pet id to delete
NSString* *apiKey = @"apiKey_example"; // NSString* | 

@try
{ 
    SWGSWGPetApi *apiInstance = [[SWGPetApi alloc] init];

    // Deletes a pet
    [apiInstance deletePetWithPetId:petId
    apiKey:apiKey
              completionHandler: ^(NSError* error)) {
                            if (error) {
                                NSLog(@"Error: %@", error);
                            }
                        }];
}
@catch (NSException *exception)
{
    NSLog(@"Exception when calling SWGPetApi->deletePet: %@ ", exception.name);
    NSLog(@"Reason: %@ ", exception.reason);
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **petId** | **NSNumber***| Pet id to delete | 
 **apiKey** | **NSString***|  | [optional] 

### Return type

void (empty response body)

### Authorization

[petstore_auth](../README.md#petstore_auth)

### HTTP reuqest headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **findPetsByStatus**
> NSArray<SWGPet>* findPetsByStatus($status)

Finds Pets by status

Multiple status values can be provided with comma separated strings

### Example 
```objc

SWGConfiguration *apiConfig = [SWGConfiguration sharedConfig];

// Configure OAuth2 access token for authorization: (authentication scheme: petstore_auth)
[apiConfig setAccessToken:@"YOUR_ACCESS_TOKEN"];


NSArray* /* NSString */ *status = @[@"available"]; // NSArray* /* NSString */ | Status values that need to be considered for query (default to available)

@try
{ 
    SWGSWGPetApi *apiInstance = [[SWGPetApi alloc] init];

    // Finds Pets by status
    [apiInstance findPetsByStatusWithStatus:status
              completionHandler: ^(NSArray<SWGPet>* output, NSError* error)) {
                            if (output) {
                                NSLog(@"%@", output);
                            }
                            if (error) {
                                NSLog(@"Error: %@", error);
                            }
                        }];
}
@catch (NSException *exception)
{
    NSLog(@"Exception when calling SWGPetApi->findPetsByStatus: %@ ", exception.name);
    NSLog(@"Reason: %@ ", exception.reason);
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **status** | [**NSArray* /* NSString */**](NSString*.md)| Status values that need to be considered for query | [optional] [default to available]

### Return type

[**NSArray<SWGPet>***](SWGPet.md)

### Authorization

[petstore_auth](../README.md#petstore_auth)

### HTTP reuqest headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **findPetsByTags**
> NSArray<SWGPet>* findPetsByTags($tags)

Finds Pets by tags

Muliple tags can be provided with comma seperated strings. Use tag1, tag2, tag3 for testing.

### Example 
```objc

SWGConfiguration *apiConfig = [SWGConfiguration sharedConfig];

// Configure OAuth2 access token for authorization: (authentication scheme: petstore_auth)
[apiConfig setAccessToken:@"YOUR_ACCESS_TOKEN"];


NSArray* /* NSString */ *tags = @[@"tags_example"]; // NSArray* /* NSString */ | Tags to filter by

@try
{ 
    SWGSWGPetApi *apiInstance = [[SWGPetApi alloc] init];

    // Finds Pets by tags
    [apiInstance findPetsByTagsWithTags:tags
              completionHandler: ^(NSArray<SWGPet>* output, NSError* error)) {
                            if (output) {
                                NSLog(@"%@", output);
                            }
                            if (error) {
                                NSLog(@"Error: %@", error);
                            }
                        }];
}
@catch (NSException *exception)
{
    NSLog(@"Exception when calling SWGPetApi->findPetsByTags: %@ ", exception.name);
    NSLog(@"Reason: %@ ", exception.reason);
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **tags** | [**NSArray* /* NSString */**](NSString*.md)| Tags to filter by | [optional] 

### Return type

[**NSArray<SWGPet>***](SWGPet.md)

### Authorization

[petstore_auth](../README.md#petstore_auth)

### HTTP reuqest headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getPetById**
> SWGPet* getPetById($petId)

Find pet by ID

Returns a pet when ID < 10.  ID > 10 or nonintegers will simulate API error conditions

### Example 
```objc

SWGConfiguration *apiConfig = [SWGConfiguration sharedConfig];

// Configure API key authorization: (authentication scheme: api_key)
[apiConfig setApiKey:@"YOUR_API_KEY" forApiKeyIdentifier:@"api_key"];
// Uncomment below to setup prefix (e.g. BEARER) for API key, if needed
//[apiConfig setApiKeyPrefix:@"BEARER" forApiKeyIdentifier:@"api_key"];

// Configure OAuth2 access token for authorization: (authentication scheme: petstore_auth)
[apiConfig setAccessToken:@"YOUR_ACCESS_TOKEN"];


NSNumber* *petId = @789; // NSNumber* | ID of pet that needs to be fetched

@try
{ 
    SWGSWGPetApi *apiInstance = [[SWGPetApi alloc] init];

    // Find pet by ID
    [apiInstance getPetByIdWithPetId:petId
              completionHandler: ^(SWGPet* output, NSError* error)) {
                            if (output) {
                                NSLog(@"%@", output);
                            }
                            if (error) {
                                NSLog(@"Error: %@", error);
                            }
                        }];
}
@catch (NSException *exception)
{
    NSLog(@"Exception when calling SWGPetApi->getPetById: %@ ", exception.name);
    NSLog(@"Reason: %@ ", exception.reason);
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **petId** | **NSNumber***| ID of pet that needs to be fetched | 

### Return type

[**SWGPet***](SWGPet.md)

### Authorization

[api_key](../README.md#api_key), [petstore_auth](../README.md#petstore_auth)

### HTTP reuqest headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getPetByIdInObject**
> SWGInlineResponse200* getPetByIdInObject($petId)

Fake endpoint to test inline arbitrary object return by 'Find pet by ID'

Returns a pet when ID < 10.  ID > 10 or nonintegers will simulate API error conditions

### Example 
```objc

SWGConfiguration *apiConfig = [SWGConfiguration sharedConfig];

// Configure API key authorization: (authentication scheme: api_key)
[apiConfig setApiKey:@"YOUR_API_KEY" forApiKeyIdentifier:@"api_key"];
// Uncomment below to setup prefix (e.g. BEARER) for API key, if needed
//[apiConfig setApiKeyPrefix:@"BEARER" forApiKeyIdentifier:@"api_key"];

// Configure OAuth2 access token for authorization: (authentication scheme: petstore_auth)
[apiConfig setAccessToken:@"YOUR_ACCESS_TOKEN"];


NSNumber* *petId = @789; // NSNumber* | ID of pet that needs to be fetched

@try
{ 
    SWGSWGPetApi *apiInstance = [[SWGPetApi alloc] init];

    // Fake endpoint to test inline arbitrary object return by 'Find pet by ID'
    [apiInstance getPetByIdInObjectWithPetId:petId
              completionHandler: ^(SWGInlineResponse200* output, NSError* error)) {
                            if (output) {
                                NSLog(@"%@", output);
                            }
                            if (error) {
                                NSLog(@"Error: %@", error);
                            }
                        }];
}
@catch (NSException *exception)
{
    NSLog(@"Exception when calling SWGPetApi->getPetByIdInObject: %@ ", exception.name);
    NSLog(@"Reason: %@ ", exception.reason);
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **petId** | **NSNumber***| ID of pet that needs to be fetched | 

### Return type

[**SWGInlineResponse200***](SWGInlineResponse200.md)

### Authorization

[api_key](../README.md#api_key), [petstore_auth](../README.md#petstore_auth)

### HTTP reuqest headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **petPetIdtestingByteArraytrueGet**
> NSString* petPetIdtestingByteArraytrueGet($petId)

Fake endpoint to test byte array return by 'Find pet by ID'

Returns a pet when ID < 10.  ID > 10 or nonintegers will simulate API error conditions

### Example 
```objc

SWGConfiguration *apiConfig = [SWGConfiguration sharedConfig];

// Configure API key authorization: (authentication scheme: api_key)
[apiConfig setApiKey:@"YOUR_API_KEY" forApiKeyIdentifier:@"api_key"];
// Uncomment below to setup prefix (e.g. BEARER) for API key, if needed
//[apiConfig setApiKeyPrefix:@"BEARER" forApiKeyIdentifier:@"api_key"];

// Configure OAuth2 access token for authorization: (authentication scheme: petstore_auth)
[apiConfig setAccessToken:@"YOUR_ACCESS_TOKEN"];


NSNumber* *petId = @789; // NSNumber* | ID of pet that needs to be fetched

@try
{ 
    SWGSWGPetApi *apiInstance = [[SWGPetApi alloc] init];

    // Fake endpoint to test byte array return by 'Find pet by ID'
    [apiInstance petPetIdtestingByteArraytrueGetWithPetId:petId
              completionHandler: ^(NSString* output, NSError* error)) {
                            if (output) {
                                NSLog(@"%@", output);
                            }
                            if (error) {
                                NSLog(@"Error: %@", error);
                            }
                        }];
}
@catch (NSException *exception)
{
    NSLog(@"Exception when calling SWGPetApi->petPetIdtestingByteArraytrueGet: %@ ", exception.name);
    NSLog(@"Reason: %@ ", exception.reason);
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **petId** | **NSNumber***| ID of pet that needs to be fetched | 

### Return type

**NSString***

### Authorization

[api_key](../README.md#api_key), [petstore_auth](../README.md#petstore_auth)

### HTTP reuqest headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **updatePet**
> updatePet($body)

Update an existing pet



### Example 
```objc

SWGConfiguration *apiConfig = [SWGConfiguration sharedConfig];

// Configure OAuth2 access token for authorization: (authentication scheme: petstore_auth)
[apiConfig setAccessToken:@"YOUR_ACCESS_TOKEN"];


SWGPet* *body = SwaggerClient.SWGPet*(); // SWGPet* | Pet object that needs to be added to the store

@try
{ 
    SWGSWGPetApi *apiInstance = [[SWGPetApi alloc] init];

    // Update an existing pet
    [apiInstance updatePetWithBody:body
              completionHandler: ^(NSError* error)) {
                            if (error) {
                                NSLog(@"Error: %@", error);
                            }
                        }];
}
@catch (NSException *exception)
{
    NSLog(@"Exception when calling SWGPetApi->updatePet: %@ ", exception.name);
    NSLog(@"Reason: %@ ", exception.reason);
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**SWGPet***](SWGPet*.md)| Pet object that needs to be added to the store | [optional] 

### Return type

void (empty response body)

### Authorization

[petstore_auth](../README.md#petstore_auth)

### HTTP reuqest headers

 - **Content-Type**: application/json, application/xml
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **updatePetWithForm**
> updatePetWithForm($petId, $name, $status)

Updates a pet in the store with form data



### Example 
```objc

SWGConfiguration *apiConfig = [SWGConfiguration sharedConfig];

// Configure OAuth2 access token for authorization: (authentication scheme: petstore_auth)
[apiConfig setAccessToken:@"YOUR_ACCESS_TOKEN"];


NSString* *petId = @"petId_example"; // NSString* | ID of pet that needs to be updated
NSString* *name = @"name_example"; // NSString* | Updated name of the pet
NSString* *status = @"status_example"; // NSString* | Updated status of the pet

@try
{ 
    SWGSWGPetApi *apiInstance = [[SWGPetApi alloc] init];

    // Updates a pet in the store with form data
    [apiInstance updatePetWithFormWithPetId:petId
    name:name
    status:status
              completionHandler: ^(NSError* error)) {
                            if (error) {
                                NSLog(@"Error: %@", error);
                            }
                        }];
}
@catch (NSException *exception)
{
    NSLog(@"Exception when calling SWGPetApi->updatePetWithForm: %@ ", exception.name);
    NSLog(@"Reason: %@ ", exception.reason);
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **petId** | **NSString***| ID of pet that needs to be updated | 
 **name** | **NSString***| Updated name of the pet | [optional] 
 **status** | **NSString***| Updated status of the pet | [optional] 

### Return type

void (empty response body)

### Authorization

[petstore_auth](../README.md#petstore_auth)

### HTTP reuqest headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **uploadFile**
> uploadFile($petId, $additionalMetadata, $file)

uploads an image



### Example 
```objc

SWGConfiguration *apiConfig = [SWGConfiguration sharedConfig];

// Configure OAuth2 access token for authorization: (authentication scheme: petstore_auth)
[apiConfig setAccessToken:@"YOUR_ACCESS_TOKEN"];


NSNumber* *petId = @789; // NSNumber* | ID of pet to update
NSString* *additionalMetadata = @"additionalMetadata_example"; // NSString* | Additional data to pass to server
NSURL* *file = SwaggerClient.NSURL*(); // NSURL* | file to upload

@try
{ 
    SWGSWGPetApi *apiInstance = [[SWGPetApi alloc] init];

    // uploads an image
    [apiInstance uploadFileWithPetId:petId
    additionalMetadata:additionalMetadata
    file:file
              completionHandler: ^(NSError* error)) {
                            if (error) {
                                NSLog(@"Error: %@", error);
                            }
                        }];
}
@catch (NSException *exception)
{
    NSLog(@"Exception when calling SWGPetApi->uploadFile: %@ ", exception.name);
    NSLog(@"Reason: %@ ", exception.reason);
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **petId** | **NSNumber***| ID of pet to update | 
 **additionalMetadata** | **NSString***| Additional data to pass to server | [optional] 
 **file** | **NSURL***| file to upload | [optional] 

### Return type

void (empty response body)

### Authorization

[petstore_auth](../README.md#petstore_auth)

### HTTP reuqest headers

 - **Content-Type**: multipart/form-data
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

