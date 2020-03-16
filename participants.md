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

# Executive Director
**Kaitlin Thaney**

![Kaitlin Thaney](/assets/img/KaitlinThaney.jpg){:.image-right}Kaitlin Thaney’s career has been centered around open infrastructure organizations; helping them think strategically about program design, participatory engagement, and sustainability.

Previously she served as the Endowment Director for the [Wikimedia Foundation](https://wikimediafoundation.org/), where she led [development of a fund](https://wikimediaendowment.org/) to sustain the future of Wikipedia and free knowledge. Prior to joining Wikimedia, Thaney directed the program portfolio for the [Mozilla Foundation](https://foundation.mozilla.org/en/), following her time building the [Mozilla Science Lab](https://science.mozilla.org/), a program to serve the open research community. She was on the founding team for [Digital Science](https://www.digital-science.com/), where she helped launch and advise programs to serve researchers worldwide, building on her time at [Creative Commons](https://creativecommons.org/about/program-areas/open-science/), where she crafted legal, technical, and social infrastructure for sharing data on the web.

She also serves on the board of [LYRASIS](https://www.lyrasis.org/Pages/Main.aspx), a technology and services nonprofit serving higher education, libraries, archives and museums, and recently served as the Board Chair of [Code for Science & Society](https://codeforscience.org/), Invest in Open Infrastructure’s fiscal sponsor. She resides in Brooklyn, New York with her husband, toddler, and dog.

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
