# Notes

Download the pcap file, open in wireshark and filter on http.

I then found this in a plain text HTTP response for the line-based text-data:

```
cvpbPGS{C33XNO00_1_f33_h_qrnqorrs}
```

This looked like a flag, and character frequency made me suspect a caesar cipher.
After applying a few shifts, it's ROT13:

picoCTF{P33KAB00_1_s33_u_deadbeef}
