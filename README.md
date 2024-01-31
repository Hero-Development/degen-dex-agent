# Degen DEX Agent
A step-by-step guide to building your own Telegram bot for degen season!


## Dependencies
- [python-telegram-bot (v20)](https://docs.python-telegram-bot.org/en/v20.7/)

### v0.0.1 <small>(commit [1821559](https://github.com/Hero-Development/degen-dex-agent/commit/1821559a1809693c83c69eada2fd658a7ed881ae))</small>
Add dependencies to the project

**Activities:**
1. Create `requirements.txt` and add `python-telegram-bot>=20.7`
2. Use `pip install -r requirements.txt` to install all required modules
3. Use `pip freeze | grep telegram` to verify the installation
```bash
> pip freeze | grep telegram
python-telegram-bot==20.7
```


### v0.0.2 <small>(commit [8ee04d8](https://github.com/Hero-Development/degen-dex-agent/commit/8ee04d8dbee225f027cd4b5c968a1417139a38f2))</small>
Register for a bot using [BotFather](https://core.telegram.org/bots/features#botfather), Telegram's bot registration system

**Activities:**
1. Join the BotFather channel: [https://t.me/botfather](https://t.me/botfather)
2. Send command `/newbot` to start creating a new bot
3. Follow the responses to give your bot a **Name** and **username**<br />
See `./artifacts/step 2 - bot-father.png`

4. Create a local `.env` file and add your bot's token

**Notes:**
- the username must end with "bot"<br />
- the username can only have letters, numbers, and underscores<br />

### v0.0.3 <small>(commit [8ee04d8](https://github.com/Hero-Development/degen-dex-agent/commit/8ee04d8dbee225f027cd4b5c968a1417139a38f2))</small>
First steps with your degen bot

Grab the first codeblock from the [PTB intro page](https://github.com/python-telegram-bot/python-telegram-bot/wiki/Extensions---Your-first-Bot#your-first-bot-step-by-step)<br />
See: `./src/main.py`

**Before we begin:**
The sample uses a literal `TOKEN` string:warning:.  We need to replace that without our own token, but for security, we don't want it embedded in our code!  In this commit, we upgrade the code to use environment variables, inherited from the terminal/shell.

The sample uses `async/await` to provide multitasking for python.  As this project evolves, we'll compare this strategy to threads for performance and scaling.

- [ ] TODO: add a module to load the .env file.

> :warning: Sometimes called a "magic constant", literal strings and numbers that exist in code without an explanation can lead to confusion and untraceable bugs in the future.

**Activities:**
1. Use command `export TG_TOKEN=YOUR_TOKEN_HERE` to add `TG_TOKEN` to terminal/shell memory.<br />
Verify with command `env | grep TG_TOKEN`.
2. Add an import for the `os` module, then use `os.getenv` to load it from the terminal/shell:<br />
`TG_TOKEN = os.getenv("TG_TOKEN")`
3. Run the bot: `python ./src/main.py`
4. Follow the link provided by BotFather and click the **Start** prompt or enter the `/start` command
