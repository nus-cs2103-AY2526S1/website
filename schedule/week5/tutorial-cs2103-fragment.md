{% from "common/macros.njk" import embed_topic, show_as_rounded_tab, show_faq, show_as_tab, thumb, timing_badge with context %}
{% from "_course-" + course + "/studentData-fragment.md" import ip_pr_slap_review_allocation as allocations with context %}

<box type="info">

The tutorial is held F2F from this week onwards. See [the tutorials page]({{ baseUrl }}/admin/tutorials.html) for more info.
</box>

#### {{ thumb(1) }} Discuss code quality problems of iP PRs

<!--div class="indented">

{{ icon_team }} This activity is to be done as a team. One team member needs to be connected to the TV.
</div -->

1. {{ timing_badge("prior to the tutorial, or in the first 10 minutes", "warning") }} ****Find code quality problems in iP PRs:****

   **1a) Find the PR you have been allocated to discuss** (expand the panel below). If the allocated PR is not available or suitable, you can choose the fallback option, and failing that, any random PR.

   <panel header="**PR allocation**" peek>

   {% macro get_links(username) -%}
   [{{ username }}'s PR](https://github.com/{{ course_org }}/{{ ip_repo_name }}/pulls/{{ username }})
   {%- endmacro  %}

   <d-table sortable searchable>
   Your username | PR to review       | Fallback PR to review
   --------------|--------------------|------------------
   {% if not allocations | length %}Allocation ... | ... not ... | .... available yet. {% else %}{% for allocation in allocations -%}
   {{ allocation[0] }} | {{ get_links(allocation[1]) }} | {{ get_links(allocation[2]) }}
   {% endfor %}{% endif %}
   </d-table>
   </panel>
   <p/>

   **1b) Find instances of the three code quality problems listed below**: Go through the code in the diff view (i.e., the {{ show_as_rounded_tab(':octicon-diff: files changed') }} tab) of those PRs, **and take screenshots** of instances of the following three code quality problems #r#(ignore other types of code quality problems)##:<br>
   **a) Weak <trigger trigger="click" for="modal:t4-slapDescription">SLAP</trigger>**<br>
   **b) Nesting problems**: _arrow-head style code_ or _too-deep nesting_ %%(<trigger trigger="click" for="modal:t4-arrowVsDeepNesting">what's the difference?</trigger>)%%<br>
   **c) Too-long methods**<br>
   * If you can't find at least one example, you can try the fallback option provided, and failing that, another random iP PR.
   * You may select _borderline_ and _possibly_ problematic cases too.

   <box>

   {{ icon_tip }} To identify nesting problems or long methods, zoom out and scroll through the entire PR code to do a visual inspection (no need to read the code line-by-line). After visually locating a method that looks too long/deep, have a closer look to see it can be improved by using better abstraction.

   {{ icon_tip }} If existing PR comments are getting in your way, you can hide them using the following option:
   <pic src="..\..\book\gitAndGithub\reviewPRs\images\hideExistingComments.png" />
   <include src="..\..\book\gitAndGithub\reviewPRs\text.md#tip-pr-split-view" inline />
   </box>

{{ show_faq("howToDecideTooLongOrTooDeepMethods") }}

2. {{ timing_badge("first 10 minutes", "warning") }} **Paste screenshots you took in the `T5-Workspace.pptx` file** the tutor will share with you via MSTeams.


1. {{ timing_badge("next 10 minutes", "warning") }} **Discussion**: The tutor will lead a short discussion to go through the problematic code you found.

1. {{ timing_badge("after the tutorial", "warning") }} **Apply the insights gained from this activity to improve the code quality of your own iP**, if necessary.
   <box type="info" seamless>
   You are not required to (but welcome to) post review comments in the PRs you examined.
   </box>

{{ show_faq("warmUpTaskRushed") }}
<modal large header="" id="modal:t4-slapDescription">
  <include src="../../book/codeQuality/maximizeReadability/intermediate/slapHard/unit-inParent-asPanel.md" boilerplate />
</modal>

<modal large header="" id="modal:t4-arrowVsDeepNesting">

These two often happens together, but it is possible we see an arrowhead shape that is not that deep or deep nesting that is not exactly a clean arrowhead shape e.g.,<br>
<pic src="../../images/arrowVsDeepNesting.png" />
</modal>

#### {{ thumb(2) }} User stories exercise

* **Consider the following user stories** a team came up with, for a tP that aims to build a software for tracking travel plans.

<div class="indented-level2">

1 | As a … | I can … | So that I can … | notes |
-|-------|---------|-----------------|-------|
2 | first-time user | see some sample trips when I open the app | easily try out its features without needing to add my data first |
3 | first-time user | see a help message explaining which features I should try first | start by trying features that are more suited for new users | e.g., "hey you seem to be new. Try adding a trip first"
4 | new user ready to adopt the app for my own use | purge all data | get rid of sample/dummy data and start adding my real data |
5 | busy user | track all trip-related data inside the app | save time looking for data |
6 | user | sending trip info to friends | via email or telegram |
7 | user | add a trip |  |
8 | user | delete a trip | get rid of trip no longer needed to track |
9 | user | edit trip details | correct mistakes I made when adding a trip |
10 | user | view all trip details | recall details of trips |
11 | user | see the next upcoming trip details when I open the app | save the step of searching for the trip | reason: the next upcoming trips is the most likely trip the user may want to see
</div>

* **Think of the answers to the following questions**. These will be discussed during the tutorial.
  1. Which user stories don’t follow the correct format?
  1. Any of them too big for the tP planning? %%i.e., cannot be implemented by one person within 1-2 days%%
  1. Which are must-have features %%i.e., impossible to use the app without it%%




#### {{ thumb(3) }} Prioritize tP user stories

1. If you haven't done so already, brainstorm for user stories.

{{ embed_topic("../../admin/tp-tasks-fragment.md#desc_brainstorm_user_stories", "Admin " + icon_embedding + " tP → Week 5 → **Brainstorm user stories**", "2", indent="1") }}

2. If you want to refine your user stories (based on what you learned from the tutorial activity above) that you brainstormed earlier, do that first.

1. If you haven't done so already, prioritize tP user stories as explained in the panel below.

{{ embed_topic("../../admin/tp-tasks-fragment.md#desc_prioritize_user_stories", "Admin " + icon_embedding + " tP → Week 5 → **Choose user stories for the MVP version**", "2", indent="1") }}


#### {{ thumb(4) }} <span class="badge bg-secondary">time permitting</span> Create a _feature list_ for the MVP version

* If there is time left, do the following tP task that is scheduled for the following week.

<div class="indented-level1">

<panel header="%%Admin {{ icon_embedding }} **tP → week 6 → Conceptualize the MVP version**%%" expanded >

<include src="../../admin/tp-tasks-fragment.md#desc_conceptualize_first_version" />
</panel>
</div>
