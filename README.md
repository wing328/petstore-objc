# SwaggerClient

This is a sample server Petstore server.  You can find out more about Swagger at <a href=\"http://swagger.io\">http://swagger.io</a> or on irc.freenode.net, #swagger.  For this sample, you can use the api key \"special-key\" to test the authorization filters

This ObjC package is automatically generated by the [Swagger Codegen](https://github.com/swagger-api/swagger-codegen) project:

- API version: 1.0.0
- Package version: 
- Build date: 2016-04-01T16:49:20.940+08:00
- Build package: class io.swagger.codegen.languages.ObjcClientCodegen

## Requirements

The SDK requires [**ARC (Automatic Reference Counting)**](http://stackoverflow.com/questions/7778356/how-to-enable-disable-automatic-reference-counting) to be enabled in the Xcode project.

## Installation & Usage
### Install from Github using [CocoaPods](https://cocoapods.org/)

Add the following to the Podfile:

```ruby
pod 'SwaggerClient', :git => 'https://github.com/wing328/petstore-objc.git'
```

To specify a particular branch, append `, :branch => 'branch-name-here'`

To specify a particular commit, append `, :commit => '11aa22'`

### Install from local path using [CocoaPods](https://cocoapods.org/)

Put the SDK under your project folder (e.g. ./vendor/SwaggerClient) and then add the following to the Podfile:

```ruby
pod 'SwaggerClient', :path => './vendor/SwaggerClient'
```

### Usage

Import the following:
```objc
#import <SwaggerClient/SWGApiClient.h>
#import <SwaggerClient/SWGConfiguration.h>
// load models
#import <SwaggerClient/SWGCategory>
#import <SwaggerClient/SWGInlineResponse200>
#import <SwaggerClient/SWGName>
#import <SwaggerClient/SWGOrder>
#import <SwaggerClient/SWGPet>
#import <SwaggerClient/SWGReturn>
#import <SwaggerClient/SWGSpecialModelName_>
#import <SwaggerClient/SWGTag>
#import <SwaggerClient/SWGUser>
// load API classes for accessing endpoints
#import <SwaggerClient/SWGPetApi>
#import <SwaggerClient/SWGStoreApi>
#import <SwaggerClient/SWGUserApi>

```

## Recommendation

It's recommended to create an instance of ApiClient per thread in a multi-threaded environment to avoid any potential issue.

## Getting Started

Please follow the [installation procedure](#installation--usage) and then run the following:

```objc

SWGConfiguration *apiConfig = [SWGConfiguration sharedConfig];

// Configure OAuth2 access token for authorization: (authentication scheme: petstore_auth)
[apiConfig setAccessToken:@"YOUR_ACCESS_TOKEN"];


SWGPet* *body = [[SWGPet alloc] init]; // Pet object that needs to be added to the store

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

## Documentation for API Endpoints

All URIs are relative to *http://petstore.swagger.io/v2*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*SWGPetApi* | [**addPet**](docs/SWGPetApi.md#addpet) | **POST** /pet | Add a new pet to the store
*SWGPetApi* | [**addPetUsingByteArray**](docs/SWGPetApi.md#addpetusingbytearray) | **POST** /pet?testing_byte_array=true | Fake endpoint to test byte array in body parameter for adding a new pet to the store
*SWGPetApi* | [**deletePet**](docs/SWGPetApi.md#deletepet) | **DELETE** /pet/{petId} | Deletes a pet
*SWGPetApi* | [**findPetsByStatus**](docs/SWGPetApi.md#findpetsbystatus) | **GET** /pet/findByStatus | Finds Pets by status
*SWGPetApi* | [**findPetsByTags**](docs/SWGPetApi.md#findpetsbytags) | **GET** /pet/findByTags | Finds Pets by tags
*SWGPetApi* | [**getPetById**](docs/SWGPetApi.md#getpetbyid) | **GET** /pet/{petId} | Find pet by ID
*SWGPetApi* | [**getPetByIdInObject**](docs/SWGPetApi.md#getpetbyidinobject) | **GET** /pet/{petId}?response=inline_arbitrary_object | Fake endpoint to test inline arbitrary object return by &#39;Find pet by ID&#39;
*SWGPetApi* | [**petPetIdtestingByteArraytrueGet**](docs/SWGPetApi.md#petpetidtestingbytearraytrueget) | **GET** /pet/{petId}?testing_byte_array=true | Fake endpoint to test byte array return by &#39;Find pet by ID&#39;
*SWGPetApi* | [**updatePet**](docs/SWGPetApi.md#updatepet) | **PUT** /pet | Update an existing pet
*SWGPetApi* | [**updatePetWithForm**](docs/SWGPetApi.md#updatepetwithform) | **POST** /pet/{petId} | Updates a pet in the store with form data
*SWGPetApi* | [**uploadFile**](docs/SWGPetApi.md#uploadfile) | **POST** /pet/{petId}/uploadImage | uploads an image
*SWGStoreApi* | [**deleteOrder**](docs/SWGStoreApi.md#deleteorder) | **DELETE** /store/order/{orderId} | Delete purchase order by ID
*SWGStoreApi* | [**findOrdersByStatus**](docs/SWGStoreApi.md#findordersbystatus) | **GET** /store/findByStatus | Finds orders by status
*SWGStoreApi* | [**getInventory**](docs/SWGStoreApi.md#getinventory) | **GET** /store/inventory | Returns pet inventories by status
*SWGStoreApi* | [**getInventoryInObject**](docs/SWGStoreApi.md#getinventoryinobject) | **GET** /store/inventory?response=arbitrary_object | Fake endpoint to test arbitrary object return by &#39;Get inventory&#39;
*SWGStoreApi* | [**getOrderById**](docs/SWGStoreApi.md#getorderbyid) | **GET** /store/order/{orderId} | Find purchase order by ID
*SWGStoreApi* | [**placeOrder**](docs/SWGStoreApi.md#placeorder) | **POST** /store/order | Place an order for a pet
*SWGUserApi* | [**createUser**](docs/SWGUserApi.md#createuser) | **POST** /user | Create user
*SWGUserApi* | [**createUsersWithArrayInput**](docs/SWGUserApi.md#createuserswitharrayinput) | **POST** /user/createWithArray | Creates list of users with given input array
*SWGUserApi* | [**createUsersWithListInput**](docs/SWGUserApi.md#createuserswithlistinput) | **POST** /user/createWithList | Creates list of users with given input array
*SWGUserApi* | [**deleteUser**](docs/SWGUserApi.md#deleteuser) | **DELETE** /user/{username} | Delete user
*SWGUserApi* | [**getUserByName**](docs/SWGUserApi.md#getuserbyname) | **GET** /user/{username} | Get user by user name
*SWGUserApi* | [**loginUser**](docs/SWGUserApi.md#loginuser) | **GET** /user/login | Logs user into the system
*SWGUserApi* | [**logoutUser**](docs/SWGUserApi.md#logoutuser) | **GET** /user/logout | Logs out current logged in user session
*SWGUserApi* | [**updateUser**](docs/SWGUserApi.md#updateuser) | **PUT** /user/{username} | Updated user


## Documentation For Models

 - [SWGCategory](docs/SWGCategory.md)
 - [SWGInlineResponse200](docs/SWGInlineResponse200.md)
 - [SWGName](docs/SWGName.md)
 - [SWGOrder](docs/SWGOrder.md)
 - [SWGPet](docs/SWGPet.md)
 - [SWGReturn](docs/SWGReturn.md)
 - [SWGSpecialModelName_](docs/SWGSpecialModelName_.md)
 - [SWGTag](docs/SWGTag.md)
 - [SWGUser](docs/SWGUser.md)


## Documentation For Authorization


## test_api_key_header

- **Type**: API key
- **API key parameter name**: test_api_key_header
- **Location**: HTTP header

## api_key

- **Type**: API key
- **API key parameter name**: api_key
- **Location**: HTTP header

## test_http_basic

- **Type**: HTTP basic authentication

## test_api_client_secret

- **Type**: API key
- **API key parameter name**: x-test_api_client_secret
- **Location**: HTTP header

## test_api_client_id

- **Type**: API key
- **API key parameter name**: x-test_api_client_id
- **Location**: HTTP header

## test_api_key_query

- **Type**: API key
- **API key parameter name**: test_api_key_query
- **Location**: URL query string

## petstore_auth

- **Type**: OAuth
- **Flow**: implicit
- **Authorizatoin URL**: http://petstore.swagger.io/api/oauth/dialog
- **Scopes**: 
 - **write:pets**: modify pets in your account
 - **read:pets**: read your pets


## Author

apiteam@swagger.io


