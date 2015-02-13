---
title: Webhooks Integration Guide
layout: default
section: worker
breadcrumbs:
  - ['Integrations', '/integrations']
---

Webhooks are used with IronWorker to trigger a worker based on an event. This guide is specific to the webhook generated by IronWorker when a task errors so you can be notified or trigger a responsive action.

<h2 id="start">Getting Started</h2>
To use the Webhook integration, you'll need an endpoint where the webhook can POST. A great tool for testing HTTP endpoints is <a href="http://requestb.in/">requestb.in</a>. Select 'Create a Request Bin' to generate a temporary webhook uri. You'll need this link for the Iron.io HUD.

<img src="/images/worker/integrations/webhooks_uri.png" alt="Webhook URI">

<h2 id="uri">Enter Webhook URI</h2>
With your webhook URI, head over to the Iron.io HUD. Navigate to your Profile and select the Integrations menu. Select the 'Add' button for Webhooks and copy the link in the field. Selecting 'Activate' will associate the uri.

<img src="/images/worker/integrations/webhooks_auth1.png" alt="Webhooks">
<img src="/images/worker/integrations/webhooks_auth2.png" alt="Webhooks Auth">
<img src="/images/worker/integrations/webhooks_auth3.png" alt="Webhooks Auth">

<h2 id="activate">Activate the Webhooks Integration</h2>
Once you have associated the webhook uri with Iron.io, you can activate the integration for a specific project. Selecting the Integrations icon (plug), will display a list of services you have authenticated with. Find Webhooks and toggle the switch button on to activate the integration.

<img src="/images/worker/integrations/webhooks_activation1.png" alt="Webhooks Activation">
<img src="/images/worker/integrations/webhooks_activation2.png" alt="Webhooks Activation">

<h2 id="Test">Test the Integration</h2>
With the webhook uri associated and activated, IronWorker tasks that error will trigger the webhook. To test, write, upload, and run a simple task that you know will generate an error. Once complete, refresh the Request Bin url to inspect the worker webhook.

<img src="/images/worker/integrations/webhooks_requestbin.png" alt="Webhooks Request Bin">