# Spring Security OAuth 2.0 Guide

This example shows how to create a Authorization Server with Spring Security and OAuth 2.0.

Please read [A Quick Guide to OAuth 2.0 with Spring Security](https://developer.okta.com/blog/2019/03/12/oauth2-spring-security-guide) for a tutorial that shows you how to build the applications in this repo. 

**Prerequisites:** [Java 8 or 11](https://adoptopenjdk.net/).

> [Okta](https://developer.okta.com/) has Authentication and User Management APIs that reduce development time with instant-on, scalable user infrastructure. Okta's intuitive API and expert support make it easy for developers to authenticate, manage and secure users and roles in any application.

* [Getting Started](#getting-started)
* [Help](#help)
* [Links](#links)
* [License](#license)

## Getting Started

To install this example application, run the following commands:

```bash
git clone https://github.com/oktadeveloper/okta-spring-boot-authz-server-example.git
cd okta-spring-boot-authz-server-example
```

### Create an Okta Developer Account

If you don't have one, [create an Okta Developer account](https://developer.okta.com/signup/). After you've completed the setup process, log in to your account and navigate to **Applications** > **Add Application**. Click **Web** and **Next**. On the next page, enter a name for your app (e.g., "Okta OAuth Client"), then click **Done**. 

Update the `OktaOAuthClient/src/main/resources/application.yml` to have your new app's settings:

```yaml
okta:
  oauth2:
    issuer: https://{yourOktaDomain}/oauth2/default
    client-id: {yourClientId}
    client-secret: {yourClientSecret}
```

Start the `OktaOAuthClient` app using Gradle.

```shell
cd OktaOAuthClient
./gradlew bootRun
```

After everything starts, you should be able to log in with your credentials at `http://localhost:8080`.

## Links

This example uses the following open source projects:

* [Okta Spring Boot Starter](https://github.com/okta/okta-spring-boot)
* [Spring Boot](https://spring.io/projects/spring-boot)
* [Spring Security](https://spring.io/projects/spring-security)

## Help

Please post any questions as comments on this repo's [blog post](https://developer.okta.com/blog/2019/03/12/oauth2-spring-security-guide), or visit our [Okta Developer Forums](https://devforum.okta.com/). 

## License

Apache 2.0, see [LICENSE](LICENSE).
