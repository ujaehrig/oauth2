# GRANT-TYPES

@ul

- Authorization Code
- Implicit
- Password
- Client Credentials
- Refresh

@ulend

+++

## Authorization Code

@ul
- used for user authorization
- Client doesn't see user credentials
@ulend

+++?image=https://source.unsplash.com/zdSoe8za6Hs

### Authorization Code dance

@ol
- User (resource owner) wants to access his/her data (resource) through a client
- Client redirects to authorization server login page
- User authenticates against Authorization-Server
- Redirect with authorization code back to client application
- Client exchanges the code for an access token using its credentials
@olend

+++

## Implicit

@ul
- not recommended!
- Client doesn't see user credentials
- Authentication at Authorization-Server
- Redirect with *token* to Client
- No Client-Credentials possible 
@ulend

+++

## Password

@ul
- Client & User credentials
- Client knows user credentials
- Authorization Server returns a token
@ulend

+++

## Client 

@ul
- Client credentials *only*
- Authorization Server returns a token
@ulend

+++

## Refresh

@ul
- Optional 
- Refreshes an existing token
@ulend