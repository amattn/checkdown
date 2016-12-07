# checkdown
A checklist/todo text format and tools in the spirit of markdown.

Checkdown files usually have the `.checkdown` suffix appended to the filename.

## What does a checkdown document look like?

### example.checkdown

    # Home
        [ ] Get the emission test done. -car @2016-12-06
        [x] Pay Rent -bills @2016-12-01
        [ ] Call Gobby about the New Years party.
    # Work
        [x] Schedule meeting with Kermy
        [ ] Refactor the frobber widget
    ## v7.3.3
        [ ] Release version 7.3.3 @2016-11-20 @13:00
            [ ] Update Documentation
                [x] New API Endpoints
                [ ] README
            [ ] Regression tests
    # School
        [ ] Apply to grad school due 2016-12
            [x] Look up standardized testing dates
            [ ] Narrow list to top 3 schools
            [ ] Reqeust applicaiton packets for top 3


## Philosophy

The philisophy of the format is that checkdown formatted text is easy to read in a pure text editor.
It is easy to both create and edit checkdown formatted text in both both desktop and mobile text editors.
Lastly, fully compliant clients assist with automatic, canonical formatting of checkdown documents.  A normal text editor is considered partially compliant.  A fully compliant text editor has custom formatting smarts built in.

## Components

A checkdown component consists of tasks, tags and notes.  Tasks are the star of the show and are denoted by square brackets `[ ]`.  Tasks can be nested with four spaces preceding the square brackets.  There are two type of tags, group tags and inline tags.  A group tag is essentially a hashtag on its own line.  You can actually use between 1-6 hashes to denote nested tags.  Inline Tags are short span of text preceded by a `-` or `@`.  Dash (`-`) inline tags can be any arbitrary text.  Atmark (`@`) inline tags are dedicated for people or dates.

## Fully compliant clients

Checkdown compliant clients (dedicated apps, IDE plugins, etc.) are required to have some smart autoformatting built in.  Since checkdown is designed to support mobile clients, some example of the autoformatting include:

- converting [] to [ ].
- converting 1, 2 or 3 spaces, or s single tab to 4 spaces.
- converting ( ) to [ ].
- converting Group Tags to Hashes if dashes are used.

## Misc

This project is similar in spirit to both the [todo.txt](http://todotxt.com) and the [taskpaper](https://www.taskpaper.com) formats.
