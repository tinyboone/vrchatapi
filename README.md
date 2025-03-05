# Discord VRChat Bot - README

This bot integrates Discord with VRChat, allowing users to control statuses, check user details, and detect E-Boys.

## Setup

To run this bot, follow these steps:

1. Ensure you have Python installed.
2. Install dependencies with:
   ```sh
   pip install discord requests
   ```
3. Replace `BOT_TOKEN` in the script with your Discord bot token.
4. Run the script using:
   ```sh
   python bot.py
   ```

## Commands

- **`/trollme`** - Change VRChat status (Boosters Only)
- **`/eboydetector`** - Analyze VRChat user E-Boy rating (0-10)
- **`/vrchatcheck`** - Retrieve full VRChat user profile

## How It Works

The bot communicates with VRChat’s API, updating user statuses and fetching details.

- Uses Discord buttons for interaction.
- Requires authentication via VRChat API cookies.
- Only server boosters can change the bot's VRChat status.

## Embed Preview

Below is an example of what the bot's embed messages look like:

![Embed Preview]()

*(Replace `embed-preview.png` with the actual image file showcasing the embed UI.)*

## Code Example

```python
import discord
from discord.ext import commands
import requests

bot = commands.Bot(command_prefix="!")

@bot.event
async def on_ready():
    print(f"Logged in as {bot.user}")
```

## API Usage

The bot interacts with VRChat API endpoints to fetch and update user data.

```python
VRCHAT_API_URL = 'https://vrchat.com/api/1'
HEADERS = {
    'User-Agent': 'Mozilla/5.0',
    'Cookie': 'auth=your_auth_cookie_here',
    'Content-Type': 'application/json',
}
```
## License

This project is open-source under the MIT License.
