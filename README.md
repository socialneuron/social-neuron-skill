# Social Neuron - OpenClaw Skill

OpenClaw skill for the [Social Neuron](https://socialneuron.com) MCP server. 96 tools (94 exposed remotely) for AI-powered social media content creation, distribution, analytics, and optimization.

## Install

```bash
openclaw install socialneuron/social-neuron-skill
```

Or use the MCP server directly:

```bash
npx @socialneuron/mcp-server
```

## What It Does

- Research trends and generate content ideas
- Create posts, images, and videos with 35+ AI models
- Score content through a 7-category quality gate
- Distribute to connected social platforms
- Track performance with real-time analytics
- Closed-loop learning: analytics improve future content

## Setup

1. Sign up at [socialneuron.com](https://socialneuron.com)
2. Get API key at Settings > Developer
3. Set `SOCIALNEURON_API_KEY` environment variable
4. Run `npx @socialneuron/mcp-server login --device`

See [SKILL.md](SKILL.md) for full tool reference and documentation.

## Links

- [Social Neuron](https://socialneuron.com)
- [MCP Server (npm)](https://www.npmjs.com/package/@socialneuron/mcp-server)
- [MCP Server (GitHub)](https://github.com/socialneuron/mcp-server)
- [For Developers](https://socialneuron.com/for-developers)
- [For Agents](https://socialneuron.com/for-agents)

## License

MIT
