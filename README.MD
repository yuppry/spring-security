<h1>Oauth 2</h1>

* [Javascript base64 http basic authorization encoder](http://tuxgraphics.org/toolbox/base64-javascript.html)

Get access token
```
$ http --form >http --form POST localhost:8100/oauth/token Authorization:"Basic <base64 encoded>" grant_type=client_credentials
```

Check token value return
```
$ http --form localhost:8100/oauth/check_token Authorization:"Bearer <access_token>" token=<access_token>
```
Annotation
- @EnableAuthorizationServer
- @Configuration
Class that extend to build the configuration
```
extends AuthorizationServerConfigurerAdapter
```

Annotation used to protect the resource server with OAuth2
```
@EnableResourceServer
```