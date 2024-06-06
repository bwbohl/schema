---
#layout: default
title: "Schemas and Namespace"
---

# {{ page.title }}

## MEI Namespace

The MEI Namespace is `http://www.music-encoding.org/ns/mei`

# MEI v5.0

## Schemas (2023)

A PDF version of the MEI 5.0 Guidelines is available here: [https://music-encoding.org/guidelines/v5/MEI_Guidelines_v5.0.pdf](https://music-encoding.org/guidelines/v5/MEI_Guidelines_v5.0.pdf)

New customization: MEI Basic. It provides a simplified subset of the MEI framework that reflects the capabilities of most popular "Common Western Music Notation" score-writing applications currently in use. For more details on MEI Basic [see the corresponding section in the guidelines](https://music-encoding.org/guidelines/v5/content/introduction.html#meiBasic).

- MEI Basic: [https://music-encoding.org/schema/5.0/mei-basic.rng](https://music-encoding.org/schema/5.0/mei-basic.rng)

The MEI Schemas (specific for CMN, mensural, or neumes notation) are available at the following URLs:

- MEI CMN: [https://music-encoding.org/schema/5.0/mei-CMN.rng](https://music-encoding.org/schema/5.0/mei-CMN.rng)
- MEI Mensural: [https://music-encoding.org/schema/5.0/mei-Mensural.rng](https://music-encoding.org/schema/5.0/mei-Mensural.rng)
- MEI Neumes: [https://music-encoding.org/schema/5.0/mei-Neumes.rng](https://music-encoding.org/schema/5.0/mei-Neumes.rng)

It is strongly recommended to use one of the above schemas, unless you are forced to do otherwise for good reasons. When relying on more than one of the above schemas, or checking the general validity of an MEI file, it can be reasonable to use the `MEI ALL` schema:

- MEI All: [https://music-encoding.org/schema/5.0/mei-all.rng](https://music-encoding.org/schema/5.0/mei-all.rng)

In the context of tutorial exercises (or comparable purposes), the `MEI ALL (Any Start Element)` schema could be used to provide greater flexibility in terms of removing some technical and framework constraints:

- MEI All (Any Start Element): [https://music-encoding.org/schema/5.0/mei-all_anyStart.rng](https://music-encoding.org/schema/5.0/mei-all_anyStart.rng)

Further detailed customization of a schema, allowing to restrict specific elements or attributes, can be done with the MEI Garage profiler: [https://meigarage.edirom.de/profiler](https://meigarage.edirom.de/profiler).

A detailed overview of the changes for the MEI 5.0 schema is available here: [https://music-encoding.org/archive/comparison-5.0.html](../archive/comparison-5.0.html)

## Additional files

MEI also provides additional files in the schema releases, e.g., for customization. Here is a full list of the files included in MEI v5.0:

{% assign v5 = site.collections | where: "label", "5.0" | first %}

{% for file in v5.files %}
* [{{ file.name }}]({{ file.collection }}/{{ file.name }})
{% endfor %}

# Other versions

{% for collection in site.collections %}
{% if collection.label != "5.0" and collection.label != "posts" %}
## {{ collection.label }}

{% for file in collection.files %}
* [{{ file.name }}]({{ file.collection }}/{{ file.name }})
{% endfor %}
{% endif %}
{% endfor %}
