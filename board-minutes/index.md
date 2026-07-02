---
title: EEF Board Meeting Minutes
---

# EEF Board Meeting Minutes

Official minutes of the Erlang Ecosystem Foundation Board of Directors.

{% assign pdfs = site.static_files
   | where_exp: "item", "item.dir == '/board-minutes'"
   | where_exp: "item", "item.extname == '.pdf'"
   | sort: "name"
   | reverse %}
{% for pdf in pdfs %}
{% assign parts = pdf.basename | split: "__" %}
- [{{ parts[1] }} — {{ parts[0] | remove: "EEF_Meeting_Minutes_" | replace: "_", "-" }}]({{ pdf.path | replace: "#", "%23" }})
{% endfor %}
