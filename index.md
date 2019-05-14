---
layout: default
title: "Home"
---
<components>
  <component>
    <h2>Our Statement</h2>
    <p>We imagine a world in which communities of researchers, scholars, and knowledge workers across the globe are fully enabled to share, discover, and work together. It is clear that the needs of today’s diverse scholarly communities are not being met by the existing largely uncoordinated scholarly infrastructure, which is dominated by vendor products that take ownership of the scholarly process and data. We intend to create a new open infrastructure system that will enable us to work in a more integrated, collaborative and strategic way. It will support global connections and consistency where it is appropriate, and local and contextual requirements where that is needed. <b><a href="/docs/statement0.2">Read more ></a></b></p>
  </component>

  <component>
    <h2>Sign Our Statement</h2>
    <p>See <a href="/supporters">who's supporting IOI</a> and add yourself and/or your organization as a supporter.</p>
    <p><b><a href="/supporters">Sign the statement ></a></b></p>
  </component>

  <component>
    <h2>Join the Census</h2>
    <p>The Census of Scholarly Communication Infrastructure is now open. We invite projects and programs, for profit and nonprofit corporations, and hosted initiatives of all kinds to contribute to this growing body of information.</p>
    <p><b><a href="/census">Complete the census ></a></b></p>
  </component>

  <component>
    {% for item in site.posts limit:1 %}
      <h2>{{ item.title }}</h2>
      {{ item.excerpt }} <b><a href="{{ item.url }}">Read more ></a></b>
    {% endfor %}
  </component>

  <component>
    <h2>Recent & Upcoming Events</h2>
    <h3>IOI Launch Webinar</h3>
    <p><b>Tuesday 28 May 2019 8:00–9:00 EDT (UTC -4)</b></p>
    <p><a href="https://forms.gle/DhzjNowfyyJLHn7dA">Register</a> for the 28 May workshop (<a href="https://www.timeanddate.com/worldclock/fixedtime.html?msg=IOI+Webinar&iso=20190528T08&p1=179&ah=1">check the time in your timezone</a>) to hear about the Invest in Open Infrastructure project from members of the community and learn how you can get involved. The webinar will be recorded and shared, but you can also sign up to let us know if another time that would work better for you.</p>
    <p><b><a href="/events">See all events ></a></b></p>
  </component>
</components>
