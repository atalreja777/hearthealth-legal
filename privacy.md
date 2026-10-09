---
layout: default
title: Privacy Policy
permalink: /privacy/
version: "1.0"
effective: 2026-07-29
updated: 2026-10-07
description: How the CPR360 app collects, uses, and stores data.
---

> **Name change (2026-09-19):** the app formerly called *HeartHealth* is now **CPR360**. That rename changed only the product name, not this document's substance. The URLs of these pages are unchanged.

CPR360 helps bystanders respond to cardiac emergencies. We collect as little
as possible and keep your most sensitive data on your device. This policy
describes how the app handles data.

> **Washington residents:** consumer health data is covered by a separate
> [Consumer Health Data Privacy Policy]({{ site.baseurl }}/consumer-health-data/).

> **Update (2026-10-07):** this policy now covers CPR360 on **Android (Google
> Play)** as well as iPhone and iPad. It adds what changes on Android — Google
> sign-in, the Google Maps map, and Android's notification and secure-storage
> behavior. It also describes some existing practices more fully: AED evidence
> photos, address lookups, anonymous usage events, and exactly what is kept
> after deletion (see [Delete Your Account]({{ site.baseurl }}/delete-account/)).
> None of these is new behavior on iPhone or iPad.

## Emergency contacts stay on your device
The emergency contacts you add are stored only on your device, encrypted with the
operating system's secure keystore (the iOS Keychain on iPhone and iPad; a key
held in the Android Keystore on Android), and are never uploaded to our
servers. When you tap "Call 911 + Alert Contacts", your phone's own messaging app
sends them a text — we never see it, and we never store your contacts' names or
phone numbers.

## Location
The app uses your device location for one purpose: **finding AEDs near you**, and
confirming you are actually near an AED when you verify or report one. If you tap
"Call 911 + Alert Contacts", the app also puts your rounded location in the
text your phone's messaging app sends to your contacts. That message doesn't
pass through us.

**We round your location to about 11 metres before it leaves your device.** App
stores classify a position this fine as *precise* location, and we describe it
that way too. We never receive, transmit, or store anything finer, whether for the
AED search, the proximity check, or an AED you register. We send that rounded
latitude/longitude to run the search. Apart from the AEDs you register and the AED
checks and reports you choose to make, we don't keep a history of where you go.
Location is used only while you are actively using these features.

When you register an AED, the location you submit is stored as part of that AED's
public map pin — that is the point of registering it.

**The map and street addresses come from your phone's platform.** On iPhone and
iPad, the AED map is drawn by Apple Maps. On Android, it is drawn by the
**Google Maps SDK**, a Google component built into the Android app. The map's
"you are here" dot comes straight from your phone's location services: Core
Location on iPhone and iPad, Google Play services on Android. That position is
not rounded, and CPR360 never receives it. When the map loads,
Google receives what it needs to serve it — your device's IP address, device
details such as model and OS version, a Maps-specific pseudonymous identifier,
crash data from the map component, and how you pan and zoom the map — and uses
it under [Google's Privacy Policy](https://policies.google.com/privacy) (Google
documents this
[here](https://developers.google.com/maps/documentation/android-sdk/play-data-disclosure)).
To show a street address for a location, or to look up a ZIP code you type, the
app uses your phone's built-in geocoding service (Apple's on iPhone and iPad,
Google's on Android), which receives the rounded coordinates or the ZIP code.

See the separate
[Consumer Health Data Privacy Policy]({{ site.baseurl }}/consumer-health-data/)
for how location is handled for Washington residents.

## AED registry (community-contributed)
AEDs you register — including the location, access details, and any photos — are
stored in our database and shown publicly to other users so they can find an AED
in an emergency. Please do not upload photos that contain people or private
information.

**Checking an AED also takes a photo.** Tapping "Still here" or reporting an AED
missing asks you for a live photo of it, as evidence you are there. These
evidence photos are **not public**: they are stored privately and can be seen
only by our moderators.

**Photos are stripped of their metadata before they are uploaded.** A photo file
normally carries hidden information — the exact GPS coordinates where it was
taken, a timestamp, and details about your device. Because AED photos are public,
the app re-encodes every photo on your device before sending it — AED photos and evidence
photos alike — which discards all of that. What reaches us, and what other people
can see, is the picture only.
The pin's own coordinates are the rounded (~11 m) ones described above.

## Accounts
The core features — CPR guidance, the metronome, and finding an AED — work without
an account or a profile. You only sign in to register a new AED, verify one,
report one as missing, or take part in the Community. You sign in with **Apple**
(on iPhone and iPad) or **Google** (where offered, including on Android). We never
see your Apple or Google password.

When you sign in we store an account record and a contributor profile so your
contributions can be attributed and moderated. The account record holds what
your sign-in provider shares with us: your email address (with Apple, possibly a
private relay address if you chose *Hide My Email*), and your name and, for
Google, a link to your profile picture, if the provider shares them. The display
name other people see in the Community is the one you choose in the app.

One clarification, because "no account" can be misread as "nothing identifies this
device": our push-notification provider's software starts when the app launches
and assigns this installation a device-level identifier, before and regardless of
any sign-in. See **Notifications** below.

## Community posts and comments
If you join the Community (ages 13+), the posts, comments, and reactions you
create — and the display name you choose — are stored on our servers and shown
publicly to other users. Community content is text and links only; you cannot
upload photos to the Community. Please don't post anything you wouldn't want to be
public, and don't share other people's private or medical information. Anything
can be reported, or its author blocked. When content is reported or removed we
keep a moderation record (what was reported and the action taken) for as long as
needed to keep the Community safe.

When you delete one of your own posts or comments, it is hidden from everyone
immediately, but a copy is kept on our servers for moderation and safety. You can
ask us to erase it permanently — see
[Delete Your Account]({{ site.baseurl }}/delete-account/).

## Automatic AI screening of Community text
Before a post, comment, or report appears in the Community, its text is checked
automatically by an AI moderation service that CPR360 runs on **Cloudflare
Workers AI**, a third-party provider. **Only the text you submit is sent** — never
your name, your account, or your location.

Cloudflare's published Workers AI data-usage documentation states:

> Cloudflare does not use your Customer Content to (1) train any AI models made
> available on Workers AI or (2) improve any Cloudflare or third-party services

and separately:

> Cloudflare does not make your Customer Content available to any other
> Cloudflare customer.

("Customer Content" is Cloudflare's own defined term for what we send them —
here, your submitted text. Source:
<https://developers.cloudflare.com/workers-ai/platform/data-usage/>, last updated
21 April 2026.)

The underlying models are third-party models supplied through Cloudflare and
carry their own licenses.

If the check cannot run, your post is held unpublished until it can be looked at.

**We ask your permission for this separately.** Before you can take part in the
Community, CPR360 asks for this specific permission on its own screen, with
its own button — it is not bundled into accepting the Terms. Nothing you write is
sent for screening until you grant it.

Declining costs you nothing else: the CPR metronome, voice guidance, the AED map,
and Learn all keep working exactly as before. Only the Community stays closed,
because screening happens before publication and there is no path that skips it.
You can change your answer any time while signed in, under **Profile → Settings →
Community AI screening**,
in either direction. If we ever change the processor, what is sent, or why, we
will ask again rather than rely on the permission you gave for the old
arrangement.

## Deleting your account
You can delete your account any time in the app, under **Profile → Settings →
Delete account**, or — without the app — by emailing us. Our
[Delete Your Account]({{ site.baseurl }}/delete-account/) page has both routes
and the full list of what is deleted and what is kept.

Deleting removes your personal account data — your login, contributor profile,
notification record, reputation record, reactions, and block list. If you signed
in with Apple, the app also revokes CPR360's Sign in with Apple token. If you
signed in with Google, CPR360 holds no Google token on its servers, so there is
nothing for us to revoke; you can remove CPR360 from your Google Account's
third-party connections at any time.

Some things intentionally survive, in anonymized form — no longer linked to you:

- **AEDs you added**, and their photos, stay on the public map so others can still
  find a defibrillator in an emergency.
- **Your "Still here" checks and missing reports**, with their private evidence
  photos, stay as part of each AED's history.
- **Community posts and comments you wrote** stay, shown as "[deleted]", so
  conversations others took part in remain intact. Posts and comments you deleted
  earlier also remain stored, hidden. Ask us if you want them erased for good.

Moderation records are retained as needed for safety. Irreversible anonymization
is used so we can satisfy erasure requests while keeping public-safety data and
community threads usable.

## Notifications
**This version of CPR360 does not send you push notifications.** The app never
asks for notification permission — on iPhone, iPad, or Android 13 and later, that
means none can be shown. (Android 12 and earlier allow notifications by default
without asking; we still send none. The only notification the system can send is
an internal alert to our own Community moderators.)

What does happen: our push provider's software (OneSignal) starts when the app
launches and registers this installation, creating a **device-level identifier**.
If you sign in, that identifier is associated with your account so that a future
version could deliver notifications to the right person. OneSignal also records
basic app-usage events, such as when the app is opened. This is why our App Store
and Google Play privacy disclosures list a device identifier and a user
identifier — the identifiers exist even though no notification is ever sent.

Signing out or deleting your account removes the association from this
installation; we do not currently erase OneSignal's own copy of that record.
Deleting the app removes the identifier from your device.

## Service providers
We use a small number of processors:

| Provider | What it does | What it receives |
|---|---|---|
| **Supabase** | Database, sign-in, AED photo storage | Account record, AED pins and photos, Community content, and your location (rounded to ~11 m, which app stores classify as precise) used to run the nearby-AED search |
| **Cloudflare** | Workers AI screening of Community text | The submitted text only |
| **OneSignal** | Push infrastructure (dormant — see Notifications) | Device identifier, basic app-usage events, and your user id once signed in |
| **Sentry** | Crash and error reporting | Crash and error reports, which may include device model and OS version. We configure Sentry not to receive identity, request, or location details. Also a few anonymous usage events: for example, that a CPR session started, its mode, a rough duration, and a compression count |
| **Apple / Google sign-in** | Signing you in, if you choose to | Apple or Google confirms who you are and shares your email with us, and depending on the provider your name and profile-picture link |
| **Google Maps SDK** (Android only) | Drawing the AED map | IP address, device details, a Maps-specific identifier, map crash data, and map interactions — used by Google under its own privacy policy |

These processors act on our instructions; Google additionally uses the Maps data
described above under its own privacy policy. We do not sell your data, and we have no
affiliates — no company under common ownership or control with us receives any of
it.

## How long we keep things
- **Emergency contacts** — on your device only, until you delete them or remove the app. Never on our servers.
- **Account and profile** — until you delete your account.
- **AED pins and photos**: shown while the pin is useful to the community. A pin taken off the map stays as a hidden record; we don't delete AED records or photos automatically. Anonymized, not deleted, when you delete your account.
- **AED checks, missing reports, and their evidence photos**: kept indefinitely, because we don't delete them automatically. They are anonymized when you delete your account.
- **Community posts and comments**: as above, retained and anonymized. Posts and comments you delete, or that moderators remove, are hidden from everyone but kept indefinitely, unless you ask us to erase yours.
- **Moderation records** — as long as needed for Community safety.
- **Location used for searching**: rounded to ~11 m, used to answer your request, and not stored as a location history.
- **Crash and error reports** — kept for a limited period under Sentry's retention schedule, then deleted.

## Security
Data in transit is encrypted with HTTPS/TLS. Emergency contacts are encrypted with
your device's secure keystore (iOS Keychain or Android Keystore). Server data sits behind per-user access rules that
restrict each account to its own records, and privileged keys are used only in
server-side functions, never shipped in the app.

No system is perfectly secure, and we don't claim otherwise.

## International transfers
Our providers operate globally, and Cloudflare, OneSignal, and Google in particular process
data across a distributed network that may route it outside your country. By using
the app you understand your data may be processed outside the jurisdiction where
you live.

## If there is a data breach
If a security breach affects your personal information, we will notify affected
users and any required authorities as the law directs, including Washington's data
breach notification statute (Ch. 19.255 RCW) where it applies.

## Donations
The Donate button opens the Gwyneth's Gift Foundation's own website in your
browser — a separate third-party site with its own privacy policy. We do not
process donations in the app and do not share your data with the foundation.
CPR360 is an independent project and is not affiliated with or endorsed by
Gwyneth's Gift Foundation.

## Children
The Community is limited to users aged 13 and older, and we ask for date of birth
before you can join. The rest of the app (CPR guidance, the metronome, finding an
AED) is general-audience. If we learn that a Community account belongs to someone
under 13, we remove the content and the account.

## What we don't do
We don't sell your data, we don't show ads, we don't store your phone number on our
servers, and we don't build a history of your movements, apart from the AEDs you
register and the AED checks and reports you choose to make. The CPR metronome and
voice guidance work fully offline. When you are online, the emergency screen sends
only the anonymous usage events to Sentry described above and, if you use the
emergency text, the address lookup described under **Location** — never your
identity or your contacts.

## Changes to this policy
We may update this policy. The version number and effective date at the top of
this page always reflect the current version. If we make a material change to how
we handle your data, we will say so in the app; where the law requires fresh
consent for a change, we will ask for it before the change applies to you.

## Governing law
CPR360 is operated from the United States. Except where a state privacy law
provides otherwise for residents of that state — such as Washington's My Health My
Data Act — this policy is governed by the laws of the Commonwealth of Virginia,
without regard to its conflict-of-laws rules.

## Contact
Questions about privacy, a privacy request, or content moderation? Email us at
[hearthealthdata@gmail.com](mailto:hearthealthdata@gmail.com). Put "Privacy" in
the subject line and we will route it accordingly.
