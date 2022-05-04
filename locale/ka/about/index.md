---
layout: about.hbs
title: პროექტის შესახებ
trademark: სავაჭრო ნიშანი
---

# Node.js-ის შესახებ®

როგორც ასინქრონული მოვლენებზე ორიენტირებული JavaScript-გარემო, Node.js შექმნილია 
მასშტაბირებადი ქსელის აპლიკაციების შესაქმნელად. ქვემოთ მოცემულია მაგალითი "გამარჯობა სამყარო",
რომელსაც შეუძლია ერთდროულად დაამუსაოს ბევრი კავშირი. ყოველი კავშირისთვის გამოიძახება გამოძახების 
ფუნქცია, თუმცა, როდესაც კავშირები არ არის, Node.js გადადის ძილის რეჟიმში.

```javascript
const http = require("http");

const hostname = "127.0.0.1";
const port = 3000;

const server = http.createServer((req, res) => {
  res.statusCode = 200;
  res.setHeader("Content-Type", "text/plain");
  res.end("Hello World\n");
});

server.listen(port, hostname, () => {
  console.log(`Server running at http://${hostname}:${port}/`);
});
```