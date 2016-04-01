# \SWGUserApi

All URIs are relative to *http://petstore.swagger.io/v2*

Method | HTTP request | Description
------------- | ------------- | -------------
[**createUser**](SWGUserApi.md#createUser) | **POST** /user | Create user
[**createUsersWithArrayInput**](SWGUserApi.md#createUsersWithArrayInput) | **POST** /user/createWithArray | Creates list of users with given input array
[**createUsersWithListInput**](SWGUserApi.md#createUsersWithListInput) | **POST** /user/createWithList | Creates list of users with given input array
[**deleteUser**](SWGUserApi.md#deleteUser) | **DELETE** /user/{username} | Delete user
[**getUserByName**](SWGUserApi.md#getUserByName) | **GET** /user/{username} | Get user by user name
[**loginUser**](SWGUserApi.md#loginUser) | **GET** /user/login | Logs user into the system
[**logoutUser**](SWGUserApi.md#logoutUser) | **GET** /user/logout | Logs out current logged in user session
[**updateUser**](SWGUserApi.md#updateUser) | **PUT** /user/{username} | Updated user


# **createUser**
> createUser($body)

Create user

This can only be done by the logged in user.

### Example 
```objc

SWGUser* body = SwaggerClient.SWGUser*(); // Created user object

@try
{ 
    SWGSWGUserApi *apiInstance = [[SWGUserApi alloc] init];

    // Create user
    [apiInstance createUserWithBody:body
              completionHandler: ^(NSError* error)) {
                            if (error) {
                                NSLog(@"Error: %@", error);
                            }
                        }];
}
@catch (NSException *exception)
{
    NSLog(@"Exception when calling SWGUserApi->createUser: %@ ", exception.name);
    NSLog(@"Reason: %@ ", exception.reason);
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**SWGUser***](SWGUser*.md)| Created user object | [optional] 

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP reuqest headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **createUsersWithArrayInput**
> createUsersWithArrayInput($body)

Creates list of users with given input array



### Example 
```objc

NSArray<SWGUser>* body = @[SwaggerClient.SWGUser()]; // List of user object

@try
{ 
    SWGSWGUserApi *apiInstance = [[SWGUserApi alloc] init];

    // Creates list of users with given input array
    [apiInstance createUsersWithArrayInputWithBody:body
              completionHandler: ^(NSError* error)) {
                            if (error) {
                                NSLog(@"Error: %@", error);
                            }
                        }];
}
@catch (NSException *exception)
{
    NSLog(@"Exception when calling SWGUserApi->createUsersWithArrayInput: %@ ", exception.name);
    NSLog(@"Reason: %@ ", exception.reason);
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**NSArray&lt;SWGUser&gt;***](SWGUser.md)| List of user object | [optional] 

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP reuqest headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **createUsersWithListInput**
> createUsersWithListInput($body)

Creates list of users with given input array



### Example 
```objc

NSArray<SWGUser>* body = @[SwaggerClient.SWGUser()]; // List of user object

@try
{ 
    SWGSWGUserApi *apiInstance = [[SWGUserApi alloc] init];

    // Creates list of users with given input array
    [apiInstance createUsersWithListInputWithBody:body
              completionHandler: ^(NSError* error)) {
                            if (error) {
                                NSLog(@"Error: %@", error);
                            }
                        }];
}
@catch (NSException *exception)
{
    NSLog(@"Exception when calling SWGUserApi->createUsersWithListInput: %@ ", exception.name);
    NSLog(@"Reason: %@ ", exception.reason);
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**NSArray&lt;SWGUser&gt;***](SWGUser.md)| List of user object | [optional] 

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP reuqest headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **deleteUser**
> deleteUser($username)

Delete user

This can only be done by the logged in user.

### Example 
```objc
SWGConfiguration *apiConfig = [SWGConfiguration sharedConfig];
// Configure HTTP basic authorization (authentication scheme: test_http_basic)
[apiConfig setUsername:@"YOUR_USERNAME"];
[apiConfig setPassword:@"YOUR_PASSWORD"];


NSString* username = @"username_example"; // The name that needs to be deleted

@try
{ 
    SWGSWGUserApi *apiInstance = [[SWGUserApi alloc] init];

    // Delete user
    [apiInstance deleteUserWithUsername:username
              completionHandler: ^(NSError* error)) {
                            if (error) {
                                NSLog(@"Error: %@", error);
                            }
                        }];
}
@catch (NSException *exception)
{
    NSLog(@"Exception when calling SWGUserApi->deleteUser: %@ ", exception.name);
    NSLog(@"Reason: %@ ", exception.reason);
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **username** | **NSString***| The name that needs to be deleted | 

### Return type

void (empty response body)

### Authorization

[test_http_basic](../README.md#test_http_basic)

### HTTP reuqest headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getUserByName**
> SWGUser* getUserByName($username)

Get user by user name



### Example 
```objc

NSString* username = @"username_example"; // The name that needs to be fetched. Use user1 for testing.

@try
{ 
    SWGSWGUserApi *apiInstance = [[SWGUserApi alloc] init];

    // Get user by user name
    [apiInstance getUserByNameWithUsername:username
              completionHandler: ^(SWGUser* output, NSError* error)) {
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
    NSLog(@"Exception when calling SWGUserApi->getUserByName: %@ ", exception.name);
    NSLog(@"Reason: %@ ", exception.reason);
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **username** | **NSString***| The name that needs to be fetched. Use user1 for testing. | 

### Return type

[**SWGUser***](SWGUser.md)

### Authorization

No authorization required

### HTTP reuqest headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **loginUser**
> NSString* loginUser($username, $password)

Logs user into the system



### Example 
```objc

NSString* username = @"username_example"; // The user name for login
NSString* password = @"password_example"; // The password for login in clear text

@try
{ 
    SWGSWGUserApi *apiInstance = [[SWGUserApi alloc] init];

    // Logs user into the system
    [apiInstance loginUserWithUsername:username
    password:password
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
    NSLog(@"Exception when calling SWGUserApi->loginUser: %@ ", exception.name);
    NSLog(@"Reason: %@ ", exception.reason);
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **username** | **NSString***| The user name for login | [optional] 
 **password** | **NSString***| The password for login in clear text | [optional] 

### Return type

**NSString***

### Authorization

No authorization required

### HTTP reuqest headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **logoutUser**
> logoutUser()

Logs out current logged in user session



### Example 
```objc


@try
{ 
    SWGSWGUserApi *apiInstance = [[SWGUserApi alloc] init];

    // Logs out current logged in user session
    [apiInstance logoutUserWithCompletionHandler: 
              ^(NSError* error)) {
                            if (error) {
                                NSLog(@"Error: %@", error);
                            }
                        }];
}
@catch (NSException *exception)
{
    NSLog(@"Exception when calling SWGUserApi->logoutUser: %@ ", exception.name);
    NSLog(@"Reason: %@ ", exception.reason);
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP reuqest headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **updateUser**
> updateUser($username, $body)

Updated user

This can only be done by the logged in user.

### Example 
```objc

NSString* username = @"username_example"; // name that need to be deleted
SWGUser* body = SwaggerClient.SWGUser*(); // Updated user object

@try
{ 
    SWGSWGUserApi *apiInstance = [[SWGUserApi alloc] init];

    // Updated user
    [apiInstance updateUserWithUsername:username
    body:body
              completionHandler: ^(NSError* error)) {
                            if (error) {
                                NSLog(@"Error: %@", error);
                            }
                        }];
}
@catch (NSException *exception)
{
    NSLog(@"Exception when calling SWGUserApi->updateUser: %@ ", exception.name);
    NSLog(@"Reason: %@ ", exception.reason);
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **username** | **NSString***| name that need to be deleted | 
 **body** | [**SWGUser***](SWGUser*.md)| Updated user object | [optional] 

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP reuqest headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

