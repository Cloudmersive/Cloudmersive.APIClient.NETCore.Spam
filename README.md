# Cloudmersive.APIClient.NETCore.Spam - the C# library for the spamapi

Easily and directly scan and block spam security threats in input.

This C# SDK is for the [Cloudmersive Spam Detection API](https://www.cloudmersive.com/spam-api):

- API version: v1
- SDK version: 2.0.6
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
            var model = model_example;  // string | Optional: Specify which AI model to use.  Possible choices are Normal and Advanced.  Default is Advanced. (optional)  (default to Advanced)
            var preprocessing = preprocessing_example;  // string | Optional: Specify which preprocessing to Use.  Possible choices are None, Compatability and Auto.  Default is Auto. (optional)  (default to Auto)
            var allowPhishing = true;  // bool? | True if phishing should be allowed, false otherwise (optional)  (default to false)
            var allowUnsolicitedSales = true;  // bool? | True if unsolicited sales should be allowed, false otherwise (optional)  (default to false)
            var allowPromotionalContent = true;  // bool? | True if promotional content should be allowed, false otherwise (optional)  (default to true)
            var customPolicyId = customPolicyId_example;  // string | Apply a Custom Policy for Spam Enforcement by providing the ID; to create a Custom Policy, navigate to the Cloudmersive Management Portal and select Custom Policies.  Requires Managed Instance or Private Cloud (optional) 
            var inputFile = new System.IO.Stream(); // System.IO.Stream |  (optional) 

            try
            {
                // Perform advanced AI spam detection and classification against input text file.
                SpamDetectionAdvancedResponse result = apiInstance.SpamDetectFileAdvancedPost(model, preprocessing, allowPhishing, allowUnsolicitedSales, allowPromotionalContent, customPolicyId, inputFile);
                Debug.WriteLine(result);
            }
            catch (Exception e)
            {
                Debug.Print("Exception when calling SpamDetectionApi.SpamDetectFileAdvancedPost: " + e.Message );
            }

        }
    }
}
```

<a name="documentation-for-api-endpoints"></a>
## Documentation for API Endpoints

All URIs are relative to *https://api.cloudmersive.com*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*SpamDetectionApi* | [**SpamDetectFileAdvancedPost**](docs/SpamDetectionApi.md#spamdetectfileadvancedpost) | **POST** /spam/detect/file/advanced | Perform advanced AI spam detection and classification against input text file.
*SpamDetectionApi* | [**SpamDetectFilePost**](docs/SpamDetectionApi.md#spamdetectfilepost) | **POST** /spam/detect/file | Perform AI spam detection and classification on an input image or document (PDF or DOCX)
*SpamDetectionApi* | [**SpamDetectFormSubmissionAdvancedPost**](docs/SpamDetectionApi.md#spamdetectformsubmissionadvancedpost) | **POST** /spam/detect/form-submission/advanced | Perform advanced AI spam detection and classification against a form submission
*SpamDetectionApi* | [**SpamDetectTextStringAdvancedPost**](docs/SpamDetectionApi.md#spamdetecttextstringadvancedpost) | **POST** /spam/detect/text-string/advanced | Perform advanced AI spam detection and classification against input text string
*SpamDetectionApi* | [**SpamDetectTextStringPost**](docs/SpamDetectionApi.md#spamdetecttextstringpost) | **POST** /spam/detect/text-string | Perform AI spam detection and classification against input text string


<a name="documentation-for-models"></a>
## Documentation for Models

 - [Model.SpamDetectionAdvancedFormField](docs/SpamDetectionAdvancedFormField.md)
 - [Model.SpamDetectionAdvancedFormSubmissionRequest](docs/SpamDetectionAdvancedFormSubmissionRequest.md)
 - [Model.SpamDetectionAdvancedRequest](docs/SpamDetectionAdvancedRequest.md)
 - [Model.SpamDetectionAdvancedResponse](docs/SpamDetectionAdvancedResponse.md)
 - [Model.SpamDetectionFormSubmissionAdvancedResponse](docs/SpamDetectionFormSubmissionAdvancedResponse.md)
 - [Model.SpamDetectionRequest](docs/SpamDetectionRequest.md)
 - [Model.SpamDetectionResponse](docs/SpamDetectionResponse.md)


<a name="documentation-for-authorization"></a>
## Documentation for Authorization

<a name="Apikey"></a>
### Apikey

- **Type**: API key
- **API key parameter name**: Apikey
- **Location**: HTTP header

