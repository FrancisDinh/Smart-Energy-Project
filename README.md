# READ ME

This project was submitted for the Fachpraktikum at IAAS Uni Stuttgart.

Title: Smart Energy - Demand and Response

Author: Muralikrishna Thulasi Raman and Tung Dinh

For more information, please refer to the [report]([https://github.com/FrancisDinh/Smart-Energy-Project/blob/master/Final%20Report.pdf](https://github.com/FrancisDinh/Smart-Energy-Project/blob/master/Final%20Report.pdf))

## Summary:


## Components
### Weather Service 
Get weather data from Weatherbit.io for estimated generated energy from renewable modules

### Supply Service
Use data from Weather Service and calculates energy generated from Simulated Wind Turbine and PV components, stores them in  the Database and gives data to the requested module. Apart from these,  it updates, stores and retrieves battery data. 

### Demand Service
Get building’s energy consumption for both controllable and non-controllable devices. Also, new buildings and devices can  be added into the system through this service. 

### Pricing Unit
Providing dynamic prices from  [entsoe]([https://transparency.entsoe.eu/transmission-domain/r2/dayAheadPrices/show?name=&defaultValue=false&viewType=TABLE&areaType=BZN&atch=false&dateTime.dateTime=29.06.2019+00:00|CET|DAY&biddingZone.values=CTY|10Y1001A1001A83F!BZN|10Y1001A1001A82H&dateTime.timezone=CET_CEST&dateTime.timezone_input=CET+(UTC+1)+/+CEST+(UTC+2)](https://transparency.entsoe.eu/transmission-domain/r2/dayAheadPrices/show?name=&defaultValue=false&viewType=TABLE&areaType=BZN&atch=false&dateTime.dateTime=29.06.2019+00:00|CET|DAY&biddingZone.values=CTY|10Y1001A1001A83F!BZN|10Y1001A1001A82H&dateTime.timezone=CET_CEST&dateTime.timezone_input=CET+(UTC+1)+/+CEST+(UTC+2)))

• For current hour  
• For current day’s 24 hours
• For next day’s 24 hours  
• Forecast for the next 24 hours

### Optimization 
Use data from Supply Service, Demand Service and Pricing  Unit to optimize the system towards the goals. Gurobi is used to solve math model of the system, and output profit for stakeholers, billing for users, operation schedule for controllable devices (start, stop time), battery status and battery energy level. 

### User Interface
Use NUXT JS and Vuetify  to obtain information from  user and also to display information from Supply Service, Demand Service,  Pricing Unit and Optimization unit

## License
[MIT](https://choosealicense.com/licenses/mit/)
