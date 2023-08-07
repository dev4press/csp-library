# Content Security Policy Library
## List of rules for popular websites and services

CSP, or Content Security Policy is an increasingly popular and important method of protecting your website and limiting what content is allowed. This project aims to gather and maintain the list of CSP rules for popular websites and online services. 

Some services (like Google or Facebook) can often change how their services work and the CSP rules can become obsolete. This is a big problem that many websites using CSP have faced already, and that requires testing and modifying the CSP to include all the changes required for third-party services to work. This is especially important when dealing with payment gateways or other sensitive services that can brake your website if not configured properly.

I invite everyone to submit pull requests with new websites or services to add to this library or modify the existing rules. If you are using any of the online services already included here, and you notice that the CSP rules have changed, please submit the pull request with the change, or open a new Issue describing the changes needed.

All the rules are in the JSON formatted file, and each service or website has a file inside the 'rules' directory.

### CSP Resources

* [Content Security Policy Reference](https://content-security-policy.com/)
* [CSP on Mozilla Developer Network](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Content-Security-Policy)
