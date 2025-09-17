saml is a way to implement sso, the flow is like this:
we as a user try to login to the service provider, 
who to verify our identity sends a saml request to the identity provider(eg azure which could have the user's data like email, name, etc) the idp sends back the saml response to the service provider asnd the service provider validates the user data and does the authentication, and depending on the idp's response allows the user to the target page.

requirements for the saml setup.
in the idp, we need to ensure that the details of the contract are established, these include entity id, saml certificate , private key, etc therefore this data has to be extracted normally in an xml format which means we need to download this meta data -xml file. which we later use during our setup of the idp.

now we also need to provide the service providers; detail in the code, so that the saml request taht is sent to the idp is recoginized by the idp, and so requirses some details if issuer, (the service providers identity) along with the assertion consumer url or the acs url which is used both by the sp and the idp for contacting with each other, eg the idp sends back the post saml response to the acs url endpoint.
once we set up the endpoints then we need to ensure that we have set up the necessary endpoints in the securityfilterchain which is a part of spring-security6+ version.
in that we need to configure urls which the user is allowed only if he is authenticated. .. or some endpoints which can be accessed without the authentication as well ie using permitall.

other things that need to be cofigured is the loginprocessingurl.
this is the url using which the service provider receives the post requst of the idp.
the sp expects the respone on this endpoint, .. and if normally configured this should mathc the acs url.

once the entire metadata setup is also done using relyingpartyregistration which we attach to the metadatafilter and use in the securityfilterchain , the spring-security should take care of the authentication of the user.

also a additional thing that we configure in the idp is if we want the response to be signed by them or not, if it is required we can check if the response that we receive from the idp is a proper response or not. 

post spring secruity authenticates the user the user is redirected to the target url which either we can configure or let the spring security decide it for us given that (it ends at the same endpoitn which the use inittiated the sso on).


[[Saml with Spring Security]]