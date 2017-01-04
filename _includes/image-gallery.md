{% for image in site.static_files %}
    {% if image.path contains {{page.project-folder}} %}
        {% if image.path contains 'thumb' %}
        {% else %}
<img src="{{ site.baseurl }}{{ image.path }}" alt="{{page.image-default-alt}}" title="{{page.image-default-title}}"/>
        {% endif %}
    {% endif %}
{% endfor %}
