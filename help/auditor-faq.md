---
description: null
seo-description: null
seo-title: Auditor FAQ
title: Auditor FAQ
uuid: 4db0781a-b288-4ec2-97ff-410a8241a61d
---

# Auditor FAQ{#auditor-faq}

This article contains the answers to frequently asked questions about Adobe Experience Platform Auditor.

* [What is Auditor?](auditor-faq.md#section-c4a9bc8d8eef41598c27e0951a2518e4) 
* [Is my company eligible to use Auditor?](auditor-faq.md#section-f90094050d1e44929066a942833435cf) 
* [Which Adobe technologies does Auditor grade?](auditor-faq.md#section-52833b71c05448aaae508e6070a387f5) 
* [How many audits can I run?](auditor-faq.md#section-caac1e50ce1249aeba76308f3ef03fa0) 
* [What is crawled for an audit?](auditor-faq.md#section-6d068ed69ece4a1bb6d0c34454550c45) 
* [How long does an audit take?](auditor-faq.md#section-5086ae27ef1f4671a9d951348654633a) 
* [What information is provided in a report?](auditor-faq.md#section-752d6b82f6744a3182c4ce16ea6b5d3f) 
* [How actionable is that information?](auditor-faq.md#section-9308c1ea882048b781087ae6d2eee9f0) 
* [Can Auditor audit non-Adobe technology?](auditor-faq.md#section-f6e73c56083b4815bbf901296038bcd4) 
* [Can I whitelist my IP addresses to allow scanning pages...](auditor-faq.md#section-011e4f54c58140ffb93bedeb0745b6cc) 
* [Does Auditor use the same IP ranges as Observepoint?](auditor-faq.md#section-39512b156e194787981bdd572ff5b5a9)

## What is Auditor? {#section-c4a9bc8d8eef41598c27e0951a2518e4}

Auditor is a service of the Adobe Experience Cloud that was co-developed with ObservePoint, experts in validating digital implementations.

With Auditor, customers can scan up to 500 webpages at a time and receive a report that shows how to improve their Adobe Experience Cloud implementations so they receive the full value of their Adobe investment.

## Am I eligible to use Auditor? {#section-f90094050d1e44929066a942833435cf}

All Adobe Experience Cloud customer organizations are granted complimentary access to Auditor (as of May 1, 2018). Each user must consent to Adobe/ObservePoint terms of use in the Adobe Experience Cloud UI before accessing the functionality. To opt-out of the terms, please contact your Account Manager.

## How do I access Auditor? {#section-531ff85f94384831a89cbb4109549daf}

After logging in at [https://experiencecloud.adobe.com](https://experiencecloud.adobe.com), you can find Auditor by clicking on **[!UICONTROL Activation]** in the top navigation. You can also go directly to [https://auditor.adobe.com](https://auditor.adobe.com).

## Which Adobe technologies does Auditor grade? {#section-52833b71c05448aaae508e6070a387f5}

* Advertising Cloud DSP 
* Advertising Cloud Search 
* Analytics 
* DTM 
* Experience Cloud ID Service (formerly Marketing Cloud ID Service) 
* Target

The following Adobe solutions are not currently included in the test rubric. Support for these solutions is planned for future updates.

* Advertising Cloud Creative 
* Audience Manager 
* Campaign 
* Launch

## How many audits can I run? {#section-caac1e50ce1249aeba76308f3ef03fa0}

There is no limit to the number of audits you can run. Users are limited to one audit running at a time. An error occurs if you try to start an audit with the same settings as the one that's running.

## What is crawled for an audit? {#section-6d068ed69ece4a1bb6d0c34454550c45}

The ObservePoint technology currently crawls URLs that are found in document links. Links found in buttons, pagination widgets, and other such page elements are not crawled.

## How do I suggest new criteria for Auditor tests? {#section-926e6ef9225b4f0bb19c2927d634cd77}

You can submit test suggestions via the Auditor Community by clicking **[!UICONTROL Share Feedback]** on this page: [https://forums.adobe.com/community/experience-cloud/platform/core-services/activation-service/auditor](https://forums.adobe.com/community/experience-cloud/platform/core-services/activation-service/auditor)

## How long does an audit take? {#section-5086ae27ef1f4671a9d951348654633a}

There are many factors contributing to the time it takes for an audit to complete, including:

* Page load time

  The ObservePoint engine loads each page of the audit in a browser. The faster a page loads, the faster the audit completes. 
* Simultaneous connections

  Adobe Auditor uses a single connection to visit each page. Full ObservePoint accounts use as many as 10 engines at once. 
* Network silence

  After each page loads, the audit waits for a network silence of seven seconds before proceeding to the next page. If a page sends a lot of network requests that occur after the page loads, the wait will timeout after 60 seconds. 
* Page Retries

  If a page or tag cannot be found, the audit stores that URL and returns to it later in the audit. The audit will visit a page up to three times to make sure that the error was not caused by a transient issue. 
* Processing

  After an audit has run, all the data it has collected is processed and filtered through the rules. This processing time is significant, though it doesn't take as much time as the scan itself.

>[!NOTE]
>
>Adobe Auditor runs a single scan at a time. Full ObservePoint accounts can run many audits consecutively.

## What information is provided in a report? {#section-752d6b82f6744a3182c4ce16ea6b5d3f}

Each scan generates a report that shows what URLs were scanned, issues found on those webpages, and recommendations on how to correct the issues found.

Results from scans are broken out into three categories:

* Configuration 
* Tag Consistency 
* Tag Presence

In addition to these three categories, the report provides alerts containing information you should be aware of but that does not necessarily require immediate action.

The recommendations that come within these categories are then broken out into three additional categories:

* Highly Recommended 
* Recommended 
* Passed

## How actionable is that information? {#section-9308c1ea882048b781087ae6d2eee9f0}

All the recommendations given through Auditor are intended to help you take action to fix a problem with your implementation of Adobe Experience Cloud solutions, such as DTM or Target. To facilitate this, the Auditor team has worked extensively to provide very granular instructions on what needs to be done where. You can export a spreadsheet of all URLs scanned and all test results so you can pinpoint problem areas easily. Here is an example of one recommendation for a DTM implementation:

<table id="table_EE67775088344BDAA5126268072D6089"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><b>pageBottom callback last</b> </p> <p>A _satellite.pageBottom() function is required for a correct DTM implementation. Add the inline script immediately prior to the closing &lt;/body&gt; tag to ensure proper DTM functionality. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Can Auditor audit non-Adobe technology? {#section-f6e73c56083b4815bbf901296038bcd4}

No. However, ObservePoint’s full offering allows customers to audit and monitor all of your marketing tags and technologies. As an Adobe customer you have access to a complimentary trial account. To access your trial account visit [ObservePoint’s Auditor Page](https://www.observepoint.com/adobe-auditor/?utm_source=Adobe&utm_medium=Auditor&utm_campaign=Premium).

## Can I whitelist my IP addresses to allow scanning pages that are protected by a login? {#section-011e4f54c58140ffb93bedeb0745b6cc}

This functionality is currently unsupported without the full ObservePoint offering.

## Does Auditor use the same IP ranges as ObservePoint? {#section-39512b156e194787981bdd572ff5b5a9}

The crawling is performed by ObservePoint, so the same IP addresses are used.

See the [ObservePoint documentation](https://help.observepoint.com/articles/2312494-observepoint-whitelisting-and-proxy-list) for more details. 
