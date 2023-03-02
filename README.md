# Stock Price App

### This is a simple web application that displays the stock price of a company in real-time.

## Overview

### The application uses the MVC pattern, dependency injection, the Options pattern, and services to display the stock price of Microsoft Corp. Firstly, a service file was added which contains the logic to retrieve data from the Finnhub API service in JSON format. The app is connected to the API with a unique token which is stored in User Secrets to make it inaccessible from outside. The token value is retrieved in the service class by using the IConfiguration interface's reference. The application also has an additional class to assign the value of Stock Symbol which is stored in appsettings.json. The IOptions pattern is used here to assign the property of the additional class to store the value from appsettings.json. We can fetch data of any company by using its unique Stock Symbol. The methods of services are called from the Controller class by passing the Stock Symbol of the company. After getting data from the API, specific ones are selected and assigned to the properties of the model class which has properties "StockSymbol", "StockName", "Price" and "Quantity". In the Controller, the values of those properties are assigned and passed to the view. In the View, the "Strongly Typed View" approach is used. There is also a JavaScript file in the view to connect to the Finnhub WebSocket and update the stock price in real-time.

## Technologies

###
* C#
* ASP.NET Core
* MVC pattern
* Dependency Injection
* Options pattern
* Razor syntax
* JavaScript
* WebSocket
