---
doc_type: hypothesis-highlights
url: 'https://ssoready.com/blog/engineering/a-gentle-intro-to-saml/'
---

# A gentle introduction to SAML | SSOReady

## Metadata
- Author: [ssoready.com]()
- Title: A gentle introduction to SAML | SSOReady
- Reference: https://ssoready.com/blog/engineering/a-gentle-intro-to-saml/
- Category: #article

## Page Notes
## Highlights
- SAML (or Security Assertion Markup Language), defines a flexible set of rules for exchanging security-related messages in XML. — [Updated on 2025-02-13 20:47:13](https://hyp.is/mijjnOodEe-S9u_zyF8PQg/ssoready.com/blog/engineering/a-gentle-intro-to-saml/) — Group: #me-only

- All SAML basically looks like this. We’re just moving XML messages around. — [Updated on 2025-02-13 20:47:38](https://hyp.is/qSf8cOodEe-ma1_HJyogrA/ssoready.com/blog/engineering/a-gentle-intro-to-saml/) — Group: #me-only

- SAML’s design emphasizes flexibility; at least in principle, you can do an awful lot of different stuff with SAML. Unfortunately, that flexibility results in complexity. — [Updated on 2025-02-13 20:47:50](https://hyp.is/sDgnkuodEe-YjwcQkDLDtQ/ssoready.com/blog/engineering/a-gentle-intro-to-saml/) — Group: #me-only

- We most commonly use SAML for single sign-on (hereafter abbreviated as SSO). For what it’s worth, SAML actually defines a few weird flavors of SSO, but we generally use the simplest of these, the Web Browser SSO Profile — [Updated on 2025-02-13 20:48:07](https://hyp.is/urJApOodEe-KLTsTTnpMQw/ssoready.com/blog/engineering/a-gentle-intro-to-saml/) — Group: #me-only

- We care about three entities in SSO: A user: someone that wants to use your application A service provider (SP): your application An identity provider (IDP): the centralized service your user will use to authenticate — [Updated on 2025-02-13 20:48:31](https://hyp.is/yHu1MOodEe-PqktGxglCOQ/ssoready.com/blog/engineering/a-gentle-intro-to-saml/) — Group: #me-only

- Every time we want a user to sign in via SAML, we’ll have to get information from their IDP; in SSO, we’re mostly just asking the IDP to confirm the user’s identity. — [Updated on 2025-02-13 20:49:29](https://hyp.is/63fUpuodEe-8_sMEqfoibQ/ssoready.com/blog/engineering/a-gentle-intro-to-saml/) — Group: #me-only

- Here’s a typical SAML SSO process: A user attempts to access part of your application in their web browser. You check whether the user has a valid security context. The user doesn’t have a valid security context, so you present a login page. The user fills in some information (e.g. an email address), which you use to determine the appropriate login method. You have pre-set records that tell you (1) that the user requires SAML SSO for authentication and (2) which IDP the user needs to use. You redirect the user to the IDP’s web address, passing a SAML message to the IDP via the user’s browser. The IDP prompts your user for credentials. The user successfully authenticates. The IDP redirects the user back to your application along with a SAML message communicating information about the user’s authentication. You process the SAML message and determine that you should, in fact, establish a security context for the user. You grant the user access to the desired part of your application — [Updated on 2025-02-13 20:50:03](https://hyp.is/_3ST6uodEe-h_Y-4zujfRA/ssoready.com/blog/engineering/a-gentle-intro-to-saml/) — Group: #me-only

- Conceptually, the <Response> just wraps up a few <Assertion> tags. An <Assertion> just wraps up claims about our user, e.g. who this is and how they authenticated with the IDP. We process the assertions to determine whether we should log in our user. — [Updated on 2025-02-13 20:55:26](https://hyp.is/v_FVXuoeEe-KUz9tK2Eqlg/ssoready.com/blog/engineering/a-gentle-intro-to-saml/) — Group: #me-only

- We call this first message – from the service provider to the IDP – a SAML request. We call the other message – from the IDP to the service provider – a SAML response. — [Updated on 2025-02-13 20:55:41](https://hyp.is/yR8dquoeEe-t6q-ZfxYsXw/ssoready.com/blog/engineering/a-gentle-intro-to-saml/) — Group: #me-only



