# pytoken
A simple Python library for generating tokens which can be used as cookies or headers in web applications.
## Installation
```bash
pip install pytoken-zzl
```

## Usage
You can set the secret key directly in the `TokenEncoder` class
```python
from pytoken-zzl.token import TokenEncoder

encoder = TokenEncoder('secret')
# life is the time in days that the token will be valid
token = encoder.encode(msg='name', life=1)
print(token)
print(encoder.decode(token))
```
or use the `PYTOKEN_SECRET` environment variable.
```python
from pytoken-zzl.token import TokenEncoder

encoder = TokenEncoder()
token = encoder.encode(msg='name', life=1)
print(token)
print(encoder.decode(token))
```
