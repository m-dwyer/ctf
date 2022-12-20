# Notes

Hint is in the name of the challenge, and also the Red/Blue buttons.
No notable request or response headers, but the Red button sends a GET /index.php, whereas the blue button does a POST /index.php

```bash
$curl -I http://mercury.picoctf.net:53554/index.php
HTTP/1.1 200 OK
flag: picoCTF{r3j3ct_th3_du4l1ty_2e5ba39f}
Content-type: text/html; charset=UTF-8
```
