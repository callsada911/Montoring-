# Montoring-
one of the labs for motioning 
Task 1: Create a Cloud Monitoring workspace
Verify resources to monitor
Three VM instances have been created for you that you will monitor.

In the Cloud Console, on the Navigation menu (Navigation menu), click Compute Engine > VM instances. Notice the nginxstack-1, nginxstack-2 and nginxstack-3 instances.
Create a Monitoring workspace
You will now setup a Monitoring workspace that's tied to your Qwiklabs GCP Project. The following steps create a new account that has a free trial of Monitoring.

In the Google Cloud Platform Console, click on Navigation menu > Monitoring.

Wait for your workspace to be provisioned.

When the Monitoring dashboard opens, your workspace is ready.

Overview.png

Why is monitoring important to Google?

Google uses monitoring to ensure they have all the important metrics for reporting purposes to customers and the other interested bodies. The number of reports requires the collection and reporting to be both broad and deep.

Monitoring is important to ensure that Google complies with regulatory requirements defined by both government and industry security bodies.

It is at the base of site reliability which incorporates aspects of software engineering and applies that to operations whose goals are to create ultra-scalable and highly reliable software systems.

Task 2: Custom dashboards
Create a dashboard
In the left pane, click Dashboards > Create Dashboard.

For New Dashboard Name, type My Dashboard, and press Confirm.

Add a chart
Click Add Chart.
For Title, give your chart a name (you can revise this before you save based on the selections you make).
For Find resource type and metric, select VM Instance.
For Metrics, select a metric to chart for the Instance resource, such as CPU utilization or Network traffic.
Note: If you are getting a 'loading failed' error message, you might have to refresh the page.

Click Filter and explore the various options.

Click View Options and explore adding a Threshold or changing the Chart mode.

Click Save to add the chart to your dashboard.

Metrics Explorer
The Metrics Explorer allows you to examine resources and metrics without having to create a chart on a dashboard. Try to recreate the chart you just created using the Metrics Explorer.

In the left pane, click Metrics Explorer.
For Find resource type and metric, type a metric or resource name.
Explore the various options and try to recreate the chart you created earlier.
Not all metrics are currently available on the Metrics Explorer, so you might not be able to find the exact metric you used on the previous step.

Task 3: Alerting policies
What is not a recommended best practice for alerts?

Report all noise to ensure all data points are presented.

Customize your alerts to the audience need.

Use multiple notification channels so you avoid a single point of failure.

Configure alerting on symptoms and not necessarily causes.

Create an alert and add the first condition
In the left pane, click Alerting > Create Policy.
Click Add Condition.
For Find resource type and metric, select VM Instance.
If you cannot locate the VM Instance resource type, you might have to refresh the page.

Select a metric you are interested in evaluating, such as CPU usage or CPU Utilization.

For Condition, select is above.

Specify the threshold value and for how long the metric must cross this set value before the alert is triggered. For example, for THRESHOLD, type 20 and set FOR to 1 minute.

Click ADD.

Add a second condition
Click Add Condition.

Repeat the steps above to specify the second condition for this policy. For example, repeat the condition for a different instance. Click ADD.

In Policy Triggers, for Trigger when, click All conditions are met.

Click Next.

Configure notifications and finish the alerting policy
Click on dropdown arrow next to Notification Channels, then click on Manage Notification Channels.
A Notification channels page will open in new tab.

Scroll down the page and click on ADD NEW for Email.
Enter your personal email in the Email Address field and a Display name.
Click Save.
Go back to the previous Create alerting policy tab.
Click on Notification Channels again, then click on the Refresh icon to get the display name you mentioned in the previous step.
Now, select your Display name and click OK.
Click Next.
Enter a name of your choice in Alert name field.
Click Save.
Click Check my progress to verify the objective.
Create alerting policies

Task 4: Resource groups
In the left pane, click Groups > Create Group.

Enter a name for the group. For example: VM instances

In the Criteria section, type nginx in the value field below Contains.

Click DONE.

Click CREATE.

Review the dashboard Cloud Monitoring created for your group.

Task 5: Uptime monitoring
Select all valid targets for Cloud Monitoring uptime alert notifications.

SMS

EC2 service

3rd party service

webhook

Pub/sub

email

In the Monitoring tab, click on Uptime Checks.
Click Create Uptime Check.
Specify the following, and leave the remaining settings as their defaults:
Property	Value (type value or select option as specified)
Title	Enter a title then click Next
Protocol	HTTP
Resource Type	Instance
Applies To	Group
Group	Select your group
Check Frequency	1 minute
Click on Next to leave the other details to default and click Test to verify that your uptime check can connect to the resource.

When you see a green check mark everything can connect. Click Create.

The uptime check you configured takes a while for it to become active.

Click Check my progress to verify the objective.
