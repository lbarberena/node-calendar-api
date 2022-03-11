# Backend MERN - Calendar

Fronend en React: [View Repo](https://github.com/lbarberena/react-calendar-app.git)

## Instructions

- **Test command:** `npm run dev`
- **PORT:** Use a .env.development file with port number 8000
> PORT = 8000

> Server will run on: `http://localhost:8000/api/`

## Endpoints

- `/auth`: POST method to login (requires: email: string & password: string).
- `/auth/new`: POST method to register new users (requires: email: string, name: string & password: string).
- `/auth/renew`: GET method to renew the auth token.
- `/events`: GET method, will response with all existing events.
- `/events`: POST method to save a new event (requires: title: string, notes: string, start: Date, end: Date).
- `/events/{eventId}`: GET method, will response with an event based on the event id.
- `/events/{eventId}`: PUT method to edit an event (requires: title: string, notes: string, start: Date, end: Date).
- `/events/{eventId}`: DELETE method to erase an specific event.

### Example Auth's endpoints responses
```
{
  "ok": true,
  "uid": "622aa3f7c5269009d31aa7da",
  "name": "My Name",
  "token": "token goes here"
}
```

### Example event's endpoints responses (GET)
```
{
  "ok": true,
  "eventos": [
    {
      "id": "622aa5c3c5269009d31aa7db",
      "title": "First event",
      "notes": "Just the notes of the event",
      "start": "2022-03-11T00:40:52.207Z",
      "end": "2022-03-11T02:40:52.207Z",
      "user": {
        "_id": "622aa3f7c5269009d31aa7da",
        "name": "My name"
      }
    }
  ]
}
```

### Example event's endpoints responses (GET)
```
{
  "ok": true,
  "eventos": [
    {
      "id": "622aa5c3c5269009d31aa7db",
      "title": "First event",
      "notes": "Just the notes of the event",
      "start": "2022-03-11T00:40:52.207Z",
      "end": "2022-03-11T02:40:52.207Z",
      "user": {
        "_id": "622aa3f7c5269009d31aa7da",
        "name": "My name"
      }
    }
  ]
}
```

### Example event's endpoints responses (POST & PUT)
```
{
  "ok": true,
  "evento": {
    "title": "First event",
    "notes": "Just the notes of the event",
    "start": "2022-03-11T00:40:52.207Z",
    "end": "2022-03-11T02:40:52.207Z",
    "user": "622b760da735a211c5e695ff",
    "id": "622b9157bb9d2316588689b8"
  }
}
```

### Example event's endpoints responses (DELETE)
```
{
  "ok": true,
  msg: 'Event successfully deleted'
}
```
