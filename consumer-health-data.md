---
layout: default
title: Consumer Health Data Privacy Policy
permalink: /consumer-health-data/
version: "1.0"
effective: 2026-07-29
updated: 2026-10-07
applies: Washington State consumers
description: CPR360's standalone consumer health data policy under Washington's My Health My Data Act.
---

> **Name change (2026-09-19):** the app formerly called *HeartHealth* is now **CPR360**. That rename changed only the product name, not this document's substance. The URLs of these pages are unchanged.

> **Correction (2026-10-07):** an earlier version of this page said CPR360 does
> not collect precise location. That was wrong. The app rounds your location to
> about 11 metres, and that is still *precise location information* as this law
> defines it. The app's behavior has not changed; this page now describes it
> correctly. The page also now names every recipient of location data, including
> your phone's own map and geocoding services, and covers CPR360 on Android.

This policy explains how CPR360 collects, uses, and shares **consumer health
data** as defined by Washington's My Health My Data Act (MHMDA, RCW 19.373). It is
a standalone policy, separate from our general
[Privacy Policy]({{ site.baseurl }}/privacy/). Where the two differ for Washington
consumers, this policy controls for consumer health data.

## The categories of consumer health data we collect

**Precise location information, rounded to about 11 metres.**

MHMDA's enumerated example of consumer health data is *precise location
information* that could reasonably indicate a consumer's attempt to acquire or
receive health services or supplies. The law defines precise location as
location accurate to within a radius of 1,750 feet (RCW 19.373.010).

Before your position leaves your device, the app rounds it to a grid of about 11
metres. We never receive, transmit, or store anything finer, whether for the AED
search, the proximity check, or an AED you register. But 11 metres is far inside
1,750 feet, so **the location CPR360 collects is precise location information as
MHMDA defines it.** We treat it as consumer health data because CPR360 helps you
find a nearby AED (an automated external defibrillator).

This is the only category of consumer health data we collect. We do not collect
health conditions, diagnoses, treatments, medications, vital signs, biometric
data, or any information about health care you have sought or received.

## The purpose of collection and how the data is used

Your location is used **to find AEDs near you**, and to confirm you are actually
near an AED when you verify one is still there or report one missing. The app
sends the rounded latitude/longitude and gets back the nearby results. Apart from
the AEDs you register and the AED checks and reports you choose to make, we don't
build a history of where you go.

If you tap "Call 911 + Alert Contacts" on the emergency screen, the app also puts
your rounded location, and the street address looked up for it, into the text
your phone's messaging app sends to the contacts you chose. That text is sent by
your phone and does not pass through us.

When you choose to register an AED, the location you submit becomes part of that
AED's public map pin. That is the purpose of registering it.

We do not use consumer health data for advertising, profiling, or any form of
targeting. The CPR metronome, voice guidance, and the Learn lesson do not use
location. On the emergency screen, location is used only for the emergency text
described above.

## The legal basis for collection

We collect and use this data because it is **necessary to provide a product or
service that you have requested** — RCW 19.373.030(1)(a)(ii). When you open the
AED finder, you are asking the app to find defibrillators near you; that request
cannot be answered without your location.

We rely on that basis rather than on consent. Your device's location permission
prompt is how the app obtains technical access to location — it is not, and we do
not treat it as, MHMDA consent, because an operating-system permission dialog is
not a specific, informed, opt-in authorization for health-data processing.

You can stop the collection at any time by turning off location permission for
CPR360 in your device settings. The AED finder will then be unable to search
around you.

## The categories of consumer health data we share

**We do not sell consumer health data.** We have never sold it and we do not share
it for advertising or targeting.

Location goes to these recipients, and only as needed for the feature you are
using:

- **Our database and hosting provider (Supabase), a processor.** It runs the
  nearby-AED search and stores the location of AEDs you register. It acts on our
  documented instructions and may not use the data for its own purposes.
- **Your phone's built-in geocoding service: Apple on iPhone and iPad, Google on
  Android.** It receives the rounded coordinates and returns a street address.
  This happens for the emergency text, for registering an AED, and when you take
  an AED photo. It also receives any ZIP code you type to browse the map. These
  services are part of your phone's operating system. Apple and Google run them
  under their own privacy policies, not as our processors.
- **The map component (Apple Maps on iPhone and iPad; the Google Maps SDK on
  Android).** It draws your "you are here" dot on the AED map using your phone's
  own location services (Core Location, or Google Play services on Android). That
  position is not rounded, and CPR360 never receives it. Google documents what
  the Maps SDK itself collects
  [here](https://developers.google.com/maps/documentation/android-sdk/play-data-disclosure).
- **The contacts you choose,** through the emergency text your own phone sends,
  only when you tap "Call 911 + Alert Contacts".

**We have no affiliates.** No entity under common ownership or control with
CPR360 receives consumer health data, because no such entity exists.

## Your rights

If you are a Washington consumer, you have the right to:

- **Confirm and access** — confirm whether we are processing your consumer health
  data, and access it, including a list of all third parties with whom we have
  shared it.
- **Withdraw** — withdraw from our collection and use of your consumer health
  data. Turning off location permission takes effect immediately; you may also
  ask us in writing.
- **Delete** — request deletion of your consumer health data. We will delete it
  from our records and notify our processors of the request.

Because we do not retain a location history, apart from the locations of AEDs you
register (which are part of the public map), in most cases there is little or no
stored consumer health data to return or delete. We will tell you plainly if that
is the case rather than sending an empty file.

**How to make a request.** Email
[hearthealthdata@gmail.com](mailto:hearthealthdata@gmail.com) with "Washington
consumer health data" in the subject line.

**Our response time.** We will respond within **45 days** of receiving your
request. If we need more time, we may extend once by a further **45 days**, and we
will tell you why before the first period ends.

**If we deny your request — appeal.** You may appeal in writing by replying to our
response, or by emailing the same address with "Appeal" in the subject line. We
will respond to an appeal in writing within 45 days, explaining the reasons for
our decision. If we deny the appeal, we will provide you with a method to contact
the Washington State Attorney General.

**Complaints.** You may submit a complaint to the Washington State Attorney
General at any time: <https://www.atg.wa.gov/file-complaint>.

## No geofencing around health facilities
Consistent with RCW 19.373.080, CPR360 does not use any geofence around a
health-care facility to identify or track consumers, collect data from them, or
send them messages or advertising based on their proximity to such a facility.

## Changes to this policy
If we make a material change to how we collect, use, or share consumer health
data, we will obtain your consent before the change applies to data already
collected, as MHMDA requires. The version number and effective date at the top of
this page always reflect the current version.

## Contact
[hearthealthdata@gmail.com](mailto:hearthealthdata@gmail.com) — put "Washington
consumer health data" in the subject line.

*Retention, security, international transfer, and breach-notification practices
are described in our general [Privacy Policy]({{ site.baseurl }}/privacy/); this
policy is deliberately limited to what MHMDA requires.*
