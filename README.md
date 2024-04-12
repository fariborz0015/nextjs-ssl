
<p align="center">
  <a href="https://github.com/fariborz0015/Nest-Telegram-Bot" target="blank"><img src="https://github.com/fariborz0015/nextjs-ssl/blob/main/cover.png"  alt="Nest Logo" /></a>
</p>

# Next.js HTTPS Server In Local & Development Mode

A `Node.js` server file that uses the `Next.js` for run server on a `HTTPS` protocol in local and devvelopment mode 
## Get Start

1. Clone the repository:

```bash
git clone https://github.com/fariborz0015/nextjs-ssl.git
```

2. Copy files:
- copy `ssl` folder and `server.js` file in to your root project 

3. Modify  `package.json`  file `script` section like this : 

from this : 
```json 
  "scripts": {
    "dev": "next dev",
    "build": "next build",
    "start": "next start",
    "lint": "next lint"
  },
```

to this :
```json
  "scripts": {
    "dev": "next dev",
    "dev:ssl":"node server", // add this line 
    "build": "next build",
    "start": "next start",
    "lint": "next lint"
  },

```
then run :
```bash
npm rundev:ssl
```
&nbsp; &nbsp; &nbsp; This will start the HTTPS server on the specified port and hostname.

4. Alternative way to `step 3` :
   
&nbsp;&nbsp;  you can without change the `package.js` run this `cli` command:
```bash 
node server.js
```
&nbsp; &nbsp; &nbsp; This will start the HTTPS server on the specified port and hostname.

## Config 

To Config the server runner you can change this variables in `server.js`:

```js
const { createServer } = require("https");
const { parse } = require("url");
const next = require("next");
const { readFileSync } = require("fs");

const dev = process.env.NODE_ENV !== "production";
const hostname = "localhost"; // host name 
const port = 20000;  // your wanted port 


```


## Contact
For any questions or inquiries, please reach out to the project maintainer:

 [![MIT License](https://img.shields.io/badge/Gmail-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:Fariborz0015@gmail.com)
 [![MIT License](https://img.shields.io/badge/Telegram-2CA5E0?style=for-the-badge&logo=telegram&logoColor=white)](https://t.me/fariborzjs)



Feel free to open an issue on GitHub if you encounter any problems or have suggestions for improvement.

Happy coding! 👨‍💻
## Authors

- [@fariborz0015](https://www.github.com/fariborz0015)

 


 
