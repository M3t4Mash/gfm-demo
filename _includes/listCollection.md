{{ include.currCollection }}
{% assign collectionLowerCaseLabel = {{ currCollection }} | split: "_" %}
{% assign collectionLabel = {{ collectionLowerCaseLabel }} | capitalize %}