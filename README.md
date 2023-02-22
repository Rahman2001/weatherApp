# weatherApp
### Framework : Spring Boot
### Description
This is a web application allowing users to request a weather forecast either for their current location (locates city by their IP address) or by indicating any city.
The motivation in this project is to learn builing multimodular application that can interact with each other using Retrofit.

### Challenges faced :
- [x] Learning new technologies, their benefits and implementations
- [x] Dividing responsibilities to each module and their implementations
- [x] Making an application asynchronous and event driven
- [x] Making database to automatically self - update/insert data to keep weather data fresh
- [x] Doing appropriate tests (integration test) on application components

### Solution used for each challenge:
- [x] Reading official documentations, analysing other developers' solutions and implemenations
- [x] Getting familiar with some design patterns for 'Clean Code' and understanding logic behind them
- [x] Analysing other developers' solution and implementing `CompletableFuture` API 
- [x] Using `SchedulingConfigurer` interface to dynamically schedule database operations in which it invokes internal `HTTP` clients to get weather data from external source after which it updates or/and inserts those data into database
- [x] Could do integration tests by understanding the concept of this test

### Technologies used : Retrofit, OkHttp client, Flyway Migration Tool

### Modules of application : 
- Web Module
- DataLogic Module
</br></br></br>
## Web Module
### Description 
This module is responsible for UI and user interactions only. Through this module, users can view weather forecasts and make a request for a particular city's weather forecast.
Although the UI is not implemented yet, it is possible to make request through Postman. 
### Link to module :  See [Web Module](https://github.com/Rahman2001/web/tree/fbb1c3c05222f02b9045884bb289320728ff0d15)
</br></br>
## DataLogic Module
### Description
This module is responsible for all the operations with data : 
- Data requesting from external source
- JSON processing (deleting, inserting, time zone converting, etc.)
- Database persistency (updating, inserting, deleting)

Through this module, users get weather forecasts. This module uses `Web` module to accept user requests and returns data in JSON format back to Web module where users can see weather forecasts.
 ### Link to module :  See [DataLogic Module](https://github.com/Rahman2001/dataLogic/tree/e67645b6768aabb804b31c5bfc4cd751d21efc6b)
 </br></br>
 ## Open Source API used 
 - [OpenWeatherAPI](https://openweathermap.org/api)
 - [Ip-API](https://ip-api.com/docs/api:json)
 - [Ip detection API](http://checkip.amazonaws.com/)
 - [Other resources used for this project](https://drive.google.com/file/d/1n6F8Nxtxitkq-jxO3bRlINtse1izqNUx/view?usp=share_link)
