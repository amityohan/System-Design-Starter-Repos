# Raftly System Promise

## Scope

Raftly will provide a mobile-compatible fleet monitoring and dispatch API that exposes the latest reported truck locations, driver ratings and incident history, driver approval, and off-route alert configuration and breach intake. The dashboard can present location data on a map and the alert workflow can support push notifications once the integration details are agreed.

## Out of Scope

Driver-to-dispatcher chat, fuel-cost tracking, offline operation and synchronization, and dark mode are not part of this MVP.

## Critical Unknowns

- Which map provider will be used, and what location-update interval qualifies as "real-time"?
- Which push channel and recipients should receive off-route notifications?
- Does "work on mobile" mean a responsive web app or native apps?
- What measurable latency and availability targets define "really fast and reliable"?

## System Boundaries

- The API exposes fleet, driver, approval, and alert operations; it does not own telematics data collection.
- The telematics provider supplies location updates and posts geofence-breach webhooks.
- The client renders the dashboard and map; a selected notification service delivers push notifications.
