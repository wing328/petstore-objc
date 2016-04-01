# \SWGStoreApi

All URIs are relative to *http://petstore.swagger.io/v2*

Method | HTTP request | Description
------------- | ------------- | -------------
[**deleteOrder**](SWGStoreApi.md#deleteOrder) | **DELETE** /store/order/{orderId} | Delete purchase order by ID
[**findOrdersByStatus**](SWGStoreApi.md#findOrdersByStatus) | **GET** /store/findByStatus | Finds orders by status
[**getInventory**](SWGStoreApi.md#getInventory) | **GET** /store/inventory | Returns pet inventories by status
[**getInventoryInObject**](SWGStoreApi.md#getInventoryInObject) | **GET** /store/inventory?response=arbitrary_object | Fake endpoint to test arbitrary object return by &#39;Get inventory&#39;
[**getOrderById**](SWGStoreApi.md#getOrderById) | **GET** /store/order/{orderId} | Find purchase order by ID
[**placeOrder**](SWGStoreApi.md#placeOrder) | **POST** /store/order | Place an order for a pet


# **deleteOrder**
> deleteOrder($orderId)

Delete purchase order by ID

For valid response try integer IDs with value < 1000. Anything above 1000 or nonintegers will generate API errors

### Example 
```objc


NSString* *orderId = @"orderId_example"; // NSString* | ID of the order that needs to be deleted

@try
{ 
    SWGSWGStoreApi *apiInstance = [[SWGStoreApi alloc] init];

    // Delete purchase order by ID
    [apiInstance deleteOrderWithOrderId:orderId
              completionHandler: ^(NSError* error)) {
                            if (error) {
                                NSLog(@"Error: %@", error);
                            }
                        }];
}
@catch (NSException *exception)
{
    NSLog(@"Exception when calling SWGStoreApi->deleteOrder: %@ ", exception.name);
    NSLog(@"Reason: %@ ", exception.reason);
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **orderId** | **NSString***| ID of the order that needs to be deleted | 

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP reuqest headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **findOrdersByStatus**
> NSArray<SWGOrder>* findOrdersByStatus($status)

Finds orders by status

A single status value can be provided as a string

### Example 
```objc

SWGConfiguration *apiConfig = [SWGConfiguration sharedConfig];

// Configure API key authorization: (authentication scheme: test_api_client_id)
[apiConfig setApiKey:@"YOUR_API_KEY" forApiKeyIdentifier:@"x-test_api_client_id"];
// Uncomment below to setup prefix (e.g. BEARER) for API key, if needed
//[apiConfig setApiKeyPrefix:@"BEARER" forApiKeyIdentifier:@"x-test_api_client_id"];

// Configure API key authorization: (authentication scheme: test_api_client_secret)
[apiConfig setApiKey:@"YOUR_API_KEY" forApiKeyIdentifier:@"x-test_api_client_secret"];
// Uncomment below to setup prefix (e.g. BEARER) for API key, if needed
//[apiConfig setApiKeyPrefix:@"BEARER" forApiKeyIdentifier:@"x-test_api_client_secret"];


NSString* *status = @"placed"; // NSString* | Status value that needs to be considered for query (default to placed)

@try
{ 
    SWGSWGStoreApi *apiInstance = [[SWGStoreApi alloc] init];

    // Finds orders by status
    [apiInstance findOrdersByStatusWithStatus:status
              completionHandler: ^(NSArray<SWGOrder>* output, NSError* error)) {
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
    NSLog(@"Exception when calling SWGStoreApi->findOrdersByStatus: %@ ", exception.name);
    NSLog(@"Reason: %@ ", exception.reason);
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **status** | **NSString***| Status value that needs to be considered for query | [optional] [default to placed]

### Return type

[**NSArray<SWGOrder>***](SWGOrder.md)

### Authorization

[test_api_client_id](../README.md#test_api_client_id), [test_api_client_secret](../README.md#test_api_client_secret)

### HTTP reuqest headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getInventory**
> NSDictionary* /* NSString, NSNumber */ getInventory()

Returns pet inventories by status

Returns a map of status codes to quantities

### Example 
```objc

SWGConfiguration *apiConfig = [SWGConfiguration sharedConfig];

// Configure API key authorization: (authentication scheme: api_key)
[apiConfig setApiKey:@"YOUR_API_KEY" forApiKeyIdentifier:@"api_key"];
// Uncomment below to setup prefix (e.g. BEARER) for API key, if needed
//[apiConfig setApiKeyPrefix:@"BEARER" forApiKeyIdentifier:@"api_key"];



@try
{ 
    SWGSWGStoreApi *apiInstance = [[SWGStoreApi alloc] init];

    // Returns pet inventories by status
    [apiInstance getInventoryWithCompletionHandler: 
              ^(NSDictionary* /* NSString, NSNumber */ output, NSError* error)) {
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
    NSLog(@"Exception when calling SWGStoreApi->getInventory: %@ ", exception.name);
    NSLog(@"Reason: %@ ", exception.reason);
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**NSDictionary* /* NSString, NSNumber */**](NSDictionary.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP reuqest headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getInventoryInObject**
> NSObject* getInventoryInObject()

Fake endpoint to test arbitrary object return by 'Get inventory'

Returns an arbitrary object which is actually a map of status codes to quantities

### Example 
```objc

SWGConfiguration *apiConfig = [SWGConfiguration sharedConfig];

// Configure API key authorization: (authentication scheme: api_key)
[apiConfig setApiKey:@"YOUR_API_KEY" forApiKeyIdentifier:@"api_key"];
// Uncomment below to setup prefix (e.g. BEARER) for API key, if needed
//[apiConfig setApiKeyPrefix:@"BEARER" forApiKeyIdentifier:@"api_key"];



@try
{ 
    SWGSWGStoreApi *apiInstance = [[SWGStoreApi alloc] init];

    // Fake endpoint to test arbitrary object return by 'Get inventory'
    [apiInstance getInventoryInObjectWithCompletionHandler: 
              ^(NSObject* output, NSError* error)) {
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
    NSLog(@"Exception when calling SWGStoreApi->getInventoryInObject: %@ ", exception.name);
    NSLog(@"Reason: %@ ", exception.reason);
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

**NSObject***

### Authorization

[api_key](../README.md#api_key)

### HTTP reuqest headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getOrderById**
> SWGOrder* getOrderById($orderId)

Find purchase order by ID

For valid response try integer IDs with value <= 5 or > 10. Other values will generated exceptions

### Example 
```objc

SWGConfiguration *apiConfig = [SWGConfiguration sharedConfig];

// Configure API key authorization: (authentication scheme: test_api_key_header)
[apiConfig setApiKey:@"YOUR_API_KEY" forApiKeyIdentifier:@"test_api_key_header"];
// Uncomment below to setup prefix (e.g. BEARER) for API key, if needed
//[apiConfig setApiKeyPrefix:@"BEARER" forApiKeyIdentifier:@"test_api_key_header"];

// Configure API key authorization: (authentication scheme: test_api_key_query)
[apiConfig setApiKey:@"YOUR_API_KEY" forApiKeyIdentifier:@"test_api_key_query"];
// Uncomment below to setup prefix (e.g. BEARER) for API key, if needed
//[apiConfig setApiKeyPrefix:@"BEARER" forApiKeyIdentifier:@"test_api_key_query"];


NSString* *orderId = @"orderId_example"; // NSString* | ID of pet that needs to be fetched

@try
{ 
    SWGSWGStoreApi *apiInstance = [[SWGStoreApi alloc] init];

    // Find purchase order by ID
    [apiInstance getOrderByIdWithOrderId:orderId
              completionHandler: ^(SWGOrder* output, NSError* error)) {
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
    NSLog(@"Exception when calling SWGStoreApi->getOrderById: %@ ", exception.name);
    NSLog(@"Reason: %@ ", exception.reason);
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **orderId** | **NSString***| ID of pet that needs to be fetched | 

### Return type

[**SWGOrder***](SWGOrder.md)

### Authorization

[test_api_key_header](../README.md#test_api_key_header), [test_api_key_query](../README.md#test_api_key_query)

### HTTP reuqest headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **placeOrder**
> SWGOrder* placeOrder($body)

Place an order for a pet



### Example 
```objc

SWGConfiguration *apiConfig = [SWGConfiguration sharedConfig];

// Configure API key authorization: (authentication scheme: test_api_client_id)
[apiConfig setApiKey:@"YOUR_API_KEY" forApiKeyIdentifier:@"x-test_api_client_id"];
// Uncomment below to setup prefix (e.g. BEARER) for API key, if needed
//[apiConfig setApiKeyPrefix:@"BEARER" forApiKeyIdentifier:@"x-test_api_client_id"];

// Configure API key authorization: (authentication scheme: test_api_client_secret)
[apiConfig setApiKey:@"YOUR_API_KEY" forApiKeyIdentifier:@"x-test_api_client_secret"];
// Uncomment below to setup prefix (e.g. BEARER) for API key, if needed
//[apiConfig setApiKeyPrefix:@"BEARER" forApiKeyIdentifier:@"x-test_api_client_secret"];


SWGOrder* *body = SwaggerClient.SWGOrder*(); // SWGOrder* | order placed for purchasing the pet

@try
{ 
    SWGSWGStoreApi *apiInstance = [[SWGStoreApi alloc] init];

    // Place an order for a pet
    [apiInstance placeOrderWithBody:body
              completionHandler: ^(SWGOrder* output, NSError* error)) {
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
    NSLog(@"Exception when calling SWGStoreApi->placeOrder: %@ ", exception.name);
    NSLog(@"Reason: %@ ", exception.reason);
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**SWGOrder***](SWGOrder*.md)| order placed for purchasing the pet | [optional] 

### Return type

[**SWGOrder***](SWGOrder.md)

### Authorization

[test_api_client_id](../README.md#test_api_client_id), [test_api_client_secret](../README.md#test_api_client_secret)

### HTTP reuqest headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

