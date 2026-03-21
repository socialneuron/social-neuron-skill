---
name: social-neuron
description: AI-powered social media management with 52 MCP tools. Create content, distribute to multiple platforms, track analytics, and optimize with closed-loop learning.
version: 1.0.0
metadata:
  openclaw:
    requires:
      env:
        - SOCIALNEURON_API_KEY
      bins:
        - npx
    primaryEnv: SOCIALNEURON_API_KEY
    homepage: https://socialneuron.com/for-agents
    install:
      - kind: node
        package: "@socialneuron/mcp-server"
        bins: [socialneuron-mcp]
---

# Social Neuron

AI-powered social media management through 52 MCP tools. Create content with 35+ AI models, distribute to multiple platforms, track analytics, and let performance data improve future content automatically.

## Setup

### 1. Install

```bash
npm install -g @socialneuron/mcp-server
```

### 2. Get API Key

Sign up at https://socialneuron.com and generate an API key at Settings > Developer.

```bash
export SOCIALNEURON_API_KEY="your_api_key_here"
```

### 3. Authenticate

```bash
# Device code flow (recommended)
npx @socialneuron/mcp-server login --device

# Or paste API key directly
npx @socialneuron/mcp-server login --paste
```

### 4. Verify

```bash
npx @socialneuron/mcp-server health
```

## What This Skill Does

Social Neuron runs a closed-loop content system:

1. **Research** trends and competitor activity
2. **Generate** content ideas based on brand voice and audience data
3. **Create** posts, images, and videos with 35+ AI models
4. **Score** content through a 7-category quality gate before publishing
5. **Distribute** to connected social platforms
6. **Track** performance with real-time analytics
7. **Learn** what works and feed insights back into step 1

The loop gets smarter over time. Every post teaches the system what resonates with your audience.

## Tools (52 total)

### Research and Ideation
- `fetch_trends` - Discover trending topics and hashtags by platform
- `get_ideation_context` - Fetch brand guidelines and past performance to seed ideation
- `suggest_next_content` - AI suggestions based on analytics
- `extract_url_content` - Extract content from URLs for research
- `search_tools` - Browse available tools by keyword or category

### Content Generation
- `generate_content` - Create platform-specific social content using AI
- `adapt_content` - Transform content between platform formats
- `generate_image` - Generate on-brand images
- `generate_video` - Create short-form videos with captions
- `generate_voiceover` - AI voice narration
- `generate_carousel` - Multi-slide carousel content

### Content Planning
- `plan_content_week` - AI-assisted weekly content planning
- `save_content_plan` / `get_content_plan` / `update_content_plan` - Manage content plans
- `submit_content_plan_for_approval` - Route plans for team review

### Quality and Brand
- `quality_check` - 7-category content quality scoring (engagement, brand alignment, platform fit, readability, visual quality, hook strength, CTA effectiveness)
- `quality_check_plan` - Bulk quality analysis
- `get_brand_profile` / `save_brand_profile` - Brand voice and guidelines
- `update_platform_voice` - Platform-specific voice customization

### Distribution
- `schedule_post` - Schedule posts to connected platforms
- `schedule_content_plan` - Batch schedule entire content plans
- `find_next_slots` - Find optimal posting times
- `list_connected_accounts` - View connected social accounts

### Analytics
- `fetch_analytics` - Post-level performance metrics
- `fetch_youtube_analytics` - YouTube-specific metrics
- `refresh_platform_analytics` - Force refresh analytics data
- `get_performance_insights` - AI-powered performance analysis
- `get_best_posting_times` - Audience engagement patterns
- `generate_performance_digest` - Executive performance summary
- `detect_anomalies` - Identify unusual engagement patterns

### Comments and Engagement
- `list_comments` / `reply_to_comment` / `post_comment` - Comment management
- `moderate_comment` / `delete_comment` - Moderation tools

### Automation
- `list_autopilot_configs` / `update_autopilot_config` / `get_autopilot_status` - Automation workflows
- `run_content_pipeline` - Full pipeline: plan, generate, approve, schedule
- `create_plan_approvals` / `list_plan_approvals` / `respond_plan_approval` - Approval workflows

### System
- `get_credit_balance` / `get_budget_status` / `get_mcp_usage` - Usage tracking
- `get_loop_summary` - End-to-end content loop summary
- `check_status` - Server and account health check

## Example Workflows

### Daily Content Batch
```
fetch_trends -> get_ideation_context -> generate_content -> quality_check -> schedule_post
```

### Weekly Analytics Review
```
fetch_analytics -> get_performance_insights -> detect_anomalies -> generate_performance_digest
```

### Full Autopilot Pipeline
```
run_content_pipeline (handles: plan -> generate -> quality_check -> approve -> schedule)
```

### Cross-Platform Repurpose
```
extract_url_content -> adapt_content -> quality_check -> schedule_content_plan
```

## Authentication

OAuth 2.0 + PKCE with device code flow. Access controlled through hierarchical scopes:

- `mcp:read` - Read posts, analytics, brand profiles
- `mcp:write` - Generate content, manage plans
- `mcp:distribute` - Schedule and publish posts
- `mcp:analytics` - Performance data and insights
- `mcp:comments` - Comment management
- `mcp:autopilot` - Automation workflows
- `mcp:full` - All of the above

## Pricing

| Tier | Price | Credits/mo | MCP Access |
|------|-------|-----------|------------|
| Free | $0 | 100 | None |
| Starter | $29/mo | 800 | Read + Analytics |
| Pro | $79/mo | 2,000 | Full |
| Team | $199/mo | 6,500 | Full + multi-user |

## Links

- Website: https://socialneuron.com
- npm: https://www.npmjs.com/package/@socialneuron/mcp-server
- GitHub: https://github.com/socialneuron/mcp-server
- For Agents: https://socialneuron.com/for-agents
- For Developers: https://socialneuron.com/for-developers
- Support: socialneuronteam@gmail.com
