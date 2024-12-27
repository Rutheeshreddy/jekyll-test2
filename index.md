---
#
# By default, content added below the "---" mark will appear in the home page
# between the top bar and the list of recent posts.
# To change the home page layout, edit the _layouts/home.html file.
# See: https://jekyllrb.com/docs/themes/#overriding-theme-defaults
#
layout: base
---

# Upcoming Events

<div class="events-container">
  {% for event in site.data.events %}
    <div class="event-card">
      <!-- Event Content -->
      <div class="event-content">
        <h2 class="event-title">{{ event.title }}</h2>
        <p class="event-description">{{ event.description }}</p>
      </div>

      <!-- Event Details -->
      <div class="event-details">
        <div class="event-detail">
          <span class="event-label">Time:</span>
          <span class="event-value">{{ event.time }}</span>
        </div>
        <div class="event-detail">
          <span class="event-label">Venue:</span>
          <span class="event-value">{{ event.venue }}</span>
        </div>
        <div class="event-detail">
          <span class="event-label">Date:</span>
          <span class="event-value">{{ event.date }}</span>
        </div>
      </div>

      <!-- Event Link (Optional) -->
      {% if event.event_link %}
        <div class="event-link">
          <a href="{{ event.event_link }}">Learn More</a>
        </div>
      {% endif %}
    </div>
  {% endfor %}
</div>

<br>
Join our <a href="" style="color:green"><i class="fa fa-whatsapp"></i> whatsapp group</a> to know last minute changes and other updates!
