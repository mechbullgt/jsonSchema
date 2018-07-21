# jsonSchema
A node based web application to generate JSON schema (Draft-4) from any given JSON file.


Use:
node schema.js <inputJSONLocation> <OutputSchemaLocation> 

Example: 
  maqbool:jsonSchema maqbool$ node schema.js ./responseJSON/Input.json ~/Desktop/Out.json
  
  JSON_Location:./responseJSON/Input.json
  Schema_Location:/Users/mindstix/Desktop/Out.json
  
  {
    "checked": false,
    "dimensions": {
      "width": 5,
      "height": 10
    },
    "id": 1,
    "name": "A green door",
    "price": 12.5,
    "tags": [
      "home",
      "green"
    ]
  }

  {
    "$schema": "http://json-schema.org/draft-04/schema#",
    "type": "object",
    "properties": {
      "checked": {
        "type": "boolean"
      },
      "dimensions": {
        "type": "object",
        "properties": {
          "width": {
            "type": "number"
          },
          "height": {
            "type": "number"
          }
        }
      },
      "id": {
        "type": "number"
      },
      "name": {
        "type": "string"
      },
      "price": {
        "type": "number"
      },
      "tags": {
        "type": "array",
        "items": {
          "type": "string"
        }
      }
    }
  }
JSON Schema generated at: /Users/mindstix/Desktop/Out.json
maqbool:jsonSchema maqbool$  
