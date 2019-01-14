# GRANT-TYPES

## Standard Grant Types

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
- Client doesn't see user credentials
- Authentication at Authorization-Server
- Redirect with code to Client 
- Client requests token with client credentials
@ulend

+++

# Implicit

@ul
- not recommended!
- Client doesn't see user credentials
- Authentication at Authorization-server
- Redirect with token to Client
- No Client-Credentials possible 
@ulend

+++

# Password

@ul
- Client & User credentials
- Client knows user credentials
- Authorization Server returns a token
@ulend

+++

# Client 

@ul
- Client credentials *only*
- Authorization Server returns a token
@ulend

+++

# Refresh

@ul
- Optional 
- Refreshes an existing token
@ulend