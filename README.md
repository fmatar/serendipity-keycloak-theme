<p align="center">
  <img src="./serendipity-logo.svg" alt="Serendipity" width="400"/>
</p>

<h1 align="center">Serendipity Keycloak Theme</h1>

![divider](./divider.png)

## ❯ Start a new keycloak instance
```shell script
docker-compose up
```

Make sure you import your realm, this repo doesn't include one. 


For theme developers: Copy `standalone.xml` to your keycloak instance.

```shell script
docker cp standalone.xml keycloak:/opt/jboss/keycloak/standalone/configuration/
```

Restart your keycloak server, you'll only have to do this once. 


```shell script
#Stop keycloak
docker-compose stop keycloak

#Start keycloak
docker-compose start keycloak
```
 

## ❯ Introduction

The Serendipity Identity Service uses Keycloak. Keycloak provides support for OpenID Connect, OAuth 2.0 and SAML 2.0.
However, Serendipity's user experience is quite different from Keycloaks so we need to provide a custom Keycloak theme.

![divider](./divider.png)

## ❯ Documentation

* Administrator Documentation
* Developer Documentation
  * [Quick Start Guide](./docs/developer/quick-start-guide.md)
  * [Build Management](./docs/developer/build-management.md)
* User Documentation

![divider](./divider.png)

## ❯ Deploy to Keycloak
Once the theme is packaged (see [Build Management](./docs/developer/build-management.md)) you can now deploy the theme to the keycloak instance.

```
# Unzip the package
unzip serendipity-keycloak-theme-1.0.zip

# The content will be extracted to a folder called docker serendipity, copy the serendipity folder to the keycloak instance

docker cp ./serendipity keycloak:/opt/jboss/keycloak/themes/
```

Now select the new theme and enjoy :) 

![divider](./divider.png)

## ❯ Screen Shots

Register (Sign up) page:

<p align="center">
  <img src="https://github.com/Robinyo/serendipity-keycloak-theme/blob/master/screen-shots/oidc-register.png">
</p>

Login (Sign in) page:

<p align="center">
  <img src="https://github.com/Robinyo/serendipity-keycloak-theme/blob/master/screen-shots/oidc-login.png">
</p>

![divider](./divider.png)

##❯ Resources

### Blog Posts

* Rob Ferguson's blog: [Keycloak Themes - Part 1](https://robferguson.org/blog/2020/04/12/keycloak-themes-part-1/)
* Rob Ferguson's blog: [Keycloak Themes - Part 2](https://robferguson.org/blog/2020/04/17/keycloak-themes-part-2/)

![divider](./divider.png)
