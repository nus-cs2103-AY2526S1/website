<div id="testingPreparations">

* Ensure that you have accepted the invitation to join the GitHub org used by the course. Go to [{{ url_course_org }}]({{ url_course_org }}) to accept the invitation.

* Ensure you have access to a **computer that is able to run course projects** %%e.g., has the right Java version%%.

* **Ensure you can use [CATcher](https://catcher-org.github.io/CATcher/)** on your computer. You should have done this when you smoke-tested CATcher earlier in the semester.

<div class="indented-level1">

<panel header="If not using CATcher" minimized>

<div id="not-using-catcher-warning">

<box type="warning">

Issues created for PE-D and PE need to be in a precise format for our grading scripts to work. Incorrectly-formatted responses will have to discarded. Therefore, you are **<span class="text-danger">not allowed to use the GitHub interface for PE-D and PE activities, unless you have obtained  our permission first</span>**.

</box>

</div>

{% set pe_session = 'ped' if (current_week | int) < 11 else 'pe' %}
{% set pe_session_upper = (pe_session | upper) %}

<div id="pe-create-repo">

* Create a public repo in your GitHub account with the name `{{ pe_session }}`
* Enable its issue tracker and add the following labels to it (the label names should be precisely as given).

<include src="appendixE-gitHub.md#bug-severity" />
<include src="tp-pe-fragment.md#type-labels" />
</div>

</panel><p/>
</div>

* **Have a good screen grab tool** with annotation features so that you can quickly take a screenshot of a bug, annotate it, and post in using CATcher.<br>
  {{ icon_tip }} You can use <kbd>Ctrl</kbd>+<kbd>V</kbd> to paste a picture from the clipboard into a text box in a bug report.

* **[Optional] Have a good screen recording tool** if you plan to use screen recording clips as part of your bug reports. Ensure that your screen recording tool can create small files as CATcher doesn't allow files bigger than 10Mb.<br>
  {{ icon_important }} As the CATcher support for uploading screen recordings is new and limited, use it only if strictly necessary -- use screenshots for other cases.

* **<span class="text-danger">Download the product to be tested</span>**.

<tabs active="{{ pe_active_tab }}" add-class="ml-4">
<tab header="PE Dry Run (at **{{ version_penultimate }}**)">

* After you have been notified which team to test (likely to be in the morning of PE-D day), #r#wait until you are no more than 2 hours from the PE-D start time##, and download the JAR file and the UG/DG PDF file from the team's latest release. Downloading the files any earlier runs the risk of you testing an outdated version of the product.

</tab>
<tab header="PE (at **{{ version_final }}**)">

<div id="zip-download-unzip-info" >
<box type="info" header="++Downloading and unzipping JAR/PDF files you will test in the PE++" icon=":fas-download:">

The files you need for the PE (i.e., `.jar` file, UG and DG `.pdf` files, and the source code) will be **given to you as an encrypted zip file**. Here are the two steps involved in using it.

1. **Downloading the zip file**: After we inform you the details (via email), go to the download location (a Dropbox folder), and download the zip file bearing your partial student number (e.g., `A---0000X.zip`).
   * The **dropbox password needed to download this** file is `{{ course | lower }}`.
   * ==You must download this file in advance.== Trying to download it during the PE can cause Dropbox to block you due to 'too many attempts'.
1. **Unzipping the zip file**: You will **need a second two-part password** to unzip this file. That password has two parts.
   * The second part will be unique to each student, and will be given in the same email mentioned above.
   * The first part of the password (common to all) will only be given at the start of the PE, by your PE invigilator.
</box>
</div>

</tab>
</tabs>
<p/>

<div class="indented">

<box>

****Testing tips****{.text-success}

{% set tip %}<span class="text-success">**:fas-lightbulb:**</span>{% endset %}

{{ tip }} **Use easy-to-remember patterns in test data.** For example, if you use `12345678` as a phone number while testing and it appears as `2345678` somewhere else in the UI, you can easily spot that the first digit has gone missing. But if you used a random number instead, detecting that bug won't be as easy. Similarly, if you use `Alice Bee`, `Benny Lee`, `Charles Pereira` as test data (note how the names start with letters A, B, C), it will be easy to detect if one goes missing, or they appear in the incorrect order.

{{ tip }} **Go wide before you go deep**. Do a light testing of all features first. That will give you a better idea of which features are likely to be more buggy. Spending equal time for all features or testing in the order the features appear in the UG is not always the best approach.

</box>
</div>
<p/>
<!--
* **Charge your computer** before coming to the session. The testing venue might not have enough charging points.
-->
</div>
