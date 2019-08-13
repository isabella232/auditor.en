---
description: This reference provides more information about the alerts Auditor displays for tests.
seo-description: This reference provides more information about the alerts Auditor displays for tests.
seo-title: Alerts
title: Alerts
uuid: 8f05b3c1-2427-4691-a88f-1de98f120a02

---

# Alerts{#alerts}

This reference provides more information about the alerts Auditor displays for tests.

## Alerts {#alerts}

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
      CAce6db25bc8c443409f0fcc5ac9d622c3 
    </draft-comment> <p><b>DTM - pageBottom callback placement</b> </p> <p>Weight: 0 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/dtm/t_add_header_fooder_code.html" format="html" scope="external"> Additional information</a> </p> 
    <draft-comment>
      TEa9df69942f404055a64262889c8b21d3 
    </draft-comment> </td> 
   <td colname="col2"> <p>Dynamic Tag Management requires the <span class="codeph"> _satellite.pageBottom()</span> function. Add the inline script immediately prior to the closing <span class="codeph"> &lt;/body&gt;</span> tag to ensure proper DTM functionality. </p> <p> <p>Note: It is best practice that the tag be the <i>last</i> tag in the <span class="codeph"> &lt;body&gt;</span>. If it's found within the <span class="codeph"> &lt;body&gt;</span> tag, it has a chance of functioning, but as it is not best practice, it could function incorrectly or with unexpected or undesired results. </p> </p> </td> 
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
      1.0.5 
    </draft-comment> <p><b>Launch - pageBottom callback placement</b> </p> <p>Weight: 0 </p> <p><a href="https://docs.adobelaunch.com/getting-started" format="https" scope="external"> Additional information</a> </p> 
    <draft-comment>
      TE48c499b022f545c5bccc6f8bde169685 
    </draft-comment> </td> 
   <td colname="col2"> <p>Launch should have a <span class="codeph"> pageBottom </span>callback function defined last in the body of the page if synchronously deployed. </p> <p> <p>Note: It is best practice that the tag be the <i>last</i> tag in the <span class="codeph"> &lt;body&gt;</span>. If it's found within the <span class="codeph"> &lt;body&gt;</span> tag, it has a chance of functioning, but as it is not best practice, it could function incorrectly or with unexpected or undesired results. </p> </p> </td> 
   <td colname="col3"> <p>Launch requires the <span class="codeph"> _satellite.pageBottom()</span> function for synchronous deployments. Add the inline script immediately prior to the closing <span class="codeph"> &lt;/body&gt;</span> tag to ensure proper Launch functionality. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Launch - Self-Hosted</b> </p> <p>Weight: 0 </p> <p><a href="https://docs.adobelaunch.com/getting-started" format="https" scope="external"> Getting started with Launch</a> </p> <p><a href="https://docs.adobelaunch.com/client-side-information/asynchronous-deployment" format="https" scope="external"> Launch asynchronous deployment</a> </p> </td> 
   <td colname="col2"> <p>The Launch library is being hosted on Adobe's Akamai instance at <span class="filepath"> assets.adobedtm.com</span>. </p> <p>Self-hosting is the recommended approach for loading Launch because it provides greater control of website performance through cache control, reducing third-party script dependencies, and greater control of the publishing process. The Launch libraries can be hosted and managed through your own web hosting or CDN. </p> </td> 
   <td colname="col3"> <p>Although Launch hosting via the Akamai CDN works in most cases, it is recommended that self-hosting be implemented as the first step in improving page performance. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Launch - should be asynchronously deployed</b> </p> <p>Weight: 0 </p> <p><a href="https://docs.adobelaunch.com/getting-started" format="https" scope="external"> Additional information</a> </p> </td> 
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

