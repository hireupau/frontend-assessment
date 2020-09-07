# Front-end Assessment - Searchable Select List/Autocomplete Combobox

## Overview

We'd like you to create a searchable select list that retrieves Marvel characters from our Superhero API.

The style and behaviour of the select list should match the images shown below.

## Prerequisites

1. Node.js and NPM installed on your local machine

## API set-up

Within this repo is an api folder that contains a script for running a local REST server and some data.

The server can be started with:

`npm install`

`npm start`

### Request

To retrieve a list of all characters:

`GET http://localhost:1337/superheroes `

To query for characters by their name:

`GET http://localhost:1337/superheroes?name_like=Iron`

This can be combined with filtering by other fields

`GET http://localhost:1337/superheroes?name_like=Iron&work.base_like=New%20York`

Details and more advanced queries can be found [here](https://github.com/typicode/json-server#routes)


### Response

An example response can be seen below.

```json
[
  {
    "id": 345,
    "name": "Iron Fist",
    "slug": "345-iron-fist",
    "powerstats": {
      "intelligence": 75,
      "strength": 55,
      "speed": 33,
      "durability": 50,
      "power": 95,
      "combat": 100
    },
    "appearance": {
      "gender": "Male",
      "race": "Human",
      "height": [
        "5'11",
        "180 cm"
      ],
      "weight": [
        "175 lb",
        "79 kg"
      ],
      "eyeColor": "Blue",
      "hairColor": "Blond"
    },
    "biography": {
      "fullName": "Danny Rand",
      "alterEgos": "No alter egos found.",
      "aliases": [
        "Daredevil",
        "Daniel Thomas Rand",
        "the Living Weapon",
        "Young Dragon",
        "Danny Rand"
      ],
      "placeOfBirth": "-",
      "firstAppearance": "Marvel Premiere #15 (May 1974)",
      "publisher": "Marvel Comics",
      "alignment": "good"
    },
    "work": {
      "occupation": "Adventurer; formerly co-owner of Rand-Meachum, Inc., bodyguard, private investigator, research assistant, warrior",
      "base": "New York"
    },
    "connections": {
      "groupAffiliation": "New Avengers, Heroes for Hire, Inc., Secret Defenders, Defenders, Misty Knight, Luke Cage",
      "relatives": "Wendell Rand-K'ai (father, deceased), Heather Duncan Rand (mother, deceased), Yu-Ti (adopted uncle), Miranda Rand-K'ai (half-sister), Lord Tuan (adopted paternal grandfather, deceased), Lady Ming (adopted paternal grandmother, deceased), Thomas Duncan (maternal grandfather)"
    },
    "images": {
      "xs": "https://cdn.rawgit.com/akabab/superhero-api/0.2.0/api/images/xs/345-iron-fist.jpg",
      "sm": "https://cdn.rawgit.com/akabab/superhero-api/0.2.0/api/images/sm/345-iron-fist.jpg",
      "md": "https://cdn.rawgit.com/akabab/superhero-api/0.2.0/api/images/md/345-iron-fist.jpg",
      "lg": "https://cdn.rawgit.com/akabab/superhero-api/0.2.0/api/images/lg/345-iron-fist.jpg"
    }
  }
]
```

## Requirements

- Must be completed in Vue or React (you're welcome to scaffold the project using a starter kit).
- Cannot use a third party search select/autocomplete combobox library.
- Behaviour and style roughly equal the [designs](#designs) below. You can choose which fields you want to use for the description. 
- Items in the list should be selectable via a mouse click and Enter key. On select, the character name should be written to the console.
- A spinner should be shown when the results are being queried from the API.

## Bonus Points

- Think about the accessibility requirements and considerations of building this solution.
- Pay attention to the CSS architecture as much as the JavaScript architecture.

## Guidance on Time Spent

While you should be free to decide how much time you'd like to spend developing your solution, in the interests of not taking up all your time, we strongly advise to limit yourself to five hours or less.

## Submission

The submission should be committed to Github and a link provided to the submission along with a README on how to setup and run the solution. If you run out of time, detail in the README what else you would have liked to achieve.

The solution is expected to incorporate good software development practices such as comments, tests and a sensible architecture.

**If you have any problems with this assessment, you can create a GitHub issue that will be answered shortly by one of the Hireup development team or email us directly at tech@hireup.com.au**

## Designs

### Desktop - Closed

![Screenshot1](https://i.imgur.com/9ooq75J.jpg)

### Desktop - Opened with results

![Screenshot2](https://i.imgur.com/LIlF1Bd.jpg)

### Desktop - Opened with no results

![Screenshot3](https://i.imgur.com/SmLh1sZ.jpg)

### Mobile - Closed

![ScreenShot4](https://i.imgur.com/KUaenjW.jpg)

### Mobile - Opened with results

![ScreenShot5](https://i.imgur.com/KAJvi1s.jpg)

### Mobile - Opened with no results

![ScreenShot6](https://i.imgur.com/0938RCR.jpg)

