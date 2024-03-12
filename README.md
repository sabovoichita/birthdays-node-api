Node JS CRUD API example

- [x] store info in JSON file
- [x] store info in DB (MYSQL)

## Install

    npm run devstart

Team members are stored inside [data/birthday.json](data/birthday.json)

```js
// GET birthdays-json
fetch("http://localhost:3000/birthdays-json", {
  method: "GET",
  headers: {
    "Content-Type": "application/json"
  }
});

// POST birthdays-json/create
fetch("http://localhost:3000/birthdays-json/create", {
  method: "POST",
  headers: {
	@@ -39,6 +41,7 @@ fetch("http://localhost:3000/birthdays-json/create", {
  body: JSON.stringify({ firstName: "Your", lastName: "Name", gitHub: "youaredev" })
});

// DELETE birthdays-json/delete
fetch("http://localhost:3000/birthdays-json/delete", {
  method: "DELETE",
  headers: {
	@@ -47,6 +50,7 @@ fetch("http://localhost:3000/birthdays-json/delete", {
  body: JSON.stringify({ id: "fedcba1610309909431" })
});

// PUT birthdays-json/update
fetch("http://localhost:3000/birthdays-json/update", {
  method: "PUT",
  headers: {
	@@ -60,3 +64,12 @@ fetch("http://localhost:3000/birthdays-json/update", {
  })
});
```

### DB (MySQL) as storage

Team members are stored mysql

- configure user & pass for mysql connection [routes/birthdays-db.js](routes/birthdays-db.js)
- create a database named **birthdays**
- run [http://localhost:3000/birthdays/install](http://localhost:3000/birthdays/install)
- now you can any other CRUD operations (the same as for json but change url "birthday-json" -> "birthdays")
