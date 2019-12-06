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
      "Observer": {
        "type": "array",
        "items": {
          "type": "object",
          "properties": {
            "ObserverStartDateTime": {
              "type": "string",
              "minLength": 1
            },
            "ObserverEndDateTime": {
              "type": "string",
              "minLength": 1
            },
            "ObserverTripId": {
              "type": "string",
              "minLength": 1
            }
          },
          "required": [
            "ObserverStartDateTime",
            "ObserverEndDateTime",
            "ObserverTripId"
          ]
        }
      }    
    }
  }
}  
```

