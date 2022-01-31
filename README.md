# otp
```console
usage: otp.py [-h] [-s] key input output

OTP Encryption

positional arguments:
  key                   key file
  input                 input file
  output                output file

optional arguments:
  -h, --help            show this help message and exit
  -s, --secure          prevent key from being re-used
  ```
# keygen
You use the keygen script to generate the key. It uses the python os.urandom() function internally.
```console
usage: keygen.py [-h] size {kb,mb,gb,tb} path

Generate a key file

positional arguments:
  size           size of key file
  {kb,mb,gb,tb}  unit of size
  path           key file
```
- You can also use your own DRBG, seeded from a secondary key. This will reduce the key-length at the cost of weaker encryption.
- Another option is to use a TRNG, with a key-length the size of the message. This offers perfect/maximum encryption.
