# Introduction:
AIP allows you to retrieve geolocation information for a specified IP address or the IP address of the client making the request. It provides details such as the city, country, continent, ISP (Internet Service Provider), region, and coordinates (latitude and longitude). This API is useful for applications that require location-based functionality or need to customize user experiences based on geolocation data..

# Endpoint:

**URL:** https://carlbot-61041ca.000webhostapp.com/index3.php
**Method:** *GET*

# Parameters:

* `ip` (optional): Specify a custom IP address to retrieve geolocation information for that IP. If not provided, the API will use the IP address of the client making the request.

# Response:

* The API responds with JSON data containing geolocation information for the specified or default IP address.

# Code examples

## LuaU

``` lua
local http = game:GetService("HttpService")
local url = "https://carlbot-61041ca.000webhostapp.com/index3.php"
local response = http:GetAsync(url)
local data = http:JSONDecode(response)

print("City:", data.City)
print("Country:", data.Country)
print("Coordinates:", data.Coords)
```
## PHP

```php
$apiUrl = "https://carlbot-61041ca.000webhostapp.com/index3.php";
$response = file_get_contents($apiUrl);
$data = json_decode($response);

echo "City: " . $data->City . "<br>";
echo "Country: " . $data->Country . "<br>";
echo "Coordinates: " . $data->Coords . "<br>";
```

## JavaScript

```javascript
const apiUrl = "https://carlbot-61041ca.000webhostapp.com/index3.php";
fetch(apiUrl)
  .then(response => response.json())
  .then(data => {
    console.log("City:", data.City);
    console.log("Country:", data.Country);
    console.log("Coordinates:", data.Coords);
  });
```

## Python

```python
import requests

api_url = "https://carlbot-61041ca.000webhostapp.com/index3.php"
response = requests.get(api_url)
data = response.json()

print("City:", data["City"])
print("Country:", data["Country"])
print("Coordinates:", data["Coords"])
```

# Error Handling:

* If an invalid IP address is provided, the API will respond with the following error message:
```json
{
    "error": "IP Invalid, error 4#xm1!"
}
```

* In case there are any issues retrieving geolocation information, the API will respond with the following error message:
* 
```json
{
    "error": "Failed to retrieve geolocation information, error 4#xm2!"
}
```

# Example Usage:

* Retrieve geolocation information for the default IP address:

  Request: `GET https://carlbot-61041ca.000webhostapp.com/index3.php`
  
  Response:
  ```json
  {
    "IP": "192.168.0.1",
    "City": "New York",
    "Country": "United States",
    "Continent": "America/New_York",
    "ISP": "Example ISP",
    "Region": "NY",
    "Coords": "40.7128,-74.0060"
  }
  ``` 

* Retrieve geolocation information for a custom IP address:

  Request: `GET https://carlbot-61041ca.000webhostapp.com/index3.php?ip=123.45.67.89`
  Response: 
    ```json
    {
    "IP": "123.45.67.89",
    "City": "London",
    "Country": "United Kingdom",
    "Continent": "Europe/London",
    "ISP": "Example ISP",
    "Region": "ENG",
    "Coords": "51.5074,-0.1278"
    }
    ```

