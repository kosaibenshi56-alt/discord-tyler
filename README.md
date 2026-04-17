# Discord Coin Bot

## Features
- 1 message = 1 coin
- Shop system with 5 items
- Buy → Inventory → Redeem flow
- Admin redeem management with DM notifications
- Coinflip gambling
- Owner/Co-Owner give & remove coins
- Verified-role-gated transfers

## Setup

1. **Install dependencies**
   ```
   npm install
   ```

2. **Create your `.env` file** (copy `.env.example`):
   ```
   DISCORD_TOKEN=your_bot_token
   CLIENT_ID=your_app_client_id
   GUILD_ID=your_server_id
   ```

3. **Run the bot**
   ```
   npm start
   ```

## Role Names (must match exactly in your server)
| Role | Used For |
|------|----------|
| `Owner` | /givecoin, /removecoin |
| `Co Owner` or `Co-Owner` | /givecoin, /removecoin |
| `Admin Perm` (any role containing this) | /see-redeems, /finish-redeem |
| `Verified` | /give (coin transfer) |

## Commands
| Command | Description | Who |
|---------|-------------|-----|
| `/balance` | Check coin balance | Everyone |
| `/shop` | View shop | Everyone |
| `/buy <id>` | Buy item | Everyone |
| `/inventory` | View inventory | Everyone |
| `/redeem <id> <roblox> <gamepass>` | Submit redeem | Everyone |
| `/coinflip <amount> <side>` | Flip a coin | Everyone |
| `/give <user> <amount>` | Give coins | Verified only |
| `/see-redeems` | View pending redeems | Admin only |
| `/finish-redeem <id>` | Complete a redeem | Admin only |
| `/givecoin <user> <amount>` | Give coins (admin add) | Owner/Co-Owner |
| `/removecoin <user> <amount>` | Remove coins | Owner/Co-Owner |

## Railway Deployment
1. Push this folder to a GitHub repo
2. Connect repo to Railway
3. Add environment variables in Railway dashboard
4. Deploy!
