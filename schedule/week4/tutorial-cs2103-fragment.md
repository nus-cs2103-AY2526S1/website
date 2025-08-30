{% from "common/macros.njk" import show_faq, thumb with context %}

{% if semester != "AY2425S2" %}
#### {{ thumb(1) }} **Discuss iP progress**

* If you managed to add a GUI to your app, demo it to others.

#### {{ thumb(2) }} **Interpret class/object diagrams**
{% else %}
#### {{ thumb(1) }} **Interpret class/object diagrams**
{% endif %}

* Do the two exercise given below, as directed by the tutor.

<box type="tip" seamless>

**Use the ==[UML Reference Sheet]({{ baseUrl }}/admin/uml-reference-sheet.md)==** to quickly look up UML notation.
</box>

<div class="indented-level2">

<include src="../../book/combined/exercises/interpretClassAndObjectDiagramAllNotations.md" />
<include src="../../book/modeling/modelingStructures/classDiagramsIntermediate/q-explainClassDiagramNotation.md" />
<p/>
</div>

{{ show_faq("umlIsItUsedInIndustry") }}
{{ show_faq("umlAreWeOverdoing") }}
<!--
#### {{ thumb(4) }} **Share Git tips** {{ icon_extra }}

* Find out how to do these git tasks and share with others
  * modify the most recent commit
  * undo the most recent commit
  * delete the most recent commit
  * stash changes
  * squash commits
  * cherrypick commits
-->
