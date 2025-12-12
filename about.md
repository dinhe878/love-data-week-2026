---
title: About the Love Data Week
menu_title: About
menu_icon: globe2
---

Love Data Week is an international celebration of data, taking place every year during the week of Valentine’s day. Universities, nonprofit organizations, government agencies, corporations and individuals are encouraged to host and participate in data-related events and activities.

For more information about other international activities please visit [ICPSR event website](https://www.icpsr.umich.edu/sites/icpsr/about/news-events/international-love-data-week).

## The organising team

{:.lead}
To contact us about the Nordic Love Data Week, please reach out to our team

<table class="team-list">
    {% for member in site.team %}
    <tr>
        <td>
            <img alt="{{ member.name }}" src="{{ member.image }}">
        </td>
        <td>
            <strong>{{ member.name }}</strong>
            {% if member.links %}
            <span class="profile-links">
                {% for link in member.links %}
                <a title="{{ link.title }}" href="{{ link.url }}"><i class="bi {{ link.icon }}"></i></a>
                {% endfor %}
            </span>
            {% endif %}
            <br>{{ member.affiliation }}
            {% if member.title %}<br>{{ member.title }}{% endif %}
            <br><a href="mailto:{{ member.email }}">{{ member.email }}</a>
        </td>
    </tr>
    {% endfor %}
</table>
