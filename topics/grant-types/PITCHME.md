# GRANT-TYPES

@ul

- Authorization Code
- Implicit
- Password
- Client Credentials
- Refresh

@ulend

+++?image=https://source.unsplash.com/zdSoe8za6Hs

# Authorization Code

@ul
- OAuth dance
- server doesn't see user credentials
- authentication at authorization-server
- redirect with code to server 
- server requests token with client credential
@ulend

+++

# Implicit

@ul
- not recommended
- server doesn't see user credentials
- authentication at authorization-server
- redirect with token to server 
@ulend

+++

# Password

@ul
- Client & User credentials
- Server knows user credentials
- returns a token
@ulend

+++

# Client Credentials

@ul
- Client credential *only*
- returns a token
@ulend

+++

# Refresh

@ul
- optional 
- refreshes an existing token
@ulend