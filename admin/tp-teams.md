{% from "common/macros.njk" import embed_topic with context %}
{% from "common/admin.njk" import show_admin_page with context %}

{% call show_admin_page("tp-teams") %}
<div id="main">

<pic eager src="{{baseUrl}}/admin/images/team.png" width="300px"></pic><br>
<small>%%[Picture: The team that was at the top of early Google]%%</small>
<p/>

#### When to form teams
{% set session = "tutorial" %}
{% if cs2103 %}* {{ course }}T: Your team will be formed by the CS2101 side.{% endif %}
* {{ course  }}: Team forming will be done at the _start_ of the week 3 {{ session }}. If you are not there at the team forming time and others in the class are unaware which team you wanted to be in, we'll have to put you into a team randomly.

#### Team size

* The default ==team size is five==.

#### Team composition

* **We allow some freedom in choosing team members**, subject to these constraints:
  * **All team members should be in the same tutorial.** ==Delay forming teams until your place in a tutorial is confirmed.== We do not allow changing tutorials to team up with your preferred teammates.
  * **Teams of a single nationality are not allowed**  unless the only language common among all team members is English. e.g., an all-Singaporean team that include both Chinese and Malay students. %%Rationale: to train you to work in multicultural teams, to ensure that English is used for all project communication%%
  * **No more than one exchange students per team** %%Rationale: to increase interaction between exchange students and NUS students.%%
  * **Same gender teams are discouraged but allowed.** %%Rationale: to train you for mixed-gender work environments.%%
* **If you prefer not to form teams yourselves**, not to worry; we'll put you in a team.
* **We may have to modify teams** when circumstances call for it. There is no avenue for you to object. Staying with your preferred team is not guaranteed.

</div>
<div id="teamIdFormat">

#### Team ID

* **To be given to you after forming teams.**
* **Has the form `TUTORIAL_ID-TEAM_NUMBER`** e.g, `{{ course }}-W14-2` means you are in tutorial `{{ course }}-W14` (i.e., in course `{{ course }}`, on `Wednesday`, at `1400-1500`), team `2`.

<div class="indented-level1">

{{ embed_topic("tutorials.md#tutorialTimetable", "Admin " + icon_embedding + " Tutorials → Tutorial IDs", "3") }}
</div>
<p>

</div>
<div id="teamCommunication" tags="m--cs2103 m--cs2113">

#### Team Communications

* **Use English** for all team communications, both spoken and written.
* **We recommend at least one 1-2 hour ==synchronous (online or f2f)== project meeting per week**, in addition to any asynchronous communicating. %%Reason: Having all members available at the same time will facilitate easier collaboration and more peer-learning%%.
  <!--* **We recommend at least one 1-2 hour ==face-to-face== project meeting per week**, in addition to any online meetings. %%Reason: you need to know how to run both types of project meetings%%. The project meeting time can be used to discuss project related things, but also, can be used as a time for team members to work on the project tasks individually (having all members in the same place will facilitate easier collaboration and more peer-learning).-->

  * **Fix a weekly 1-2 hour time slot for project meetings** after the team has been finalized (latest by the end of week 3 {{ session }}). ==All members are expected to attend weekly project meetings== (not doing so could lower the peer evaluation ratings you receive, which in turn will be factored into your grade). You should also fix a venue for the meetings, if you prefer F2F meetings.
  * {{ icon_tip }} **The best time for the weekly project meeting** is the period {{ date_first_lecture | date(format_full_day, 1) }}, {{ date_first_lecture | date(format_full_day, 2) }}, {{ date_first_lecture | date(format_full_day, 3) }}, {{ date_first_lecture | date(format_full_day, 4) }} i.e., soon after the
{{ lecture_name }} but well ahead of the deadline for weekly tasks. %%Reason: _After_ the {{ lecture_name_short }} → so that you've been briefed about upcoming project tasks; _well ahead of_ the deadline → so that you can use the meeting to plan/do weekly project tasks.%%<br>
    But it's OK to choose a timeslot outside of that recommended period too, if a suitable time cannot be found within that period.

</div>

{% endcall %}
