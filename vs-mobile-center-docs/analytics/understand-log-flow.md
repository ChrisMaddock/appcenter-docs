---
title: Log Flow Page
description: Help using the Log Flow Page on Mobile Center
keywords: mobile center, analytics
author: kpiteira
ms.author: kapiteir
ms.date: 01/20/2017
ms.topic: article
ms.assetid: be4ee0a0-cd06-486a-bef1-22b6ab5dc896
ms.service: mobile-center
---

# Log Flow Page

Log Flow will show you in real time what is being received by the backend.
The main goals are:
- Check the SDK is properly wired and our backend is receiving data, as you might do a microphone check: "Is this on?"
- Ensure the backend is receiving what the app is supposed to send

## General information
Log Flow will collect and display incoming data from the current day (in the UTC timezone). The data should appear withing a few seconds after it is sent by the device.
It is possible to view:
- Start of sessions
- The fact that a crash occured
- Events, including the event name and its properties

All data includes a subset of the _installation id_ which uniquely identifies devices and the time in local timezone at which the log was emited in the application

## "Is this on?"
The main use case of Log Flow is to check that "the SDK integration works". Data will appear within seconds there, so it's the best way to check whether your 1-line integration worked after the first run.

When doing a 1-line integration, you should expect a "STARTSESSION" with the session Id, everytime the app is started.

## Checking the data received
The other use case is to check that the Mobile Center backend receives exactly the events with the names and properties that are expected to send.

It is a good idea to check the SDK integration, and especially Events by going through all the features and actions that are instrumented, in order to check that Mobile Center properly receives what is expected.

## Key characteristics

- Data sent from the SDK with the correct configuration and App Secret, should appear within seconds into Log Flow
- Log Flow will load data from 12am UTC of the current day earliest, up to 100 data points
- It will automatically refresh every 3 seconds, and will load up to 100 data points.
- If more than 100 data points were generated by the application between 2 refreshes, then the UI will indicate the "break" with an icon