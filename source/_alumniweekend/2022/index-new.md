---
layout: front-page-2022
description: "Celebrating Alumni Week in true 2022 style. Have fun, remember your roots, reignite your passions, and connect like never before as our first virtual Alumni Week zooms you back to campus."

category: aw-2022

billboard:
  date: "April 19-22, 2022"
  hero-title: "Alumni Week 2022"
  description: "Virtual & In Person"
  action-text: Register Now
  register-url: '#'

---

<section class="heading">
  <h2 class="underline">Featured Events</h2>
</section>
<div class="events-card-list fade-out-siblings">
  {% for featured in page.featured %}
    <a class="events-card" href="{{ featured.url }}">
      <div class="events-card-content">
        <div class="date">
          <div class="month">{{ featured.date | date: "%b" }}</div>
          <div class="day">{{ featured.date | date: "%d" }}</div>
        </div>
          <div class="inner">
            <div class="image">
            <img src="{{ featured.image }}" alt="{{ featured.title }}"/>
            </div>
            <div class="card-content">
              <h4 class="header underline">{{ featured.title }}</h4>
              <p class="event-description">{{ featured.description }}</p>
            <div class="tags">
              <span class="topics-title">
                <div class="time">
                <i class="fa fa-clock-o turquiose-text"></i>{{ featured.date | date: "%A, %B %e, %Y" }} {% if featured.starttime != null %} at {% endif %}{{ featured.starttime }}
                {% if featured.endtime != null %} to {{ featured.endtime }} {% endif %}
                </div>
                <div class="location">
                  <i class="fa fa-map-marker turquiose-text"></i> Virtual Event
                </div>
              </span>
            </div>
          </div>
        </div>
      </div>
    </a>
  {% endfor %}
</div>
<!-- End three current events: Tag Home to display -->
<div class="more no-border">
  <a href="https://calendar.ucsc.edu/alumni_week" class="button primary">
    View more events
  </a>
</div>
