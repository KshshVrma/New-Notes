---
doc_type: hypothesis-highlights
url: 'https://chatgpt.com/c/67b33248-91f4-800e-823b-c3006ac20cc2'
---

# ChatGPT

## Metadata
- Author: [chatgpt.com]()
- Title: ChatGPT
- Reference: https://chatgpt.com/c/67b33248-91f4-800e-823b-c3006ac20cc2
- Category: #article

## Page Notes
## Highlights

https://docs.spring.io/spring-security/reference/servlet/saml2/login/overview.html#servlet-saml2login-minimaldependencies

https://github.com/gtiwari333/spring-security-saml-test-identity-provider-and-service-provider

https://docs.spring.io/spring-security/reference/servlet/saml2/login/overview.html#servlet-saml2login-rpr-relyingpartyregistrationresolver

- now post setting the acsurl i am facing a redirection loop, for context this is the order of execution : of the current request: the user goes to the target url, from there he does a get request to target/saml/authenticate/x now the service provider gets to the identity provider with the saml request, and the idp post to the in target url/saml/sso but post that the user again gets to target/saml/authenticate/x.. so this same cycle repeats, let me know if you also want the flow pre migration to the new spring-boot version which was working earlier — [Updated on 2025-02-22 11:34:13](https://hyp.is/1z-IKPDiEe-O9cuz_eEUhg/chatgpt.com/c/67b33248-91f4-800e-823b-c3006ac20cc2) — Group: #me-only

- pre-migration flow: the user request the target url , next the service provider does a get request to the identity provider(saml) to which the identy provider responds with the saml to the target/saml/sso next the user is redirected to the target url successfully — [Updated on 2025-02-22 11:34:18](https://hyp.is/2jM5ivDiEe-YZ_-s2zyxzg/chatgpt.com/c/67b33248-91f4-800e-823b-c3006ac20cc2) — Group: #me-only

- n your case, your IdP (Azure) is posting the SAML response to a URL (like /saml/sso) that doesn't match what Spring Security expects. As a result, Spring Security isn’t picking up the authentication, and it keeps redirecting back to the authentication endpoint—hence the loop. — [Updated on 2025-02-22 11:34:27](https://hyp.is/31jmHPDiEe-x1PtUlvkdWQ/chatgpt.com/c/67b33248-91f4-800e-823b-c3006ac20cc2) — Group: #me-only

- When you migrate to the new version, Spring Security automatically sets up the default ACS endpoint as:bashCopyEdit/login/saml2/sso/{registrationId} — [Updated on 2025-02-22 11:34:37](https://hyp.is/5U74DvDiEe-_gsfyftZOmQ/chatgpt.com/c/67b33248-91f4-800e-823b-c3006ac20cc2) — Group: #me-only



i want to upgrade a spring boot project from version 2.5 to verson 3.0 however the even post some changes the sso request using saml2 was stuck in a redirect loop , now post setting the acsurl i am facing a redirection loop, for context this is the order of execution : of the current request: the user goes to the target url, from there he does a get request to target/saml/authenticate/x now the service provider gets to the identity provider with the saml request, and the idp post to the in target url/saml/sso but post that the user again gets to target/saml/authenticate/x.. so this same cycle repeats, let me know if you also want the flow pre migration to the new spring-boot version which was working earlier — - pre-migration flow: the user request the target url , next the service provider does a get request to the identity provider(saml) to which the identy provider responds with the saml to the target/saml/sso next the user is redirected to the target url successfully .. earlier i had no request handler for the idp response to /saml/sso, but still the application worked fine, so does the spring security library automatically handle the acs url in the old code?


​