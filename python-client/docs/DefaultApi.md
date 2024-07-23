# bundestag_tagesordnung.DefaultApi

All URIs are relative to *https://api.hutt.io*

Method | HTTP request | Description
------------- | ------------- | -------------
[**bt_to_csv_get**](DefaultApi.md#bt_to_csv_get) | **GET** /bt-to/csv | Tagesordnungen im CSV-Format abrufen
[**bt_to_ical_get**](DefaultApi.md#bt_to_ical_get) | **GET** /bt-to/ical | Tagesordnungen im iCal-Format abrufen
[**bt_to_json_get**](DefaultApi.md#bt_to_json_get) | **GET** /bt-to/json | Tagesordnungen im JSON-Format abrufen
[**bt_to_xml_get**](DefaultApi.md#bt_to_xml_get) | **GET** /bt-to/xml | Tagesordnungen im XML-Format abrufen


# **bt_to_csv_get**
> str bt_to_csv_get()

Tagesordnungen im CSV-Format abrufen

### Example


```python
import time
from deutschland import bundestag_tagesordnung
from deutschland.bundestag_tagesordnung.api import default_api
from pprint import pprint
# Defining the host is optional and defaults to https://api.hutt.io
# See configuration.py for a list of all supported configuration parameters.
configuration = bundestag_tagesordnung.Configuration(
    host = "https://api.hutt.io"
)


# Enter a context with an instance of the API client
with bundestag_tagesordnung.ApiClient() as api_client:
    # Create an instance of the API class
    api_instance = default_api.DefaultApi(api_client)
    year = 1 # int | Das Jahr, für das Tagesordnungen abgerufen werden sollen (optional) (optional)
    week = 1 # int | Die Kalenderwoche, für die Tagesordnungen abgerufen werden sollen (optional; kann mit Jahr kombiniert werden) (optional)

    # example passing only required values which don't have defaults set
    # and optional values
    try:
        # Tagesordnungen im CSV-Format abrufen
        api_response = api_instance.bt_to_csv_get(year=year, week=week)
        pprint(api_response)
    except bundestag_tagesordnung.ApiException as e:
        print("Exception when calling DefaultApi->bt_to_csv_get: %s\n" % e)
```


### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **year** | **int**| Das Jahr, für das Tagesordnungen abgerufen werden sollen (optional) | [optional]
 **week** | **int**| Die Kalenderwoche, für die Tagesordnungen abgerufen werden sollen (optional; kann mit Jahr kombiniert werden) | [optional]

### Return type

**str**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/csv


### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Erfolgreiche Antwort |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **bt_to_ical_get**
> str bt_to_ical_get()

Tagesordnungen im iCal-Format abrufen

### Example


```python
import time
from deutschland import bundestag_tagesordnung
from deutschland.bundestag_tagesordnung.api import default_api
from pprint import pprint
# Defining the host is optional and defaults to https://api.hutt.io
# See configuration.py for a list of all supported configuration parameters.
configuration = bundestag_tagesordnung.Configuration(
    host = "https://api.hutt.io"
)


# Enter a context with an instance of the API client
with bundestag_tagesordnung.ApiClient() as api_client:
    # Create an instance of the API class
    api_instance = default_api.DefaultApi(api_client)
    na = True # bool | Zusätzliche Kalendereinträge für Namentliche Abstimmungen erstellen (optional; kombinierbar) (optional)
    na_alarm = True # bool | Alarme 15 Minuten vor Namentlichen Abstimmungen hinzufügen (optional; kombinierbar) (optional)
    show_sw = True # bool | Ganztägige Termine für Sitzungswochen erstellen (optional; kombinierbar) (optional)

    # example passing only required values which don't have defaults set
    # and optional values
    try:
        # Tagesordnungen im iCal-Format abrufen
        api_response = api_instance.bt_to_ical_get(na=na, na_alarm=na_alarm, show_sw=show_sw)
        pprint(api_response)
    except bundestag_tagesordnung.ApiException as e:
        print("Exception when calling DefaultApi->bt_to_ical_get: %s\n" % e)
```


### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **na** | **bool**| Zusätzliche Kalendereinträge für Namentliche Abstimmungen erstellen (optional; kombinierbar) | [optional]
 **na_alarm** | **bool**| Alarme 15 Minuten vor Namentlichen Abstimmungen hinzufügen (optional; kombinierbar) | [optional]
 **show_sw** | **bool**| Ganztägige Termine für Sitzungswochen erstellen (optional; kombinierbar) | [optional]

### Return type

**str**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/calendar


### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Erfolgreiche Antwort |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **bt_to_json_get**
> [{str: (bool, date, datetime, dict, float, int, list, str, none_type)}] bt_to_json_get()

Tagesordnungen im JSON-Format abrufen

### Example


```python
import time
from deutschland import bundestag_tagesordnung
from deutschland.bundestag_tagesordnung.api import default_api
from pprint import pprint
# Defining the host is optional and defaults to https://api.hutt.io
# See configuration.py for a list of all supported configuration parameters.
configuration = bundestag_tagesordnung.Configuration(
    host = "https://api.hutt.io"
)


# Enter a context with an instance of the API client
with bundestag_tagesordnung.ApiClient() as api_client:
    # Create an instance of the API class
    api_instance = default_api.DefaultApi(api_client)
    week = 1 # int | Die Kalenderwoche, für die Tagesordnungen abgerufen werden sollen (optional) (optional)

    # example passing only required values which don't have defaults set
    # and optional values
    try:
        # Tagesordnungen im JSON-Format abrufen
        api_response = api_instance.bt_to_json_get(week=week)
        pprint(api_response)
    except bundestag_tagesordnung.ApiException as e:
        print("Exception when calling DefaultApi->bt_to_json_get: %s\n" % e)
```


### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **week** | **int**| Die Kalenderwoche, für die Tagesordnungen abgerufen werden sollen (optional) | [optional]

### Return type

**[{str: (bool, date, datetime, dict, float, int, list, str, none_type)}]**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Erfolgreiche Antwort |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **bt_to_xml_get**
> str bt_to_xml_get()

Tagesordnungen im XML-Format abrufen

### Example


```python
import time
from deutschland import bundestag_tagesordnung
from deutschland.bundestag_tagesordnung.api import default_api
from pprint import pprint
# Defining the host is optional and defaults to https://api.hutt.io
# See configuration.py for a list of all supported configuration parameters.
configuration = bundestag_tagesordnung.Configuration(
    host = "https://api.hutt.io"
)


# Enter a context with an instance of the API client
with bundestag_tagesordnung.ApiClient() as api_client:
    # Create an instance of the API class
    api_instance = default_api.DefaultApi(api_client)
    year = 1 # int | Das Jahr, für das Tagesordnungen abgerufen werden sollen (optional) (optional)
    week = 1 # int | Die Kalenderwoche, für die Tagesordnungen abgerufen werden sollen (optional; kann mit Jahr kombiniert werden) (optional)

    # example passing only required values which don't have defaults set
    # and optional values
    try:
        # Tagesordnungen im XML-Format abrufen
        api_response = api_instance.bt_to_xml_get(year=year, week=week)
        pprint(api_response)
    except bundestag_tagesordnung.ApiException as e:
        print("Exception when calling DefaultApi->bt_to_xml_get: %s\n" % e)
```


### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **year** | **int**| Das Jahr, für das Tagesordnungen abgerufen werden sollen (optional) | [optional]
 **week** | **int**| Die Kalenderwoche, für die Tagesordnungen abgerufen werden sollen (optional; kann mit Jahr kombiniert werden) | [optional]

### Return type

**str**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/xml


### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Erfolgreiche Antwort |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

