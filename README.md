# Telegram Gifts Buyer

An automated Telegram userbot that purchases new gifts as they become available in the Telegram store. The bot can handle both limited and non-limited gifts with flexible configuration options.

> 🌐 [Русская версия документации](README-RU.md)

## 📋 Features

- **Automated Gift Detection**: Continuously monitors for new gifts in the Telegram store
- **Selective Purchasing**: Buy gifts within your specified price range
- **Multiple Recipients**: Send gifts to one or more users
- **Customizable Quantity**: Send multiple copies of the same gift
- **Notification System**: Get updates on purchases through a designated Telegram channel
- **Advanced Filtering**: Choose to buy only limited or upgradable gifts

## 🛠️ Installation

### Prerequisites

- Python 3.9 or higher
- A Telegram account with API access

### Setup Steps

1. Clone the repository:

   ```bash
   git clone https://github.com/roxylapatate/Gifts-Buyer.git
   cd Gifts-Buyer
   ```

2. Install the required dependencies:

   ```bash
   pip install -r requirements.txt
   ```

3. Configure the application:
   - Edit the `config.ini` file with your API credentials
   - Set your preferred gift purchasing parameters

## ⚙️ Configuration

Open `config.ini` and configure the following sections:

### Telegram API Settings

```ini
[Telegram]
API_ID = your_api_id
API_HASH = your_api_hash
PHONE_NUMBER = +1234567890
CHANNEL_ID = -100123456789  # Channel for notifications (optional)
```

### Bot Behavior

```ini
[Bot]
INTERVAL = 10     # Check interval in seconds
TIMEZONE = UTC    # Your timezone
LANGUAGE = EN     # Interface language (EN or RU)
```

### Gift Preferences

```ini
[Gifts]
MIN_GIFT_PRICE = 0          # Minimum price to consider
MAX_GIFT_PRICE = 10000      # Maximum price to consider
GIFT_QUANTITY = 1           # Number of each gift to send
USER_ID = 123456789         # Recipients (comma-separated)
PURCHASE_NON_LIMITED_GIFTS = False    # Whether to buy non-limited gifts
PURCHASE_ONLY_UPGRADABLE_GIFTS = False  # Buy only upgradable gifts
```

## 🚀 Usage

Run the bot with:

```bash
python main.py
```

The bot will:

1. Log in to your Telegram account
2. Start monitoring for new gifts
3. Purchase gifts that match your criteria
4. Send notifications through your specified channel

## 📝 Notes

- Make sure your account has enough stars to purchase gifts
- The bot will automatically handle errors like insufficient balance
- For the best experience, run the bot on a server for 24/7 monitoring
