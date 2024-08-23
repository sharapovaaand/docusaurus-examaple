---
title: Step 1. Creating the application
---

Let's start by creating the application and the project directories. 

1. Create a directory named `node-dev` and inside it a subdirectory named `apps`. ``
2. Inside `~/node-dev/apps` create a file named  `server.js` with the following content:
```javascript
import express from "express";

const app = express();
const PORT = 80;

app.listen(PORT, () => console.log(`Server is listening to PORT ${PORT}`));

app.get("/", (req, res) => {
  res.send("Test server is running!");
});
```

   This is a simple Express server that we will use to test our development environment.

3. Inside `~/node-dev/apps` create a file named  `package.json` with the following content:
```yaml
{
"name": "node-dev",
    "version": "1.0.0",
    "type": "module",
    "scripts": {
        "dev": "nodemon server.js localhost 80"
    },
    "dependencies": {
        "express": "^4.18.2"
    },
    "devDependencies": {
        "nodemon": "^2.0.22"
    }
}
```
We will launch our server using the `nodemon` tool that will make it restart automatically whenever you change your code.

There is no need to install the dependencies now because we will do it later inside the container.