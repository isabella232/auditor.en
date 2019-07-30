---
description: null
seo-description: null
seo-title: Test rubric 1.0.1
title: Test rubric 1.0.1
uuid: 2ed2572e-ddb8-4899-b3a9-1329afdd7905

---

# Test rubric 1.0.1{#test-rubric}

## Test rubric 1.0.1 {#topic-25ed23afdfaf4a12b149ff276965b043}

## Alerts {#topic-1336e3975278436583e4215aa48f08a5}

This reference provides more information about the alerts Auditor displays for tests. 

Alerts show issues you should be aware of, but that don't affect your score. These are best practice recommendations that, in some cases, may not apply to your implementation.

<table id="table_031432C9BB804A6F90E7FF572739E169"> 
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
    </draft-comment> <p><b>Advertising Cloud - Correct Conversion Tag Implemented</b> </p> <p>Weight: 0 </p> </td> 
   <td colname="col2"> <p>Check whether the correct conversion tag is used. </p> <p> <p>Warning:  Using the deprecated TubeMogul conversion tags can result in data loss. </p> </p> </td> 
   <td colname="col3"> <p>Upgrade your conversion pixels to the new Advertising Cloud image-only conversion tags. </p> <p>This can be most easily accomplished with the Advertising Cloud Launch Extension. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Advertising Cloud - Correct JS Tag Used</b> </p> <p>Weight: 0 </p> </td> 
   <td colname="col2"> <p>Advertising Cloud should use latest JavaScript tags. </p> </td> 
   <td colname="col3"> <p>Upgrade your Advertising Cloud JavaScript to the latest version. Using the deprecated JavaScript versions can result in lost functionality. </p> <p>This can be accomplished more easily through the use of the Advertising Cloud Launch Extension. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Advertising Cloud - Image-only tag</b> </p> <p>Weight: 0 </p> </td> 
   <td colname="col2"> <p>The Advertising Cloud image pixel format should match one of the following recommended formats: </p> <p> 
     <ul id="ul_D85BE9C8A8654DE890E1A814E3573D86"> 
      <li id="li_E2AEDD76AC7044E8AD6AE8375858D198"> <p><span class="codeph"> http(s)://rtd.tubemogul.com/upi/?sid=&lt;HASH_VALUE&gt;</span> </p> </li> 
      <li id="li_1EEFA03516BF445294B5EC5DED891758"> <p><span class="codeph"> http(s)://rtd-tm.everesttech.net/upi/?sid=&lt;HASH_VALUE&gt;</span> </p> </li> 
      <li id="li_F72206B142214217BDD34356D2F3D8AD"> <p><span class="codeph"> http(s)://pixel.everesttech.net/px2/&lt;NUMERIC_ID&gt;?</span> </p> </li> 
     </ul> </p> </td> 
   <td colname="col3"> <p>Upgrade your Advertising Cloud pixels to the new Advertising Cloud image-only tags, which ensure you are taking advantage of the full Advertising Cloud functionality. </p> <p>This can be most easily accomplished with the Advertising Cloud Launch Extension. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Advertising Cloud - Segment Pixels DSP Syncing Enabled</b> </p> <p>Weight: 0 </p> </td> 
   <td colname="col2"> <p>Check whether the TubeMogul segment pixel contains a DSP Syncing setting, and recommend that the setting be added to the pixel. </p> <p>The DSP Syncing setting is determined by the use of a query string parameter, so </p> <p>IF the tag is being fired to<span class="codeph"> ("https://rtd.tubemogul.com/upi/?sid=&lt;HASH_VALUE&gt;"</span> </p> <p> OR <span class="codeph"> "http(s)://rtd-tm.everesttech.net/upi/?sid=&lt;HASH_VALUE&gt;"</span> </p> <p> OR <span class="codeph"> "http(s)://pixel.everesttech.net/px2/&lt;NUMERIC_ID&gt;?"</span> </p> <p>AND the tag contains the URL parameter <span class="codeph"> "sid=")</span> </p> <p>THEN check to see if the URL parameter <span class="codeph"> "cs=0"</span> or<span class="codeph"> "cs=1"</span> exists, and if not recommend that <span class="codeph"> "cs=1"</span> be added to those pixels so that the audience match rates can improve. </p> </td> 
   <td colname="col3"> <p> Add the URL parameter <span class="codeph"> "cs=1"</span> to your Advertising Cloud pixels so that DSP Syncing can occur, which increases audience match rates. </p> <p>This can most easily be accomplished with the Advertising Cloud Launch Extension. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>DTM - pageBottom callback placement</b> </p> <p>Weight: 0 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/dtm/t_add_header_fooder_code.html" format="html" scope="external"> Additional information</a> </p> 
    <draft-comment>
      TEa9df69942f404055a64262889c8b21d3 
    </draft-comment> </td> 
   <td colname="col2"> <p>Dynamic Tag Management requires the <span class="codeph"> _satellite.pageBottom()</span> function. Add the inline script immediately prior to the closing body tag to ensure proper DTM functionality. </p> <p> <p>Note: It is best practice that the tag be the <i>last</i> tag in the <span class="codeph"> &lt;body&gt;</span>. If it's found within the <span class="codeph"> &lt;body&gt;</span> tag, it has a chance of functioning, but as it is not best practice, it could function incorrectly or with unexpected or undesired results. </p> </p> </td> 
   <td colname="col3"> <p>Add the inline script immediately prior to the closing <span class="codeph"> &lt;/body&gt;</span> tag to ensure proper DTM functionality. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>DTM - Self-Hosted</b> </p> <p>Weight: 0 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/dtm/deployment.html" format="html" scope="external"> Additional information</a> </p> </td> 
   <td colname="col2"> <p> The DTM library is being hosted on Adobe's Akamai instance at <span class="filepath"> assets.adobedtm.com</span>. </p> <p> Self-hosting is the recommended approach for loading DTM because it provides greater control of website performance through cache control, reducing third-party script dependencies, and greater control of the publishing process. The DTM libraries can be hosted and managed through your own web hosting or CDN. </p> </td> 
   <td colname="col3"> <p>Self-hosting is the recommended approach for loading DTM on a page. Although DTM hosting via the Akamai CDN works in most cases, self-hosting improves page performance. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b> Experience Cloud ID Service - Use only one AdobeOrg</b> </p> <p>Weight: 0 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/mcvid/mcvid_id_request.html" format="html" scope="external"> Additional information</a> </p> </td> 
   <td colname="col2"> <p>In a normal MCID implementation, a single AdobeOrg should be used. </p> </td> 
   <td colname="col3"> <p>Validate that multiple AdobeOrg IDs exist for this implementation. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Launch - pageBottom callback placement</b> </p> <p>Weight: 0 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/experience-cloud/launch/t_quick-start.html" format="html" scope="external"> Additional information</a> </p> 
    <draft-comment>
      TE48c499b022f545c5bccc6f8bde169685 
    </draft-comment> </td> 
   <td colname="col2"> <p>Launch should have a <span class="codeph"> pageBottom </span>callback function defined last in the body of the page if synchronously deployed </p> <p> <p>Note: It is best practice that the tag be the <i>last</i> tag in the <span class="codeph"> &lt;body&gt;</span>. If it's found within the <span class="codeph"> &lt;body&gt;</span> tag, it has a chance of functioning, but as it is not best practice, it could function incorrectly or with unexpected or undesired results. </p> </p> </td> 
   <td colname="col3"> <p>Add the inline script immediately prior to the closing <span class="codeph"> &lt;/body&gt;</span> tag to ensure proper DTM functionality. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Launch - Self-Hosted</b> </p> <p>Weight: 0 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/experience-cloud/launch/t_quick-start.html" format="html" scope="external"> Additional information</a> </p> </td> 
   <td colname="col2"> <p>The Launch library is being hosted on Adobe's Akamai instance at <span class="filepath"> assets.adobedtm.com</span>. </p> <p>Self-hosting is the recommended approach for loading Launch because it provides greater control of website performance through cache control, reducing third-party script dependencies, and greater control of the publishing process. The Launch libraries can be hosted and managed through your own web hosting or CDN. </p> </td> 
   <td colname="col3"> <p>Although Launch hosting via the Akamai CDN works in most cases, it is recommended that self-hosting be implemented as the first step in improving page performance. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Launch - should be asynchronously deployed</b> </p> <p>Weight: 0 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/experience-cloud/launch/t_quick-start.html" format="html" scope="external"> Additional information</a> </p> </td> 
   <td colname="col2"> <p>Launch should be asynchronously deployed for optimal performance. </p> </td> 
   <td colname="col3"> <p>Include the async parameter in the inline script to ensure proper async Launch functionality </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b> Target - Content in mboxDefault</b> </p> <p>Weight: 0 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/target/ov2/r_target-atjs-mboxcreate.html" format="html" scope="external"> Additional information</a> </p> </td> 
   <td colname="col2"> <p> Content should exist in mboxDefault when using at.js. </p> </td> 
   <td colname="col3"> <p>Verify that the content is available. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Configuration {#topic-a5ebc362c9864209a2c3fdadcae35d18}

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
    </draft-comment> <p><b>Launch - Latest Version</b> </p> <p>Weight: 2 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/experience-cloud/launch/t_quick-start.html" format="html" scope="external"> Additional information</a> </p> </td> 
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

## Tag consistency {#topic-a65cca9b5a294706b4069a93bc9c9d76}

This reference provides more information about the tests Auditor performs for tag consistency. 

Auditor's consistency tests look for inconsistencies across all scanned pages. These are values or configurations that should be the same across all pages on the site to ensure accurate data collection.

<table id="table_4F9ED873BAF741D19BFB0F297B3A1FDB"> 
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
    </draft-comment> <p><b>Analytics - Consistent code version </b> </p> <p>Weight: 5 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/sc/implement/choose-implementation-method.html" format="html" scope="external"> Additional information</a> </p> </td> 
   <td colname="col2"> <p> More than one version of the Analytics code was found. </p> </td> 
   <td colname="col3"> <p>Replace all instances of Analytics with the current version. </p> </td> 
  </tr> 
 </tbody> 
</table>

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
      1.0.1 
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
      1.0.1 
    </draft-comment> <p><b> Launch - Library loaded</b> </p> <p>Weight: 5 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/experience-cloud/launch/t_quick-start.html" format="html" scope="external"> Additional information</a> </p> </td> 
   <td colname="col2"> <p> A global _satellite object was not found in the DOM. Launch is either not installed or failing to execute. </p> </td> 
   <td colname="col3"> <p>Verify that the Launch library is implemented on the page and is not blocked by subsequent script activities. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Launch - Not have multiple embed scripts</b> </p> <p>Weight: 5 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/experience-cloud/launch/t_quick-start.html" format="html" scope="external"> Additional information</a> </p> </td> 
   <td colname="col2"> <p>There should not be multiple embed scripts loaded on the page. Production sites should only load one Launch library. </p> </td> 
   <td colname="col3"> <p>Verify that only the production library is loading on the page. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Launch - pageBottom callback exists in &lt;body&gt;</b> </p> <p>Weight: 5 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/experience-cloud/launch/t_quick-start.html" format="html" scope="external"> Additional information</a> </p> </td> 
   <td colname="col2"> <p> The <span class="codeph"> _satellite.pageBottom()</span> callback was not found within the <span class="codeph"> &lt;body&gt;</span> of the page, which is required by Launch. </p> <p>This test fails if the <span class="codeph"> pageBottom </span>call isn't found at all on the page, or if it's in the <span class="codeph"> &lt;head&gt;</span> tag (or some other unexpected location). It will only pass if <span class="codeph"> pageBottom</span> is found somewhere within the <span class="codeph"> &lt;body&gt;</span> tag. If it's not on the page at all, it won't function and the other two <span class="codeph"> pageBottom</span> tests will also fail. </p> </td> 
   <td colname="col3"> <p>Add the inline script immediately prior to the closing <span class="codeph"> &lt;/body&gt;</span> tag to ensure proper Launch functionality. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Launch - pageBottom callback should not exist when asynchronously deployed</b> </p> <p>Weight: 5 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/experience-cloud/launch/t_quick-start.html" format="html" scope="external"> Additional information</a> </p> </td> 
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
      1.0.1 
    </draft-comment> <p><b> Target - Library loaded in &lt;head&gt;</b> </p> <p>Weight: 4 </p> <p><a href="https://docs.adobe.com/content/help/en/target/using/implement-target/implementing-target.html" format="html" scope="external"> Additional information</a> </p> 
    <draft-comment>
      TE61c380082a4b4706b28a84aa047599a7 
    </draft-comment> </td> 
   <td colname="col2"> <p> The Target library should be loaded in the <span class="codeph"> &lt;head&gt;</span> tag. </p> </td> 
   <td colname="col3"> <p> Check to be sure that the Target library is loaded in the <span class="codeph"> &lt;head&gt;</span> tag. </p> </td> 
  </tr> 
 </tbody> 
</table>

