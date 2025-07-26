<frontmatter>
title: "Admin Info"
header: header.md
footer: footer.md
head: adminHead.md
pageNav: 2
</frontmatter>

<div class="website-content" id="main">

# **TEE3201 Software Engineering**

<!-- .......................................................................................... --> {{ line_dotted }}

# Course overview
<div class="indented" id="course-info">

<pic eager src="{{baseUrl}}/images/growingPlant.png" width="700"></pic>

_TEE3201 Software Engineering_ contains roughly a **50-50 balance of theory and practice** of SE. It covers the knowledge/skills necessary to do small software projects.
</div>

<!-- .......................................................................................... --> {{ line_dotted }}

# Using this course website

<div class="indented" id="website-info">
<include src="usingThisWebsite.md#main" />
</div>

<!-- .......................................................................................... --> {{ line_dotted }}

# Instructors
<div class="indented">

#### Lecturer
<div class="container">
  <div class="row">
    <div class="col-3">

<br>

![Damith]({{ baseUrl }}/admin/images/damith.png)
    </div>
    <div class="col">

**Damith Chatura RAJAPAKSE**<br>
Associate Professor, NUS School of Computing<br>
PhD, Software Engineering, NUS, 2002-2006<br>
BSc, Computer Science & Engineering, University of Moratuwa, 1996-2001<br>
%%:fas-envelope:%% <span id="prof-email">`damith`[at]`comp.nus.edu.sg`</span><br>
%%:fas-map-marker-alt:%% COM2-02-57<br>
%%:fas-phone-square:%% 651 64359<br>
%%:fas-home:%% https://www.comp.nus.edu.sg/~damithch
    </div>
  </div>
  <div class="row">

  </div>
</div>

#### Tutors:
* **Khoo Jin Xiang**:&nbsp;&nbsp; %%:fas-envelope:%% <span id="ta-email">`e0958193`[at]`u.nus.edu`</span>

</div>

<!-- .......................................................................................... --> {{ line_dotted }}

# Lectures + Tutorials
<div class="indented" id="lectures-info">

%%:far-clock:%% Wednesdays 1800-2130<br>
%%:fas-map-marker-alt:%% Venue: {{ lecture_venue }}<br>

**==The first lecture will be in F2F mode==, and will start at 7pm.**

**Subsequent lecture + tutorial time is divided into three parts, as given below and will be in hybrid mode.**<br>
You can continue to attend them using F2F mode but those who show good progress in weekly tasks will have the option to join live via Zoom, or watch the recording later.

* 1800-1900: Do exercises related to previous week topics. Consult prof/tutor (via MS Teams or F2F) if you encounter problems.
* 1900-2000: Short lecture/briefing, introducing topics for the current week.<br>
  Delivered in ==hybrid mode (i.e., you can attend F2F, join via Zoom, or watch the recording later)==. After that, watch the pre-recorded videos and follow the textbook sections provided.
* 2000-2130: Optionally, you can stay back and do exercises for the current week. Consult prof/TA (F2F or using MS Teams) for help, as needed.<br>


**{{ icon_slides }} Lecture slides will be uploaded to Canvas after the lecture**, usually by midnight of the same day. **Lecture slides are not suitable to be used as reference materials** as they have been <tooltip content="i.e., heavy use of graphics and animations">optimized for lecture delivery</tooltip> instead.


</div>

<!-- .......................................................................................... --> {{ line_dotted }}

# Textbook

**Software Engineering Textbook**:

A customized **online text book** is used for this course. Topic coverage may not follow the exact topic sequence in the book. There are several ways for you to access the text book.
* Full version is [here]({{baseUrl}}/se-book-adapted/index.html): The relevant sections are embedded under the corresponding week in the [schedule page]({{baseUrl}}/schedule/index.html).
* {{ icon_print }} Printable version is [here]({{baseUrl}}/se-book-adapted/print.html). ==You are encouraged to use the online full version when possible== (instead of the printable version or the PDF version), as it has more content %%videos, exercises, etc.%%

**Programming Textbook**:

[An additional **guide on programming basics**]({{baseUrl}}/programming/index.html) is provided for you to get started or programming. The topics in that textbook are to help you do the programming part of the project. Furthermore, we try to use external resources as much as possible in our guide so that you can continue your learning using those resources beyond the scope of this course.

<!-- .......................................................................................... --> {{ line_dotted }}

# Programming Language

This course uses Python programming language to teach you programming basics required for software engineering. <span class="text-danger">A basic knowledge of Python is expected in the final exam, to the extent it was used in the weekly exercises and the project.</span> For example, some questions might use Python code snippets as part of the question.

**Install [Python (the latest 3.x version)](https://www.python.org/downloads/)** on your computer.

<!-- .......................................................................................... --> {{ line_dotted }}

# Programming Exercises
<span id="exercises-info">

In some weeks, there will be some programming exercises for you to submit (on Coursemology). You should do the exercises as you learn the topics.

<box type="warning">

**Learn the topic first before trying the exercises**. While these are exercises provided to self-test your knowledge, the more important thing is to read and understand the topic content. Furthermore, not all topics are tested by exercises.
</box>
</span>

# Project

<div  id="project-info">

* The project is to be done **individually**.
* The project based on a [generic project called Monty](../programming/chapters/monty.html).
* In the project, you will build a small chatbot, **using Python**.
* The project is to be done in small increments. You will be given a schedule of what increments to be done in each week.
* Some project increments will be common to all students, while some will vary from student to student (to be announced near to the date). That means your final product will be unique in terms of total features, but some features will be common to other students in the class.
* Constraints:
  1. You should not use relational/SQL databases e.g., MySQL
  1. The software should work in a Windows computer that has Python 3. If your software needs other software to be installed (e.g., third-party libraries), please get prof's permission first.
</div>

<panel header="### Weekly Project Increments">
{% for i in range(1, 14) %}

#### <span class="badge bg-dark">Week {{ i }}:</span>
<include src="../schedule/week{{ i }}/admin-tee3201-fragment.md#week{{ i }}-project" />
<hr>
{%-endfor %}
</panel>
<p/>

<div id="final-submission-info">

### Week 13: Final Submission

**Submission Deadline**: Sunday of week 13 (#r#{{ date_w13_start | date("YYYY-MM-DD", 6) }} 23:59##).

* An extra week can be given (upon request) for a small late submission penalty of `-2` marks.
* Submissions later than the above one-week extra time are liable to a late submission penalty, to be fair to those who submitted on time. But given you are part-time students, late submission penalty will be more lenient than otherwise (e.g., `-1 per day`) and will be on a case-by-case basis.

**Deliverables**:
1. **Code** of the working program: zip (not rar) the code.
   * Submission: via Canvas assignments
   * File name: `{Your Name}.zip` e.g., `Jun Hao.zip`
1. **Project report**: a single .docx or a pdf file that ==follows the template given== (template file will be available in Canvas).
   * Submission: via Canvas assignments
   * File name: `{Your Name}.docx/pdf`  e.g., `Jun Hao.docx`
   * Optionally, you can get feedback on an early project report draft by emailing it to the prof <span class="text-danger">no later than {{ date_w13_start | date("YYYY-MM-DD", 2) }}</span> (i.e., week 13 Wednesday). Note that such feedback will be limited to high-level comments only (reason: the report is graded), and given only once per student.
1. **Demo video**:
   * Record a demo video showcasing the features of your product. You can use any screen recording software for this. One simple way is to start a Zoom meeting and record the meeting while screen-sharing your demo.
   * Use the exact version of the code you submitted (i.e., the demo should match the submitted code exactly).
   * Recommended length 7 minutes, max length 10 minutes.
   * Audio narration is optional if the demo can be understood without the audio.
   * Ensure the video is in a format that can be played by any computer.
   * Submission: via Canvas assignments
   * File name: `{Your Name}.mp4`  e.g., `Jun Hao.mp4`
1. **Code Reuse Declaration**:
   * Submit the Canvas survey 'Code Reuse Declaration' when it opens in week 13, to declare your level of code reuse in the project.
   * This is compulsory. You <span class="text-danger">must submit this even if you did not reuse</span> any code.

</div>

<!-- .......................................................................................... --> {{ line_dotted }}

# Policies

<div id="deadlines-info">

### Deadlines
* Deadline for weekly tasks:
  * **If a specific deadline is given**, adhere to that.
  * **If no specific deadline is given**,
    * Soft deadline: try to complete tasks allocated to a week before the following lecture.
    * Hard deadline: In case you fail to meet the soft deadline, there will be no penalty if a task is done within one week after the soft deadline.
</div>

<div id="plagiarism-info">

### Plagiarism
* You may view/discuss others' work or get help from others. However, <span class="text-danger"> ==the work you submit should be your own==. In case of similar submissions, ~~marks will be divided among those submissions~~</span> ~~e.g., if your submission scored 8/10 and there is another submission that is similar to your work (beyond coincidental similarity), each submission will get 4 marks~~ (new policy: NUS requires all plagiarism cases to reported to the university).
* If you reuse/adapt code from elsewhere (e.g., from an online site such as stackoverflow), you must cite the source in the code. e.g.,
  ```python{.no-line-numbers}
  # Solution below adapted from https://stackoverflow.com/a/16252290
  {Your implementation of the reused solution here ...}
  ```

<include src="policies-fragment.md#cite-reuse-immediately" />

<include src="policies-fragment.md#using-tool-generated-code" />
</div>

<!-- .......................................................................................... --> {{ line_dotted }}

# Tools
<div class="indented">
<div id="coursemology-info">

### Coursemology

* We'll be using [Coursemology](http://coursemology.org/) for coding exercises (compulsory).
* You'll receive the invitation link near to the first lecture.
* More info about assignment submission will be given in the first week's lecture.


</div>
<div id="intellij-info">

### PyCharm

* PyCharm is the recommended Python editor. While using PyCharm is optional, there will be no help/instructions given for other editors.

* In the initial weeks, `repl.it` online editor is good enough for writing Python code. As your project code gets bigger in later weeks, you can consider installing [PyCharm](https://www.jetbrains.com/pycharm/download) on your computer. You may use the Community Edition (free) or the Professional Edition (free for students).
</div>
</div>
<!-- .......................................................................................... --> {{ line_dotted }}


# Getting Help
<span id="help-info">

If you face difficulties/doubts while learning the weekly topics, doing weekly exercises/tasks, here are the ways to get help, in the order of preference (most preferred on the top).
1. **[Preferred] Post in [MS Teams ==channel for the class==]({{ url_ms_teams_class }})**:
   * If there is any chance that the question can be relevant to other classmates, post in the `General` channel.
   * Otherwise, post in the `YOUR_NAME - Help Channel` private channel we have created for each of you.
   * If there is no response from us after 24 hours (in which case it is likely that we didn't get the MS Teams notification), feel free to remind us by emailing `{{ course | lower }}@comp.nus.edu.sg`.
1. **Email `{{ course | lower }}@comp.nus.edu.sg`**. These emails will be answered by the prof or forwarded to the TA for follow up.
1. You may also post in the [Canvas forum]({{ url_forum }}) or [Coursemology forum]({{ url_coursemology_classroom }}/forums).

</span>
<!-- .......................................................................................... --> {{ line_dotted }}

<span id="assessment-info">

# Assessment

* **10%: Participation** -- To get full marks, submit weekly programming exercises and weekly project increments <trigger trigger="click" for="modal:adminInfo-deadlineInfo">on time</trigger>. In a week that has a quiz, they will be counted for participation as well.
* **30%: Project**
  * 10%: Documentation
  * 20%: Functionality, code
* **60%: Final Exam**


<modal large header="The Policy on Deadlines" id="modal:adminInfo-deadlineInfo">
  <include src="index-{{ course | lower }}-fragment.md#deadlines-info"/>
</modal>

</span>

<!-- .......................................................................................... --> {{ line_dotted }}


# Exam

<div class="indented">

<include src="exam-pen-and-paper.md" />

</div>

</div>
