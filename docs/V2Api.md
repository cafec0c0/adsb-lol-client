# V2Api

All URIs are relative to *https://api.adsb.lol*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**v2CallsignFilterV2CallsignCallsignGet**](V2Api.md#v2CallsignFilterV2CallsignCallsignGet) | **GET** /v2/callsign/{callsign} | Aircrafts with specific callsign (JBU1942) |
| [**v2ClosestV2ClosestLatLonRadiusGet**](V2Api.md#v2ClosestV2ClosestLatLonRadiusGet) | **GET** /v2/closest/{lat}/{lon}/{radius} | Single aircraft closest to a point (lat, lon) |
| [**v2HexFilterV2HexIcaoHexGet**](V2Api.md#v2HexFilterV2HexIcaoHexGet) | **GET** /v2/hex/{icao_hex} | Aircrafts with specific transponder hex code (4CA87C) |
| [**v2HexFilterV2IcaoIcaoHexGet**](V2Api.md#v2HexFilterV2IcaoIcaoHexGet) | **GET** /v2/icao/{icao_hex} | Aircrafts with specific transponder hex code (4CA87C) |
| [**v2LaddV2LaddGet**](V2Api.md#v2LaddV2LaddGet) | **GET** /v2/ladd | Aircrafts on LADD (Limiting Aircraft Data Displayed) |
| [**v2MilV2MilGet**](V2Api.md#v2MilV2MilGet) | **GET** /v2/mil | Military registered aircrafts |
| [**v2PiaV2PiaGet**](V2Api.md#v2PiaV2PiaGet) | **GET** /v2/pia | Aircrafts with PIA addresses (Privacy ICAO Address) |
| [**v2PointV2LatLatLonLonDistRadiusGet**](V2Api.md#v2PointV2LatLatLonLonDistRadiusGet) | **GET** /v2/lat/{lat}/lon/{lon}/dist/{radius} | Aircrafts surrounding a point (lat, lon) up to 250nm |
| [**v2PointV2PointLatLonRadiusGet**](V2Api.md#v2PointV2PointLatLonRadiusGet) | **GET** /v2/point/{lat}/{lon}/{radius} | Aircrafts surrounding a point (lat, lon) up to 250nm |
| [**v2RegFilterV2RegRegistrationGet**](V2Api.md#v2RegFilterV2RegRegistrationGet) | **GET** /v2/reg/{registration} | Aircrafts with specific registration (G-KELS) |
| [**v2RegFilterV2RegistrationRegistrationGet**](V2Api.md#v2RegFilterV2RegistrationRegistrationGet) | **GET** /v2/registration/{registration} | Aircrafts with specific registration (G-KELS) |
| [**v2SquawkFilterV2SqkSquawkGet**](V2Api.md#v2SquawkFilterV2SqkSquawkGet) | **GET** /v2/sqk/{squawk} | Aircrafts with specific squawk (1200, 7700, etc.) |
| [**v2SquawkFilterV2SquawkSquawkGet**](V2Api.md#v2SquawkFilterV2SquawkSquawkGet) | **GET** /v2/squawk/{squawk} | Aircrafts with specific squawk (1200, 7700, etc.) |
| [**v2TypeFilterV2TypeAircraftTypeGet**](V2Api.md#v2TypeFilterV2TypeAircraftTypeGet) | **GET** /v2/type/{aircraft_type} | Aircrafts of specific type (A320, B738) |



## v2CallsignFilterV2CallsignCallsignGet

> V2ResponseModel v2CallsignFilterV2CallsignCallsignGet(callsign)

Aircrafts with specific callsign (JBU1942)

Returns aircraft filtered by [callsign](https://en.wikipedia.org/wiki/Aviation_call_signs).

### Example

```java
// Import classes:
import net.adambruce.adsb.lol.client.ApiClient;
import net.adambruce.adsb.lol.client.ApiException;
import net.adambruce.adsb.lol.client.Configuration;
import net.adambruce.adsb.lol.client.models.*;
import net.adambruce.adsb.lol.api.V2Api;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.adsb.lol");

        V2Api apiInstance = new V2Api(defaultClient);
        String callsign = "JBU1942"; // String | 
        try {
            V2ResponseModel result = apiInstance.v2CallsignFilterV2CallsignCallsignGet(callsign);
            System.out.println(result);
        } catch (ApiException e) {
            System.err.println("Exception when calling V2Api#v2CallsignFilterV2CallsignCallsignGet");
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
| **callsign** | **String**|  | |

### Return type

[**V2ResponseModel**](V2ResponseModel.md)

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


## v2ClosestV2ClosestLatLonRadiusGet

> V2ResponseModel v2ClosestV2ClosestLatLonRadiusGet(lat, lon, radius)

Single aircraft closest to a point (lat, lon)

Returns the closest aircraft to a point described by the latitude and longtidude within a radius up to 250nm.

### Example

```java
// Import classes:
import net.adambruce.adsb.lol.client.ApiClient;
import net.adambruce.adsb.lol.client.ApiException;
import net.adambruce.adsb.lol.client.Configuration;
import net.adambruce.adsb.lol.client.models.*;
import net.adambruce.adsb.lol.api.V2Api;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.adsb.lol");

        V2Api apiInstance = new V2Api(defaultClient);
        Double lat = 51.89508D; // Double | 
        Double lon = 2.79437D; // Double | 
        Long radius = 250L; // Long | 
        try {
            V2ResponseModel result = apiInstance.v2ClosestV2ClosestLatLonRadiusGet(lat, lon, radius);
            System.out.println(result);
        } catch (ApiException e) {
            System.err.println("Exception when calling V2Api#v2ClosestV2ClosestLatLonRadiusGet");
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
| **lat** | **Double**|  | |
| **lon** | **Double**|  | |
| **radius** | **Long**|  | |

### Return type

[**V2ResponseModel**](V2ResponseModel.md)

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


## v2HexFilterV2HexIcaoHexGet

> V2ResponseModel v2HexFilterV2HexIcaoHexGet(icaoHex)

Aircrafts with specific transponder hex code (4CA87C)

Returns aircraft filtered by [transponder hex code](https://en.wikipedia.org/wiki/Aviation_transponder_interrogation_modes#ICAO_24-bit_address).

### Example

```java
// Import classes:
import net.adambruce.adsb.lol.client.ApiClient;
import net.adambruce.adsb.lol.client.ApiException;
import net.adambruce.adsb.lol.client.Configuration;
import net.adambruce.adsb.lol.client.models.*;
import net.adambruce.adsb.lol.api.V2Api;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.adsb.lol");

        V2Api apiInstance = new V2Api(defaultClient);
        String icaoHex = "4CA87C"; // String | 
        try {
            V2ResponseModel result = apiInstance.v2HexFilterV2HexIcaoHexGet(icaoHex);
            System.out.println(result);
        } catch (ApiException e) {
            System.err.println("Exception when calling V2Api#v2HexFilterV2HexIcaoHexGet");
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
| **icaoHex** | **String**|  | |

### Return type

[**V2ResponseModel**](V2ResponseModel.md)

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


## v2HexFilterV2IcaoIcaoHexGet

> V2ResponseModel v2HexFilterV2IcaoIcaoHexGet(icaoHex)

Aircrafts with specific transponder hex code (4CA87C)

Returns aircraft filtered by [transponder hex code](https://en.wikipedia.org/wiki/Aviation_transponder_interrogation_modes#ICAO_24-bit_address).

### Example

```java
// Import classes:
import net.adambruce.adsb.lol.client.ApiClient;
import net.adambruce.adsb.lol.client.ApiException;
import net.adambruce.adsb.lol.client.Configuration;
import net.adambruce.adsb.lol.client.models.*;
import net.adambruce.adsb.lol.api.V2Api;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.adsb.lol");

        V2Api apiInstance = new V2Api(defaultClient);
        String icaoHex = "4CA87C"; // String | 
        try {
            V2ResponseModel result = apiInstance.v2HexFilterV2IcaoIcaoHexGet(icaoHex);
            System.out.println(result);
        } catch (ApiException e) {
            System.err.println("Exception when calling V2Api#v2HexFilterV2IcaoIcaoHexGet");
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
| **icaoHex** | **String**|  | |

### Return type

[**V2ResponseModel**](V2ResponseModel.md)

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


## v2LaddV2LaddGet

> V2ResponseModel v2LaddV2LaddGet()

Aircrafts on LADD (Limiting Aircraft Data Displayed)

Returns all aircrafts on [LADD](https://www.faa.gov/pilots/ladd) filter.

### Example

```java
// Import classes:
import net.adambruce.adsb.lol.client.ApiClient;
import net.adambruce.adsb.lol.client.ApiException;
import net.adambruce.adsb.lol.client.Configuration;
import net.adambruce.adsb.lol.client.models.*;
import net.adambruce.adsb.lol.api.V2Api;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.adsb.lol");

        V2Api apiInstance = new V2Api(defaultClient);
        try {
            V2ResponseModel result = apiInstance.v2LaddV2LaddGet();
            System.out.println(result);
        } catch (ApiException e) {
            System.err.println("Exception when calling V2Api#v2LaddV2LaddGet");
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

[**V2ResponseModel**](V2ResponseModel.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful Response |  -  |


## v2MilV2MilGet

> V2ResponseModel v2MilV2MilGet()

Military registered aircrafts

Returns all military registered aircraft.

### Example

```java
// Import classes:
import net.adambruce.adsb.lol.client.ApiClient;
import net.adambruce.adsb.lol.client.ApiException;
import net.adambruce.adsb.lol.client.Configuration;
import net.adambruce.adsb.lol.client.models.*;
import net.adambruce.adsb.lol.api.V2Api;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.adsb.lol");

        V2Api apiInstance = new V2Api(defaultClient);
        try {
            V2ResponseModel result = apiInstance.v2MilV2MilGet();
            System.out.println(result);
        } catch (ApiException e) {
            System.err.println("Exception when calling V2Api#v2MilV2MilGet");
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

[**V2ResponseModel**](V2ResponseModel.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful Response |  -  |


## v2PiaV2PiaGet

> V2ResponseModel v2PiaV2PiaGet()

Aircrafts with PIA addresses (Privacy ICAO Address)

Returns all aircraft with [PIA](https://nbaa.org/aircraft-operations/security/privacy/privacy-icao-address-pia/) addresses.

### Example

```java
// Import classes:
import net.adambruce.adsb.lol.client.ApiClient;
import net.adambruce.adsb.lol.client.ApiException;
import net.adambruce.adsb.lol.client.Configuration;
import net.adambruce.adsb.lol.client.models.*;
import net.adambruce.adsb.lol.api.V2Api;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.adsb.lol");

        V2Api apiInstance = new V2Api(defaultClient);
        try {
            V2ResponseModel result = apiInstance.v2PiaV2PiaGet();
            System.out.println(result);
        } catch (ApiException e) {
            System.err.println("Exception when calling V2Api#v2PiaV2PiaGet");
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

[**V2ResponseModel**](V2ResponseModel.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful Response |  -  |


## v2PointV2LatLatLonLonDistRadiusGet

> V2ResponseModel v2PointV2LatLatLonLonDistRadiusGet(lat, lon, radius)

Aircrafts surrounding a point (lat, lon) up to 250nm

Returns aircraft located in a circle described by the latitude and longtidude of its center and its radius.

### Example

```java
// Import classes:
import net.adambruce.adsb.lol.client.ApiClient;
import net.adambruce.adsb.lol.client.ApiException;
import net.adambruce.adsb.lol.client.Configuration;
import net.adambruce.adsb.lol.client.models.*;
import net.adambruce.adsb.lol.api.V2Api;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.adsb.lol");

        V2Api apiInstance = new V2Api(defaultClient);
        Double lat = 51.89508D; // Double | 
        Double lon = 2.79437D; // Double | 
        Long radius = 250L; // Long | 
        try {
            V2ResponseModel result = apiInstance.v2PointV2LatLatLonLonDistRadiusGet(lat, lon, radius);
            System.out.println(result);
        } catch (ApiException e) {
            System.err.println("Exception when calling V2Api#v2PointV2LatLatLonLonDistRadiusGet");
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
| **lat** | **Double**|  | |
| **lon** | **Double**|  | |
| **radius** | **Long**|  | |

### Return type

[**V2ResponseModel**](V2ResponseModel.md)

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


## v2PointV2PointLatLonRadiusGet

> V2ResponseModel v2PointV2PointLatLonRadiusGet(lat, lon, radius)

Aircrafts surrounding a point (lat, lon) up to 250nm

Returns aircraft located in a circle described by the latitude and longtidude of its center and its radius.

### Example

```java
// Import classes:
import net.adambruce.adsb.lol.client.ApiClient;
import net.adambruce.adsb.lol.client.ApiException;
import net.adambruce.adsb.lol.client.Configuration;
import net.adambruce.adsb.lol.client.models.*;
import net.adambruce.adsb.lol.api.V2Api;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.adsb.lol");

        V2Api apiInstance = new V2Api(defaultClient);
        Double lat = 51.89508D; // Double | 
        Double lon = 2.79437D; // Double | 
        Long radius = 250L; // Long | 
        try {
            V2ResponseModel result = apiInstance.v2PointV2PointLatLonRadiusGet(lat, lon, radius);
            System.out.println(result);
        } catch (ApiException e) {
            System.err.println("Exception when calling V2Api#v2PointV2PointLatLonRadiusGet");
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
| **lat** | **Double**|  | |
| **lon** | **Double**|  | |
| **radius** | **Long**|  | |

### Return type

[**V2ResponseModel**](V2ResponseModel.md)

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


## v2RegFilterV2RegRegistrationGet

> V2ResponseModel v2RegFilterV2RegRegistrationGet(registration)

Aircrafts with specific registration (G-KELS)

Returns aircraft filtered by [aircarft registration code](https://en.wikipedia.org/wiki/Aircraft_registration).

### Example

```java
// Import classes:
import net.adambruce.adsb.lol.client.ApiClient;
import net.adambruce.adsb.lol.client.ApiException;
import net.adambruce.adsb.lol.client.Configuration;
import net.adambruce.adsb.lol.client.models.*;
import net.adambruce.adsb.lol.api.V2Api;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.adsb.lol");

        V2Api apiInstance = new V2Api(defaultClient);
        String registration = "G-KELS"; // String | 
        try {
            V2ResponseModel result = apiInstance.v2RegFilterV2RegRegistrationGet(registration);
            System.out.println(result);
        } catch (ApiException e) {
            System.err.println("Exception when calling V2Api#v2RegFilterV2RegRegistrationGet");
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
| **registration** | **String**|  | |

### Return type

[**V2ResponseModel**](V2ResponseModel.md)

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


## v2RegFilterV2RegistrationRegistrationGet

> V2ResponseModel v2RegFilterV2RegistrationRegistrationGet(registration)

Aircrafts with specific registration (G-KELS)

Returns aircraft filtered by [aircarft registration code](https://en.wikipedia.org/wiki/Aircraft_registration).

### Example

```java
// Import classes:
import net.adambruce.adsb.lol.client.ApiClient;
import net.adambruce.adsb.lol.client.ApiException;
import net.adambruce.adsb.lol.client.Configuration;
import net.adambruce.adsb.lol.client.models.*;
import net.adambruce.adsb.lol.api.V2Api;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.adsb.lol");

        V2Api apiInstance = new V2Api(defaultClient);
        String registration = "G-KELS"; // String | 
        try {
            V2ResponseModel result = apiInstance.v2RegFilterV2RegistrationRegistrationGet(registration);
            System.out.println(result);
        } catch (ApiException e) {
            System.err.println("Exception when calling V2Api#v2RegFilterV2RegistrationRegistrationGet");
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
| **registration** | **String**|  | |

### Return type

[**V2ResponseModel**](V2ResponseModel.md)

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


## v2SquawkFilterV2SqkSquawkGet

> V2ResponseModel v2SquawkFilterV2SqkSquawkGet(squawk)

Aircrafts with specific squawk (1200, 7700, etc.)

Returns aircraft filtered by \&quot;squawk\&quot; [transponder code](https://en.wikipedia.org/wiki/List_of_transponder_codes).

### Example

```java
// Import classes:
import net.adambruce.adsb.lol.client.ApiClient;
import net.adambruce.adsb.lol.client.ApiException;
import net.adambruce.adsb.lol.client.Configuration;
import net.adambruce.adsb.lol.client.models.*;
import net.adambruce.adsb.lol.api.V2Api;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.adsb.lol");

        V2Api apiInstance = new V2Api(defaultClient);
        String squawk = "1200"; // String | 
        try {
            V2ResponseModel result = apiInstance.v2SquawkFilterV2SqkSquawkGet(squawk);
            System.out.println(result);
        } catch (ApiException e) {
            System.err.println("Exception when calling V2Api#v2SquawkFilterV2SqkSquawkGet");
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
| **squawk** | **String**|  | |

### Return type

[**V2ResponseModel**](V2ResponseModel.md)

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


## v2SquawkFilterV2SquawkSquawkGet

> V2ResponseModel v2SquawkFilterV2SquawkSquawkGet(squawk)

Aircrafts with specific squawk (1200, 7700, etc.)

Returns aircraft filtered by \&quot;squawk\&quot; [transponder code](https://en.wikipedia.org/wiki/List_of_transponder_codes).

### Example

```java
// Import classes:
import net.adambruce.adsb.lol.client.ApiClient;
import net.adambruce.adsb.lol.client.ApiException;
import net.adambruce.adsb.lol.client.Configuration;
import net.adambruce.adsb.lol.client.models.*;
import net.adambruce.adsb.lol.api.V2Api;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.adsb.lol");

        V2Api apiInstance = new V2Api(defaultClient);
        String squawk = "1200"; // String | 
        try {
            V2ResponseModel result = apiInstance.v2SquawkFilterV2SquawkSquawkGet(squawk);
            System.out.println(result);
        } catch (ApiException e) {
            System.err.println("Exception when calling V2Api#v2SquawkFilterV2SquawkSquawkGet");
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
| **squawk** | **String**|  | |

### Return type

[**V2ResponseModel**](V2ResponseModel.md)

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


## v2TypeFilterV2TypeAircraftTypeGet

> V2ResponseModel v2TypeFilterV2TypeAircraftTypeGet(aircraftType)

Aircrafts of specific type (A320, B738)

Returns aircraft filtered by [aircraft type designator code](https://en.wikipedia.org/wiki/List_of_aircraft_type_designators).

### Example

```java
// Import classes:
import net.adambruce.adsb.lol.client.ApiClient;
import net.adambruce.adsb.lol.client.ApiException;
import net.adambruce.adsb.lol.client.Configuration;
import net.adambruce.adsb.lol.client.models.*;
import net.adambruce.adsb.lol.api.V2Api;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.adsb.lol");

        V2Api apiInstance = new V2Api(defaultClient);
        String aircraftType = "A320"; // String | 
        try {
            V2ResponseModel result = apiInstance.v2TypeFilterV2TypeAircraftTypeGet(aircraftType);
            System.out.println(result);
        } catch (ApiException e) {
            System.err.println("Exception when calling V2Api#v2TypeFilterV2TypeAircraftTypeGet");
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
| **aircraftType** | **String**|  | |

### Return type

[**V2ResponseModel**](V2ResponseModel.md)

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

