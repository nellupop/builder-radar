# Builder Radar — install / use

No install step. This is a portable instruction package — `SKILL.md`
plus a fixture file. Drop the `builder-radar/` folder into any agent
workspace that can read local files (and fetch URLs, if you're pointing
it at live pages). No plugin, secret, login, or subscription required.

```
builder-radar/
  SKILL.md                              # the skill itself
  fixtures/builder-radar-input.json     # synthetic 5-record demo input
  demo/builder-radar-report.md          # sample Markdown output
  demo/builder-radar-report.json        # sample JSON output
  README.md                             # this file
```

## Copy-paste invocation (synthetic demo run)

```
Follow builder-radar/SKILL.md exactly.
Sources: fixtures/builder-radar-input.json (local, synthetic, 5 records — do not expand this list).
Produce both a Markdown radar report and a JSON radar report per the output schema in SKILL.md.
Set meta.run_label to "synthetic" and label the Markdown title SYNTHETIC.
Cap the demonstration at 3 ranked ideas and 600 words total in the Markdown report.
```

## Copy-paste invocation (real run)

```
Follow builder-radar/SKILL.md exactly.
Sources (max 5, do not expand): <list of up to 5 public URLs and/or a local records file>
Produce both a Markdown radar report and a JSON radar report per the output schema in SKILL.md.
Set meta.run_label to "live".
```

Swap the source list for whatever ≤5 URLs or local records you want
scanned. The skill will refuse to add a 6th source, refuse to message,
transact, sign up, or read anything outside that list, and will label
any synthetic input it's given.
