# Cloudmersive.APIClient.NET.FraudDetection.Api.FraudDetectionApi

All URIs are relative to *https://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**DocumentDetectFraud**](FraudDetectionApi.md#documentdetectfraud) | **POST** /fraud-ai/detection/document | AI Fraud Detection for Documents
[**DocumentDetectFraudAdvanced**](FraudDetectionApi.md#documentdetectfraudadvanced) | **POST** /fraud-ai/detection/document/advanced | Advanced AI Fraud Detection for Documents


<a name="documentdetectfraud"></a>
# **DocumentDetectFraud**
> FraudDetectionResult DocumentDetectFraud (System.IO.Stream inputFile = null)

AI Fraud Detection for Documents

Perform fraud detection and classification on input document and user context.  Input document formats supported include DOCX, PDF, PNG and JPG.

### Example
```csharp
using System;
using System.Diagnostics;
using Cloudmersive.APIClient.NET.FraudDetection.Api;
using Cloudmersive.APIClient.NET.FraudDetection.Client;
using Cloudmersive.APIClient.NET.FraudDetection.Model;

namespace Example
{
    public class DocumentDetectFraudExample
    {
        public void main()
        {
            // Configure API key authorization: Apikey
            Configuration.Default.AddApiKey("Apikey", "YOUR_API_KEY");
            // Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
            // Configuration.Default.AddApiKeyPrefix("Apikey", "Bearer");

            var apiInstance = new FraudDetectionApi();
            var inputFile = new System.IO.Stream(); // System.IO.Stream | Input document, or photos of a document, to perform fraud detection on (optional) 

            try
            {
                // AI Fraud Detection for Documents
                FraudDetectionResult result = apiInstance.DocumentDetectFraud(inputFile);
                Debug.WriteLine(result);
            }
            catch (Exception e)
            {
                Debug.Print("Exception when calling FraudDetectionApi.DocumentDetectFraud: " + e.Message );
            }
        }
    }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **inputFile** | **System.IO.Stream**| Input document, or photos of a document, to perform fraud detection on | [optional] 

### Return type

[**FraudDetectionResult**](FraudDetectionResult.md)

### Authorization

[Apikey](../README.md#Apikey)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a name="documentdetectfraudadvanced"></a>
# **DocumentDetectFraudAdvanced**
> AdvancedFraudDetectionResult DocumentDetectFraudAdvanced (string userEmailAddress = null, bool? userEmailAddressVerified = null, System.IO.Stream inputFile = null)

Advanced AI Fraud Detection for Documents

Perform advanced fraud detection and classification on input document and user context.  Input document formats supported include DOCX, PDF, PNG and JPG.

### Example
```csharp
using System;
using System.Diagnostics;
using Cloudmersive.APIClient.NET.FraudDetection.Api;
using Cloudmersive.APIClient.NET.FraudDetection.Client;
using Cloudmersive.APIClient.NET.FraudDetection.Model;

namespace Example
{
    public class DocumentDetectFraudAdvancedExample
    {
        public void main()
        {
            // Configure API key authorization: Apikey
            Configuration.Default.AddApiKey("Apikey", "YOUR_API_KEY");
            // Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
            // Configuration.Default.AddApiKeyPrefix("Apikey", "Bearer");

            var apiInstance = new FraudDetectionApi();
            var userEmailAddress = userEmailAddress_example;  // string | User email address for context (optional) (optional) 
            var userEmailAddressVerified = true;  // bool? | True if the user's email address was verified (optional) (optional) 
            var inputFile = new System.IO.Stream(); // System.IO.Stream | Input document, or photos of a document, to perform fraud detection on (optional) 

            try
            {
                // Advanced AI Fraud Detection for Documents
                AdvancedFraudDetectionResult result = apiInstance.DocumentDetectFraudAdvanced(userEmailAddress, userEmailAddressVerified, inputFile);
                Debug.WriteLine(result);
            }
            catch (Exception e)
            {
                Debug.Print("Exception when calling FraudDetectionApi.DocumentDetectFraudAdvanced: " + e.Message );
            }
        }
    }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **userEmailAddress** | **string**| User email address for context (optional) | [optional] 
 **userEmailAddressVerified** | **bool?**| True if the user&#39;s email address was verified (optional) | [optional] 
 **inputFile** | **System.IO.Stream**| Input document, or photos of a document, to perform fraud detection on | [optional] 

### Return type

[**AdvancedFraudDetectionResult**](AdvancedFraudDetectionResult.md)

### Authorization

[Apikey](../README.md#Apikey)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

