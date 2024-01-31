# Degen DEX Agent
A step-by-step guide to building your own Telegram bot for degen season!


## Dependencies
- [python-telegram-bot (v20)](https://docs.python-telegram-bot.org/en/v20.7/)

### v0.0.1 <small>(commit [1821559](https://github.com/Hero-Development/degen-dex-agent/commit/1821559a1809693c83c69eada2fd658a7ed881ae))</small>
Add dependencies to the project
1. Create `requirements.txt` and add `python-telegram-bot>=20.7`
2. Use `pip install -r requirements.txt` to install all required modules
3. Use `pip freeze | grep telegram` to verify the installation
```bash
> pip freeze | grep telegram
python-telegram-bot==20.7
```


### v0.0.2 <small>(commit []())</small>
Register for a bot using [BotFather](https://core.telegram.org/bots/features#botfather), Telegram's bot registration system

1. Join the BotFather channel: [https://t.me/botfather](https://t.me/botfather)
2. Send command `/newbot` to start creating a new bot
3. Follow the responses to give your bot a **Name** and **username**<br />
See `./artifacts/step 2 - bot-father.png`

4. Create a local `.env` file and add your bot's token

**Notes:**
- the username must end with "bot"<br />
- the username can only have letters, numbers, and underscores<br />