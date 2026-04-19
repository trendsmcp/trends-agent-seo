# trends-agent-seo

Live keyword and search trend data for AI SEO agents. One MCP
connection to Google Search, YouTube, news volume, Amazon, Reddit,
Wikipedia, TikTok, and more, with a free tier. A reliable Pytrends
alternative for any AI SEO workflow.

> Live trend data for AI agents. One connection. Every platform.
> Powered by [trendsmcp.ai](https://trendsmcp.ai)

## Why this exists

Most SEO agents stitch together a Pytrends scraper, a YouTube search
proxy, a Reddit wrapper, and a few brittle scrapers for Amazon and the
news. Trends MCP gives your agent every one of those signals through one
clean MCP server, with one API key and a normalized 0 to 100 scale so
you can compare them directly.

## Get your free API key

1. Go to [trendsmcp.ai](https://trendsmcp.ai)
2. Enter your email, key sent instantly
3. 100 free requests per month, no credit card

[Get your free key](https://trendsmcp.ai)

## Connect any AI tool in 30 seconds

Trends MCP works with every major AI client. Pick the one your SEO team
uses. Full snippets are at
[trendsmcp.ai/docs](https://trendsmcp.ai/docs).

- **Claude Desktop / Claude.ai / Claude mobile.** Add a custom
  connector with name `Trends MCP` and server URL
  `https://www.trendsmcp.ai/mcp`.
- **Cursor.** `Cursor Settings` → `Tools & MCP` → `Add a Custom MCP Server`.
- **Windsurf.** `Settings` → `Advanced Settings` → `Cascade` → `Add custom server +`.
- **VS Code Copilot.** Add to `.vscode/mcp.json` under `servers`.
- **Direct API for any agent.** `POST https://api.trendsmcp.ai/api`
  with `Authorization: Bearer YOUR_API_KEY`.

```bash
curl -s -X POST https://api.trendsmcp.ai/api \
  -H "Authorization: Bearer YOUR_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{"source":"google search","keyword":"running shoes"}'
```

## What you can ask an SEO agent

- "Using TrendsMCP, give me 5 year Google Search trend for `air fryer`."
- "Via TrendsMCP, compare YouTube search vs Google search for `cold plunge` over 1 year."
- "Using TrendsMCP, find rising subreddits in the personal finance niche over the last 90 days."
- "Via TrendsMCP, show 12 month Amazon search growth for `kettlebell`."
- "Using TrendsMCP, what is the news volume trend for `electric vehicles` over 6 months?"
- "Via TrendsMCP, get the Wikipedia page view trend for `Bitcoin` weekly."
- "Using TrendsMCP, what are the top trending hashtags on TikTok right now in `fitness`?"

## SEO use cases this unlocks

- **AI keyword research.** Pull comparable trend data across Google,
  YouTube, TikTok, Amazon, Reddit, and Wikipedia in one call set, then
  let the agent rank topic clusters.
- **Pytrends alternative for AI agents.** Skip the scraping, the rate
  limits, and the random `429`s. Use a clean MCP tool with a free tier.
- **Content briefs that ship.** Have your agent compare Google +
  YouTube + TikTok growth before deciding what to write.
- **Demand validation for new pages.** Check whether real search demand
  exists before spending tokens to write the article.
- **Topical authority maps.** Build cluster scores from rising
  subreddits, Wikipedia views, and Google News volume.
- **Brand and competitor share of voice.** Compare Google Search +
  YouTube + Reddit + Amazon on a normalized scale.
- **Internal SEO copilots.** Wire one MCP into Claude, Cursor, or
  ChatGPT and your team gets keyword data without leaving the chat.

## Three tools your AI gets

- `get_trends`, historical time series for any keyword on any source
  (5 years weekly, 30 days daily where supported).
- `get_growth`, percentage change over any period (7D, 1M, 3M, 6M, 1Y,
  YTD, custom dates).
- `get_top_trends`, what is trending right now across live platform feeds.

## All data sources in one connection

This is what makes Trends MCP different. Most SEO data tools cover one
silo. Trends MCP gives your agent every one of these through one MCP
server, with one API key.

### Keyword sources (Get Trends and Get Growth)

| source | What it measures | Keyword format |
| --- | --- | --- |
| `google search` | Google search volume | Any keyword or phrase |
| `google images` | Google image search volume | Any keyword or phrase |
| `google news` | Google News search volume | Any keyword or phrase |
| `google shopping` | Google Shopping search volume | Any keyword or phrase |
| `youtube` | YouTube search volume | Any keyword or phrase |
| `tiktok` | TikTok hashtag volume | Hashtag or topic |
| `reddit` | Subreddit subscribers | Subreddit name only, no `r/` prefix |
| `amazon` | Amazon product search volume | Product name or category |
| `wikipedia` | Wikipedia page views | Article title or topic |
| `news volume` | News article mention volume | Any keyword or phrase |
| `news sentiment` | News sentiment score (positive / negative) | Any keyword or phrase |
| `app downloads` | Mobile app download estimates (Android) | Package id or app identifier |
| `npm` | npm package weekly downloads | Exact package name e.g. react |
| `steam` | Steam concurrent players (monthly) | Game display name e.g. Elden Ring |

All values are normalized to a 0 to 100 scale where the pipeline supports
it, so you can compare different sources directly.

### Live leaderboards (Get Top Trends)

Google Trends, Google News Top News, TikTok Trending Hashtags, YouTube
Trending, X (Twitter) Trending, Reddit Hot Posts, Reddit World News,
Wikipedia Trending, Amazon Best Sellers Top Rated, Amazon Best Sellers by
Category, App Store Top Free, App Store Top Paid, Google Play, Top
Websites, Spotify Top Podcasts, Steam Most Played, GitHub Trending Repos,
IMDb MOVIEmeter, Trending Books.

The source list evolves over time. Authoritative reference at
[trendsmcp.ai/docs](https://trendsmcp.ai/docs).

## Pricing

Free forever for 100 requests per month. Paid plans available. See
[trendsmcp.ai/pricing](https://trendsmcp.ai/pricing).

## Resources

- [Get a free API key](https://trendsmcp.ai)
- [Documentation and full reference](https://trendsmcp.ai/docs)
- [Pricing](https://trendsmcp.ai/pricing)
- [All TrendsMCP repositories](https://github.com/trendsmcp)

## Security

Never commit your API key to a public repository. Use environment
variables or your OS secret store. Keys can be rotated at any time from
your TrendsMCP dashboard. The `YOUR_API_KEY` placeholder above is a
literal string to replace with your own key after you copy the snippet
locally.

## License

MIT. See [LICENSE](./LICENSE).
