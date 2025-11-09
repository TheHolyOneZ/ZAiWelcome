# ZAiWelcome
A sophisticated Discord bot cog that creates personalized, AI-generated welcome messages for new members using Google's Gemini AI. Each welcome can be uniquely tailored based on member profiles, activities, avatars, and customizable personality "gems."

> 💡 **Built for the Zygnal Ecosystem — to download and use this extension, you must be part of the Zygnal Ecosystem.**  
> This extension (cog) is part of the **Zygnal Ecosystem** and is only available through its supported platforms.  
> You can use it with:  
> - The **[Discord Bot Framework](https://github.com/TheHolyOneZ/discord-bot-framework)** — ideal for developers who want full control and flexibility *(includes an integrated extension marketplace)*, or  
> - The **[ZygnalBot](https://zygnalbot.de)** — a prebuilt, plug-and-play Discord bot *(also includes an integrated extension marketplace)*.  
>
> Browse and install extensions at [zygnalbot.com/extension](https://zygnalbot.com/extension).  
> For help or community discussions, join us on Discord: [discord.gg/sgZnXca5ts](https://discord.gg/sgZnXca5ts)


# ZAiWelcome - AI-Powered Discord Welcome Bot

A sophisticated Discord bot cog that creates personalized, AI-generated welcome messages for new members using Google's Gemini AI. Each welcome can be uniquely tailored based on member profiles, activities, avatars, and customizable personality "gems."

---

## Table of Contents

- [Overview](#overview)
- [Key Features](#key-features)
- [Getting Started](#getting-started)
- [Command Reference](#command-reference)
- [Control Panel Navigation](#control-panel-navigation)
- [Personality Gems System](#personality-gems-system)
- [Configuration Options](#configuration-options)
- [Auto-Role Assignment](#auto-role-assignment)
- [Logging & Analytics](#logging--analytics)
- [Advanced Features](#advanced-features)
- [Best Practices](#best-practices)
- [Troubleshooting](#troubleshooting)
- [Privacy & Security](#privacy--security)

---

## Overview

ZAiWelcome transforms the standard member welcome experience by using artificial intelligence to craft unique, contextual greetings. The bot analyzes user profiles including usernames, bios, activities, account age, and even avatars to generate personalized messages that make new members feel genuinely welcomed.

### What Makes ZAiWelcome Special?

- **Dynamic Personality System**: Create multiple "gems" - each with unique personalities and styles
- **Deep Profile Analysis**: Incorporates username, bio, activities, Spotify listening, custom status, and more
- **Avatar Recognition**: Optional AI-powered avatar analysis with intelligent caching
- **Flexible Deployment**: Choose between AI mode or traditional static messages
- **Smart Queue Management**: Handles member join spikes with configurable rate limiting
- **Comprehensive Logging**: Track welcomes, view analytics, and debug with extreme logging mode

---

## Key Features

### 🤖 AI-Powered Generation
- Utilizes Google Gemini 2.0 Flash for natural, contextual messages
- Analyzes member profiles including activities, bio, account age
- Optional avatar analysis with visual element recognition
- Intelligent caching to reduce API costs

### 💎 Personality Gems
- Create unlimited welcome personalities
- Configure tone, length, and emoji usage per gem
- Channel-specific gem assignment (include/exclude modes)
- Enable/disable gems without deletion
- Per-gem avatar analysis settings

### 📊 Smart Management
- Encrypted API key storage
- Automatic API key validation (24-hour watchdog)
- Configurable concurrent request limiting
- Avatar analysis caching (reduces costs by ~70%)
- Queue-based processing for join spikes

### 🎭 Auto-Role Assignment
- Assign roles automatically to new members
- Multiple role support
- Hierarchy-aware role management

### 📈 Analytics & Logging
- Track welcome message history
- Monitor API usage and token consumption
- Extreme debug logging for troubleshooting
- Owner-only metrics dashboard

---

## Getting Started

### Prerequisites

1. **Bot Permissions Required**:
   - Send Messages
   - Embed Links
   - Manage Roles (for auto-role feature)
   - Manage Guild (for invite tracking)
   - Read Message History

2. **Gemini API Key**:
   - Visit [Google AI Studio](https://aistudio.google.com/apikey)
   - Create a new API key
   - Keep it secure - you'll enter it in the bot settings

### Initial Setup

1. Invite the bot to your server with required permissions
2. Run `/zaiwelcome` to open the control panel
3. Navigate to **Settings** tab
4. Click "🔑 Set Gemini API Key" and paste your key
5. Click "📺 Set Welcome Channel" and provide your welcome channel ID
6. Toggle the system **ON** from the Main tab
7. Toggle **AI Mode ON** (or leave off for static messages)

---

## Command Reference

### Primary Command

**`/zaiwelcome`**
- Opens the interactive control panel
- Requires: Manage Guild permission, admin role, or server owner
- All configuration is done through the panel interface

---

## Control Panel Navigation

The control panel has 5 main tabs accessible via buttons:

### 1️⃣ Main Tab
**Overview & Quick Actions**

Displays:
- System status (Active/Inactive)
- Current mode (AI/Static)
- API key status
- Active gem count
- 30-day welcome statistics

Buttons:
- **Toggle System ON/OFF**: Master enable/disable switch
- **Toggle AI Mode**: Switch between AI-generated and static messages

### 2️⃣ 💎 Gems Tab
**Personality Management**

View all configured gems with:
- Enabled status (✅/❌)
- Name and description
- Tone setting
- Channel mode (all/include/exclude)

Buttons:
- **➕ Create New Gem**: Opens gem creation modal
- **🛠️ Manage Gem**: Select and edit existing gems

### 3️⃣ ⚙️ Settings Tab
**System Configuration**

Displays:
- Welcome channel
- Log channel
- Extreme log channel and mode
- Static message preview
- API rate limit
- Avatar cache size

Buttons:
- **📺 Set Welcome Channel**: Configure where welcomes are sent
- **🔑 Set Gemini API Key**: Add/update API key
- **📋 Set Log Channel**: Configure member join/leave logging
- **✉️ Set Static Message**: Set fallback/static welcome text
- **⚡ API Settings**: Configure rate limiting and caching
- **🔬 Set Extreme Log** (Owner Only): Configure debug logging
- **📊 View Metrics** (Owner Only): View API usage statistics

### 4️⃣ 📜 Logs Tab
**Recent Activity**

Shows the 10 most recent welcomes:
- Timestamp
- Username
- Gem used
- Message preview

Buttons:
- **🔄 Refresh**: Reload log data

### 5️⃣ 🎭 Roles Tab
**Auto-Role Configuration**

Lists all configured auto-roles.

Buttons:
- **➕ Add Auto-Role**: Add role to assign on join
- **➖ Remove Auto-Role**: Remove role from auto-assignment

---

## Personality Gems System

Gems are the heart of ZAiWelcome's customization. Each gem defines a unique welcome personality.

### Creating a Gem

1. Navigate to **💎 Gems** tab
2. Click **➕ Create New Gem**
3. Fill in the modal:
   - **Gem Name**: Identifier (e.g., "Friendly Bot", "Meme Lord")
   - **Description**: Brief purpose description
   - **Personality/Style Instructions**: Detailed AI behavior instructions

**Example Personality Instructions**:
```
You are an enthusiastic gaming community greeter who loves memes and emojis. 
You reference popular games, use gaming slang, and always include at least 
one game-related joke or reference. Keep it casual and fun!
```

### Editing a Gem

From **🛠️ Manage Gem** interface:

**Toggle Enabled**: Activate/deactivate without deleting

**Edit Details**: Change name and description

**Edit Personality**: Modify AI behavior instructions

**Channel Filter**: Configure where this gem is active
- **All Channels**: Gem works in any welcome channel
- **Include Specific**: Only works in specified channels
- **Exclude Specific**: Works everywhere except specified channels

**Style Settings**:
- **Tone**: None (pure personality), Friendly, Professional, Casual, Enthusiastic, Formal
- **Length**: Short (1-2 sentences), Medium (2-4), Long (4-6)
- **Emoji Level**: None, Minimal (1-2), Moderate (3-5), Heavy (frequent)

**Toggle Avatar Analysis**: Enable/disable avatar image analysis for this gem

**Toggle Activities**: Include/exclude member activities in context

**Toggle Embed Mode**: Send as Discord embed vs plain text

**❌ Delete Gem**: Permanently remove gem (requires confirmation)

### Gem Selection Logic

When a member joins:
1. Bot checks enabled gems
2. Evaluates channel mode filters
3. Selects first matching gem
4. Generates message using that gem's configuration

---

## Configuration Options

### Welcome Channel Setup

**Purpose**: Where welcome messages are sent

**Setup**:
1. Settings tab → "📺 Set Welcome Channel"
2. Right-click your welcome channel → Copy ID
3. Paste ID in modal

### API Key Configuration

**Purpose**: Authenticate with Google Gemini API

**Setup**:
1. Settings tab → "🔑 Set Gemini API Key"
2. Paste your API key
3. Bot automatically validates key
4. Key is encrypted and stored securely

**Security Features**:
- Encrypted storage using Fernet encryption
- Unique encryption key per installation
- 24-hour automatic validation
- System auto-disables if key becomes invalid

### Log Channel Setup

**Purpose**: Track member joins/leaves

**Setup**:
1. Settings tab → "📋 Set Log Channel"
2. Paste channel ID
3. Bot sends embed notifications for joins/leaves

**Log Includes**:
- Member mention and ID
- Account creation date (relative timestamp)
- Current member count
- Member avatar thumbnail

### Static Welcome Message

**Purpose**: Fallback message or AI-disabled mode

**Setup**:
1. Settings tab → "✉️ Set Static Message"
2. Write custom message
3. Use variables:
   - `{user}` - Member mention
   - `{server}` - Server name
   - `{member_count}` - Total member count

**Example**:
```
Welcome {user} to **{server}**! 🎉 You're member #{member_count}!
```

---

## Auto-Role Assignment

Automatically assign roles to new members upon joining.

### Adding Auto-Roles

1. Navigate to **🎭 Roles** tab
2. Click **➕ Add Auto-Role**
3. Right-click role → Copy ID
4. Paste ID in modal

**Requirements**:
- Bot must have "Manage Roles" permission
- Bot's role must be higher than assigned role in hierarchy
- Role must exist in server

### Removing Auto-Roles

1. Navigate to **🎭 Roles** tab
2. Click **➖ Remove Auto-Role**
3. Paste role ID to remove

**Note**: Removed roles won't affect members who already have them.

---

## Logging & Analytics

### Standard Logging

**Welcome Log**: Tracks all welcome messages
- User ID and username
- Join timestamp
- Gem used
- Message content
- Channel sent
- Token usage

**Admin Log**: Records configuration changes
- Timestamp
- User who made change
- Action description

### Extreme Debug Logging (Owner Only)

**Purpose**: Deep troubleshooting and AI transparency

**Setup**:
1. Settings tab → "🔬 Set Extreme Log"
2. Paste channel ID
3. Choose mode via "⚡ API Settings" → "Set Extreme Log Mode"

**Modes**:
- **All Welcomes**: Log every single welcome generation
- **10% Sample**: Randomly log 10% of welcomes (reduces spam)
- **Off**: Disable extreme logging

**Logged Information**:
- Complete user data sent to AI
- Server information provided
- Avatar analysis results (with cached indicator)
- AI processing details
- Final generated message
- Token consumption
- Analyzed avatar image (if avatar analysis enabled)

**⚠️ Privacy Warning**: This channel exposes ALL data sent to AI, including potentially sensitive profile information. Keep it private and owner-only.

### API Metrics Dashboard (Owner Only)

**Access**: Settings tab → "📊 View Metrics"

**Displays**:
- Total API calls made
- Total tokens consumed
- Average tokens per call
- Avatar analyses performed
- Cached avatar hits
- Average calls per day
- Estimated cost (approximate)
- Days since tracking began

**Actions**:
- **Reset Metrics**: Clear all statistics (starts fresh)

---

## Advanced Features

### API Rate Limiting

**Purpose**: Control concurrent AI generations during member join spikes

**Setup**: Settings tab → "⚡ API Settings" → "Set Rate Limit"

**Recommended Values**:
- Small servers (<100 members): 5-10
- Medium servers (100-1000): 10-15
- Large servers (1000+): 15-20

**How It Works**:
- Members join → Added to queue
- Bot processes up to N concurrent requests
- Remaining members wait in queue
- Prevents API rate limit errors
- Ensures stable performance

### Avatar Analysis Caching

**Purpose**: Reduce API costs by caching avatar analyses

**How It Works**:
- First time avatar analyzed: Full AI vision analysis performed
- Result cached for 1 hour
- Subsequent joins with same avatar: Uses cached analysis
- Cache automatically cleaned (max 100 entries)
- Can be manually cleared via API Settings

**Cost Savings**: Approximately 70% reduction in vision API calls for avatars that appear multiple times.

**Cache Entry Shows**:
- In extreme logs: "[CACHED]" tag on avatar analysis field
- In metrics: "Cached Avatars" count

### Queue Management

**Purpose**: Handle large member influxes gracefully

**Process**:
1. Member joins → Added to guild-specific queue
2. Background task processes queue every 0.5 seconds
3. Rate limiter controls concurrent generations
4. Failed generations fall back to simple welcome
5. Successful welcomes logged

**Benefits**:
- No lost welcomes during raids/mass joins
- Prevents bot crashes
- Maintains API rate limits
- Graceful degradation

### Invite Tracking

**Purpose**: Track which invite was used (future feature expansion)

**How It Works**:
- Bot caches all server invites on startup
- Tracks invite use changes on member join
- Requires "Manage Guild" permission

**Current Use**: Prepared for future invite-based gem selection or statistics.

---

## Best Practices

### API Key Management

✅ **DO**:
- Keep your API key private
- Set up billing alerts in Google Cloud
- Monitor usage via metrics dashboard
- Use API rate limiting

❌ **DON'T**:
- Share your API key
- Use keys from untrusted sources
- Ignore invalid key warnings

### Gem Configuration

✅ **DO**:
- Create specific, detailed personality instructions
- Test gems in your welcome channel
- Use channel filters for themed channels
- Disable unused gems instead of deleting

❌ **DON'T**:
- Make personality instructions too vague
- Enable all gems without channel filters (random selection)
- Use offensive or controversial personalities

### Performance Optimization

✅ **DO**:
- Enable avatar analysis only for important gems
- Use moderate rate limits (10-15 for most servers)
- Enable avatar caching
- Use 10% sample mode for extreme logs

❌ **DON'T**:
- Enable avatar analysis on all gems unnecessarily
- Set rate limit too low (<5) or too high (>25)
- Use "All Welcomes" extreme log mode on large servers

### Member Experience

✅ **DO**:
- Keep messages welcoming and positive
- Test with your own alt account
- Use medium length for best engagement
- Include emoji for personality

❌ **DON'T**:
- Make messages too long (overwhelming)
- Use overly formal tone for casual communities
- Ignore negative feedback from members

---

## Troubleshooting

### Bot Not Sending Welcomes

**Check**:
1. System enabled? (Main tab, green status)
2. Welcome channel set? (Settings tab)
3. Bot has Send Messages permission in that channel?
4. If AI mode: API key configured and valid?
5. If AI mode: At least one gem enabled?

### API Key Errors

**"Invalid API Key"**:
- Verify key copied correctly (no extra spaces)
- Check key hasn't been deleted in Google AI Studio
- Ensure billing is enabled on Google Cloud account
- Test key directly at https://aistudio.google.com

**System Auto-Disabled**:
- Check log channel for error message
- Likely invalid/expired API key
- Re-enter valid key in Settings
- Toggle system back ON

### Welcomes Using Wrong Gem

**Issue**: Different gem than expected

**Cause**: First matching gem is selected based on:
1. Gem enabled status
2. Channel mode filters

**Solution**:
- Check gem order (newest first)
- Verify channel filters
- Disable competing gems
- Use Include/Exclude modes strategically

### Slow Welcome Messages

**Causes**:
- API rate limit too restrictive
- Many members joining simultaneously
- Avatar analysis enabled (adds time)

**Solutions**:
- Increase rate limit (Settings → API Settings)
- Disable avatar analysis for faster gems
- Consider queue-based processing is working as intended

### Missing Permissions

**"Cannot Send Messages"**:
- Check bot role has Send Messages permission
- Verify channel-specific permission overrides
- Ensure bot role isn't below muted role

**"Cannot Assign Roles"**:
- Bot needs Manage Roles permission
- Bot's role must be ABOVE assigned roles in hierarchy
- Check role still exists

---

## Privacy & Security

### Data Storage

**What's Stored**:
- Guild configuration (channels, settings)
- Gem definitions (name, personality, settings)
- Welcome logs (username, message content, timestamps)
- Admin action logs
- Extreme debug logs (if enabled)

**Where**:
- Local SQLite databases (one per guild)
- Encrypted API keys (Fernet encryption)
- Unique encryption key per bot installation

**Data Access**:
- Only bot owner/admins can access via commands
- Database files stored in bot's data directory
- No external transmission except to Gemini API

### API Privacy

**Data Sent to Google Gemini**:
- Server name, member count, description
- Member username, display name, ID
- Account age, join date
- Member bio (if include_bio enabled)
- Member activities/status (if include_activities enabled)
- Avatar image (if analyze_avatar enabled)

**Data NOT Sent**:
- Message history
- DMs
- Other members' information
- Server invite links
- Email addresses

**Google's Usage**:
- Gemini API processes requests
- Google's data usage policy applies
- Data not used to train models (per Gemini API terms)

### Extreme Logging Risks

⚠️ **Warning**: Extreme logs contain ALL data sent to AI

**Includes**:
- Full user profiles
- Avatar images
- Activities and statuses
- Bio information
- AI-generated content

**Recommendations**:
- Use owner-only channel
- Use 10% sample mode
- Don't enable in public channels
- Periodically clean logs
- Inform staff if they have access

---

## Support & Resources

### Getting Help

- **Bug Reports**: Report to bot developer
- **Feature Requests**: Contact bot owner
- **API Issues**: Check Google AI Studio status page

### Useful Links

- [Google AI Studio](https://aistudio.google.com)
- [Gemini API Documentation](https://ai.google.dev/docs)
- [Discord Developer Portal](https://discord.com/developers)

### Credits

**Created by**: TheHolyOneZ (TheZ)  
**Powered by**: Google Gemini AI  
**Framework**: discord.py  

---

## Version Information

**Bot Name**: ZAiWelcome  
**Model**: Gemini 2.0 Flash Experimental  
**License**: Custom License (See source file header)  

---

*This bot cog is designed to create welcoming, personalized experiences for your community members. Use responsibly and always prioritize member privacy and comfort.*
