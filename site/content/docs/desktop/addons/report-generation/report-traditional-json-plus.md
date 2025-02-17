---
# This page was generated from the add-on.
title: Traditional JSON Report with Requests and Responses
type: userguide
---

# Traditional JSON Report with Requests and Responses

### Sample

```
{
    "@version": "Dev Build",
    "@generated": "Fri, 4 Feb 2022 13:04:51",
    "site":[
        {
            "@name": "http://localhost:8080",
            "@host": "localhost",
            "@port": "8080",
            "@ssl": "false",
            "alerts": [
                {
                    "pluginid": "40012",
                    "alertRef": "40012",
                    "alert": "Cross Site Scripting (Reflected)",
                    "name": "Cross Site Scripting (Reflected)",
                    "riskcode": "3",
                    "confidence": "2",
                    "riskdesc": "High (Medium)",
                    "desc": "<p>Cross-site Scripting (XSS) is an attack technique that involves ...</p>",
                    "instances":[
                        {
                            "uri": "http://localhost:8080/bodgeit/search.jsp?q=%3C%2Ffont%3E%3CscrIpt%3Ealert%281%29%3B%3C%2FscRipt%3E%3Cfont%3E",
                            "method": "GET",
                            "param": "q",
                            "attack": "</font><scrIpt>alert(1);</scRipt><font>",
                            "evidence": "</font><scrIpt>alert(1);</scRipt><font>",
                            "request-header": "GET http://localhost:8080/bodgeit/search.jsp?q=%3C%2Ffont%3E%3CscrIpt%3Ealert%281%29%3B%3C%2FscRipt%3E%3Cfont%3E HTTP/1.1\r\n...",
                            "request-body": "",
                            "response-header": "HTTP/1.1 200\r\nContent-Type: text/html;charset=ISO-8859-1\r\nContent-Length: 2045\r\nDate: Fri, 04 Feb 2022 11:56:38 GMT\r\n\r\n",
                            "response-body": "\n\n\n\n\n\n\n<!DOCTYPE HTML PUBLIC \"-//W3C//DTD HTML 3.2//EN\">\n<html>..."
                        },
                        {
                            "uri": "http://localhost:8080/bodgeit/contact.jsp",
                            "method": "POST",
                            "param": "comments",
                            "attack": "</td><scrIpt>alert(1);</scRipt><td>",
                            "evidence": "</td><scrIpt>alert(1);</scRipt><td>",
                            "request-header": "POST http://localhost:8080/bodgeit/contact.jsp HTTP/1.1\r\nHost: localhost:8080\r\nUser-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64; rv:92.0)...",
                            "request-body": "null=&anticsrf=0.7583553183173598&comments=%3C%2Ftd%3E%3CscrIpt%3Ealert%281%29%3B%3C%2FscRipt%3E%3Ctd%3E",
                            "response-header": "HTTP/1.1 200\r\nContent-Type: text/html;charset=ISO-8859-1\r\nContent-Length: 2025\r\nDate: Fri, 04 Feb 2022 11:56:35 GMT\r\n\r\n",
                            "response-body": "\n\n\n\n\n\n<!DOCTYPE HTML PUBLIC \"-//W3C//DTD HTML 3.2//EN\">\n<html>..."
                        }
                    ],                   
                    "count": "2", 
                    "solution": "<p>Phase: Architecture and Design</p><p>Use a vetted library or framework that does not ...</p>",
                    "otherinfo": "",
                    "reference": "<p>http://projects.webappsec.org/Cross-Site-Scripting</p><p>http://cwe.mitre.org/data/definitions/79.html</p>",
                    "cweid": "79",
                    "wascid": "8",
                    "sourceid": "36977",
                    "tags":[ 
                        {
                            "tag": "OWASP_2021_A03",
                            "link": "https://owasp.org/Top10/A03_2021-Injection/"
                        },
                        {
                            "tag": "WSTG-v42-INPV-01",
                            "link": "https://owasp.org/www-project-web-security-testing-guide/v42/4-Web_Application_Security_Testing/07-Input_Validation_Testing/01-Testing_for_Reflected_Cross_Site_Scripting"
                        },
                        {
                            "tag": "OWASP_2017_A07",
                            "link": "https://owasp.org/www-project-top-ten/2017/A7_2017-Cross-Site_Scripting_(XSS).html"
                        }
                    ]
                },

```
