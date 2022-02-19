# api-docs

## Basic
- `/login` POST
Receives `email` and `password` from `data` in `application/json` format. Returns a token and `organizer_id` associated w/ the acccount.

## Organizer
- `/organizer` POST
**Organizer Registration** Receives info and creates a new organzier. Returns success message on completion.
```
data: {
  "name": "string",
  "password": "string",
  "email": "string",
  "type": "string"
}
```

## Event
- `/event/<id>` GET
**Event Details** Fetches event details of the event with `id`. Returns the data as below:

- `/event/` POST
**Event Registration** Receives event info and creates a new event. Returns success message on completion
```
data: {
  "name": "String"
  "start_time": "date-time"
  "end_time": "date-time"
  "description": "string"
  "banner": "string"
  "type": "string"
  "privacy": "string"
  "tags": "string"
  "ticket_price": "number"
  "promote": "string"
  "email_filter" : "string"
}
```
