# Permissions

@ul

- Scopes
- Authorities

@ulend

+++

# Scopes

@ul

- Defined in RFC
- OAuth Client *only*
- Allowed scopes defined on Auth-Server

@ulend

+++

# Authorities

@ul

- Spring Security specific
- Defined on OAuth Client and User
- Client Authorities *only* used for client grant-type
- User authorities overwrite Client Authorities 

@ulend

+++

# Access

@ul
- Spring Security
- on method level
- on endpoint (any URI/HTTP method combination)
- SpEL @note[Spring Expression Language]
@ulend

+++

## Method 

@ul

- Enabled with `@EnableGlobalMethodSecurity`
- @PreAuthorize @note[SpEL might be used ]
- @PostAuthorize
- @Secured / @RolesAllowed @note[@RolesAllowed is like @Secured, but JSR-250]
- @PreFilter / @PostFilter

@ulend

+++

```java
@PreAuthorize("#username == authentication.principal.username")
public void someMethod(String username) {
    ...
}
```

+++

## Endpoint

@ul

- Enabled with `@EnableResourceServer`
- Configured in ResourceServerConfiguration @note[ extends ResourceServerConfigurerAdapter ]

@ulend

+++ 

```java
http
  .authorizeRequests()
    .antMatchers(POST, uri).hasAuthority("auth1") 
    .antMatchers(GET, uri).hasAnyAuthority("auth1", "auth2")
    .antMatchers(PUT, uri).access(
        "hasAuthority('auth1') or #oauth2.hasScope('scope1')")
```
@[3](check for one authority)
@[4](check for one of multiple authorities)
@[5](check for SpEL)
