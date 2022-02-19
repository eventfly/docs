# api-docs

## /*
#### /login
- GET: Not allowed
- POST: Match login creds through provided data and return basic info as below respectively
```
data: {
  "email": string
  "password": string
}
```
```
data: {
  id : number
  name: string
  email : string
}
```

#### /register
- GET: Not allowed
- POST: Get data as below and create a new organizer/staff accordingly
```
data: {
  name: string
  email: string
  password: string
  type: "organizer"/"staff"
}
```

#### /logout
- GET: Not allowed
- POST: Just send a blank POST request. The logout mainly happens in frontend

***

## /organizer/*
#### /organizer
- GET: Return a list of all organizers
- POST: Not allowed

#### /organizer/<id>
- GET: Get details of the organizer with that ID
- POST: Not allowed

***
  
**Under Update**
## /event/*
#### /event/?organizer_id=
- GET: Return a list of all events under that organizer w/ ID. If organizer not specified, return all events.
- POST: Create a new event with data
```
data: {
  name: string,
  start_time: string
  end_time: string
  description: string
  banner: string
  type: "online"/"offline"
  privacy: "public"/"private"
  tags: list(string)
  ticket_price: number
  promote: "yes"/"no"
  email_filter: string
}
```
  
#### /event/<id>
- GET: Return event details w/ that event ID
- POST: Not allowed
  
#### /event/<id>/add-staff
- GET: Not allowed
- POST: Add staff under that event from data
```
data: {
  email: string
}
```

***
  
## /staff/*
#### /staff
- GET: Get list of all staff
- POST: Not allowed
  
#### /staff/<id>
- GET: Return staff details w/ that staff ID
- POST: Not allowed
  
