# Cloudmersive.APIClient.NETCore.Spam.Api.SpamDetectionApi

All URIs are relative to *https://api.cloudmersive.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**SpamDetectFileAdvancedPost**](SpamDetectionApi.md#spamdetectfileadvancedpost) | **POST** /spam/detect/file/advanced | Perform advanced AI spam detection and classification against input text file.
[**SpamDetectFilePost**](SpamDetectionApi.md#spamdetectfilepost) | **POST** /spam/detect/file | Perform AI spam detection and classification on an input image or document (PDF or DOCX)
[**SpamDetectFormSubmissionAdvancedPost**](SpamDetectionApi.md#spamdetectformsubmissionadvancedpost) | **POST** /spam/detect/form-submission/advanced | Perform advanced AI spam detection and classification against a form submission
[**SpamDetectTextStringAdvancedPost**](SpamDetectionApi.md#spamdetecttextstringadvancedpost) | **POST** /spam/detect/text-string/advanced | Perform advanced AI spam detection and classification against input text string
[**SpamDetectTextStringPost**](SpamDetectionApi.md#spamdetecttextstringpost) | **POST** /spam/detect/text-string | Perform AI spam detection and classification against input text string


<a name="spamdetectfileadvancedpost"></a>
# **SpamDetectFileAdvancedPost**
> SpamDetectionAdvancedResponse SpamDetectFileAdvancedPost (string model = null, string preprocessing = null, bool? allowPhishing = null, bool? allowUnsolicitedSales = null, bool? allowPromotionalContent = null, string customPolicyId = null, System.IO.Stream inputFile = null)

Perform advanced AI spam detection and classification against input text file.

Analyzes input content as well as embedded URLs with AI deep learning to detect spam, phishing and other unsafe content.  Uses 25-100 API calls depending on model selected.  Supported file formats include DOCX, PDF, XLSX, PPTX, EML, MSG, JPG, PNG and WEBP.

### Example
```csharp
using System;
using System.Diagnostics;
using Cloudmersive.APIClient.NETCore.Spam.Api;
using Cloudmersive.APIClient.NETCore.Spam.Client;
using Cloudmersive.APIClient.NETCore.Spam.Model;

namespace Example
{
    public class SpamDetectFileAdvancedPostExample
    {
        public void main()
        {
            // Configure API key authorization: Apikey
            Configuration.Default.AddApiKey("Apikey", "YOUR_API_KEY");
            // Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
            // Configuration.Default.AddApiKeyPrefix("Apikey", "Bearer");

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

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **model** | **string**| Optional: Specify which AI model to use.  Possible choices are Normal and Advanced.  Default is Advanced. | [optional] [default to Advanced]
 **preprocessing** | **string**| Optional: Specify which preprocessing to Use.  Possible choices are None, Compatability and Auto.  Default is Auto. | [optional] [default to Auto]
 **allowPhishing** | **bool?**| True if phishing should be allowed, false otherwise | [optional] [default to false]
 **allowUnsolicitedSales** | **bool?**| True if unsolicited sales should be allowed, false otherwise | [optional] [default to false]
 **allowPromotionalContent** | **bool?**| True if promotional content should be allowed, false otherwise | [optional] [default to true]
 **customPolicyId** | **string**| Apply a Custom Policy for Spam Enforcement by providing the ID; to create a Custom Policy, navigate to the Cloudmersive Management Portal and select Custom Policies.  Requires Managed Instance or Private Cloud | [optional] 
 **inputFile** | **System.IO.Stream**|  | [optional] 

### Return type

[**SpamDetectionAdvancedResponse**](SpamDetectionAdvancedResponse.md)

### Authorization

[Apikey](../README.md#Apikey)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a name="spamdetectfilepost"></a>
# **SpamDetectFilePost**
> SpamDetectionResponse SpamDetectFilePost (string model = null, System.IO.Stream inputFile = null)

Perform AI spam detection and classification on an input image or document (PDF or DOCX)

Analyzes input content as well as embedded URLs with AI deep learnign to detect spam, phishing and other unsafe content.  Uses 100-125 API calls depending on model selected.  Supported file formats include DOCX, PDF, XLSX, PPTX, EML, MSG, JPG, PNG and WEBP.

### Example
```csharp
using System;
using System.Diagnostics;
using Cloudmersive.APIClient.NETCore.Spam.Api;
using Cloudmersive.APIClient.NETCore.Spam.Client;
using Cloudmersive.APIClient.NETCore.Spam.Model;

namespace Example
{
    public class SpamDetectFilePostExample
    {
        public void main()
        {
            // Configure API key authorization: Apikey
            Configuration.Default.AddApiKey("Apikey", "YOUR_API_KEY");
            // Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
            // Configuration.Default.AddApiKeyPrefix("Apikey", "Bearer");

            var apiInstance = new SpamDetectionApi();
            var model = model_example;  // string | Model to use; default setting is Advanced (optional)  (default to Advanced)
            var inputFile = new System.IO.Stream(); // System.IO.Stream |  (optional) 

            try
            {
                // Perform AI spam detection and classification on an input image or document (PDF or DOCX)
                SpamDetectionResponse result = apiInstance.SpamDetectFilePost(model, inputFile);
                Debug.WriteLine(result);
            }
            catch (Exception e)
            {
                Debug.Print("Exception when calling SpamDetectionApi.SpamDetectFilePost: " + e.Message );
            }
        }
    }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **model** | **string**| Model to use; default setting is Advanced | [optional] [default to Advanced]
 **inputFile** | **System.IO.Stream**|  | [optional] 

### Return type

[**SpamDetectionResponse**](SpamDetectionResponse.md)

### Authorization

[Apikey](../README.md#Apikey)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a name="spamdetectformsubmissionadvancedpost"></a>
# **SpamDetectFormSubmissionAdvancedPost**
> SpamDetectionFormSubmissionAdvancedResponse SpamDetectFormSubmissionAdvancedPost (SpamDetectionAdvancedFormSubmissionRequest body = null)

Perform advanced AI spam detection and classification against a form submission

Analyzes form input content as well as embedded URLs with AI deep learnign to detect spam, phishing and other unsafe content.  Uses 25-100 API calls depending on model selected.

### Example
```csharp
using System;
using System.Diagnostics;
using Cloudmersive.APIClient.NETCore.Spam.Api;
using Cloudmersive.APIClient.NETCore.Spam.Client;
using Cloudmersive.APIClient.NETCore.Spam.Model;

namespace Example
{
    public class SpamDetectFormSubmissionAdvancedPostExample
    {
        public void main()
        {
            // Configure API key authorization: Apikey
            Configuration.Default.AddApiKey("Apikey", "YOUR_API_KEY");
            // Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
            // Configuration.Default.AddApiKeyPrefix("Apikey", "Bearer");

            var apiInstance = new SpamDetectionApi();
            var body = new SpamDetectionAdvancedFormSubmissionRequest(); // SpamDetectionAdvancedFormSubmissionRequest | Spam detection request (optional) 

            try
            {
                // Perform advanced AI spam detection and classification against a form submission
                SpamDetectionFormSubmissionAdvancedResponse result = apiInstance.SpamDetectFormSubmissionAdvancedPost(body);
                Debug.WriteLine(result);
            }
            catch (Exception e)
            {
                Debug.Print("Exception when calling SpamDetectionApi.SpamDetectFormSubmissionAdvancedPost: " + e.Message );
            }
        }
    }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**SpamDetectionAdvancedFormSubmissionRequest**](SpamDetectionAdvancedFormSubmissionRequest.md)| Spam detection request | [optional] 

### Return type

[**SpamDetectionFormSubmissionAdvancedResponse**](SpamDetectionFormSubmissionAdvancedResponse.md)

### Authorization

[Apikey](../README.md#Apikey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a name="spamdetecttextstringadvancedpost"></a>
# **SpamDetectTextStringAdvancedPost**
> SpamDetectionAdvancedResponse SpamDetectTextStringAdvancedPost (SpamDetectionAdvancedRequest body = null)

Perform advanced AI spam detection and classification against input text string

Analyzes input content as well as embedded URLs with AI deep learnign to detect spam, phishing and other unsafe content.  Uses 25-100 API calls depending on model selected.

### Example
```csharp
using System;
using System.Diagnostics;
using Cloudmersive.APIClient.NETCore.Spam.Api;
using Cloudmersive.APIClient.NETCore.Spam.Client;
using Cloudmersive.APIClient.NETCore.Spam.Model;

namespace Example
{
    public class SpamDetectTextStringAdvancedPostExample
    {
        public void main()
        {
            // Configure API key authorization: Apikey
            Configuration.Default.AddApiKey("Apikey", "YOUR_API_KEY");
            // Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
            // Configuration.Default.AddApiKeyPrefix("Apikey", "Bearer");

            var apiInstance = new SpamDetectionApi();
            var body = new SpamDetectionAdvancedRequest(); // SpamDetectionAdvancedRequest | Spam detection request (optional) 

            try
            {
                // Perform advanced AI spam detection and classification against input text string
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

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**SpamDetectionAdvancedRequest**](SpamDetectionAdvancedRequest.md)| Spam detection request | [optional] 

### Return type

[**SpamDetectionAdvancedResponse**](SpamDetectionAdvancedResponse.md)

### Authorization

[Apikey](../README.md#Apikey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a name="spamdetecttextstringpost"></a>
# **SpamDetectTextStringPost**
> SpamDetectionResponse SpamDetectTextStringPost (SpamDetectionRequest body = null)

Perform AI spam detection and classification against input text string

Analyzes input content as well as embedded URLs with AI deep learnign to detect spam, phishing and other unsafe content.  Uses 25-75 API calls depending on model selected.

### Example
```csharp
using System;
using System.Diagnostics;
using Cloudmersive.APIClient.NETCore.Spam.Api;
using Cloudmersive.APIClient.NETCore.Spam.Client;
using Cloudmersive.APIClient.NETCore.Spam.Model;

namespace Example
{
    public class SpamDetectTextStringPostExample
    {
        public void main()
        {
            // Configure API key authorization: Apikey
            Configuration.Default.AddApiKey("Apikey", "YOUR_API_KEY");
            // Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
            // Configuration.Default.AddApiKeyPrefix("Apikey", "Bearer");

            var apiInstance = new SpamDetectionApi();
            var body = new SpamDetectionRequest(); // SpamDetectionRequest | Spam detection request (optional) 

            try
            {
                // Perform AI spam detection and classification against input text string
                SpamDetectionResponse result = apiInstance.SpamDetectTextStringPost(body);
                Debug.WriteLine(result);
            }
            catch (Exception e)
            {
                Debug.Print("Exception when calling SpamDetectionApi.SpamDetectTextStringPost: " + e.Message );
            }
        }
    }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**SpamDetectionRequest**](SpamDetectionRequest.md)| Spam detection request | [optional] 

### Return type

[**SpamDetectionResponse**](SpamDetectionResponse.md)

### Authorization

[Apikey](../README.md#Apikey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

