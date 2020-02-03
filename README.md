# af-backend-node

https://documenter.getpostman.com/view/9228779/SWTEbbBB?version=latest

BASE URL https://africa-leighton-repo.herokuapp.com/

Endpoints below

## AUTHORIZATION

---

REGISTER
Post

/auth/register

{
"username" : "bob",
"password" : "password",
"department" : "seller"
}

## NOTE - Must register as either buyer or seller

LOGIN
Post

/auth/login

{
"username" : "bob",
"password" : "password",
"department" : "seller"
}

## NOTE - Must login as either buyer or seller

## USER ROUTES

---

Get list of all users
Token required

## /users/

Get a single user by id
Token required

## users/:id/

Get specific user's items
Token required

## users/:id/items/

Delete a single user
Token required

## users/:id/

## ITEMS ROUTES

---

Get a list of all items
Token required

## /items

Get a single item
Token required

## /items/:id

Adds an item to the database
Must have a user-id. The other key value pairs are optional
Token required

Post
/items/additem/

{"name": "rocks",
"description": "bash it down",
"price": "456",
"location": "Congo",
"category": "spam",
"URL": "https://fake",
"user_id": 7
}

---

update/edit a single item
compare the change to post above.
Token required

/items/:id

{"name": "rocks",
"description": "bash it down to the ground fafsf",
"price": "45667",
"location": "Sauti",
"category": "spam",
"URL": "https://fakedsdsadsdasdasdasasfasfsaaaaaaaaaaaaaadas",
"user_id": 7
}

---

Deletes a single item
Token required
/items/:id

---

Get all items in a category
Token required

/items/category/:category
