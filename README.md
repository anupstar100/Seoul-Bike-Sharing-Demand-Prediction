# Seoul-Bike-Sharing-Demand-Prediction

## ***Problem Statement***
Data provided by Seoul Bike Sharing Company. These public bikes are made available to the persons who are 15 and older. Seoul bike docking stations are equipped in excessive traffic areas including subway entrances/exits, bus stops, residential complexes, public offices, schools, and banks. Docking stations are computerized stands for the purpose of pickup and drop off of the rental bikes. Users of Seoul public bikes can rent and return
rental bikes at any docking station.

The main objective is to build a model which can predict the number of bikes required each hour. This would help the company to made bike available for rent on the basis of future demand.
## ***Introduction***
In a span of few decades, the sharing of bicycle system has seen enormous growth (Fishman, 2016). This system is a recently developed transportation system which provides people with bicycle for common use. Bicycle system provides user to rent a bike from one docking station, where user can ride and then return in another docking station. Amsterdam in Netherlands was the one where initial bicycle sharing system has started in 1965 (Shaheen, Guzman, & Zhang, 2010). Main motive of the system was to focus on environmental and social welfare. With enormous advancement of Intelligent Transportation System and information technology after 2000s, this bicycle system employed globally. Situation over decade has changed in sharing bicycle. Today it is much easier for the public to rent bicycles. Global Positioning System enabled mobile application allows people to know the nearby bicycle station for renting the bicycle.

Till today there are more than 50 countries having 712 which implemented bicycle sharing method (Shaheen, Martin, Cohen, Chan, & Pogodzinski, 2014). They have now found to be important face of transportation system in major cities due to several factors such as health problems, heavy traffic and environmental conditions. Bike sharing Systems namely OFO and Mo-bike in places like Beijing has enabled people to find position of unused bicycle and use them. Once the bicycle is used, it can be locked at any docking station across the city. For expanding availability of bicycle for public use, the operators running this service allocate a truck that collects bicycles parked in various station and relocate them to the original station gradually (Schuijbroek, Hampshire, & Van Hoeve, 2017). There are number of policy issues involved in the management of intelligent bicycle sharing system (Gast, Massonnet, Reijsbergen, & Tribastone, 2015).

Many countries have bike sharing system, such as Ddareungi is a bike sharing system in South Korea, which started in the year 2015, known as Seoul bike in English. It was started to overcome issues like greater oil prices, congestion in traffic and pollution in the environment and to develop a healthy environment for citizen of Seoul to live. Han River is the initial place where Ddareungi was first started on October 2015 in Seoul, few months later, total number of bike – sharing station touched 150 with as much as 1500 were there. In order to cover the entire people in Seoul, in 2016 there is a gradual incline in number of docking station. As large as 20,000 bikes were made available which was confirmed by Seoul Mayor Park won-soon. With the help of growing technologies, Seoul city is now equipped with 1500 bike renting station which are operational round the clock. With the help of internet-enabled device or mobile phone, people can know the number of bikes available for the people to rent. Bike are locked which can be unlocked with the help of password which people accessing to it will receive the password through mail. Users are allowed and can rent and leave the bike in any station. Seoul Rental Bikes are built to be utilized by all kinds of people including women, elderly persons and infirm. Seoul Bikes are manufactured using durable and light-weight materials. This giving user more stability in driving and convenience. Users can verify their trip details (distance, duration) and measure of bodily activities (burnt calories) at My Page > Usage Details. With this kind of smart technology and convenience, the use of Rental bike is increasing every day. So, there is a need to manage the bike rental demand and manage the continuous and convenient service for the users. This study proposes a data mining-based approach including weather data to predict whole city public bike demand. A rule-based model is used to predict the number of rental bikes needed at each hour. The following figure presents the picture of rental bike stations in Seoul.
## ***Attribute Inforamation***
  * *Date:* Year – Month – Day.
  * *Rented Bike Count:* Count of bikes rented each hour (our dependent variable).
  * *Hour:* Hour of the day.
  * *Temperature:* Temperature of the day in ℃.
  * *Humidity:* Humidity of the day in %.
  * *Windspeed:* Speed of the wind in 𝑚/𝑠𝑒𝑐.
  * *Visibility:* Visibility within 10 𝑚 range.
  * *Dew Point Temperature:* In ℃.
  * *Solar Radiation:* In 𝑀𝐽/𝑚2.
  * *Seasons:* Winter, Spring, Summer, Autumn.
  * *Holiday:* Holiday or No Holiday.
  * *Functional Day:* No Funct (Nonfunctional hours), Fun (Functional Hours)

## ***Reason for Bike Renting System***
This system is designed to help the customers to take bikes or two-wheelers for rent. When we go on any trip outside the town or country, we want to be free of time so instead of going through metros and taxis, we prefer to have our own vehicle for rent.

Using this system vehicle owners can register as sellers and customers who want to take bikes on rent can register themselves as renters and can take any bike on rent. Address of the both are required as the customer can only take bike by going to the address provided and the vehicle owners can know the address that a customer is verified or not. The customer also has to upload some proofs to take the bike on rent.

## ***Diagnosing the DataFrame***
By diagnosing the DataFrame, we got the following
  * There are 14 features with 8760 rows of data.
  * There are 4 categorical columns and 10 numerical columns.
  * Columns ‘Date’, ‘Seasons’ and ‘Functioning Day’ are of 𝑜𝑏𝑗𝑒𝑐𝑡 data type
  * Columns ‘Rented Bike Count’, ‘Hour’, ‘Humidity (%)' and ‘Visibility (10𝑚)' are of 𝑖𝑛𝑡64 data type
  * Columns ‘Temperature Temperature (℃)’, ‘Wind Speed (𝑚/𝑠)’, ‘Dew Point Temperature (℃)’,‘Solar Radiation (𝑀𝐽/𝑚2)’,‘Rainfall (𝑚𝑚)' and ‘Snowfall(𝑐𝑚) are of 𝑓𝑙𝑜𝑎𝑡64 data type

## ***Exploratory Data Analysis and Visualization***
  1. There are no null values.
### *2. Correlation:*
  1. We can see that with our targer variable (Rented Bike Count), the most correlated variables are:
  * Hour
  * Temperature
  * Dew point temperature
  * solar radiation
  2. Dew point tempearture is highly correlated with our target variable. This can cause multicolinearity problem in future. So, we can drop it.

### *3. Rented Bikes Count wrt Date:*
  1. There is a high raise between april to automn of bikes rent i.e., in Summer.
  2. The main reason is:
  * Temperature: In case of temperature, in summer, temperature is high. So, korean people migh like driving bike in summer when the day is hot.
  * Humidity: In case of humidity, the spread in all four seasons is almost equal. So, maybe humidity is not a big factor.
  * Wind Speed: In case of wind sppe, the values are almost equal.
  * Visiability: In case of visibility, the values are almost same.
  * Solar Radiation: In case of soalr radiation, in summer, solar radiation is high. So, korean people might like driving a when the solar radiation is high.
  * Snowfall: In summer, snowfall is 0 which is obvious. So, it might not a big factor.
