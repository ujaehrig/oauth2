# Introduction

+++

# Why?

@ul
- Distributed systems also need a security layer @note[no single security context like in a monolith, making sure only allowed services can access each other]
- A standardized (RFC6749) framework
@ulend

+++
@snap[north]
# Terms
@snapend

@snap[west fragment]
## @css[transition](Players)

@ul

- Resource Owner @note[An entity capable of granting access to a protected resource. E.g. the end-user]
- Client @note[An application making protected resource requests on behalf of the resource owner]
- Resource Server @note[The server hosting the protected resources]
- Authorization Server @note[A server issuing access tokens to the client after authenticating the resource owner]
@ulend
@snapend

@snap[east fragment]
## Items

@ul
- access token @note[a token issued from Authorization server used as a key to access resources]
- refresh token @note[renew access token without re-authenticating again]
- authorization code @note[a temporary, one use code used during authorazation_code workflow]
@ulend
@snapend

+++ 
# Terms

## Items
@ul
- access token @note[a token issued from Authorization server used as a key to access resources]
- refresh token @note[renew access token without re-authenticating again]
- authorization code @note[a temporary, one use code used during authorazation_code workflow]
@ulend

+++

# Protocol Flow
![Protocol flow](assets/img/abstract%20OAuth2%20protocol%20flow.png)

