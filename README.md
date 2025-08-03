# Authentication Microservice
REST API for the endpoints /register, /login and /validate

**Communication Contract**
## 1) How to request data
The microservice is a REST API that should be run locally. It is configured to run on `http://localhost:3000` but the port can be changed.

### **POST /register**
Registers a new user and returns an authentication token 

### **Example Request**
```js
const response = await fetch("http://localhost:3000/register", {
  method: "POST",
  headers: { "Content-Type": "application/json" },
  body: JSON.stringify({ username: "bob", password: "bob123" })
});
```

### **POST /Login**
If valid credentials are given and user exists, session info is returned 

### **Example Request**
```js
const response = await fetch("http://localhost:3000/login", {
  method: "POST",
  headers: { "Content-Type": "application/json" },
  body: JSON.stringify({ username: "bob", password: "bob123" })
});
```


### **POST /validate**
Returns session infor when valid session exists 

### **Example Request**
```js
const response = await fetch("http://localhost:3000/validate", {
  method: "POST",
  headers: { "Content-Type": "application/json" },
  body: JSON.stringify({ token: "abcd1234" })
});
```

## 2) How to receive data



