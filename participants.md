---
layout: default
title: Participants
permalink: /participants/
redirect_from: "/participants.html"
---

# Participating Organizations
<organizations>
{%- assign organizations = site.data.participants.orgs | where:"type","org" | sort_natural: 'org' -%}
{%- for organization in organizations -%}
  <organization>
    <logo>
      {%- if organization.logo -%}
        {%- if organization.url -%}<a href="{{ organization.url }}">{%- endif -%}
        {{ organization.logo | prepend: '<img src="/assets/img/' | append: '" alt="' | append: organization.nick | append: ' logo" />' }}
        {%- if organization.url -%}</a>{%- endif -%}
      {%- endif -%}
    </logo>
    <name>
      {%- if organization.url -%}<a href="{{ organization.url }}">{%- endif -%}
      {{ organization.org }}
      {%- if organization.nick != organization.org -%}{{ organization.nick | prepend: ' (' | append: ')' }}{%- endif -%}
      {%- if organization.url -%}</a>{%- endif -%}
    </name>
  </organization>
{%- endfor -%}
</organizations>

# Steering Committee
<people>
<ol>
  {%- assign individuals = site.data.participants.orgs | where:"type","person" | sort: 'namefamily' -%}
  {%- for individual in individuals -%}
    <li>
      {%- if individual.url -%}<a href="{{ individual.url }}">{%- endif -%}
      {%- if individual.namegiven -%}{{ individual.namegiven | append: ' ' }}{%- endif -%}
      {{ individual.namefamily }}
      {%- if individual.url -%}</a>{%- endif -%}
      {%- if individual.org -%}{{ individual.org | prepend: ', ' }}{%- endif -%}
    </li>
  {%- endfor -%}
</ol>
</people>
