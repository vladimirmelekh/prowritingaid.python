# ProWritingAidSDK
Official ProWritingAid API Version 2

This Python package is automatically generated by the [Swagger Codegen](https://github.com/swagger-api/swagger-codegen) project:

- API version: v2
- Package version: 2.0.0
- Build package: io.swagger.codegen.languages.PythonClientCodegen
For more information, please visit [https://prowritingaid.com/en/App/API](https://prowritingaid.com/en/App/API)

## Requirements.

Python 2.7 and 3.4+

## Installation & Usage
### pip install

If the python package is hosted on Github, you can install directly from Github

```sh
pip install git+https://github.com/prowriting/prowritingaid.python.git
```
(you may need to run `pip` with root permission: `sudo pip install git+https://github.com/prowriting/prowritingaid.python.git`)

Then import the package:
```python
import ProWritingAidSDK 
```

### Setuptools

Install via [Setuptools](http://pypi.python.org/pypi/setuptools).

```sh
python setup.py install --user
```
(or `sudo python setup.py install` to install the package for all users)

Then import the package:
```python
import ProWritingAidSDK
```

## Getting Started

Please follow the [installation procedure](#installation--usage) and then run the following:

```python
from __future__ import print_function
import ProWritingAidSDK
from ProWritingAidSDK.rest import ApiException
from pprint import pprint

configuration = ProWritingAidSDK.Configuration()
configuration.host = 'https://api.prowritingaid.com'
configuration.api_key['licenseCode'] = 'YOUR_API_KEY'

# create an instance of the API class
api_instance = ProWritingAidSDK.ContextualThesaurusApi(ProWritingAidSDK.ApiClient('https://api.prowritingaid.com'))
task_id = 'task_id_example'  # str |

try:
    api_request = ProWritingAidSDK.ContextualThesaurusRequest("This is a sample text in English to test the sdk "
                                                              "thesaurus. This is a second paragraph in the document."
                                                              " This  is a new line.",
                                                              17,
                                                              20)
    api_response = api_instance.post(api_request)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling ContextualThesaurusApi->get: %s\n" % e)
```

## Documentation for API Endpoints

All URIs are relative to *https://localhost:5004*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*ContextualThesaurusApi* | [**get**](docs/ContextualThesaurusApi.md#get) | **GET** /api/async/contextualthesaurus/result/{taskId} | Tries to get the result of a request using the task id of the request
*ContextualThesaurusApi* | [**post**](docs/ContextualThesaurusApi.md#post) | **POST** /api/async/contextualthesaurus | Analyses text and returns contextual thesaurus entries
*HtmlApi* | [**get**](docs/HtmlApi.md#get) | **GET** /api/async/html/result/{taskId} | Tries to get the result of a request using the task id of the request
*HtmlApi* | [**post**](docs/HtmlApi.md#post) | **POST** /api/async/html | Analyses HTML and adds suggestion tags to it
*SummaryApi* | [**get**](docs/SummaryApi.md#get) | **GET** /api/async/summary/result/{taskId} | Tries to get the result of a request using the task id of the request
*SummaryApi* | [**post**](docs/SummaryApi.md#post) | **POST** /api/async/summary | Gets the summary analysis of a document
*TextApi* | [**get**](docs/TextApi.md#get) | **GET** /api/async/text/result/{taskId} | Tries to get the result of a request using the task id of the request
*TextApi* | [**post**](docs/TextApi.md#post) | **POST** /api/async/text | Analyses html and adds suggestions tags to it
*ThesaurusApi* | [**post**](docs/ThesaurusApi.md#post) | **POST** /api/thesaurus | Returns the thesaurus entries for a specific word
*WordCloudApi* | [**get**](docs/WordCloudApi.md#get) | **GET** /api/async/wordcloud/result/{taskId} | Tries to get the result of a request using the task id of the request
*WordCloudApi* | [**post**](docs/WordCloudApi.md#post) | **POST** /api/async/wordcloud | Analyses text and returns a word cloud (as an image)


## Documentation For Models

 - [AnalysisSettings](docs/AnalysisSettings.md)
 - [AnalysisSummary](docs/AnalysisSummary.md)
 - [AnalysisSummaryGraph](docs/AnalysisSummaryGraph.md)
 - [AnalysisSummaryGraphItem](docs/AnalysisSummaryGraphItem.md)
 - [AnalysisSummaryItem](docs/AnalysisSummaryItem.md)
 - [AnalysisSummarySubItem](docs/AnalysisSummarySubItem.md)
 - [AsyncResponseContextualThesaurusResponse](docs/AsyncResponseContextualThesaurusResponse.md)
 - [AsyncResponseHtmlAnalysisResponse](docs/AsyncResponseHtmlAnalysisResponse.md)
 - [AsyncResponseSummaryAnalysisResponse](docs/AsyncResponseSummaryAnalysisResponse.md)
 - [AsyncResponseTextAnalysisResponse](docs/AsyncResponseTextAnalysisResponse.md)
 - [AsyncResponseWordCloudResponse](docs/AsyncResponseWordCloudResponse.md)
 - [ContextualThesaurusRequest](docs/ContextualThesaurusRequest.md)
 - [ContextualThesaurusResponse](docs/ContextualThesaurusResponse.md)
 - [DocTag](docs/DocTag.md)
 - [EntryMeaning](docs/EntryMeaning.md)
 - [HtmlAnalysisRequest](docs/HtmlAnalysisRequest.md)
 - [HtmlAnalysisResponse](docs/HtmlAnalysisResponse.md)
 - [SuggestionCategory](docs/SuggestionCategory.md)
 - [SummaryAnalysisRequest](docs/SummaryAnalysisRequest.md)
 - [SummaryAnalysisResponse](docs/SummaryAnalysisResponse.md)
 - [TextAnalysisRequest](docs/TextAnalysisRequest.md)
 - [TextAnalysisResponse](docs/TextAnalysisResponse.md)
 - [ThesaurusRequest](docs/ThesaurusRequest.md)
 - [ThesaurusResponse](docs/ThesaurusResponse.md)
 - [WordCloudRequest](docs/WordCloudRequest.md)
 - [WordCloudResponse](docs/WordCloudResponse.md)


## Documentation For Authorization


## licenseCode

- **Type**: API key
- **API key parameter name**: licenseCode
- **Location**: HTTP header


## Author

prowritingaid.com

