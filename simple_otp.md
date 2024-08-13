Description:
```
We all know OTP is unbreakable...
```

We are provided with a file named main.py with the content:

```
import random

encoded_with_xor = b'\x81Nx\x9b\xea)\xe4\x11\xc5 e\xbb\xcdR\xb7\x8f:\xf8\x8bJ\x15\x0e.n\\-/4\x91\xdcN\x8a'

random.seed(0)
key = random.randbytes(32)
```

The variable `encoded_with_xor` is the flag, but using XOR, it has been encoded. So to get the flag, we have to decode it.

A simple script to add at the bottom to decode this is:
```
decoded_data = bytes([b ^ k for b, k in zip(encoded_with_xor, key)])
print(decoded_data)
```
The `decoded_data` stores the final value, and the print statement will print the decoded string which is our flag.
`b'LITCTF{sillyOTPlol!!!!sdfsgvkhf}'` : This will be printed out.

So the flag is: `LITCTF{sillyOTPlol!!!!sdfsgvkhf}`
