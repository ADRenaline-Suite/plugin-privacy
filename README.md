<p align="right">Language:&emsp;<img alt="English" src="https://raw.githubusercontent.com/ADRenaline-Suite/.github/main/profile/lang-en-on.svg" align="middle" style="vertical-align:middle"> <a href="README.es.md" style="vertical-align:middle"><img alt="Español" src="https://raw.githubusercontent.com/ADRenaline-Suite/.github/main/profile/lang-es-off.svg" align="middle" style="vertical-align:middle"></a></p>

# Privacy (`plugin-privacy`)

Records one processing activity: the categories, the purpose, who decides, and how long it is kept. It does not choose a legal basis.

The instructions are in English. The file the plugin saves follows the language of the request. Files go in `adrenaline/privacy/`.

## /priv-processing

The categories and the purpose. An identifier that singles out a person stays out.

## /priv-roles

Who decides the purpose, and who processes for them, only when the person named the parties.

## /priv-retention

How long each category is kept. A period nobody gave stays a gap.

## Help

## /priv-help

The catalog of this plugin. It does not write a file.

## Who it is for

Someone who needs the record of one activity the person described. The technical control stays with `plugin-security`. This plugin does not give legal advice and does not copy the security skill.

## What it includes

Portable, for any agent that follows [Agent Skills](https://agentskills.io/specification):

- `record-processing` records the activity, the roles, and the retention.

Cursor and Claude Code: the commands above. In Cursor, `/priv-processing`. In Claude Code, `/plugin-privacy:priv-processing`.

Cursor only: rules `output-folder`, `no-legal-basis`. Claude Code does not load rules. The same restrictions are in the skills.

## Install

In Cursor, install the plugin from this repository in Customize.

In Claude Code:

```text
claude plugin marketplace add ADRenaline-Suite/plugin-privacy
claude plugin install plugin-privacy@plugin-privacy
```

To try a local copy, start Claude Code with `claude --plugin-dir <path to this repository>`.

## Example

Ask `/priv-processing` and describe the activity. The file lists only the categories you named. The legal-basis heading stays a gap.

## Configuration

Files go in `adrenaline/privacy/`. One named activity goes in `<subject>/`.

## License

MIT. Copyright (c) 2026 Ricardo Plascencia.

