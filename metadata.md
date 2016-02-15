---
search: exclude
---
{
    "@context":
    {
        "@vocab":"http://www.essepuntato.it/lode/http://purl.org/spar/doco",
        "fabio":"http://www.essepuntato.it/lode/http://purl.org/spar/fabio",
        "creator":"http://purl.org/dc/elements/1.1/creator",
        "instructional_work": "fabio:instructional_work",
        "title":"http://purl.org/dc/elements/1.1/title"
        "url":"fabio:hasURL"
        "summary":"http://purl.org/spar/doco/Abstract"
    },
    "@graph": [
        /elationfoundation/using-tor-browser-bundle/9b21f60dbd8d3e57053e7b519371d9d91534ae4a/_en/addtional_resources.md
        {% for page in site.en %}
        {% capture raw_base %}https://raw.githubusercontent.com/{{site.github.owner_name}}/{{site.github.repository_name}}{% endcapture %}
           {% capture item_url %}{{raw_base}}/{{site.github.build_revision}}/{{page.path}}{% endcapture %}
        {% if page.adids_category != null %}
        {
             '@id' : {{ page.id | jsonify }}
             '@type' : {{ page.type | jsonify }},
             'creator'  : {{ page.creator | jsonify }},
             'platforms'  : {{ page.platforms | jsonify }},
             'contains'     : {{ page.contains | jsonify }},
             'adids_category'  : {{ page.adids_category | jsonify }},
             'duration'  : {{ page.duration | jsonify }},
             'summary'  : {{ page.summary | jsonify }},
             'last_updated'  : {{ page.last_updated | jsonify }},
             'url' : {{ item_url | jsonify}}
             }{% unless forloop.last %},{% endunless %}
         {% else %}
             {
             'creator'  : {{ page.creator | jsonify }},
             '@id'  : {{ page.id | jsonify }},
             'title'  : {{ page.title | jsonify }},
             'last_updated'  : {{ page.last_updated | jsonify }},
             'url' : {{ item_url | jsonify}}
             }{% unless forloop.last %},{% endunless %}
        {% endif %}
        {% endfor %}
    ]
}
