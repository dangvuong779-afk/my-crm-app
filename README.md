p# my-crm-app
Demo Node.js app for Render deployment
// index.js
const express = require("express");
const app = express();
const PORT = process.env.PORT || 3000;

app.get("/", (req, res) => {
  res.send("🚀 Hello! App CRM chạy thành công trên Render");
});

app.listen(PORT, () => {
  console.log(`✅ Server is running on port ${PORT}`);
});
{
  "name": "my-crm-app",
  "version": "1.0.0",
  "description": "Demo Node.js app for Render deployment",
  "main": "index.js",
  "scripts": {
    "start": "node index.js"
  },
  "dependencies": {
    "express": "^4.18.2"
  }
}
services:
  - type: web
    name: my-crm-app
    env: node
    plan: free
    buildCommand: "npm install"
    startCommand: "npm start"
