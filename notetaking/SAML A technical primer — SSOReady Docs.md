---
doc_type: hypothesis-highlights
url: 'https://ssoready.com/docs/saml/saml-technical-primer'
---
[[A gentle introduction to SAML  SSOReady]]
# SAML: A technical primer — SSOReady Docs

## Metadata
- Author: [ssoready.com]()
- Title: SAML: A technical primer — SSOReady Docs
- Reference: https://ssoready.com/docs/saml/saml-technical-primer
- Category: #article

## Page Notes
## Highlights
- You should think of SAML as a self-contained login method. You probably already let your users log into your product using things like username+password, email magic links, “Log in with Google”, etc. Think of SAML as another login method. — [Updated on 2025-02-18 18:39:47](https://hyp.is/oPjAuO35Ee-y5Gs7uI0QxA/ssoready.com/docs/saml/saml-technical-primer) — Group: #me-only

- SAML is a protocol that lets your customer’s employees securely prove to you what their email address is, without you having to worry about sending them confirmation emails — [Updated on 2025-02-18 18:39:55](https://hyp.is/pe3Qwu35Ee-vyYdpB4zbYA/ssoready.com/docs/saml/saml-technical-primer) — Group: #me-only

- Your login page needs to know that SAML is a login option for a customer. There are a couple common UI flows for doing this. We cover these in depth in the Integrating SAML with your Login UI guide. Ultimately, your login page will, at a technical level, initiate a SAML login. Your login backend system needs to be able to handle SAML assertions. We cover this in depth in the Handling SAML Logins guide. — [Updated on 2025-02-18 18:41:12](https://hyp.is/02HZQO35Ee-wTW-Atj5xEQ/ssoready.com/docs/saml/saml-technical-primer) — Group: #me-only

- If you don’t use an open-source library like SSOReady to help implement SAML, the lack of structure that SAML imposes on you — as well as historical baggage from the early days of SAML — can lead you astray in two common ways: SAML supports the idea of putting “metadata” on a login session, configuring “conditional access”, and lots of other fancy functionality. It might seem like supporting SAML means having your entire system be able to honor these advanced SAML-specific features. — [Updated on 2025-02-18 18:42:13](https://hyp.is/98Hytu35Ee-wTmvkSAH0eA/ssoready.com/docs/saml/saml-technical-primer) — Group: #me-only

- SAML is, unfortunately, much more annoying to configure than any other login method you already support. The technical details of these SAML settings are covered later in this article here — [Updated on 2025-02-18 18:42:45](https://hyp.is/CwCXzu36Ee-x60_99zR9UQ/ssoready.com/docs/saml/saml-technical-primer) — Group: #me-only

- You just need to store three small pieces on your backend (two strings plus an X.509 certificate), and those settings change very infrequently. — [Updated on 2025-02-18 18:44:07](https://hyp.is/PD-Jsu36Ee-xWrOpvosgWw/ssoready.com/docs/saml/saml-technical-primer) — Group: #me-only

- SAML at a technical level — [Updated on 2025-02-18 18:44:29](https://hyp.is/SM92ku36Ee-NLn8AmCExFg/ssoready.com/docs/saml/saml-technical-primer) — Group: #me-only

- . When you get a SAML payload, you can securely know: Which of your corporate customers sent you the payload, What email address, according to that corporate customer, this user has That the corporate customer wants you to log this user in right away — [Updated on 2025-02-18 18:45:59](https://hyp.is/fvLy2u36Ee-2a9dc4GUTzA/ssoready.com/docs/saml/saml-technical-primer) — Group: #me-only

- The tricky part about SAML is that you need to watch out for: Forged SAML assertions, wherein an attacker pretends to be one of your corporate customers Malicious or misconfigured corporate customers sending assertions about other company’s employees, e.g. EvilCorp (evilcorp.com) telling you to log someone in as the CEO of AcmeCorp (ceo@acmecorp.com). — [Updated on 2025-02-18 18:46:15](https://hyp.is/iDVVBO36Ee-O4j-IBh2jwg/ssoready.com/docs/saml/saml-technical-primer) — Group: #me-only

- For each of your customers, you will have five settings associated with the SAML connection you have with them. These settings are: An Assertion Consumer Service (“ACS”) URL. You assign this value. It’s a URL where you run an HTTP endpoint that’s ready to handle SAML assertions. When the identity provider redirects the user back to your application, they’ll send the user to the ACS URL. An SP Entity ID. You assign this value, and it must be unique for every customer. It’s a generic string, but conventionally it’s formatted as a URL. The identity provider will include this SP Entity ID in the assertions it sends you, and you’ll use it to ensure the assertion was meant for you and not some other application. An IDP Redirect URL. The IDP assigns this value. When you initiate a SAML login, this is the URL you redirect the user to. An IDP Entity ID. The IDP assigns this value. It’s a generic string, but conventionally it’s formatted as a URL. When you initiate a SAML login, you include this value so the IDP knows which application is starting the login. The IDP will include this IDP Entity ID in the assertions it sends you, and you’ll use it to make sure the assertion is coming from the right identity provider. An IDP Certificate. The IDP assigns this value. The IDP will use this certificate to cryptographically sign the assertions it sends you. You will use this certificate to authenticate that the identity provider really generated the assertion, and that it wasn’t forged or tampered with. — [Updated on 2025-02-18 19:18:05](https://hyp.is/-nXsnO3-Ee-WTs9yQ09q8w/ssoready.com/docs/saml/saml-technical-primer) — Group: #me-only

- The Issuer needs to be equal to the SP Entity ID. — [Updated on 2025-02-18 19:20:58](https://hyp.is/YY-n2O3_Ee-7mIvyqJvZwg/ssoready.com/docs/saml/saml-technical-primer) — Group: #me-only

- That POST request needs to be pointed at the IDP Redirect URL. The POST request needs to be a standard HTTP form, with the AuthnRequest.xml being base64-encoded and set as a form field called SAMLRequest. — [Updated on 2025-02-18 19:21:09](https://hyp.is/aGuRNO3_Ee-pAbOtE0mLRg/ssoready.com/docs/saml/saml-technical-primer) — Group: #me-only

- Including a RelayState When initiating a SAML login, you can optionally include a RelayState parameter. You include this data as an additional parameter in the POST reques — [Updated on 2025-02-18 19:23:53](https://hyp.is/yjdNGO3_Ee-PJFtxYDhFjQ/ssoready.com/docs/saml/saml-technical-primer) — Group: #me-only

- Whatever you put in RelayState will be echoed back to you when you handle the SAML assertion. The HTTP POST you receive will contain, alongside the usual SAMLResponse entry, a RelayState entry. The typical use-case for RelayState is to keep track of what page your user was on before forced them to log in with SAML. — [Updated on 2025-02-18 19:24:01](https://hyp.is/zrUDlO3_Ee-sbX_rYpxdZQ/ssoready.com/docs/saml/saml-technical-primer) — Group: #me-only

- But if the login succeeds, then your user’s web browser will be redirected back to your SAML ACS URL — [Updated on 2025-02-18 19:28:02](https://hyp.is/Xl0kNu4AEe-3Jf8ZoH4vFw/ssoready.com/docs/saml/saml-technical-primer) — Group: #me-only

- Validating the assertion signature is what cryptographically authenticating a SAML assertion is all about. — [Updated on 2025-02-18 19:32:22](https://hyp.is/-Xci-u4AEe-EPbuEjVVf1g/ssoready.com/docs/saml/saml-technical-primer) — Group: #me-only



