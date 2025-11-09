
# Convogram Bot - AI-Powered Telegram Inbox Manager

A sophisticated Telegram bot built with Mastra framework that provides intelligent message management, inbox organization, and multi-chain wallet integration.

## Features

- 🤖 **AI-Powered Analysis**: Automatic message categorization and sentiment analysis
- 📬 **Smart Inboxes**: Create and manage multiple ConvoBoxes with custom rules
- 💰 **Multi-Chain Wallet**: Support for Solana and EVM chains (Ethereum, Base, etc.)
- 📅 **Meeting Scheduler**: Schedule and manage meetings with automatic reminders
- 🔔 **Group Management**: Create and manage Telegram groups with payment gates
- 🎯 **Flexible Filtering**: Filter messages by category, urgency, and custom preferences

## Tech Stack

- **Framework**: [Mastra](https://mastra.ai) - AI agent orchestration framework
- **Runtime**: Node.js 22+
- **Database**: PostgreSQL
- **AI**: OpenAI/OpenRouter integration
- **Blockchain**: Solana & EVM chains via web3.js and viem
- **Workflow Engine**: Inngest for background jobs

## Deployment on Replit

This project is designed to run on [Replit](https://replit.com) with the following features:

1. **Automatic Setup**: Fork this Repl and all dependencies will be installed automatically
2. **PostgreSQL Integration**: Built-in database for storing users, messages, and inboxes
3. **Secrets Management**: Use Replit Secrets to configure:
   - `TELEGRAM_BOT_TOKEN`: Your Telegram bot token from [@BotFather](https://t.me/botfather)
   - `OPENAI_API_KEY` or `OPENROUTER_API_KEY`: For AI analysis
   - Other API keys as needed

4. **One-Click Deploy**: Use the Deploy button in Replit to publish to production

## Setup Instructions

### 1. Fork to Replit
Click the "Fork" button to create your own copy of this project.

### 2. Configure Secrets
Add these required secrets in the Replit Secrets tool:
- `TELEGRAM_BOT_TOKEN` - Get from [@BotFather](https://t.me/botfather)
- `OPENAI_API_KEY` or `OPENROUTER_API_KEY` - For AI features
- `DATABASE_URL` - Auto-configured by Replit PostgreSQL

### 3. Run the Project
Click the "Run" button. The bot will:
- Initialize the database schema
- Start the Mastra development server
- Set up the Telegram webhook automatically

### 4. Deploy to Production
Click the "Deploy" button to publish your bot with:
- Autoscale deployment for handling traffic
- Persistent PostgreSQL database
- Custom domain support (optional)

## Bot Commands

- `/start` - Initialize your account
- `/profile` - View and edit your profile settings
- `/inboxes` - Manage your ConvoBoxes
- `/messages` - View your inbox messages
- `/wallet` - Manage your multi-chain wallet
- `/groups` - Create and manage groups
- `/meetings` - Schedule meetings

## Project Structure

```
src/
├── mastra/
│   ├── agents/          # AI agents for message analysis
│   ├── workflows/       # Mastra workflows
│   ├── tools/           # Custom tools (inbox, message, wallet)
│   └── inngest/         # Background job functions
├── triggers/            # Telegram webhook handlers
└── utils/               # Utilities (DB, wallets, API helpers)
```

## Database Schema

The bot uses PostgreSQL with tables for:
- `users` - User profiles and preferences
- `inboxes` - ConvoBox configurations
- `messages` - Received messages with AI analysis
- `wallets` - Multi-chain wallet management
- `meetings` - Scheduled meetings
- `groups` - Telegram group management

## AI Analysis

Messages are automatically analyzed for:
- **Category**: business, personal, urgent, spam, etc.
- **Sentiment**: positive, negative, neutral
- **Urgency Score**: 1-10 priority rating
- **Summary**: AI-generated message summary

## Multi-Chain Wallet

Supports:
- **Solana**: Native SOL and SPL tokens
- **EVM Chains**: Ethereum, Base, Polygon, Arbitrum, Optimism
- Secure key encryption
- Transaction history
- Balance checking

## License

ISC

## Support

For issues and questions:
- Check the [Mastra documentation](https://docs.mastra.ai)
- Review [Replit deployment docs](https://docs.replit.com/deployments)
- Open an issue in this repository

## Security Notes

⚠️ **Never commit secrets to the repository**
- Use Replit Secrets for all API keys and tokens
- Private keys are encrypted in the database
- Webhook endpoints are secured via Telegram validation

---

Built with ❤️ using Mastra on Replit
