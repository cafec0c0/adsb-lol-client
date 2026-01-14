# adsb.lol Java Client

## Usage

### Adding adsb-lol-client to your project
First, add the package as a dependency in your project:

**Maven**:
```xml
 <dependency>
  <groupId>net.adambruce</groupId>
  <artifactId>adsb-lol-client</artifactId>
  <version>0.0.11</version>
</dependency> 
```

**Gradle**:
```groovy
implementation("net.adambruce:adsb-lol-client:0.0.11")
```

### Using the Client
To use the client, create an instance of the desired API and invoke any API method.
```java
V2Api v2Api = new V2Api();
V2ResponseModel response = v2Api.v2PointV2PointLatLonRadiusGet(
        51.45378916708614, -0.0998748436362988, 100L);

System.out.println("Local aircraft:");
response.getAc().forEach(
    aircraft -> System.out.println("Call sign: " + aircraft.getFlight())
);
```

###
See the [Documentation](#documentation) section for more information.

### Fields of Variable Type
As Java is a strongly typed language, fields that could be different types (e.g. number or string)
aren't properly supported by constructors (they become ambiguous for null), so we have to use the
generic `Object` type for these.

To determine what an Object field is, use the `instanceof` operator. e.g.
```java
if (aircraft.getAltBaro() instanceof Integer baroAltInt) {
    // baroAltInt is automatically created as an integer
} else if(aircraft.getAltBaro() instanceof String baroAltString) {
    // baroAltInt is automatically created as an string    
}
```
or
```java
if (aircraft.getAltBaro() instanceof Integer) {
    Integer baroAlt = (Integer)(aircraft.getAltBaro());
} else {
    String baroAlt = (String)(aircraft.getAltBaro());    
}
```

## Documentation
Documentation is generated from the OpenAPI spec, you can read the generated Markdown documentation 
in the [docs](./docs) directory. 

## Building from Source
To build from source, you will require:
- Java 11+ (some plugins require a version greater than 8, but the package remains Java 8 compatible)
- Maven
- jq (for substituting the server's url into the openapi spec. This can be done manually if jq is not available)