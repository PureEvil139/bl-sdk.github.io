---
layout: mod

authors: "juso" # Authors of the mod
title: RogueLands # Title of the mod
version: "1.3" # Version of the mod
supported: "BL2" # Supported games; currently can only display as "BL2", "BL2 + TPS", or "TPS"

tagline: "Turns BL2 into Rogue-Lite game." # A short description of the mod itself.
description: "Turns BL2 into Rogue-Lite game." # This is set in order to keep the SEO proper
longDescription: "RogueLands is a mod that turns Borderlands into a Rogue-Lite game. \nThis mod works similar to the 1life challenge, but with the twist, that when you die, you respawn at the start of the game with all your Exp. \nYou will lose all your items, but you will keep your stats and skills. \nAll progress with this mod will count towards the UVHM. You do not need to have it unlocked to play. \nOverpower Levels will also be ignored, it is recommended to create a new character for this mod!\nTo complete the mod you must complete a set of challenges. (Check modded keybinds)\n" # Description of what the mod can do
categories: ['Gameplay'] # Category of the type of mod

requirements: ['UserFeedback >= 1.5'] # Requirements for the given mod
requirementTitles: ['UserFeedback'] # The link-friendly name of the requirements

issues: "https://github.com/juso40/bl2sdk_Mods/issues"
download: "https://github.com/juso40/bl2sdk_Mods/raw/master/RogueLands/RogueLands.zip"
source: "https://github.com/juso40/bl2sdk_Mods/" # Link to source code
license: ['MIT', 'https://choosealicense.com/licenses/mit'] # License name, link about the license from https://choosealicense.com/

---
**Contents**
* TOC
{:toc}

## {{page.title}}

Mod by: {{page.authors}}
Current Version: {{page.version}}

<p></p>
### Description

{{page.longDescription | markdownify }}

Currently Supports: `{{page.supported}}`

{% if page.categories.size > 0 %}
Categories:
{% for category in page.categories %}
  * [{{category}}](/types/{{category}})
{% endfor %}
<p></p>
{% endif %}

{% if page.requirements.size > 0 %}
### Requirements

{% for requirement in page.requirements %}

{% assign reqName = page.requirementTitles[forloop.index0] %}

{% for mod in site.mods %}

{% assign modName = mod.path | remove_first: '_mods/' %}
{% assign xz = reqName | append: '.md' %}

{% if modName == xz %}
* [{{ requirement }}]( {{ reqName | relative_url | prepend: '/mods'}} ) <sup>[(Direct Download)]({{mod.download}})</sup>
{% endif %}
{% endfor %}

{% endfor %}
<p></p>
{% endif %}

### Links

{% if page.download != "" %}
You can download {{page.title}} here: [Download Link]({{page.download}})
{% endif %}

{% if page.issues != "" %}
Report issues here: [Issue Tracker]({{page.issues}})
{% endif %}

{% if page.source != "" %}
View the source code here: [Source Code]({{page.source}})
{% endif %}

{% if page.license.size > 0 %}
This mod is licensed using {{page.license[0]}} <sup>[?]({{page.license[1]}})</sup>
{% endif %}