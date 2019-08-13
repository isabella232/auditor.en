---
description: null
seo-description: null
seo-title: Test rubric 0.0.8
title: Test rubric 0.0.8
uuid: c62b7169-a650-4650-876f-c254eb57cb25

---

# Test rubric 0.0.8{#test-rubric}

## Test rubric 0.0.8

![](assets/space.png)

## Alerts {#alerts}

This reference provides more information about the alerts Auditor displays for tests. 

Alerts show issues you should be aware of, but that don't affect your score.

|Test|Criteria|Recommendation|
|--- |--- |--- |
|Advertising Cloud - Correct Conversion Tag Implemented  Weight: 0|Check whether the correct conversion tag is used.   Warning:  Using the deprecated TubeMogul conversion tags can result in data loss.|Upgrade your conversion pixels to the new Advertising Cloud image-only conversion tags.  This can be most easily accomplished with the Advertising Cloud Launch Extension.|
|Advertising Cloud - Image-only tag  Weight: 0|The Advertising Cloud image pixel format should match one of the following recommended formats: <br>http(s)://rtd.tubemogul.com/upi/?sid=<HASH_VALUE><br/>http(s)://rtd-tm.everesttech.net/upi/?sid=<HASH_VALUE><br/>http(s)://pixel.everesttech.net/px2/<NUMERIC_ID>?|Upgrade your Advertising Cloud pixels to the new Advertising Cloud image-only tags, which ensure you are taking advantage of the full Advertising Cloud functionality.  This can be most easily accomplished with the Advertising Cloud Launch Extension.|
|Advertising Cloud - Segment Pixels DSP Syncing Enabled  Weight: 0|Check whether the TubeMogul segment pixel contains a DSP Syncing setting, and recommend that the setting be added to the pixel.  The DSP Syncing setting is determined by the use of a query string parameter, so  IF the tag is being fired to ("https://rtd.tubemogul.com/upi/?sid=<HASH_VALUE>"   OR  "http(s)://rtd-tm.everesttech.net/upi/?sid=<HASH_VALUE>"   OR  "http(s)://pixel.everesttech.net/px2/<NUMERIC_ID>?"  AND the tag contains the URL parameter  "sid=")  THEN check to see if the URL parameter  "cs=0" or "cs=1" exists, and if not recommend that  "cs=1" be added to those pixels so that the audience match rates can improve.|Add the URL parameter  "cs=1" to your Advertising Cloud pixels so that DSP Syncing can occur, which increases audience match rates.  This can most easily be accomplished with the Advertising Cloud Launch Extension.|
|DTM - pageBottom callback placement  Weight: 0   Additional information <br/> TEa9df69942f404055a64262889c8b21d3|Dynamic Tag Management requires the _satellite.pageBottom() function.  It is best practice that the tag be the last tag in the  <body>. If it's found within the  <body> tag, it has a chance of functioning, but as it is not best practice, it could function incorrectly or with unexpected or undesired results.|Add the inline script immediately prior to the closing  </body> tag to ensure proper DTM functionality.|
|Experience Cloud ID Service - Use only one AdobeOrg  Weight: 0   Additional information|In a normal MCID implementation, a single AdobeOrg should be used.|Validate that multiple AdobeOrg IDs exist for this implementation.|
|Target - Content in mboxDefault  Weight: 0   Additional information|Content should exist in mboxDefault when using at.js.|Verify that the content is available.|





![](assets/space.png)

## Configuration {#configuration}

This reference provides more information about the tests Auditor performs for configuration. 

Auditor evaluates the tags against other rules and recommended best practices.

|Test|Criteria|Recommendation|
|--- |--- |--- |
|Advertising Cloud - Conversion names use only alpha-numeric characters  Weight: 3|The  ev_conversion_property_name parameter should only contain numeric and decimal values EXCEPT for " ev_transid" parameter (the  ev_transid value can contain text or numeric values)  Look for  everesttech.net pixels that contain a URL parameter starting with  ev_.  Example:   http://pixel.everesttech.net/1180/t?ev_page_load=1&ev_revenue=$12&ev_transid=1hf74i47|Make sure your transaction property parameters only contain numeric and decimal values.   Warning:  Any other value types might cause data loss.|
|Advertising Cloud - Conversion names use URL-safe characters  Weight: 3|Conversion property names should not contain an ampersand or question mark.   Example:   http://pixel.everesttech.net/1180/t?ev_revenue&order=12&ev_transid=|Make sure transaction property parameters do not contain a non-encoded ampersand or question mark. These break the URL format.   Warning: Property parameters that contain a non-encoded ampersand or question mark, (for example:  ev_formComplete?=1 or  ev_formComplete&Submit=1), might result in data loss.|
|Advertising Cloud - Transaction ID Implemented Correctly  Weight: 1|The property name  ev_transid= should not be empty.  Example:   http://pixel.everesttech.net/1180/t?ev_page_load=1&ev_revenue= 12& ev_transid=|The property name  ev_transid= should not be left without a value ( ev_transid=). If this is left without a value, there could be transaction data loss. Assign a value to the  ev_transid= or remove the parameter from the pixel.|
|Analytics - Instantiated in DOM  Weight: 5   Additional information|The Adobe Analytics code is either not installed or failing to execute. Returns 0 when no analytics code is found web page.|Verify that the Analytics tag is implemented on the page and is not blocked by subsequent script activities.|
|Analytics - Instantiated once  Weight: 5   Additional information|The Adobe Analytics code was detected more than once on the page. . Returns 0 when no analytics code is found web page.|Make sure there is only one Analytics tag on the page.|
|Analytics - Latest version  Weight: 3   Additional information|Your pages are not running the latest version of the Analytics code library. Code libraries that power Experience Cloud technologies are constantly being updated and tweaked in order to take advantage of performance improvements and provide the latest features. Returns 0 when no analytics code is found web page.|Install the latest version of the Analytics library.|
|DTM - Self-Hosted  Weight: 4   Additional information|The DTM library is being hosted on Adobe's Akamai instance at  assets.adobedtm.com.   Self-hosting is the recommended approach for loading DTM because it provides greater control of website performance through cache control, reducing third-party script dependencies, and greater control of the publishing process. The DTM libraries can be hosted and managed through your own web hosting or CDN.|Self-hosting is the recommended approach for loading DTM on a page. Although DTM hosting via the Akamai CDN works in most cases, self-hosting improves page performance.|
|DTM - Third-party tags load asynchronously after DOM ready  Weight: 3   Additional information|To strike a balance between a good user experience and collecting accurate data, 3rd party tags should be triggered at DOM ready. This will ensure that those tracking scripts execute while not impacting site functionality.|Resolve this issue by adjusting all rules that execute 3rd party pixels to fire at DOM Ready.|
|Experience Cloud ID Service - Latest Version  Weight: 2   Additional information|Your pages are not running the latest version of the Visitor ID Service code library,  visitorAPI.js. Code libraries that power Experience Cloud technologies are constantly being updated and tweaked in order to take advantage of performance improvements and provide the latest features.|Install the latest version of the Visitor ID service library.|
|Target - Latest version  Weight: 2   Additional information|Your pages are not running the latest version of the Target code library. Code libraries that power Experience Cloud technologies are constantly being updated and tweaked in order to take advantage of performance improvements and provide the latest features.|Install the latest version of the Target library.|
|Target - mboxDefault precedes mboxCreate   Weight: 5   Additional information|The proper use of  mboxCreate looks similar to this:    <div class="mboxDefault"><!-Customer content--></div><script>mboxCreate('myMboxName')</script>|Be sure to include a  <div class="mboxDefault"></div> tag before invoking  mboxCreate(). at.js will not add one for you.|
|Target - Valid DOCTYPE  Weight: 5   Additional information|An invalid DOCTYPE was detected. No mboxes will be fired in this scenario.  For at.js, the DOCTYPE must be in Standards mode or Target will not work.|Update the DOCTYPE on the page.|


![](assets/space.png)

## Tag consistency {#tag-consistency}

This reference provides more information about the tests Auditor performs for tag consistency. 

Auditor evaluates whether the tags are consistent across URLs.

|Test|Criteria|Recommendation|
|--- |--- |--- |
|Analytics - Consistent code version   Weight: 5   Additional information|More than one version of the Analytics code was found.|Replace all instances of Analytics with the current version.|

|  |
|---|

![](assets/space.png)

## Tag presence {#tag-presence}

This reference provides more information about the tests Auditor performs for tag presence. 

Auditor evaluates whether the tag exists, and whether it's in the right place in your page code, and so on. 

|Test|Criteria|Recommendation|
|--- |--- |--- |
|Advertising Cloud - Code presence  Weight: 5|The Advertising Cloud tag is not available in the DOM.|Implement the Advertising Cloud tag using the Advertising Cloud Launch Extension.|
|Advertising Cloud - Segment Pixel Implemented  Weight: 5|Upgrade your Advertising Cloud segment pixels to the new Advertising Cloud image-only tags. Using the deprecated AMO segment tags can result in data loss.|Implement the Advertising Cloud segment pixel using the Advertising Cloud Launch Extension.|
|Analytics - Loaded in DOM  Weight: 5   Additional information|The Adobe Analytics tag was not detected.|Install the latest version of Analytics.|
|DTM - Library loaded  Weight: 5  Additional information: DTM Troubleshooting - Add header and footer code|A global _satellite object was not found in the DOM. Dynamic Tag Management is either not installed or failing to execute.|Verify that the DTM library is implemented on the page and is not blocked by subsequent script activities.|
|DTM - One embed code  Weight: 5   Additional information|Production sites should only load one DTM library.|Verify that only the production library is loading on the page.|
|DTM - pageBottom callback exists in <body>  Weight: 5   Additional information|The  _satellite.pageBottom() callback was not found within the  <body> of the page, which is required by Dynamic Tag Management.  This test fails if the  pageBottom call isn't found at all on the page, or if it's in the  <head> tag (or some other unexpected location). It will only pass if  pageBottom is found somewhere within the  <body> tag. If it's not on the page at all, it won't function and the other two  pageBottom tests will also fail.|Add the inline script immediately prior to the closing  </body> tag to ensure proper DTM functionality.|
|DTM - pageBottom tag fired  Weight: 5   Additional information|The DTM  pageBottom tag was not detected.  This could occur if the call is within an  if statement that results in something similar to  if (false) {_satellite.pageBottom()}. So, while it might exist and be correctly placed, the tag still might not fire.|Install the DTM  pageBottom call on every page.|
|Experience Cloud ID Service - Cookie presence  Weight: 5   Additional information|The  AMCV_ cookie was not found. You must instantiate a visitor object from the  VisitorAPI.js code.|If this is a DTM implementation, verify that the AdobeOrg ID is properly entered into the MCID tool.|
|Experience Cloud ID Service - MID value present  Weight: 5   Additional information|The mid value was not found in the  AMCV_ cookie.|Test again to check for any MCID API latency. If the condition persists, contact Adobe Customer Care.|
|Experience Cloud ID Service - Should be installed  Weight: 5   Additional information|The Experience Cloud ID Service code was not found. The ECID is highly recommended to ensure you get the most value out of your Experience Cloud solutions and is critical to ID management across EC solutions.|Please install the most recent version of MCID.|
|Target - Library loaded in <head>  Weight: 4   Additional information |The Target library should be loaded in the  <head> tag.|Check to be sure that the Target library is loaded in the  <head> tag.|

