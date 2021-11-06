# Liker
Liker is a Telegram bot that allows you to add reactions (likes, etc.) to channel posts. Liker also supports post comments.

## How to use Liker
You can either use an existing Liker bot available at https://t.me/liker10_bot. In order to do that:

1. Give Liker bot an admin permission to edit posts in your channel.

2. If you have a discussion group (e.g. post comments) — add Liker to the group also.

3. In order to customize reactions (👍 is a default reaction) send the following command to Liker in Telegram:
```
/set_reactions —channel_id [YOUR_CHANNEL_ID] —reactions [SPACE_SEPARATED_REACTIONS]
```
For example:
```
/set_reactions —channel_id @awesome_channel —reactions 👍 ❤ 😡
```

[![Deploy](https://www.herokucdn.com/deploy/button.svg)](https://heroku.com/deploy?template=https://github.com/obliviouzx/liker-bot)

## Build liker from sources
To build your own version of Liker:

1. Download the source code
```
git clone --recurse-submodules https://github.com/luckybots/liker.git
```
If you don't add `--recurse-submodules` -- you'll get an error during `make build` (make: *** No rule to make target 'build')

2. Create and customize `data/config.json` according to `data/config_example.json`.
In the `config.json` provide `bot_token` value.

3. To run with Docker use
```
make build
make run-it
```
