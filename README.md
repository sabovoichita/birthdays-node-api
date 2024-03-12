Node JS CRUD API example

- [x] store info in JSON file
- [x] store info in DB (MYSQL)

## Install

    @@ -24,13 +24,15 @@ npm run devstart

Team members are stored inside [data/team.json](data/team.json)

```js
// GET teams-json
fetch("http://localhost:3000/teams-json", {
  method: "GET",
  headers: {
    "Content-Type": "application/json"
  }
});

// POST teams-json/create
fetch("http://localhost:3000/teams-json/create", {
  method: "POST",
  headers: {
	@@ -39,6 +41,7 @@ fetch("http://localhost:3000/teams-json/create", {
  body: JSON.stringify({ firstName: "Your", lastName: "Name", gitHub: "youaredev" })
});

// DELETE teams-json/delete
fetch("http://localhost:3000/teams-json/delete", {
  method: "DELETE",
  headers: {
	@@ -47,6 +50,7 @@ fetch("http://localhost:3000/teams-json/delete", {
  body: JSON.stringify({ id: "fedcba1610309909431" })
});

// PUT teams-json/update
fetch("http://localhost:3000/teams-json/update", {
  method: "PUT",
  headers: {
	@@ -60,3 +64,12 @@ fetch("http://localhost:3000/teams-json/update", {
  })
});
```

### DB (MySQL) as storage

Team members are stored mysql

- configure user & pass for mysql connection [routes/teams-db.js](routes/teams-db.js)
- create a database named **teams**
- run [http://localhost:3000/teams/install](http://localhost:3000/teams/install)
- now you can any other CRUD operations (the same as for json but change url "teams-json" -> "teams")
