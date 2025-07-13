{% from "common/macros.njk" import embed_topic, show_as_tab, thumb, timing_badge with context %}
{% from "common/admin.njk" import show_admin_summary with context %}


{% call show_admin_summary() %}
1. Submit the quiz

{{ icon_project }} **Project:**
1. Implement increments `Level-8`,  `A-JavaDoc`, `A-Gradle`, `A-JUnit`
2. Merge branches
{% endcall %}

<!-- ==================================================================================================== -->
{{ heading_project }}
<div id="project">

#### {{ thumb(1) }} Implement increments `Level-8`,  `A-JavaDoc`, `A-Gradle`, `A-JUnit`

<div class="indented">
<include src="dukeFragment.md" boilerplate var-displacement="../.." var-header="**`Level-8`: Dates and Times**" var-fragment="text.md#Level-8" />
<include src="dukeFragment.md" boilerplate var-displacement="../.." var-header="**`A-JavaDoc`: JavaDoc**" var-fragment="extensions-fragment.md#A-JavaDoc" />

<include src="../../admin/ip-tasks-fragment.md#pulling-branch-from-upstream" />

<include src="dukeFragment.md" boilerplate var-displacement="../.." var-header="**`A-Gradle`: Gradle**" var-fragment="extensions-fragment.md#A-Gradle" />

<box type="tip" seamless>

The `A-JUnit` project increment given below can be done using Gradle or without using Gradle. It's easier if you choose to do it using Gradle.
</box>

<include src="dukeFragment.md" boilerplate var-displacement="../.." var-header="**`A-JUnit`: JUnit Testing**" var-fragment="extensions-fragment.md#A-JUnit" />

</div>
<p/>

#### {{ thumb(2) }} Merge branches

<div class="indented">

This task is ==optional but strongly recommended==.

To get a very basic sense of how to use Git in a team project, this exercise simulates a situation where some others are also writing code for your project. Here are the steps.

1. Imagine you are using the GitHub repo {{ url_course_org }}/{{ ip_repo_name }} to collaborate among the team members of your Duke project.

<div class="indented">

<box type="info" seamless>

Although that repo was set up by the teaching team, you could have created one yourself -- all it requires you to do is to create a GitHub organization, create a repository inside it, push your code to it, and add other team members to that GitHub organization.

Alternatively, you could have added the team members as 'collaborators' to your own fork so that they can push code to your fork directly.

</box>
</div>

2. Now, imagine one of the team members have pushed her new code as a branch named `tweak-readme` to the remote repo (we have added such a branch to that repo already). Fetch that branch and merge it to your `master` branch.
   * Here are the steps for doing that, using the Git command line.
     1. Add the upstream repo as a remote, and give it the name `upstream`:<br>
     `git remote add upstream {{ url_course_org }}/{{ ip_repo_name }}.git`
     1. Switch to the `master` branch, if you are not on it already:<br>
     `git checkout master`
     1. Fetch the `tweak-readme` from the remote `upstream`:<br>
     `git fetch upstream tweak-readme`
     1. Merge the branch (the `--no-ff` tells git not to use a _fast-forward_ merge):<br>
     `git merge --no-ff upstream/tweak-readme`


3. Suppose another member has pushed another branch `add-details-to-readme` to the same remote repo. Pull that one too and merge it. If there is a merge conflict, resolve it too.
1. Push your master branch to your fork.

</div>
</div>
