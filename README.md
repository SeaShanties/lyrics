# Sea Shanty Lyrics
A repository of lyrics to Sea Shanties stored in json for easy usage in projects and code

# Puprose
Lyrics are often found in different formats and on different websites. This project strives to create an archive in a reasonable format which can
be used in various projects such as digital sea shanty song books.

# Json file structure
The file shall be named in the format of `ShantyName.json` and should have the following structure:

The json object must have a key called `name` this is the same as the name of the file but with correct spacing and possible special chars that are unfit for a filename.
The other top level value is an array called `versions`. This is required even if there only is one version. There are often different lyrics to the same song depending on who's performing it. Therefore a `name` value of the version must be specified as well as `credit` where the group or individual who performed the version used as lyrical refrence is credited.

Each version contains the keys `chorus` and `verses`. `chorus` is self-explanatory, it is an array of the lines for the chorus. `verses` is a list of each verse as well as a chorus marker for when there is a chorus. This means that if possible the chorus does not need to be repeated several times and if it is a song without chorus or a changing chorus it can simply be added as another verse.

It is recommended but not required to in a call and response shanty to indicate the response of the group by putting it in parentheses. Chorus is often assumed to be sung by all and it might not fit very well depending on the shanty and the decision to use parentheses is up to the contrubutor, ask a maintainer if you're unsure.

The file `available-shanties.json` contains a json list of all the names of the shanty json files in the `shanties` folder. If a shanty is added and the file is not already in the list, go ahead and add it.

**For a better explanation see the [Example shanty](#example-file-structure-exampleshantyjson)**

# Contributing
**There are always more shanties out there and contributions are welcome but please take note of the following things:**
- Only create pull requests that reference or solve issue(s). If there is no issue for what you want to work on feel free to create one. This ensures that the change can be discussed before time and efforts are commited to something that might be more of a hindrance than acctually helpful.
- Remember to add the file name (excluding extension) to the `available-shanties.json`
- Make sure your branch is up to date, rebase if it isn't.
- Make sure your JSON is valid by runing a JSON validator.

# Example file structure: ExampleShanty.json
```Json
{
    "name": "Example Shanty",
    "versions": [
        {
            "name": "Example Name",
            "credit": "Shanty group",
            "chorus": [
                "Oh this is the chorus",
                "The jolly jolly chours",
                "where we all sing together"
            ],
            "verses": [
                [
                    "Oh this is verse one",
                    "the jolly jolly verse",
                    "One more pull, one more heave",
                    "Now we've sung the first verse"
                ],
                {
                    "chorus": true
                },
                [
                    "Oh this is verse two",
                    "the jolly jolly verse",
                    "One more pull, one more heave",
                    "Now we've sung the second verse"
                ],
                {
                    "chorus": true
                },
                [
                    "Oh this is verse three",
                    "the jolly jolly verse",
                    "One more pull, one more heave",
                    "Now we've sung the third verse"
                ],
                {
                    "chorus": true
                },
                [
                    "Oh this is the last verse",
                    "the jolly jolly verse",
                    "One last pull, one last heave",
                    "Now we've sung the example shanty"
                ]
            ]
        },
        {
            "name": "the Example Shanty 2nd revision",
            "credit": "Shanty choir",
            "chorus": [
                "Oh this is the chorus",
                "The jolly jolly chours",
                "where we all sing together"
            ],
            "verses": [
                [
                    "sing high and sing low",
                    "this jolly jolly song",
                    "one more pull, one more heave",
                    "Now we've sung the first verse"
                ],
                {
                    "chorus": true
                },
                [
                    "sing high and sing low",
                    "this jolly jolly song",
                    "one more pull, one more heave",
                    "Now we've sung the first verse"
                ],
                {
                    "chorus": true
                },
                [
                    "sing high and sing low",
                    "this jolly jolly song",
                    "One last pull, one last heave",
                    "Now we've sung the example shanty"
                ]
            ]
        }
    ]
}
```

# Maintainer(s)

| [<img src="https://avatars1.githubusercontent.com/u/31237758?v=4" width="100px;"/><br /><sub><b>Lenore</b></sub>](https://github.com/SpaceLenore) |
| :---: |
