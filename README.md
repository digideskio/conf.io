# Conf.io - NodeKnockout 2013 Entry

This application enables speakers to deliver real-time video seminars to over 
250 participants at once and transcribes the speaker's voice into text and 
translates it into the language of each individual participant.

> This repository exists for historical purposes. **It will not be actively 
> maintained**. However, it is also here for your hacking pleasure so feel free
> to fork and use any part as the basis for your project or pick the bits from
> which you might benefit.

Conf.io was a NodeKnockout 2013 entry. We placed 7th overall and got some great 
feedback from industry professionals and the like. We have decided to take the
concept further and explore the possiblities the application has for business. 
What we developed in the 48 hours now belongs to the interwebs (and *you*)!

## Setup

First install dependencies using NPM.

```
~# cd path/to/conf.io
~# [sudo] npm install
```

You will need to generate a Google Translate API key and place it as the value
of the `key` parameter on line 82 in *lib/client/classes.coffee*. Example:

```coffeescript
translate: (text, language_from=en, language_to=en) ->
    data =
        format: "html"
        key: "" # place google translate api key here
        prettyprint: yes
        source: language_from
        target: language_to
        q: text
```

After this, simply run `npm start` from the project root and party!
