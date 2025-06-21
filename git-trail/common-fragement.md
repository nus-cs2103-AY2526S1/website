{% from "common/topics.njk" import  panopto, slugify with context %}
{% from "common/macros.njk" import embed_topic with context %}

{% set trail = {
  tour_recording_snapshots: {
    title: "Tour 1: Recording the History of a Folder",
    lesson_git_prep: {path: "gitAndGithub/gitPrep", title: "Lesson: Preparing to Use Git"},
    lesson_init: {path: "gitAndGithub/init", title: "Lesson: Putting a Folder Under Git's Control"},
    lesson_stage: {path: "gitAndGithub/stage", title: "Lesson: Specifying What to Include in a Snapshot"},
    lesson_commit: {path: "gitAndGithub/commit", title: "Lesson: Saving a Snapshot"}
  }
} %}


{% macro show_lesson_overview(lesson_data) %}
<div class="indented-level1">

<div class="border border-success pt-2 ps-2 pb-1 pe-1 border-bottom-0 rounded-top" style="background-color: #e6fff2">
<include src="../book/{{ lesson_data.path }}/text.md#overview" inline />
</div>


&nbsp;&nbsp;→ **[{{ lesson_data.title }}](#{{ slugify(lesson_data.title) }})** covers that part.
</div>
{% endmacro %}


{% macro show_lesson(lesson_data) %}
<panel type="seamless" expanded>
<div slot="header" class="card-title">

## <span class="text-success">{{ lesson_data.title }}</span>
</div>

<div class="indented-level1">

<small>[<span class="font-weight-bold text-muted">Textbook location: <include src="../book/{{ lesson_data.path }}/../path.md" inline trim /> **<include src="../book/{{ lesson_data.path }}/text.md#title" inline />**]</span></small>
</div>
{{ panopto(video) if video else '' }}
<include src="../book/{{ lesson_data.path }}/unit-inElsewhere-asPanelBody.md" boilerplate />
</panel>
{% endmacro %}


<!-- To be deprecated, in favor of show_lesson() -->
{% macro show_trail_unit(path, title, video='') %}
<panel type="seamless" expanded>
<div slot="header" class="card-title">

## <span class="text-success">{{ title }}</span>
</div>

<div class="indented-level1">

<small>[<span class="font-weight-bold text-muted">Textbook location: <include src="../book/{{ path }}/../path.md" inline trim /> **<include src="../book/{{ path }}/text.md#title" inline />**]</span></small>
</div>
{{ panopto(video) if video else '' }}
<include src="../book/{{ path }}/unit-inElsewhere-asPanelBody.md" boilerplate />
</panel>
{% endmacro %}


{% macro divider(text) %}# <div class="text-white bg-success p-1"><span class="text-light">:fas-map-marker-alt:</span> {{ text }}</div>{% endmacro %}
