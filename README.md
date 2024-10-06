# Cloudmersive.APIClient.NETCore.Spam - the C# library for the phishingapi

Easily and directly scan and block phishing security threats.

This C# SDK is for the [Cloudmersive Spam Detection API](https://www.cloudmersive.com/spam-api):

- API version: v1
- SDK version: 1.0.1
- Build package: io.swagger.codegen.languages.CSharpClientCodegen

<a name="frameworks-supported"></a>
## Frameworks supported
- .NET Core >=1.0
- .NET Framework >=4.6
- Mono/Xamarin >=vNext
- UWP >=10.0

<a name="dependencies"></a>
## Dependencies
- FubarCoder.RestSharp.Portable.Core >=4.0.7
- FubarCoder.RestSharp.Portable.HttpClient >=4.0.7
- Newtonsoft.Json >=10.0.3

<a name="installation"></a>
## Installation
Generate the DLL using your preferred tool

Then include the DLL (under the `bin` folder) in the C# project, and use the namespaces:
```csharp
using Cloudmersive.APIClient.NETCore.Spam.Api;
using Cloudmersive.APIClient.NETCore.Spam.Client;
using Cloudmersive.APIClient.NETCore.Spam.Model;
```
<a name="getting-started"></a>
## Getting Started

```csharp
using System;
using System.Diagnostics;
using Cloudmersive.APIClient.NETCore.Spam.Api;
using Cloudmersive.APIClient.NETCore.Spam.Client;
using Cloudmersive.APIClient.NETCore.Spam.Model;

namespace Example
{
    public class Example
    {
        public void main()
        {

            // Configure API key authorization: Apikey
            Configuration.Default.ApiKey.Add("Apikey", "YOUR_API_KEY");
            // Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
            // Configuration.Default.ApiKeyPrefix.Add("Apikey", "Bearer");

            var apiInstance = new SpamDetectionApi();
            var body = new SpamDetectionAdvancedRequest(); // SpamDetectionAdvancedRequest |  (optional) 

            try
            {
                SpamDetectionAdvancedResponse result = apiInstance.SpamDetectTextStringAdvancedPost(body);
                Debug.WriteLine(result);
            }
            catch (Exception e)
            {
                Debug.Print("Exception when calling SpamDetectionApi.SpamDetectTextStringAdvancedPost: " + e.Message );
            }

        }
    }
}
```

<a name="documentation-for-api-endpoints"></a>
## Documentation for API Endpoints

All URIs are relative to *https://localhost*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*SpamDetectionApi* | [**SpamDetectTextStringAdvancedPost**](docs/SpamDetectionApi.md#spamdetecttextstringadvancedpost) | **POST** /spam/detect/text-string/advanced | 


<a name="documentation-for-models"></a>
## Documentation for Models

 - [Model.SpamDetectionAdvancedRequest](docs/SpamDetectionAdvancedRequest.md)
 - [Model.SpamDetectionAdvancedResponse](docs/SpamDetectionAdvancedResponse.md)


<a name="documentation-for-authorization"></a>
## Documentation for Authorization

<a name="Apikey"></a>
### Apikey

- **Type**: API key
- **API key parameter name**: Apikey
- **Location**: HTTP header

