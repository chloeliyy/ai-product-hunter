# 🔭 AI Product Hunter

A SKILL.md agent skill for discovering and deeply analyzing AI products — from Product Hunt rankings to any product you're curious about.

Generates structured Obsidian-compatible Markdown notes with a unique 7-layer analysis framework, including a **Taste layer** that captures the product judgment and design philosophy behind AI products.

## What It Does

**Mode 1: Product Hunt Watchlist** — Say "PH周榜" or "Product Hunt this week" and get a curated list of trending AI products from Product Hunt's weekly/monthly rankings.

**Mode 2: Deep Analysis** — Say "分析一下 Cursor" and get a comprehensive report covering company background, strategy, UX, business model, technical capabilities, product taste, and actionable insights.

## The 7-Layer Analysis Framework

| Layer | What It Covers |
|-------|---------------|
| 🏢 Company | Team, funding, vision |
| 🎯 Strategy | Value prop, moat, positioning |
| ✨ Experience | Interaction paradigm, UI/UX, onboarding |
| 💰 Business | Pricing, growth, market data |
| ⚙️ Capability | Multimodal, context window, understanding |
| 🎨 Taste | Human-AI collaboration, model strategy, product soul |
| 📊 Verdict | Strengths, weaknesses, transferable insights |

The **Taste layer** is what makes this skill different — it evaluates products through lenses inspired by Kevin Weil (OpenAI), Amanda Askell (Anthropic), Josh Woodward (Google), and Nan Yu (Linear).

## Compatible Platforms

SKILL.md is an open agent skill standard. This skill works on:

| Platform | Install Path | Status |
|----------|-------------|--------|
| **Claude Code** | `~/.claude/skills/ai-product-hunter/` | ✅ Native |
| **OpenAI Codex** | `~/.codex/skills/ai-product-hunter/` | ✅ Native |
| **Cursor** | `.cursor/skills/ai-product-hunter/` (or convert to `.cursorrules`) | ✅ Supported |
| **Windsurf** | `.windsurf/skills/ai-product-hunter/` | ✅ Supported |
| **Trae** | `.trae/skills/ai-product-hunter/` | ✅ Supported |
| **Gemini CLI** | `~/.gemini/skills/ai-product-hunter/` | ✅ Supported |
| **GitHub Copilot** | `.github/skills/ai-product-hunter/` | ✅ Supported |

> For Tier 2 platforms (Cursor, Windsurf, Trae), you may need to convert SKILL.md to their native format (`.cursorrules`, `.windsurfrules`, etc.). Tools like [agent-skill-creator](https://github.com/FrancyJGLisboa/agent-skill-creator) or [killer-skills CLI](https://killer-skills.com) can automate this.

## Installation

### Claude Code (Recommended)

```bash
git clone https://github.com/chloeliyy/ai-product-hunter.git ~/.claude/skills/ai-product-hunter
```

Restart Claude Code. Done.

### Cursor / Windsurf / Trae

```bash
# Clone to project directory
git clone https://github.com/chloeliyy/ai-product-hunter.git .cursor/skills/ai-product-hunter
```

Or use the universal installer:

```bash
npx killer-skills add chloeliyy/ai-product-hunter
```

### Manual

Download the repo and copy the folder to your agent's skill directory.

## Usage

```
# Product Hunt weekly ranking
> PH这周有什么好产品

# Product Hunt monthly ranking  
> Product Hunt 月榜

# Deep analysis of a specific product
> 分析一下 Perplexity

# Quick analysis
> Notion AI 怎么样
```

## Output

Generates Obsidian-compatible `.md` files in `AI Product Hunt/` folder:

```
AI Product Hunt/
├── 2026-04-14_Cursor.md
├── 2026-04-15_Perplexity.md
└── ...
```

Each file includes YAML frontmatter with tags for Obsidian's property system, source citations for all factual claims, and `⚠️ 信息不足` markers instead of fabricated information.

## File Structure

```
ai-product-hunter/
├── SKILL.md                         # Main skill file
└── references/
    ├── analysis-dimensions.md       # Full dimension checklist with guiding questions
    ├── taste-framework.md           # Taste analysis framework with expert references
    └── output-template.md           # Obsidian output template
```

## License

MIT
