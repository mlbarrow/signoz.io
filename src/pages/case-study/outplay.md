---
title:  How Outplay uses SigNoz to improve their backend API response time by 35%
slug: outplay
image: /img/case_study/outplay-banner-min.jpg
authors: [pranay]

---
import { LiteYoutubeEmbed } from "react-lite-yt-embed";

# How Outplay uses SigNoz to improve their backend API response time by 35%

<head>
  <link rel="canonical" href="https://signoz.io/case-study/outplay/"/>
  <meta property="og:image" content="https://signoz.io/img/case_study/outplay-banner-min.jpg"/>
  <meta property="twitter:card" content="summary_large_image"/>
  <meta property="twitter:url" content="https://signoz.io/case-study/outplay/"/>
  <meta property="twitter:title" content="How Outplay uses SigNoz to improve their backend API response time by 35% | SigNoz"/>
  <meta property="twitter:description" content=""/>
  <meta name ="twitter:image" content="https://signoz.io/img/case_study/outplay-banner-min.jpg"/>


</head>

<div class="avatar">
  <a
    class="avatar__photo-link avatar__photo avatar__photo--lg"
    href="https://twitter.com/pranay01">
    <img
      alt="Pranay Profile"
      src="/img/authors/pranay_profile_pic.webp" />
  </a>
  <div class="avatar__intro">
    <div class="avatar__name">Pranay Prateek</div>
    <small class="avatar__subtitle">
      Maintainer, SigNoz
    </small>
  </div>
</div>

<br />
<br />


*I sat down with Vijay, Technical Lead  at <a href = "https://outplayhq.com" rel="noopener noreferrer nofollow" target="_blank" >Outplay</a> to understand how they use SigNoz at Outplay. Here’s a few snippets from our conversation (edited for legibility)*

![Outplay Case Study](/img/case_study/outplay-banner.webp)

### What were the business problems you were trying to solve with SigNoz?

Main area of focus was to have APM metrics on the application to understand the performance and bottlenecks for optimisation. Signoz provided us the capabilities along with monitoring of API to get alerted in case API failures.

### Any specific use cases?

Basically, we had to find the application API whose performance needs to be optimised? Is it the back end or the database query? What kind of queries which needs tuning? 

These were the questions we wanted to figure out from an APM.

### What's the business impact?
Outplay is used by salespeople to reach their prospects and close deals. Salespeople are always under pressure to hit their targets and time is money. The more efficient they are, the more they can engage with more prospects. If the application is down, their productivity is impacted and since Outplay also supports multiple CRMs integrations, automatic data flow would also be impacted.

### How did SigNoz help?
We migrated our entire workload from EC2 to Kubernetes, so that scaling would be easier. Then we started optimising the backend, that's when SigNoz helped us. We started getting a list of APIs and database call times which we started optimising. We are able to load more users now with the same infra and the backend response time is 35% faster. We handle peak load 3000 active concurrent connections currently.

Generating traces for background services and DB calls to understand and improve their services. Also, track all the DB call traces from background workers to check for potential bottlenecks.
We use traces in the dev and staging environment to find any performance issues. The QA team also uses APM tools in the staging environment to check if any APIs are taking a lot of time or finding any anomalies.

### How did you leverage SigNoz to improve performance for your app?

So, we wanted to analyze application metrics and how the DB is performing, what all things can be made to improvise the application.

First thing, we did was we collected the entire metrics. We took the top ten endpoints where the DB tuning was needed, and using the APM tool, we pointed out the exact points or the exact stored procedures, which needs to be optimized.

Optimisation and DB tuning gave very good results to our platform and is now able to handle higher loads.

That was one of the major reason. A second thing was we wanted to make this as a complete process where we test most of our things on staging. We have a deployment of SigNoz on staging environment as well. So that we find the issues as early as possible before putting into production. Because if there is an issue on staging, it will be a bigger one in production.

We have test engineers in our team go to the SigNoz platform on staging environment and they verify if any calls is taking more than the defined limits.

<br />
<LiteYoutubeEmbed id="nh79MBqwc0w" mute={false} />
<br />
<br />

### Why did you choose SigNoz over other solutions?

We were also checking out another tool, Tempo from Grafana. But the number of components inside Tempo is huge.

We wanted to keep the number of components as small as possible. We don't want to deploy a lot of components. That increases the complexity and managing systems with many moving parts can be messy. You would need separate people to handle the issues in maintaining such systems.

We needed something which just works after deploying and doesn't need continuous maintenance.
<br />
<br />

<LiteYoutubeEmbed id="diaVE3TT2Ck" mute={false} />

<br />
<br />

### Any advice for teams implementing observability systems for the first time

So, first thing is make your platform. as simple as possible. Don't bring in lot of components as that would become a mess. Failure of one component can bring down your whole observability stack.


Try to have back end storage for storing the observability data. Something like s3, so that you don't have to think about loosing your telemetry data.

SigNoz provides that option where you can connect your S3 to ClickHouse and configure it in such a way that after 80% of disk storage is used, it automatically shifts data to s3.

Now with open telemetry becoming a standard, which supports all kinds of programming languages, you don't have to worry about how we are exporting the data. The devops teams should focus on the right tools to store the data and visualising it.

<p>&nbsp;</p>

---

Thank you for taking out the time to read this case study. If you have any feedback or want to share your story using SigNoz, please feel free to reach out to `hello@signoz.io` with `Case Study` as subject.

Sharing stories of how different teams are using SigNoz helps the community in learning different use cases and problems SigNoz can solve and also showcases how you are solving issues in a unique way.

Feel free to join our slack community and say hi! 👋

[![SigNoz Slack community](/img/blog/common/join_slack_cta.png)](https://signoz.io/slack)
