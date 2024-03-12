# node-api

Node JS CRUD API example

- [x] store info in JSON file
- [ ] store info in DB (MYSQL)

## Install

```sh
git clone https://github.com/sabovoichita/Birthdays-node-api.git
cd node-api
npm install
```

## JS Usage

```sh
npm run devstart
```

### JSON file as storage

Birthday members are stored inside [data/birthdays.json](data/birthdays.json)

```js
fetch("http://localhost:3000/birthdays-json", {
  method: "GET",
  headers: {
    "Content-Type": "application/json"
  }
});

fetch("http://localhost:3000/birthdays-json/create", {
  method: "POST",
  headers: {
    "Content-Type": "application/json"
  },
  body: JSON.stringify({ firstName: "Your", lastName: "Name", gitHub: "youaredev" })
});

fetch("http://localhost:3000/birthdays-json/delete", {
  method: "DELETE",
  headers: {
    "Content-Type": "application/json"
  },
  body: JSON.stringify({ id: "fedcba1610309909431" })
});

fetch("http://localhost:3000/birthdays-json/update", {
  method: "PUT",
  headers: {
    "Content-Type": "application/json"
  },
  body: JSON.stringify({
    id: "fedcba1610310163146",
    firstName: "UpdatedName",
    lastName: "Name",
    gitHub: "youaredev"
  })
});
```
