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

The high level vision of checkdown is a format that is easy to use humans and to a lesser extent for tools.

The philisophy of the format is that checkdown formatted text is easy to read in a pure text editor.
It is easy to both create and edit checkdown formatted text in both desktop and mobile text editors.
Lastly, there the format should be tool friendly. A fully compliant checkdown editor will assist with automatic, canonical formatting of checkdown documents.  A normal text editor is considered partially compliant.  A fully compliant text editor has custom formatting smarts built in.

## Components

A checkdown component consists of tasks, tags and notes.  

Tasks are the star of the show and are denoted by square brackets `[ ]`.  Tasks can be nested with four spaces preceding the square brackets.  

There are two type of tags, group tags and inline tags.  A group tag is essentially a hashtag on its own line.  Any following tasks are automattically tagged with the current set of group tags.  You can actually use between 1-6 hashes to denote nested tags.  Inline Tags are short span of text preceded by a `-` or `@`.  Dash (`-`) inline tags can be any arbitrary text.  Atmark (`@`) inline tags are dedicated for people or dates.

The following checkdown text:

    # Work
    ## Project A
    [ ] task 1
    ## Project B
    [ ] task 2
    [ ] task 3
    # Home
    [ ] task 4

is symantically equivalent to the following:

    [ ] task 1 -Work -"Project A"
    [ ] task 2 -Work -"Project B"
    [ ] task 3 -Work -"Project B"
    [ ] task 4 -Home

If you need to reset the current set of group tags, you have two optoins.  An empty hashtag will reset at the appropriate nested level.  Or you can use a markdown-style divider (`---`) to do a full reset.

Notes are just lines of text that start with neither square brackets (`[]`), dividers (`---`), or hashtags (`#`).

## Fully compliant clients

Checkdown is designed to be mobile friendly.  On many mobile devices, certain characters are easier to get to or require fewer taps.  These typically include dot (`.`), dash (`-`), exclamation mark (`!`), and question mark (`?`).  Furthermore, parenthesis (`()`) are typically easier to type than square brackets (`[]`).  

Checkdown fully-compliant clients (dedicated apps, IDE plugins, etc.) are required to have some smart autoformatting built in.  Since checkdown is designed to support mobile clients, some example of the autoformatting include:

- converting [] to [ ].
- converting 1, 2 or 3 spaces, or a single tab to 4 spaces.
- converting ( ) to [ ].
- converting Group Tags to Hashes if dashes are used.
- converting any other encoding to UTF-8.

## Misc

This project is similar in spirit to both the [todo.txt](http://todotxt.com) and the [taskpaper](https://www.taskpaper.com) formats.

## Versioning and project state

This project should currently be considered alpha.  As progress is made, and the format evolves, the project will go through the following stages:

- alpha: (current) Any changes, include non-compatible changes are possible
- beta: Format is to be considered very stable. Backward-incompatible changes are unlikely and extremely discouraged.
- final: Only forward compatible changes will be made