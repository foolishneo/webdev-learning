## Learn web programming

### HTTP (HyperText Transfer Protocol)
HTTP is the protocol (the language) that is used by web servers and browsers to communicate and exchange data. When the browser needs information, it will create HTTP requests and send them to a web server. When the web server receives a request, it will create a HTTP response and send it back to the browser.

### API (Application Programming Interface)
APIs allows an application to get/modify/delete data of another application.

![API](https://miro.medium.com/max/2825/1*OcmVkcsM5BWRHrg8GC17iw.png "API")

### REST (REpresentational State Transfer)
REST is an architectural style, or design pattern, for APIs. Think of it as a guideline to architect your APIs

### JSON Schema

JSON Schema is a vocabulary that allows you to annotate and validate JSON documents.

```
"TripActivity": {
  "type": "array",
  "items": {
    "type": "object",
    "additionalProperties": false,
    "required": [
      "TripActivityNumber"
    ],
    "properties": {
      "TripActivityNumber": {
        "type": "string",
        "minLength": 1
      },
      "Regulator": {
        "type": "array",
        "items": {
          "type": "object",
          "properties": {
            "RegulatorStartDateTime": {
              "type": "string",
              "minLength": 1
            },
            "RegulatorEndDateTime": {
              "type": "string",
              "minLength": 1
            },
            "RegulatorId": {
              "type": "string",
              "minLength": 1
            }
          },
          "required": [
            "RegulatorStartDateTime",
            "RegulatorEndDateTime",
            "RegulatorTripId"
          ]
        }
      }    
    }
  }
}  
```
Write a script to validate a given JSON object against the above schema

