---
title: "Set up PagerDuty"
chapter: false
weight: 53
pre: "<b>5.3 </b>"
---

Next we will set up your PagerDuty Developer Platform. If you do not yet have a developer platform, you can sign up and get a free developer platform instance [here](https://developer.pagerduty.com/sign-up/).

{{% notice info %}}
PagerDuty provides many ways for developers to integrate with their platform. You can learn more through their [developer documentation](https://developer.pagerduty.com/docs/get-started/getting-started/).
{{% /notice %}}

1. In your PagerDuty, go to **Services** > **Service Directory**.
{{% notice info %}}
A service may represent an application, component, or team you wish to open incidents against. Services contain integrations, as well as determine the routing and incident settings for events triggered by integrations associated with the service.
{{% /notice %}}
2. We will create two services: (1) Xray Vulnerabilities and (2) JFrog Pipelines Events. Click **+ New Service **.
3. Name the service _Xray Vulnerabilities_ and click **Next**.
   ![New PD Service](/images/newpdservice.png)
4. Choose **Generate an Escalation Policy** and click **Next**.
   ![New PD Escalation](/images/newpdescalation.png)
5. Choose **Intelligent** for the **Alert Grouping** and click **Next**.
   ![New PD Alert](/images/pdalertgrouping.png)
6. For **Integrations**, search for _JFrog Xray + PagerDuty Notifications_ and click **Create Service**.
   ![New PD Alert](/images/pdxray.png)
7. Copy the **Integration URL** for later.
   ![New PD Xray Key](/images/pdxraykey.png)
8. Let's now create a service for JFrog Pipelines events. Click **+ New Service **.
9. Name the service _Pipelines Events_ and click **Next**.
10. Choose **Generate an Escalation Policy** and click **Next**.
11. Choose **Intelligent** for the **Alert Grouping** and click **Next**.
12. For **Integrations**, search for _JFrog Pipelines Changes_ and click **Create Service**.
   ![New PD Alert](/images/pdpipelines.png)
13. Copy the **Integration Key** for later.
   ![New PD Pipeline Key](/images/pdpipelinekey.png)
14. An API token is also required for the JFrog Pipelines + Pagerduty Notifications integration.
15. Click on your avatar in the top right and **My Profile**.
   ![MyProfile](/images/MyProfile.png)
17. Click on the **User Settings** tab and inside the **API Access** section click on **Create API User Token**.
   ![APIToken](/images/APIToken.png)
18. Copy the token. We will use this when creating the integration in JFrog Pipelines for PagerDuty.
    
Congratulations! You have set up PagerDuty with the JFrog Xray and Pipelines integrations.