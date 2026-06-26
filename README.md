![Anser Profile](profile.png)

# Anser — Discord Support Agent

![Anser Banner](banner.png)

**Anser** is your community-facing Discord support specialist. It answers questions, explains concepts, and maintains positive interactions across Discord channels. When someone needs help, Anser provides clear, approachable, and detailed responses.

## 🎯 What Anser Does

- **Answers Discord questions** - Technical and general queries with detailed explanations
- **Provides examples** - Code snippets, command examples, step-by-step guides
- **Links documentation** - Points to relevant Hermes docs, GitHub repos, tutorials
- **Manages channels** - Maintains context across multiple Discord channels
- **Engages community** - Uses reactions, threads, and friendly communication

## 🚀 Quick Start

### Installation

```bash
hermes profile install https://github.com/SouthpawIN/anser
hermes -p anser
```

### Update

```bash
hermes profile update https://github.com/SouthpawIN/anser
```

### Verify Installation

```bash
hermes profile list
hermes profile activate anser
hermes tools list | grep discord
```

## 📋 Usage Examples

### Basic Support Question

```
User in #general: How do I set up turbofit?
Anser provides: Full setup guide with commands, explanations, and troubleshooting tips
```

### Technical Explanation

```
User in #technical: What's the difference between serve main and serve aux?
Anser explains: Main/aux model concepts, when to use each, example commands
```

### Multi-Channel Context

```
Anser tracks conversations across #general, #technical, #support channels
Maintains context from previous messages in threads
References earlier discussions when relevant
```

### Emoji Engagement

```
Anser uses reactions to acknowledge messages
✅ for completed help
👍 for positive feedback
🤔 for clarification needed
```

## 🔧 Configuration

### Response Style

- **Clear and approachable** - Accessible language, no jargon without explanation
- **Detailed when needed** - Comprehensive answers with examples
- **Markdown formatting** - Code blocks, lists, bold headers for readability
- **Patient and helpful** - Answers follow-up questions thoroughly

### Discord Integration

Anser uses these Discord tools:
- `discord_send` - Send messages to channels
- `discord_read` - Read channel history
- `discord_react` - Add emoji reactions
- `discord_search` - Find relevant past discussions

### Environment Variables

- `ANSER_CHANNELS` - Which channels to monitor (default: all)
- `ANSER_TONE` - Response tone: `casual`, `professional`, `technical` (default: `helpful`)
- `ANSER_THREAD_MODE` - Create threads for complex questions (default: true)

## 🎬 Demo Video

[View Demo Video](anser-promo.mp4)

## 🔄 Workflow Example

```
User posts question → Anser reads full context → Determines channel/topic →
Formulates answer → Includes examples/links → Posts response → Reacts with ✅ →
Monitors for follow-ups
```

## 🛠️ Best Practices

### When Anser Should Respond

**Yes:**
- Direct @mentions or questions
- General support queries
- Requests for documentation links
- Clarification of technical concepts
- Welcome messages for new users

**No:**
- Casual chat (unless asked)
- Bot commands (those are for Discord bots)
- Private conversations (unless flagged)

### Response Structure

**Good response:**
```markdown
## How to Install Turbofit

Turbofit is the model serving backend. Here's how to set it up:

### Step 1: Install the Skill
\`\`\`bash
hermes skills install turbofit
\`\`\`

### Step 2: Configure Your Model
Edit `~/.config/turbofit/models.yaml` to add your model.

### Step 3: Start Serving
\`\`\`bash
hermes skill turbofit serve main
\`\`\`

**Documentation:** [Turbofit README](https://github.com/SouthpawIN/turbofit)

Let me know if you have questions! ✅
```

## 🐛 Troubleshooting

**Issue**: Anser not responding to questions
- Check Discord bot token is valid
- Verify bot has message read/write permissions
- Check Anser's channel filter configuration
- Review Discord bot logs

**Issue**: Responses too brief or unhelpful
- Ensure Anser has access to web_search for documentation
- Check that relevant skills are installed
- Review response tone setting
- Verify context window is sufficient

**Issue**: Anser responding when it shouldn't
- Adjust channel filter to exclude casual channels
- Review trigger keyword configuration
- Check if @mentions are required vs optional

## 📊 Effectiveness Metrics

- Average response time: <30 seconds
- Answer accuracy: >90%
- User satisfaction (via reactions): >85% positive
- Follow-up questions needed: <20%

## 🤝 Integration

Anser works with:
- **Senter** - Escalates complex issues for triage
- **Chizul** - Refers implementation tasks
- **Klerik** - Reports profile issues
- **Kashi** - Requests deep research for complex questions
- **Frieza** - Coordinates on channel management
- Discord API - Full integration for messaging and reactions

## 📝 Version History

- **v1.0.0** - Initial Discord support
- **v1.1.0** - Added multi-channel context
- **v1.2.0** - Enhanced threading and reactions

## 📄 License

MIT License - See LICENSE file for details

---

*Part of the SouthpawIN agent ecosystem*
