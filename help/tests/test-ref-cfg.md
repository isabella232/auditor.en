---
description: This reference provides more information about the tests Auditor performs for configuration.
seo-description: This reference provides more information about the tests Auditor performs for configuration.
seo-title: Configuration
title: Configuration
uuid: d40d815c-edfe-48b9-921f-cea1b0b54a0a
---

# Configuration

This reference provides more information about the tests Auditor performs for configuration.

Configuration tests scan for specific settings, values, or potential conflicts in your implementation. Auditor evaluates the tags against other rules and recommended best practices.

<table id="table_A8A1FC360482447185C8460A18426638"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Test </th> 
   <th colname="col2" class="entry"> Criteria </th> 
   <th colname="col3" class="entry"> Recommendation </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Advertising Cloud - Conversion names use only alpha-numeric characters</b> </p> <p>Weight: 3 </p> </td> 
   <td colname="col2"> <p>The <span class="codeph"> ev_conversion_property_name</span> parameter should only contain numeric and decimal values EXCEPT for "<span class="codeph"> ev_transid</span>" parameter (the <span class="codeph"> ev_transid</span> value can contain text or numeric values) </p> <p>Look for <span class="codeph"> everesttech.net</span> pixels that contain a URL parameter starting with <span class="codeph"> ev_</span>. </p> <p>Example: </p> <p><span class="codeph"> http://pixel.everesttech.net/1180/t?ev_page_load=1&amp;ev_revenue=$12&amp;ev_transid=1hf74i47 </span> </p> </td> 
   <td colname="col3"> <p> Make sure your transaction property parameters only contain numeric and decimal values. </p> <p> <p>Warning:  Any other value types might cause data loss. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Advertising Cloud - Conversion names use URL-safe characters</b> </p> <p>Weight: 3 </p> </td> 
   <td colname="col2"> <p> Conversion property names should not contain an ampersand or question mark. </p> <p> Example: </p> <p><span class="codeph"> http://pixel.everesttech.net/1180/t?ev_revenue&amp;order=12&amp;ev_transid=</span> </p> </td> 
   <td colname="col3"> <p>Make sure transaction property parameters do not contain a non-encoded ampersand or question mark. These break the URL format. </p> <p> <p>Warning: Property parameters that contain a non-encoded ampersand or question mark, (for example: <span class="codeph"> ev_formComplete?=1</span> or <span class="codeph"> ev_formComplete&amp;Submit=1</span>), might result in data loss. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Advertising Cloud - Transaction ID Implemented Correctly</b> </p> <p>Weight: 1 </p> </td> 
   <td colname="col2"> <p> The property name <span class="codeph"> ev_transid=</span> should not be empty. </p> <p>Example: </p> <p> <span class="codeph"> http://pixel.everesttech.net/1180/t?ev_page_load=1&amp;ev_revenue= 12&amp; ev_transid=</span> </p> </td> 
   <td colname="col3"> <p>The property name <span class="codeph"> ev_transid=</span> should not be left without a value (<span class="codeph"> ev_transid=</span>). If this is left without a value, there could be transaction data loss. Assign a value to the <span class="codeph"> ev_transid=</span> or remove the parameter from the pixel. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Analytics - Instantiated in DOM</b> </p> <p>Weight: 5 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/sc/implement/impl_testing.html" format="html" scope="external"> Additional information</a> </p> </td> 
   <td colname="col2"> <p> The Adobe Analytics code is either not installed or failing to execute. Returns 0 when no analytics code is found web page. </p> </td> 
   <td colname="col3"> <p>Verify that the Analytics tag is implemented on the page and is not blocked by subsequent script activities. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Analytics - Instantiated once</b> </p> <p>Weight: 5 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/sc/implement/" format="https" scope="external"> Additional information</a> </p> </td> 
   <td colname="col2"> <p> The Adobe Analytics code was detected more than once on the page. . Returns 0 when no analytics code is found web page. </p> </td> 
   <td colname="col3"> <p>Make sure there is only one Analytics tag on the page. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Analytics - Latest version</b> </p> <p>Weight: 3 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/sc/appmeasurement/release" format="https" scope="external"> Additional information</a> </p> </td> 
   <td colname="col2"> <p> Your pages are not running the latest version of the Analytics code library. Code libraries that power Experience Cloud technologies are constantly being updated and tweaked in order to take advantage of performance improvements and provide the latest features. Returns 0 when no analytics code is found web page. </p> </td> 
   <td colname="col3"> <p>Install the latest version of the Analytics library. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>DTM - Third-party tags load asynchronously after DOM ready</b> </p> <p>Weight: 3 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/dtm/load_order.html" format="html" scope="external"> Additional information</a> </p> </td> 
   <td colname="col2"> <p>To strike a balance between a good user experience and collecting accurate data, 3rd party tags should be triggered at DOM ready. This will ensure that those tracking scripts execute while not impacting site functionality. </p> </td> 
   <td colname="col3"> <p>Resolve this issue by adjusting all rules that execute 3rd party pixels to fire at DOM Ready. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Experience Cloud ID Service - Latest Version</b> </p> <p>Weight: 2 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/dtm/macid.html" format="html" scope="external"> Additional information</a> </p> </td> 
   <td colname="col2"> <p> Your pages are not running the latest version of the Visitor ID Service code library, <span class="codeph"> visitorAPI.js</span>. Code libraries that power Experience Cloud technologies are constantly being updated and tweaked in order to take advantage of performance improvements and provide the latest features. </p> </td> 
   <td colname="col3"> <p>Install the latest version of the Visitor ID service library. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Launch - Latest Version</b> </p> <p>Weight: 2 </p> <p><a href="https://docs.adobelaunch.com/getting-started" format="https" scope="external"> Additional information</a> </p> </td> 
   <td colname="col2"> <p>These pages are not running the latest version of the Launch code library (Turbine). Code libraries that power Experience Cloud technologies are constantly being updated and tweaked in order to take advantage of performance improvements and provide the latest features. </p> </td> 
   <td colname="col3"> <p> Update the Launch library by rebuilding and publishing the Launch library. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Target - Latest version</b> </p> <p>Weight: 2 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/target/dtm/update-target-tool.html" format="html" scope="external"> Additional information</a> </p> </td> 
   <td colname="col2"> <p> Your pages are not running the latest version of the Target code library. Code libraries that power Experience Cloud technologies are constantly being updated and tweaked in order to take advantage of performance improvements and provide the latest features. </p> </td> 
   <td colname="col3"> <p>Install the latest version of the Target library. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Target - mboxDefault precedes mboxCreate </b> </p> <p>Weight: 5 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/target/ov2/r_target-atjs-mboxcreate.html" format="html" scope="external"> Additional information</a> </p> </td> 
   <td colname="col2"> <p>The proper use of <span class="codeph"> mboxCreate</span> looks similar to this: </p> <p> <span class="codeph"> &lt;div class="mboxDefault"&gt;&lt;!-Customer content--&gt;&lt;/div&gt;&lt;script&gt;mboxCreate('myMboxName')&lt;/script&gt;</span> </p> </td> 
   <td colname="col3"> <p>Be sure to include a <span class="codeph"> &lt;div class="mboxDefault"&gt;&lt;/div&gt;</span> tag before invoking <span class="codeph"> mboxCreate()</span>. at.js will not add one for you. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Target - Valid DOCTYPE</b> </p> <p>Weight: 5 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/target/ov2/r_target-atjs-mboxcreate.html" format="html" scope="external"> Additional information</a> </p> </td> 
   <td colname="col2"> <p> An invalid DOCTYPE was detected. No mboxes will be fired in this scenario. </p> <p>For at.js, the DOCTYPE must be in Standards mode or Target will not work. </p> </td> 
   <td colname="col3"> <p>Update the DOCTYPE on the page. </p> </td> 
  </tr> 
 </tbody> 
</table>

