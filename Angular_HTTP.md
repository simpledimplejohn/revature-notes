# Working with Http Requests in Angular

## Setup
- AppModules import HttpClientModule and add to imports array
- Inject into service by adding to the constructor `constructor(private http: HttpClient) { }`
- import Observable to the service

## Methods
- HttpClient.get() 