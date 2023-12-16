# Business React Project

This is a simple Node.js Express server that provides several endpoints for managing appointments and user login.

## Getting Started

To get started, you need to have Node.js and npm installed on your machine.

1. Clone the repository
2. Install the dependencies using `npm install`
3. Start the server using `npm start`

now the server run on 8787 port.

## Endpoints

### `GET /`

Returns a simple "Hello World!" message.

### `POST /login`

Expects a JSON body with `name` and `password` fields. If `name` is "admin" and `password` is "123456", it returns a success message. Otherwise, it returns a failure message.

### `POST /addAppointment`

Expects a JSON body with an `dateTime` field. It checks if the time is available and if so, adds a new appointment to the appointments array and returns a success message. If the time is not available, it returns a failure message.

### `GET /appointments`

Returns all appointments.

### `POST /businessData`

Expects a JSON body with business data. It stores the data and returns it.

### `GET /businessData`

Returns the stored business data.

## Testing

You can test the endpoints using any HTTP client like curl or Postman.