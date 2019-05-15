---
layout: default
title: Events
---

# Events
Events of interest to the IOI community, listed in reverse chronological order.

<events>
{%- assign events = site.data.events.events | where:"type","event" | sort_desc: "start" -%}
{%- for event in events -%}
  {%- assign startdate = event.start |  date: "%e %B %Y" -%}
  {%- assign enddate = event.end |  date: "%e %B %Y" -%}
  <h2>{{ event.title }}</h2>
  <p><b>{{ event.start | date: "%A %e %B %Y %R" }}&ndash;{%- if enddate != startdate -%}{{ event.end | date: "%A %e %B %Y" | append: " " }}{%- endif -%}{{ event.end | date: "%R" }} {{ event.timezone }}</b></p>
  <p><b>{{ event.location | markdownify }}</b></p>
  <p>{{ event.description | markdownify }}</p>
{%- endfor -%}
</events>
