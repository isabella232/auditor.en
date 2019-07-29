---
description: This reference provides more information about the tests Auditor performs for tag presence.
seo-description: This reference provides more information about the tests Auditor performs for tag presence.
seo-title: Tag presence
title: Tag presence
uuid: 91aa355b-7022-431c-9837-e108b5ce604d
index: y
internal: n
snippet: y
---

# Tag presence{#tag-presence}

This reference provides more information about the tests Auditor performs for tag presence.

## Tag presence {#topic-10aeb8b878044ab38b815cabe136df1e}

This reference provides more information about the tests Auditor performs for tag presence. 

Auditor evaluates whether the tag exists, and whether it's in the right place in your page code. 

<table id="table_98A2E3F7B3154EEFA76D0CAE2FE97CAB"> 
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
    </draft-comment> <p><b>Advertising Cloud - Code presence</b> </p> <p>Weight: 5 </p> </td> 
   <td colname="col2"> <p> The Advertising Cloud tag is not available in the DOM. </p> </td> 
   <td colname="col3"> <p>Implement the Advertising Cloud tag using the Advertising Cloud Launch Extension. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Advertising Cloud - Segment Pixel Implemented</b> </p> <p>Weight: 5 </p> </td> 
   <td colname="col2"> <p> Upgrade your Advertising Cloud segment pixels to the new Advertising Cloud image-only tags. Using the deprecated AMO segment tags can result in data loss. </p> </td> 
   <td colname="col3"> <p>Implement the Advertising Cloud segment pixel using the Advertising Cloud Launch Extension. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Analytics - Loaded in DOM</b> </p> <p>Weight: 5 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/sc/implement/" format="https" scope="external"> Additional information</a> </p> </td> 
   <td colname="col2"> <p> The Adobe Analytics tag was not detected. </p> </td> 
   <td colname="col3"> <p>Install the latest version of Analytics. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b> DTM - Library loaded</b> </p> <p>Weight: 5 </p> <p>Additional information: </p> <p> 
     <ul id="ul_7E706EBC2E4649A69732E6982E116E22"> 
      <li id="li_9AF0257E39C347A9AE6D8D8FFBD66B38"><a href="https://experiencecloud.adobe.com/resources/help/en_US/dtm/c_Troubleshooting.html" format="html" scope="external"> DTM Troubleshooting</a> </li> 
      <li id="li_7B422BCCD2654B0A9059799FB5276BE8"><a href="https://experiencecloud.adobe.com/resources/help/en_US/dtm/t_add_header_fooder_code.html" format="html" scope="external"> Add header and footer code</a> </li> 
     </ul> </p> </td> 
   <td colname="col2"> <p> A global _satellite object was not found in the DOM. Dynamic Tag Management is either not installed or failing to execute. </p> </td> 
   <td colname="col3"> <p>Verify that the DTM library is implemented on the page and is not blocked by subsequent script activities. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b> DTM - One embed code</b> </p> <p>Weight: 5 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/dtm/code.html" format="html" scope="external"> Additional information</a> </p> </td> 
   <td colname="col2"> <p> Production sites should only load one DTM library. </p> </td> 
   <td colname="col3"> <p>Verify that only the production library is loading on the page. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.5 
    </draft-comment> <p><b>DTM - pageBottom callback exists in &lt;body&gt;</b> </p> <p>Weight: 5 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/dtm/t_add_header_fooder_code.html" format="html" scope="external"> Additional information</a> </p> </td> 
   <td colname="col2"> <p> The <span class="codeph"> _satellite.pageBottom()</span> callback was not found within the <span class="codeph"> &lt;body&gt;</span> of the page, which is required by Dynamic Tag Management. </p> <p>This test fails if the <span class="codeph"> pageBottom </span>call isn't found at all on the page, or if it's in the <span class="codeph"> &lt;head&gt;</span> tag (or some other unexpected location). It will only pass if <span class="codeph"> pageBottom</span> is found somewhere within the <span class="codeph"> &lt;body&gt;</span> tag. If it's not on the page at all, it won't function and the other two <span class="codeph"> pageBottom</span> tests will also fail. </p> </td> 
   <td colname="col3"> <p>Add the inline script immediately prior to the closing <span class="codeph"> &lt;/body&gt;</span> tag to ensure proper DTM functionality. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>DTM - pageBottom tag fired</b> </p> <p>Weight: 5 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/dtm/t_add_header_fooder_code.html" format="html" scope="external"> Additional information</a> </p> </td> 
   <td colname="col2"> <p> The DTM <span class="codeph"> pageBottom</span> tag was not detected. </p> <p>This could occur if the call is within an <span class="codeph"> if</span> statement that results in something similar to <span class="codeph"> if (false) {_satellite.pageBottom()}</span>. So, while it might exist and be correctly placed, the tag still might not fire. </p> </td> 
   <td colname="col3"> <p>Install the DTM <span class="codeph"> pageBottom</span> call on every page. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Experience Cloud ID Service - Code presence</b> </p> <p>Weight: 5 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/mcvid/mcvid-overview.htmlimplementation-guides.html" format="html" scope="external"> Additional information</a> </p> </td> 
   <td colname="col2"> <p>The Experience Cloud ID Service code was not found. The Experience Cloud ID (MCID) is highly recommended to ensure you get the most value out of your Experience Cloud solutions and is critical to ID management across Experience Cloud solutions. </p> </td> 
   <td colname="col3"> <p> Install the most recent version of MCID. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Experience Cloud ID Service - Cookie presence</b> </p> <p>Weight: 5 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/mcvid/mcvid-implementation-guides.html" format="html" scope="external"> Additional information</a> </p> </td> 
   <td colname="col2"> <p> The <span class="codeph"> AMCV_</span> cookie was not found. You must instantiate a visitor object from the <span class="codeph"> VisitorAPI.js</span> code. </p> </td> 
   <td colname="col3"> <p> If this is a DTM implementation, verify that the AdobeOrg ID is properly entered into the MCID tool. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Experience Cloud ID Service - MID value present</b> </p> <p>Weight: 5 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/mcvid/mcvid_cookies.html#concept_37156268512445F287CD4BBB2839FFAA__section_C55AF54828DC4CCE89F6118655D694C8" format="html" scope="external"> Additional information</a> </p> </td> 
   <td colname="col2"> <p> The MID value was not found in the <span class="codeph"> AMCV_</span> cookie. </p> </td> 
   <td colname="col3"> <p>Test again to check for any MCID API latency. If the condition persists, contact Adobe Customer Care. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.5 
    </draft-comment> <p><b> Launch - Library loaded</b> </p> <p>Weight: 5 </p> <p><a href="https://docs.adobelaunch.com/getting-started" format="https" scope="external"> Additional information</a> </p> </td> 
   <td colname="col2"> <p> A global _satellite object was not found in the DOM. Launch is either not installed or failing to execute. </p> </td> 
   <td colname="col3"> <p>Verify that the Launch library is implemented on the page and is not blocked by subsequent script activities. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.5 
    </draft-comment> <p><b>Launch - Not have multiple embed scripts</b> </p> <p>Weight: 5 </p> <p><a href="https://docs.adobelaunch.com/getting-started" format="https" scope="external"> Additional information</a> </p> </td> 
   <td colname="col2"> <p>There should not be multiple embed scripts loaded on the page. Production sites should only load one Launch library. </p> </td> 
   <td colname="col3"> <p>Verify that only the production library is loading on the page. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.5 
    </draft-comment> <p><b>Launch - pageBottom callback exists in &lt;body&gt;</b> </p> <p>Weight: 5 </p> <p><a href="https://docs.adobelaunch.com/getting-started" format="https" scope="external"> Additional information</a> </p> </td> 
   <td colname="col2"> <p> The <span class="codeph"> _satellite.pageBottom()</span> callback was not found within the <span class="codeph"> &lt;body&gt;</span> of the page, which is required by Launch. </p> <p>This test fails if the <span class="codeph"> pageBottom </span>call isn't found at all on the page, or if it's in the <span class="codeph"> &lt;head&gt;</span> tag (or some other unexpected location). It will only pass if <span class="codeph"> pageBottom</span> is found somewhere within the <span class="codeph"> &lt;body&gt;</span> tag. If it's not on the page at all, it won't function and the other two <span class="codeph"> pageBottom</span> tests will also fail. </p> </td> 
   <td colname="col3"> <p>Add the inline script immediately prior to the closing <span class="codeph"> &lt;/body&gt;</span> tag to ensure proper Launch functionality. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.5 
    </draft-comment> <p><b>Launch - pageBottom callback should not exist when asynchronously deployed</b> </p> <p>Weight: 5 </p> <p><a href="https://docs.adobelaunch.com/getting-started" format="https" scope="external"> Additional information</a> </p> </td> 
   <td colname="col2"> <p>The <span class="codeph"> _satellite.pageBottom()</span> callback was found on the page, which should not be the case when Launch is asynchronously deployed. </p> </td> 
   <td colname="col3"> <p>Remove the<span class="codeph"> _satellite.pageBottom()</span> script to enable proper Launch functionality. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b> Target - Code Presence</b> </p> <p>Weight: 5 </p> <p><a href="https://docs.adobe.com/content/help/en/target/using/implement-target/implementing-target.html" format="html" scope="external"> Additional information</a> </p> </td> 
   <td colname="col2"> <p>Target should be defined in the DOM. </p> </td> 
   <td colname="col3"> <p>Install the most recent version of Target (at.js). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.5 
    </draft-comment> <p><b> Target - Library loaded in &lt;head&gt;</b> </p> <p>Weight: 4 </p> <p><a href="https://docs.adobe.com/content/help/en/target/using/implement-target/implementing-target.html" format="html" scope="external"> Additional information</a> </p> 
    <draft-comment>
      TE61c380082a4b4706b28a84aa047599a7 
    </draft-comment> </td> 
   <td colname="col2"> <p> The Target library should be loaded in the <span class="codeph"> &lt;head&gt;</span> tag. </p> </td> 
   <td colname="col3"> <p> Check to be sure that the Target library is loaded in the <span class="codeph"> &lt;head&gt;</span> tag. </p> </td> 
  </tr> 
 </tbody> 
</table>

