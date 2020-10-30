



# Instructions to run and test

* Navigate to the place where the file is stored and enter this command :
```
docker-compose up
```
 1. POST API to validate a slot with a finite set of values.
 
 * To test validation of finite set of values, hit the link https://localhost:8000/validateFiniteEntity and paste this below json to test :
 
 ```
{
  "invalid_trigger": "invalid_ids_stated",
  "key": "ids_stated",
  "name": "govt_id",
  "reuse": true,
  "support_multiple": true,
  "pick_first": false,
  "supported_values": [
    "pan",
    "aadhaar",
    "college",
    "corporate",
    "dl",
    "voter",
    "passport",
    "local"
  ],
  "type": [
    "id"
  ],
  "validation_parser": "finite_values_entity",
  "values": [
    {
      "entity_type": "id",
      "value": "college"
    }
  ]
}
```



2. POST API to validate a slot with a numeric value extracted and constraints on the value extracted.

 * To test validation of finite set of values, hit the link https://localhost:8000/validateNumEntity and paste this below json to test :
 
 ```
 {
  "invalid_trigger": "invalid_age",
  "key": "age_stated",
  "name": "age",
  "reuse": true,
  "pick_first": true,
  "type": [
    "number"
  ],
  "validation_parser": "numeric_values_entity",
  "constraint": "x>=18 and x<=30",
  "var_name": "x",
  "values": [
    {
      "entity_type": "number",
      "value": 23
    }
  ]
}
```

# Docker Image Size  = 437 MB

# References

Have used djangorestframework for building the UI - https://www.django-rest-framework.org/tutorial/quickstart/

For chatbot intention utterance research - https://chatbotsmagazine.com/chatbot-vocabulary-10-chatbot-terms-you-need-to-know-3911b1ef31b4



