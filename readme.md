# Business React Project

This is a simple Node.js Express server that provides several endpoints for managing appointments and user login.

## Getting Started

To get started, you need to have Node.js and npm installed on your machine.

1. Clone the repository
2. Install the dependencies using `npm install`
3. Start the server using `npm start`

now the server run on 8787 port.

## Endpoints

### `POST /login`

Expects a JSON body with `name` and `password` fields. If `name` is "admin" and `password` is "123456", it returns a success message. Otherwise, it returns a failure message.


```bash
curl -X POST -H "Content-Type: application/json" -d '{"name":"admin","password":"123456"}' http://localhost:8787/login
```

### `POST /appointment`

Expects a JSON body with an `dateTime` field. It checks if the time is available and if so, adds a new appointment to the appointments array and returns a success message. If the time is not available, it returns a failure message.

### `GET /appointments`

Returns all appointments.

### `POST /service`

Expects a JSON body. It checks if a service with the same name isn't exist yet. if so, adds a new service to the services array and returns a success message. 

### `GET /services`

Returns all services

### `POST /businessData`

Expects a JSON body with business data. It stores the data and returns it.

### `GET /businessData`

Returns the stored business data.

## objects

### Business Object

The business object contains information about the business:

```javascript
const business = {
    id: "123",
    name: "Coding Academy",
    address: "Rothschild 60 Tel Aviv",
    phone: "03-1234567",
    owner: "Yariv Katz",
    logo: "https://coding-academy.org/images/ca_logo.png",
    description: "The best coding academy in the world",
};
```
### Service Object

The service object contains information about a service:

```javascript
const service = {
    id: "11",
    name: "פגישת ייעוץ פרונטלית",
    description: "פגישת ייעוץ פרטנית בקליניקה"
    price: 500,
    duration: 60,
};
```

### Meeting (appointment) Object

The meeting object contains information about a meeting:

```javascript
const meeting = {
    id: "758",
    serviceType: "11",
    dateTime: "2021-06-20T10:00:00.000Z",//מבנה של תאריך ושעה סטנדרטי בjs
    clientName: "אבי כהן",
    clientPhone: "050-1234567",
    clientEmail: "m@m.com",
};
```