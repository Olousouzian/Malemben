<p align="center">
  <img src="http://i.imgur.com/tvjPERO.png" alt="Malemben_logo"/>
</p>


## Synopsis

Malemben provides you a structure for all your status code. Very useful when you can't use RESTful with your API.

## Malemben structure

A error code must be construct with this following model : 

| Structure of Malemben |             |       |       |       |
|:---------------------:|:-----------:|:-----:|:-----:|:-----:|
|   Abstract Stucture   |  Character  | Digit | Digit | Digit |
|     Signification     | Level error |   ID  |   ID  |   ID  |
|        Example        |      W      |   1   |   5   |   2   |

4 levels of error : 

- **C**ritical
- **W**arning
- **I**nformation
- **S**uccess

3 digits for the identifications : 

**Warning** : The first digit must be different of 0. This restriction prevents all humans errors for the futur.

Example : 

- 125
- 409

## Language & file

One rule : 1 file = 1 language 

Per example : 

en_US.errors.json

````json
{
    "C" :
    {
        "label" : "Critical",
        "codes" : 
        {
            "100" :
            {
                "label" : "USER_NOT_FOUND",
                "description" : "The user cannot be found"
            }
        }
    },
    "W" :
    {
        "label" : "Warning",
        "code" :
        {
            "100" :
            {
                "label": "USER_CHILD_NOT_FOUND",
                "description" : "The user have not child"
            }
        }
    },
    "I" :
    {
        "label" : "Information",
        "code" :
        {
            "100" :
            {
                "label" : "SYSTEM_HEALTH_OK",
                "description" : "The current system seems to be OK"
            }
        }
    },
    "S" : 
    {
        "label" : "Success",
        "code" :
        {
            "100" :
            {
                "label" : "SUCCESS_OK",
                "description" : "The operation is valid"
            }
        }
    }
}
````
