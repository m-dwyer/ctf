# Notes

full string = "picoCTF{1n_7h3_|<3y_of_xxxxxxxx}

Magic happens in the check_key() function

1. Check length of user-entered key matches "MORTON"
2. The script expects start of entered key to match picoCTF
3. we check subsequent characters in entered key against sha256 hex digest of "MORTON":

```python
>>> import hashlib
>>> import base64
>>> username_trial = b"MORTON"
>>> digest = hashlib.sha256(username_trial).hexdigest()
'281f75c0145b05e6ccbeecc66a61614d8c974c1a49356c118fcbab4735862fea'
>>> digest[4] + digest[5] + digest[3] + digest[6] + digest[2] + digest[7] + digest[1] + digest[8]
'75fc1081'

```

we enter key picoCTF{1n_7h3_|<3y_of_75fc1081}, which creates a new keygenme.py.  This is also the flag.
