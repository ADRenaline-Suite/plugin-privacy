---
name: priv-help
description: "ADRenaline. Help: catalog of plugin-privacy (skills, rules, commands)."
---

# Help — ADRenaline Privacy

Print this catalog as the reply. Do not run any skill or command. Do not invent entries that are not listed. If a component was added to the plugin and is missing here, add one line from its frontmatter `description` and say the catalog was refreshed.

When this help command is the first command in the message, every command, skill, or rule named after it is the subject of the help. Do not run those names. Do not print the full catalog. For each name, in the order given, print its catalog line (the linked id and the sentence). When the README has a heading for that command, also print the paragraphs under that heading, up to the next heading. A skill name uses the skill's catalog line and the README group that names that skill, up to its first command heading. A name that is not in this catalog is one line: it is not in this plugin. Do not invent what it does, and do not write a file.

Write the sentences in the language of the request. Keep command names, file ids, and every URL unchanged. Every id is a markdown link to the GitHub URL on its line. Do not print a repository `name` as the visible label of a plugin.

Keep the section headings, in this order: Plugin, Commands, Skills, Rules, then Agents, Hooks, and MCP when the plugin has them, then Output, then Not in this plugin. The title and the Plugin line show `ADRenaline` plus the `displayName`, then one sentence on what the plugin does. Under Commands, group the lines by the skill named in the line. Each group opens with that skill name linked to its SKILL.md. One line per item: the linked id, then the sentence. Output links this plugin's GitHub repository under that same label. A plugin under Not in this plugin uses `ADRenaline` plus its short name, and links to `https://github.com/<owner>/<other-plugin>` only when that repository exists.

## Plugin

- [**ADRenaline Privacy**](https://github.com/ADRenaline-Suite/plugin-privacy/blob/main/README.md) — Writes one processing activity the person described, with the role and the retention they gave.

## Commands

- [**/priv-help**](https://github.com/ADRenaline-Suite/plugin-privacy/blob/main/README.md) — This help (one-line catalog of the plugin).
- [**record-processing**](https://github.com/ADRenaline-Suite/plugin-privacy/blob/main/skills/record-processing/SKILL.md) — Records one processing activity: what, why, who, and for how long.
- [**/priv-processing**](https://github.com/ADRenaline-Suite/plugin-privacy/blob/main/skills/record-processing/references/processing.md) — Processing activity: the categories and the purpose the person stated.
- [**/priv-roles**](https://github.com/ADRenaline-Suite/plugin-privacy/blob/main/skills/record-processing/references/roles.md) — Roles: who decides the purpose (controller) and who processes on their behalf.
- [**/priv-retention**](https://github.com/ADRenaline-Suite/plugin-privacy/blob/main/skills/record-processing/references/retention.md) — Retention: how long this category is kept, and what happens after.

## Skills

- [**record-processing**](https://github.com/ADRenaline-Suite/plugin-privacy/blob/main/skills/record-processing/SKILL.md) — Records one processing activity: what, why, who, and for how long.

## Rules

- [**output-folder**](https://github.com/ADRenaline-Suite/plugin-privacy/blob/main/rules/output-folder.mdc) — Every file goes in `adrenaline/privacy/` (or in `outputDirs["plugin-privacy"]` of `.cursor/adrenaline.json`). The artifact follows the language of the request.
- [**no-legal-basis**](https://github.com/ADRenaline-Suite/plugin-privacy/blob/main/rules/no-legal-basis.mdc) — The record describes the processing. It does not pick a legal basis. The technical control stays in security.

## Output

- Repository: [**ADRenaline Privacy**](https://github.com/ADRenaline-Suite/plugin-privacy).
- Folder: `adrenaline/privacy/`. One named subject goes in `<subject>/`. `<NNN>` is monotonic across the whole folder.

## Not in this plugin

- Security control → ADRenaline plugin-security.
