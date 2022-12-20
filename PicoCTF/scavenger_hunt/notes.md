# Notes:

```bash
curl -v http://mercury.picoctf.net:27278/

<!-- Here's the first part of the flag: picoCTF{t --
```

```bash
curl -v http://mercury.picoctf.net:27278/mycss.css

/* CSS makes the page look nice, and yes, it also has part of the flag. Here's part 2: h4ts_4_l0 */
```

```bash
curl -v http://mercury.picoctf.net:27278/robots.txt

# Part 3: t_0f_pl4c
# I think this is an apache server... can you Access the next flag?
```

Ran gobuster:

```bash
gobuster dir -u http://mercury.picoctf.net:27278/ -w /usr/share/wordlists/dirb/common.txt
```

found .htaccess:

```bash
# Part 4: 3s_2_lO0k
# I love making websites on my Mac, I can Store a lot of information there.
```

From the hint above, I tried:

```bash
$curl http://mercury.picoctf.net:27278/.DS_Store
Congrats! You completed the scavenger hunt. Part 5: _a69684fd}
```

picoCTF{th4ts_4_l0t_0f_pl4c3s_2_lO0k_a69684fd}
