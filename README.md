this is just exercise that i did when learning fullstack engineer at codecademy. therefore, the whole code wasnt mine. i only put a few lines to complete exercise

goal of this exercise is to apply what i've learn abt preventions for xss attacks.

what i've done in this exercise:

*data validation and sanitization*
1. add check function from express-validator in app.js' top section
2. i then add middleware to validate email and restaurant info in the /review endpoint

*protecting the DOM*
3. change a code in home.ejs from this:
document.write("<b>Current URL</b> : " + document.baseURI);
- to this:
document.getElementById("urlinfo").textContent = document.baseURI;
4. add "<b>Current URL</b><span id="urlinfo"></span>" in body section

5. add a cookie object to the existing session in app.js' app.use part: httpOnly and secure
6. implement the helmet middleware at app.js' top section: const helmet = require('helmet'); and then add app.use(helmet()); to use it
