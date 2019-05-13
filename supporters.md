---
layout: default
title: Supporters
---

# Statement in Support of Invest in Open Infrastructure
**_Uniting initiatives to expand the scope of current open source for open science._**

Scholarship is at its best when communities of researchers, scholars, and knowledge workers can share, discover, and collaborate. However, the needs of this community are not well-served by the existing scholarly communication infrastructure, which is dominated by commercial vendors whose missions and values often run counter to those of the scholarly community. When the business models of these vendors favor lock-in, consolidation and monopoly, they create a market where opportunity for healthy competition is limited.

While many promising open infrastructure projects have demonstrated their value, most operate independently, and struggle with securing ongoing operational funding. There is a pressing need for a coordinated, global effort to provide collective support for developing and sustaining open infrastructure that operates in a manner that is aligned with the values of the scholarly community it serves.

Our organizations support this global effort to sustain open scholarly infrastructure. We believe that a network of shared open systems and tools governed by and managed for the benefit of those who use them is an essential step towards creating a healthy scholarly ecosystem. By investing in, integrating, building on, and/or expanding current and emerging open infrastructure initiatives, we can ensure that the services and software that the scholarly community relies upon to share its work with all who need access is high-quality, reliable, persistently available, and operated in a manner consistent with our community’s values.

**[Sign now](https://forms.gle/C9HRedT3Fbsns82T8)** to add yourself and/or your organization as a supporter of Invest in Open Infrastructure.

## Supporting Organizations
<ol>
  {%- assign supportingorgs = site.data.supporters | where:"Status","My Institution" | sort_natural: 'NameGiven' -%}
  {%- for org in supportingorgs -%}
    <li><b>{{ org.NameGiven }} {{ org.NameFamily }}</b>, {{ org.Title }}, for <a href="{{ org.URL }}">{{ org.Organization }}</a></li>
  {%- endfor -%}
</ol>

## Supporting Individuals
<ol>
  {%- assign supportingpeople = site.data.supporters | where:"Status","Myself" | sort: 'NameGiven' -%}
  {%- for person in supportingpeople -%}
    <li><b>{{ person.NameGiven }} {{ person.NameFamily }}</b>, {{ person.Title }} at <a href="{{ person.URL }}">{{ person.Organization }}</a></li>
  {%- endfor -%}
</ol>
