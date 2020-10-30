# Table of Contents
- [Table of Contents](#table-of-contents)
- [Problem Context](#problem-context)
- [Problem Statement](#problem-statement)
- [Intention validator](#intention-validator)
- [Assumptions](#assumptions)
- [Instructions](#instructions)
- [Run Automated Tests](#run-automated-tests)

# Problem Context
Every statement user speaks or dialects could be considered as an utterance . Inside each utterance, a user can have an intent behind it. Each of these intentions is modifiable via entity . E.g-  \
"show me yesterday’s financial news" --> utterance \
"show me" --> Intent : of somthing to be shown \
"financial" --> Entity that modifies the Intent \
Ref: [ChatbotMagzine](https://chatbotsmagazine.com/chatbot-vocabulary-10-chatbot-terms-you-need-to-know-3911b1ef31b4)

# Problem Statement
Not every entity servers to identify an intent and an ability to discriminate between valid one and invalid one becomes an important tasks for Chatbots to resolve. Hence the task was to create the apis which a Chatbot could easily refer to while validating entities: We can assume that the validation criteria to be already provided some other service. Our task is to validate the entities based on this criteria


# Intention validator

[![Build Status](https://travis-ci.org/joemccann/dillinger.svg?branch=master)](https://travis-ci.org/joemccann/dillinger)

This project intendes to validates intention composed of entities behind the utterance. It's a basic Django app which has three POST Apis
  - validate_finite_entity : https://localhost:8000/validateFiniteEntity
  - validate_num_entity: https://localhost:8000/validateNumEntity
  - Slot_Validation: https://localhost:8000/slotValidate

Futher information can be found in _problem statetment.txt_

# Assumptions
* If pick_first is present, it will simply overide the behaviour of support_multiple key and first value will be picked regardless the entity value is valid or not
* Constraint is considered to be boolean or bad request response is thrown

# Instructions
* Inside the project directory  run
```
docker-compose up
```
# Run Automated Tests
You can run the already pre-built tests for the apis to test sanity functions as follows
```
./manage.py test
```
Or
```
python3 manage.py test
```
