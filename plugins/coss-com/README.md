# coss.com for Claude (skill only)

The coss.com Agent Skill, packaged for the Claude Directory: it teaches Claude the coss SDK's conventions and how to
set up and debug coss.com's products (email, AI agent inboxes, SMS, one-time codes, e-signatures, forms, scheduling,
webhooks and risk checks). Docs: [coss.com/docs/agents](https://coss.com/docs/agents).

This build has no MCP server. For the full plugin, which adds the coss.com MCP server (`coss-mcp`: docs search,
delivery diagnosis and the API), install `coss` from this repository's marketplace:

```sh
/plugin install coss --marketplace cosscom/skills
```

MIT licensed, maintained by coss.com, from the team behind Cal.com.

## Data

The skill sends nothing anywhere by itself. It has Claude run `npx coss-cli` and the `coss` SDK in your project, which
call coss.com's API (`api.coss.com`) with your project's `COSS_API_KEY`: what a command sends, such as an email's
recipients and content, goes to coss.com and is kept for the periods in
[coss.com/docs/data-retention](https://coss.com/docs/data-retention), under the
[privacy policy](https://coss.com/legal/privacy).
