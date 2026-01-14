# V0Api

All URIs are relative to *https://api.adsb.lol*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**apiAirportApi0AirportIcaoGet**](V0Api.md#apiAirportApi0AirportIcaoGet) | **GET** /api/0/airport/{icao} | Airports by ICAO |
| [**apiAirportApi0AirportIcaoGet_0**](V0Api.md#apiAirportApi0AirportIcaoGet_0) | **GET** /api/0/airport/{icao} | Airports by ICAO |
| [**apiMe0MeGet**](V0Api.md#apiMe0MeGet) | **GET** /0/me | Information about your receiver and global stats |
| [**apiMy0MyGet**](V0Api.md#apiMy0MyGet) | **GET** /0/my | My Map redirect based on IP |
| [**apiRoutesetApi0RoutesetPost**](V0Api.md#apiRoutesetApi0RoutesetPost) | **POST** /api/0/routeset | Routes for a list of aircraft callsigns |
| [**apiRoutesetApi0RoutesetPost_0**](V0Api.md#apiRoutesetApi0RoutesetPost_0) | **POST** /api/0/routeset | Routes for a list of aircraft callsigns |



## apiAirportApi0AirportIcaoGet

> String apiAirportApi0AirportIcaoGet(icao)

Airports by ICAO

Data by https://github.com/vradarserver/standing-data/

### Example

```java
// Import classes:
import net.adambruce.adsb.lol.client.ApiClient;
import net.adambruce.adsb.lol.client.ApiException;
import net.adambruce.adsb.lol.client.Configuration;
import net.adambruce.adsb.lol.client.models.*;
import net.adambruce.adsb.lol.api.V0Api;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.adsb.lol");

        V0Api apiInstance = new V0Api(defaultClient);
        String icao = "icao_example"; // String | 
        try {
            String result = apiInstance.apiAirportApi0AirportIcaoGet(icao);
            System.out.println(result);
        } catch (ApiException e) {
            System.err.println("Exception when calling V0Api#apiAirportApi0AirportIcaoGet");
            System.err.println("Status code: " + e.getCode());
            System.err.println("Reason: " + e.getResponseBody());
            System.err.println("Response headers: " + e.getResponseHeaders());
            e.printStackTrace();
        }
    }
}
```

### Parameters


| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **icao** | **String**|  | |

### Return type

**String**

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful Response |  -  |
| **422** | Validation Error |  -  |


## apiAirportApi0AirportIcaoGet_0

> String apiAirportApi0AirportIcaoGet_0(icao)

Airports by ICAO

Data by https://github.com/vradarserver/standing-data/

### Example

```java
// Import classes:
import net.adambruce.adsb.lol.client.ApiClient;
import net.adambruce.adsb.lol.client.ApiException;
import net.adambruce.adsb.lol.client.Configuration;
import net.adambruce.adsb.lol.client.models.*;
import net.adambruce.adsb.lol.api.V0Api;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.adsb.lol");

        V0Api apiInstance = new V0Api(defaultClient);
        String icao = "icao_example"; // String | 
        try {
            String result = apiInstance.apiAirportApi0AirportIcaoGet_0(icao);
            System.out.println(result);
        } catch (ApiException e) {
            System.err.println("Exception when calling V0Api#apiAirportApi0AirportIcaoGet_0");
            System.err.println("Status code: " + e.getCode());
            System.err.println("Reason: " + e.getResponseBody());
            System.err.println("Response headers: " + e.getResponseHeaders());
            e.printStackTrace();
        }
    }
}
```

### Parameters


| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **icao** | **String**|  | |

### Return type

**String**

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful Response |  -  |
| **422** | Validation Error |  -  |


## apiMe0MeGet

> String apiMe0MeGet()

Information about your receiver and global stats

### Example

```java
// Import classes:
import net.adambruce.adsb.lol.client.ApiClient;
import net.adambruce.adsb.lol.client.ApiException;
import net.adambruce.adsb.lol.client.Configuration;
import net.adambruce.adsb.lol.client.models.*;
import net.adambruce.adsb.lol.api.V0Api;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.adsb.lol");

        V0Api apiInstance = new V0Api(defaultClient);
        try {
            String result = apiInstance.apiMe0MeGet();
            System.out.println(result);
        } catch (ApiException e) {
            System.err.println("Exception when calling V0Api#apiMe0MeGet");
            System.err.println("Status code: " + e.getCode());
            System.err.println("Reason: " + e.getResponseBody());
            System.err.println("Response headers: " + e.getResponseHeaders());
            e.printStackTrace();
        }
    }
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

**String**

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful Response |  -  |


## apiMy0MyGet

> Object apiMy0MyGet()

My Map redirect based on IP

### Example

```java
// Import classes:
import net.adambruce.adsb.lol.client.ApiClient;
import net.adambruce.adsb.lol.client.ApiException;
import net.adambruce.adsb.lol.client.Configuration;
import net.adambruce.adsb.lol.client.models.*;
import net.adambruce.adsb.lol.api.V0Api;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.adsb.lol");

        V0Api apiInstance = new V0Api(defaultClient);
        try {
            Object result = apiInstance.apiMy0MyGet();
            System.out.println(result);
        } catch (ApiException e) {
            System.err.println("Exception when calling V0Api#apiMy0MyGet");
            System.err.println("Status code: " + e.getCode());
            System.err.println("Reason: " + e.getResponseBody());
            System.err.println("Response headers: " + e.getResponseHeaders());
            e.printStackTrace();
        }
    }
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

**Object**

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful Response |  -  |


## apiRoutesetApi0RoutesetPost

> String apiRoutesetApi0RoutesetPost(planeList)

Routes for a list of aircraft callsigns

Look up routes for multiple planes at once.     Data by https://github.com/vradarserver/standing-data/

### Example

```java
// Import classes:
import net.adambruce.adsb.lol.client.ApiClient;
import net.adambruce.adsb.lol.client.ApiException;
import net.adambruce.adsb.lol.client.Configuration;
import net.adambruce.adsb.lol.client.models.*;
import net.adambruce.adsb.lol.api.V0Api;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.adsb.lol");

        V0Api apiInstance = new V0Api(defaultClient);
        PlaneList planeList = new PlaneList(); // PlaneList | 
        try {
            String result = apiInstance.apiRoutesetApi0RoutesetPost(planeList);
            System.out.println(result);
        } catch (ApiException e) {
            System.err.println("Exception when calling V0Api#apiRoutesetApi0RoutesetPost");
            System.err.println("Status code: " + e.getCode());
            System.err.println("Reason: " + e.getResponseBody());
            System.err.println("Response headers: " + e.getResponseHeaders());
            e.printStackTrace();
        }
    }
}
```

### Parameters


| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **planeList** | [**PlaneList**](PlaneList.md)|  | |

### Return type

**String**

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful Response |  -  |
| **422** | Validation Error |  -  |


## apiRoutesetApi0RoutesetPost_0

> String apiRoutesetApi0RoutesetPost_0(planeList)

Routes for a list of aircraft callsigns

Look up routes for multiple planes at once.     Data by https://github.com/vradarserver/standing-data/

### Example

```java
// Import classes:
import net.adambruce.adsb.lol.client.ApiClient;
import net.adambruce.adsb.lol.client.ApiException;
import net.adambruce.adsb.lol.client.Configuration;
import net.adambruce.adsb.lol.client.models.*;
import net.adambruce.adsb.lol.api.V0Api;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.adsb.lol");

        V0Api apiInstance = new V0Api(defaultClient);
        PlaneList planeList = new PlaneList(); // PlaneList | 
        try {
            String result = apiInstance.apiRoutesetApi0RoutesetPost_0(planeList);
            System.out.println(result);
        } catch (ApiException e) {
            System.err.println("Exception when calling V0Api#apiRoutesetApi0RoutesetPost_0");
            System.err.println("Status code: " + e.getCode());
            System.err.println("Reason: " + e.getResponseBody());
            System.err.println("Response headers: " + e.getResponseHeaders());
            e.printStackTrace();
        }
    }
}
```

### Parameters


| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **planeList** | [**PlaneList**](PlaneList.md)|  | |

### Return type

**String**

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful Response |  -  |
| **422** | Validation Error |  -  |

