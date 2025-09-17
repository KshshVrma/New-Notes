---
doc_type: hypothesis-highlights
url: >-
  https://docs.spring.io/spring-security/reference/servlet/saml2/login/overview.html
---

# SAML 2.0 Login Overview :: Spring Security

## Metadata
- Author: [docs.spring.io]()
- Title: SAML 2.0 Login Overview :: Spring Security
- Reference: https://docs.spring.io/spring-security/reference/servlet/saml2/login/overview.html
- Category: #article

## Page Notes
## Highlights
- Identity Provider and Asserting Party are synonymous, as are Service Provider and Relying Party. These are frequently abbreviated as AP and RP, respectively. — [Updated on 2025-02-22 12:37:35](https://hyp.is/sT1yTvDrEe-5phfKDoW9Hw/docs.spring.io/spring-security/reference/servlet/saml2/login/overview.html) — Group: #me-only

- spring: security: saml2: relyingparty: registration: adfs: identityprovider: entity-id: https://idp.example.com/issuer verification.credentials: - certificate-location: "classpath:idp.crt" singlesignon.url: https://idp.example.com/issuer/sso singlesignon.sign-request: false — [Updated on 2025-02-22 12:37:44](https://hyp.is/ttiK6vDrEe-phkdlpsVH2A/docs.spring.io/spring-security/reference/servlet/saml2/login/overview.html) — Group: #me-only

- Runtime Expectations As configured earlier, the application processes any POST /login/saml2/sso/{registrationId} request containing a SAMLResponse parameter: POST /login/saml2/sso/adfs HTTP/1.1 SAMLResponse=PD94bWwgdmVyc2lvbj0iMS4wIiBlbmNvZGluZ... — [Updated on 2025-02-22 12:38:50](https://hyp.is/3dzeUvDrEe-JeXPTvLJZEw/docs.spring.io/spring-security/reference/servlet/saml2/login/overview.html) — Group: #me-only



