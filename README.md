# swagger-client
The SnackRisk API logs potential risks in GenAI-generated bot responses.  1. Visit: https://www.datasnack.ai/ 2. Sign up for an account. 3. Click the \"Account\" menu button to obtain your API key. 4. Copy the API key. 5. Click the \"Documentation\" menu button. 6. Click \"Authorize\" and enter your API key.  Creating your 1st project:  1. Send a request to `/api/v1/createProject` 2. Once the above request is submitted, DataSnack's proprietary chunking and embedding algorithm typically takes around 5 minutes to process documents that are between 15 to 30 pages in length. 3. Send a request to `/api/v1/runRisk` using the `clientId` and `deptId` you obtained from creating the project, along with the content you want to run a risk check against. 

This Python package is automatically generated by the [Swagger Codegen](https://github.com/swagger-api/swagger-codegen) project:

- API version: 0.1
- Package version: 1.0.0
- Build package: io.swagger.codegen.v3.generators.python.PythonClientCodegen

## Requirements.

Python 2.7 and 3.4+

## Installation & Usage
### pip install

If the python package is hosted on Github, you can install directly from Github

```sh
pip install git+https://github.com/GIT_USER_ID/GIT_REPO_ID.git
```
(you may need to run `pip` with root permission: `sudo pip install git+https://github.com/GIT_USER_ID/GIT_REPO_ID.git`)

Then import the package:
```python
import swagger_client 
```

### Setuptools

Install via [Setuptools](http://pypi.python.org/pypi/setuptools).

```sh
python setup.py install --user
```
(or `sudo python setup.py install` to install the package for all users)

Then import the package:
```python
import swagger_client
```

## Getting Started

Please follow the [installation procedure](#installation--usage) and then run the following:

```python
from __future__ import print_function
import time
import swagger_client
from swagger_client.rest import ApiException
from pprint import pprint

# Configure API key authorization: ApiKeyAuth
configuration = swagger_client.Configuration()
configuration.api_key['Authorization'] = 'YOUR_API_KEY'
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['Authorization'] = 'Bearer'

# create an instance of the API class
api_instance = swagger_client.AddClientCompanyApi(swagger_client.ApiClient(configuration))
body = swagger_client.ModelsClientCompany() # ModelsClientCompany | Add client company

try:
    # AddClientCompany
    api_response = api_instance.api_v1_add_client_company_post(body)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling AddClientCompanyApi->api_v1_add_client_company_post: %s\n" % e)
```

## Documentation for API Endpoints

All URIs are relative to *https://datasnackapi.uc.r.appspot.com*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*AddClientCompanyApi* | [**api_v1_add_client_company_post**](docs/AddClientCompanyApi.md#api_v1_add_client_company_post) | **POST** /api/v1/addClientCompany | AddClientCompany
*AddDeptSilosApi* | [**api_v1_add_dept_silo_post**](docs/AddDeptSilosApi.md#api_v1_add_dept_silo_post) | **POST** /api/v1/addDeptSilo | AddDeptSilos
*AddDomainIntelApi* | [**api_v1_add_domain_intel_post**](docs/AddDomainIntelApi.md#api_v1_add_domain_intel_post) | **POST** /api/v1/addDomainIntel | AddDomainIntel
*AddPolicyApi* | [**api_v1_add_policy_post**](docs/AddPolicyApi.md#api_v1_add_policy_post) | **POST** /api/v1/addPolicy | AddPolicy
*CreateProjectApi* | [**api_v1_create_project_post**](docs/CreateProjectApi.md#api_v1_create_project_post) | **POST** /api/v1/createProject | CreateProject
*GetClientCompaniesApi* | [**api_v1_get_client_companies_get**](docs/GetClientCompaniesApi.md#api_v1_get_client_companies_get) | **GET** /api/v1/getClientCompanies | GetClientCompanies
*GetDeptSilosApi* | [**api_v1_get_dept_silos_get**](docs/GetDeptSilosApi.md#api_v1_get_dept_silos_get) | **GET** /api/v1/getDeptSilos | GetDeptSilos
*GetDomainIntelApi* | [**api_v1_get_domain_intel_get**](docs/GetDomainIntelApi.md#api_v1_get_domain_intel_get) | **GET** /api/v1/getDomainIntel | GetDomainIntel
*GetFullRiskReportsApi* | [**api_v1_get_full_risk_reports_get**](docs/GetFullRiskReportsApi.md#api_v1_get_full_risk_reports_get) | **GET** /api/v1/getFullRiskReports | GetFullRiskReports
*GetPoliciesApi* | [**api_v1_get_policies_get**](docs/GetPoliciesApi.md#api_v1_get_policies_get) | **GET** /api/v1/getPolicies | GetPolicies
*RunRiskApi* | [**api_v1_run_risk_post**](docs/RunRiskApi.md#api_v1_run_risk_post) | **POST** /api/v1/runRisk | RunRisk

## Documentation For Models

 - [ModelsClientCompany](docs/ModelsClientCompany.md)
 - [ModelsClientPolicies](docs/ModelsClientPolicies.md)
 - [ModelsCreateProjectClient](docs/ModelsCreateProjectClient.md)
 - [ModelsCreateProjectResponse](docs/ModelsCreateProjectResponse.md)
 - [ModelsCreateProjectStatus](docs/ModelsCreateProjectStatus.md)
 - [ModelsDeptSilo](docs/ModelsDeptSilo.md)
 - [ModelsDomainIntelRequest](docs/ModelsDomainIntelRequest.md)
 - [ModelsFullRiskReport](docs/ModelsFullRiskReport.md)
 - [ModelsPolicy](docs/ModelsPolicy.md)
 - [ModelsResult](docs/ModelsResult.md)
 - [ModelsRisk](docs/ModelsRisk.md)
 - [ModelsRiskCheckerRequest](docs/ModelsRiskCheckerRequest.md)
 - [ModelsRiskReport](docs/ModelsRiskReport.md)
 - [ModelsRiskType](docs/ModelsRiskType.md)

## Documentation For Authorization


## ApiKeyAuth

- **Type**: API key
- **API key parameter name**: Authorization
- **Location**: HTTP header


## Author

support@datasnack.ai
# datasnack-python-sdk