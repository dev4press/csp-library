# Content Security Policy Library
## List of rules for popular websites and services

CSP, or Content Security Policy is an increasingly popular and important method of protecting your website and limiting what content is allowed. This project aims to gather and maintain the list of CSP rules for popular websites and online services. 

Some services (like Google or Facebook) can often change how their services work and the CSP rules can become obsolete. This is a big problem that many websites using CSP have faced already, and that requires testing and modifying the CSP to include all the changes required for third-party services to work. This is especially important when dealing with payment gateways or other sensitive services that can brake your website if not configured properly.

I invite everyone to submit pull requests with new websites or services to add to this library or modify the existing rules. If you are using any of the online services already included here, and you notice that the CSP rules have changed, please submit the pull request with the change, or open a new Issue describing the changes needed.

All the rules are in the JSON formatted file, and each service or website has a file inside the 'rules' directory.

### CSP Resources

* [Content Security Policy Reference](https://content-security-policy.com/)
* [CSP on Mozilla Developer Network](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Content-Security-Policy)

### CSP Directives

This is the list of the current CSP directives supported by the majority of browsers. Some new directives may be added or tested, and some may be deprecated so that this list will change over time.

* default-src
* script-src
* style-src
* img-src
* font-src
* media-src
* connect-src
* child-src
* frame-src
* manifest-src
* object-src
* worker-src
* form-action
* script-src-attr
* script-src-elem
* style-src-attr
* style-src-elem
* base-uri

### Rules File Format

The JSON file format used for each website or service rule is straightforward. It contains properties for the website or service name and description. And, most important property is 'rules' where each directive needed is listed, and each directive is an array of required values (URL's or other special values supported by CSP). Here is the Adobe Typekit rules file, with 5 required directives to make the Adobe Typekit integration work

```
{
    "name": "Adobe Typekit",
    "description": "",
    "rules": {
        "script-src": [
            "use.typekit.net"
        ],
        "style-src": [
            "'unsafe-inline'",
            "*.typekit.net"
        ],
        "img-src": [
            "*.typekit.net"
        ],
        "font-src": [
            "data:",
            "use.typekit.net"
        ],
        "connect-src": [
            "performance.typekit.net",
            "use.typekit.net"
        ]
    }
}
```

At this time, I have not filled in the descriptions, but that might change over time. Make a pull request if you want to help with that too.
