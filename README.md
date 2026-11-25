# COI Watch

Check your subs' insurance certificates against your rules. Spot low limits and end dates.

It's a hosted MCP server, so there's nothing to install. This repo is just the listing. The server code isn't here.

## Add it

Connector URL: `https://coi.rowhousesoftware.com/mcp`

In Claude Code, with your access key:

```
claude mcp add -t http coi-watch https://coi.rowhousesoftware.com/mcp -H "Authorization: Bearer YOUR_KEY"
```

Leave off the header to try the example tool only.

## Tools

- `coi_example`: Shows an example check with gaps and a reminder draft. Made-up data.
- `coi_table`: Reads your subs, rule checks, end dates and reminder drafts.
- `coi_rules`: Reads your saved insurance rules.
- `coi_draft`: Reads the reminder draft for one sub. Nothing is sent.

All four only read. They can't send a note, buy a plan or change billing.

## Sign in

The example tool is open. The other three read your own table, so they need a private access key. Sign in at https://coi.rowhousesoftware.com/connect/ and make one. It lasts 30 days. Send it as a Bearer token in the Authorization header. Your client must support that header.

## Free and paid

The free checker on the site reads one ACORD 25 PDF at a time, in your browser. A paid plan is $39 a month. It keeps every sub's file and emails you a list of gaps and end dates each night or week.

A check means the saved fields meet your rules. It does not prove coverage.

## Help

- Site: https://coi.rowhousesoftware.com
- Email: support@rowhousesoftware.com

Made by [Rowhouse Software](https://rowhousesoftware.com).
