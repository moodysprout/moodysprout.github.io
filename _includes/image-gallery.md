{% for image in site.static_files %}
    {% if image.path contains {{page.project-folder}} %}
        {% if image.path contains 'thumb' %}
        {% else %}
![Image]({{ site.baseurl }}{{ image.path }})
        {% endif %}
    {% endif %}
{% endfor %}
