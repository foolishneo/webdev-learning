## Learn web programming

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

