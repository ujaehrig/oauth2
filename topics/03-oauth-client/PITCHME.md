# OAuth Client

@ul

- An OAuth Client represents the accessing service @note[All services interacting with Authorization server, whether they retrieve tokens or just verify them are clients]
- OAuth Clients can request a token alone or behalf of a user 
- OAuth Clients may (and should) be limited to special grant-types @note[example: not allowing user authentication flows for non-user related services (e.g. betting import)]
- Scopes (default or subset) 

@ulend