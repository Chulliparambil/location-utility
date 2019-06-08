# location-utility

## Description:
The utility will allow you to search for locations and also list places for the same. It also allows to search for location based on category, type and other location related attributes.

Default Port: 8081

## Installation:

**Pre-requisites:**
Install the following on your machine
- Java 1.8
- Git
- Maven

Clone the repository on your local machine and run the following commands to start the application:

##### Build the application without test-cases
``` mvn clean install -DskipTests```
##### Run the application
``` mvn spring-boot:run```
##### Run tests
``` mvn test```


## API endpoints

#### Search for location by name
Returns location details like city,state,country etc.
> GET : http://localhost:8081/api/location/getLocationByName/

**Parameters:**
- name: (Required) name of location passed in path
e.g. http://localhost:8081/api/location/getLocationByName/chicago

#### Get place details
Returns a list of places for a given location with specified attributes like category,radius,searchQuery.
> POST: http://localhost:8081/api/location/getPlaces

**Parameters:**
- name: (Required) name of location
- categoryId: (Optional) Category  id for a category obtained from category API.
- radius: (Optional) Radius in meters for bring places in and around that radius of given location.
- limit: (Optional) Limit the number of records to fetch.
- searchQuery:(Optional) Search text will be applied on the list of places obtained.
- categoryName: (Optional) Search for place by category name.

## LOCATION PROVIDER SERVICE
Using FOURSQUARE place APIs for fetching location details.
> Link for reference: https://developer.foursquare.com/places-api
