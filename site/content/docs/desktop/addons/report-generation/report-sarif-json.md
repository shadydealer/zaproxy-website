---
# This page was generated from the add-on.
title: SARIF JSON Report
type: userguide
---

# SARIF JSON Report

### Sample

```
{
   "runs": [
      {
         "results": [ 
            {
               "level": "error",
               "locations": [
                  {
                     "physicalLocation": {
                        "artifactLocation": {
                           "uri": "https://127.0.0.1:8080/greeting?name=%3C%2Fp%3E%3Cscript%3Ealert%281%29%3B%3C%2Fscript%3E%3Cp%3E"
                        },
                        "region": {
                           "startLine": 10, 
                           "snippet": {
                               "text": "<\/p><script>alert(1);<\/script><p>"
                           }
                        }
                     },
                     "properties": {
                         "attack": "<\/p><script>alert(1);<\/script><p>"
                     }
                  }
               ],
               "message": {
                  "text": "Some other additional information which shall appear inside the message"
               },
               "ruleId": "40012",
               "webRequest": {
                   "protocol": "HTTP",
                   "version": "1.1",
                   "target": "https://127.0.0.1:8080/greeting?name=%3C%2Fp%3E%3Cscript%3Ealert%281%29%3B%3C%2Fscript%3E%3Cp%3E",
                   "method": "GET",
                   "headers": {
                       "Cache-Control" : "no-cache",
                       "Content-Length" : "0",
                       "Cookie" : "JSESSIONID=38AA1F7A61982DF1073D7F43A3707798; locale=de",
                       "Host" : "127.0.0.1:8080",
                       "Pragma" : "no-cache",
                       "Referer" : "https:\/\/127.0.0.1:8080\/hello",
                       "User-Agent" : "Mozilla\/5.0 (Windows NT 10.0; Win64; x64; rv:92.0) Gecko\/20100101 Firefox\/92.0"
                   },
                   "body": {
                       
                   }
               },
               "webResponse": {
                   "statusCode": 200,
                   "reasonPhrase": "",
                   "protocol": "HTTP",
                   "version": "1.1",
                   "headers": {
                       "Cache-Control" : "no-cache, no-store, max-age=0, must-revalidate",
                       "Content-Language" : "en-US",
                       "Content-Security-Policy" : "script-src 'self'",
                       "Content-Type" : "text\/html;charset=UTF-8",
                       "Date" : "Thu, 11 Nov 2021 09:56:20 GMT",
                       "Expires" : "0",
                       "Pragma" : "no-cache",
                       "Referrer-Policy" : "no-referrer",
                       "Set-Cookie" : "locale=de; HttpOnly; SameSite=strict",
                       "Strict-Transport-Security" : "max-age=31536000 ; includeSubDomains",
                       "X-Content-Type-Options" : "nosniff",
                       "X-Frame-Options" : "DENY",
                       "X-XSS-Protection" : "1; mode=block"
                   },
                   "body": {
                       "text": "<!DOCTYPE HTML>\n<html>\n<head>\n    <title>Getting Started: Serving Web Content<\/title>\n    <meta http-equiv=\"Content-Type\" content=\"text\/html; charset=UTF-8\" \/>\n<\/head>\n<body>\n    <!-- unsecure text used (th:utext instead th:text)- to create vulnerability (XSS) -->\n    <!-- simple usage: http:\/\/localhost:8080\/greeting?name=Test2<\/p><script>;alert(\"hallo\")<\/script> -->\n    <p >XSS attackable parameter output: <\/p><script>alert(1);<\/script><p>!<\/p>\n<\/body>\n<\/html>"
                   },
                   "noResponseReceived": false
               }
            }
         ],
         "taxonomies": [
            {
               "downloadUri": "https://cwe.mitre.org/data/xml/cwec_v4.8.xml.zip",
               "guid":  "b000a760-3e52-3565-a35c-f61369da53b7",
               "informationUri": "https://cwe.mitre.org/data/published/cwe_v4.8.pdf/",
               "isComprehensive": true,
               "language": "en",
               "minimumRequiredLocalizedDataSemanticVersion": "4.8",
               "name":  "CWE",
               "organization": "MITRE",
               "releaseDateUtc": "2022-06-28",
               "shortDescription": {
                  "text": "The MITRE Common Weakness Enumeration"
               },
               "taxa": [
                  {
                     "guid": "5dd429c8-e5e3-37a8-bf40-f7b2d72a9085",
                     "helpUri": "https://cwe.mitre.org/data/definitions/79.html",
                     "id": "79"
                  }
               ],
               "version": "4.4"
            }
         ],
         "tool": {
            "driver": {
               "guid": "840570e4-2388-38c0-8afe-ed426f2f5199",
               "informationUri": "https://www.zaproxy.org/",
               "name": "OWASP ZAP",
               "rules": [ 
                  {
                     "id": "40012",
                     "defaultConfiguration": {
                        "level": "error"
                     },
                     "fullDescription": {
                        "text": "CSS Description\nMultiple lines\n\nEnd"
                     },
                     "name": "Cross Site Scripting",
                     "properties": {
                            "references": [
                                "http://projects.webappsec.org/Cross-Site-Scripting",
                                "http://cwe.mitre.org/data/definitions/79.html"
                            ],
                            "solution": {
                                "text": "Phase: 1\n\nDo ...."
                            },
                            "confidence": "medium"
                     },
                     "relationships": [ 
                        {
                           "kinds": [
                              "superset"
                           ],
                           "target": {
                              "guid":"5dd429c8-e5e3-37a8-bf40-f7b2d72a9085",
                              "id": "79",
                              "toolComponent": {
                                 "guid": "b000a760-3e52-3565-a35c-f61369da53b7",
                                 "name": "CWE"
                              }
                           }
                        }
                        
                     ],
                     "shortDescription": {
                        "text": "Cross Site Scripting"
                     }
                  }
                  
               ],
               "semanticVersion": "Dev Build",
               "supportedTaxonomies": [ 
                  {
                     "guid": "b000a760-3e52-3565-a35c-f61369da53b7",
                     "name": "CWE"
                  }
               ],
               "version": "Dev Build"
            }
         }
      }
   ],
   "$schema": "https://raw.githubusercontent.com/oasis-tcs/sarif-spec/master/Schemata/sarif-schema-2.1.0.json",
   "version": "2.1.0"
}
```
