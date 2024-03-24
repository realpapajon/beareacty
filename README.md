# beareacty
A Discord bot that logs reactions and shows statistics or pins messages.

## Description
A fork of Reacty that changes command behavior to allow for calling the !scores command with a custom emoji.

## Usage
Any time a message is reacted to the emoji-count for that emoji and that message owner is updated. Decreases counter when emoji is removed as well.

React with a :pushpin: to save a message to the pin channel. Pin channel must have been registered (see below).

### Comands

Show statistics an emoji
```
!scores :emoji:
```

Clear all scores
```
!clear-scores
```

Set channel as place for bot to put pinned messages. Actual message should not contain quotation marks, just the channel name.
```
!set-pin-channel 'channel'
```

## Setup
Install Docker if you don't already have it.

While in project root, run
```
docker-compose up
```
That will build the container and then start it. To run it detached run
```
docker-compose up -d
```

A QUICK NOTE: Bot currently can't handle multiple guilds

## Technical details
Bot is built using Discord.js with a SQLite backend for persistance. Docker is used to keep bot management easy, database is kept in a volume called database.
