---
layout: default
title: Privacy Policy
permalink: /privacy/
version: "1.0"
effective: 2026-07-29
description: How the CPR360 app collects, uses, and stores data.
---

> **Name change (2026-09-19):** the app formerly called *HeartHealth* is now **CPR360**. Only the product name changed — this document, its version, and its effective date are otherwise unaffected. The URLs of these pages are unchanged.

CPR360 helps bystanders respond to cardiac emergencies. We collect as little
as possible and keep your most sensitive data on your device. This policy
describes how the app handles data.

> **Washington residents:** consumer health data is covered by a separate
> [Consumer Health Data Privacy Policy]({{ site.baseurl }}/consumer-health-data/).

## Emergency contacts stay on your device
The emergency contacts you add are stored only on your device, in the operating
system's encrypted keystore (iOS Keychain), and are never uploaded to our
servers. When you tap "Call 911 + Alert Contacts", your phone's own messaging app
sends them a text — we never see it, and we never store your contacts' names or
phone numbers.

## Location
The app uses your device location for one purpose: **finding AEDs near you**, and
confirming you are actually near an AED when you verify or report one.

**We collect approximate coordinates, not your exact position.** Before your
location ever leaves your device, the app rounds it to a grid of roughly 11
metres. We never receive, transmit, or store a finer position than that — not for
the AED search, not for the proximity check, not for an AED you register. We send
that approximate latitude/longitude and a timestamp to run the search, and we do
not keep a long-term history of where you go. Location is used only while you are
actively using those features.

When you register an AED, the location you submit is stored as part of that AED's
public map pin — that is the point of registering it.

See the separate
[Consumer Health Data Privacy Policy]({{ site.baseurl }}/consumer-health-data/)
for how location is handled for Washington residents.

## AED registry (community-contributed)
AEDs you register — including the location, access details, and any photos — are
stored in our database and shown publicly to other users so they can find an AED
in an emergency. Please do not upload photos that contain people or private
information.

**Photos are stripped of their metadata before they are uploaded.** A photo file
normally carries hidden information — the exact GPS coordinates where it was
taken, a timestamp, and details about your device. Because AED photos are public,
the app re-encodes every photo on your device before sending it, which discards
all of that. What reaches us, and what other people can see, is the picture only.
The pin's own coordinates are the approximate ones described above.

## Accounts
The core features — CPR guidance, the metronome, and finding an AED — work without
an account or a profile. You only sign in (with Apple) to register a new AED,
verify one, report one as missing, or take part in the Community. When you sign in
we store an account record and a contributor profile so your contributions can be
attributed and moderated.

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
You can change your answer any time under **Settings → Community AI screening**,
in either direction. If we ever change the processor, what is sent, or why, we
will ask again rather than rely on the permission you gave for the old
arrangement.

## Deleting your account
You can delete your account any time in the app, under **Settings → Delete
account**. Deleting removes your personal account data — your login, contributor
profile, notification record, and reputation record. If you signed in with Apple,
we also revoke CPR360's Sign in with Apple token.

Two things intentionally survive, in anonymized form:

- **AEDs you added**, and their photos, stay on the public map so others can still
  find a defibrillator in an emergency.
- **Community posts and comments you wrote** stay, shown as "[deleted]", so
  conversations others took part in remain intact. Delete them yourself first if
  you would rather they be removed.

Moderation records are retained as needed for safety. Irreversible anonymization
is used so we can satisfy erasure requests while keeping public-safety data and
community threads usable.

## Notifications
**This version of CPR360 does not send you push notifications.** The app never
asks for notification permission, so none can be delivered.

What does happen: our push provider's software (OneSignal) starts when the app
launches and registers this installation, creating a **device-level identifier**.
If you sign in, that identifier is associated with your account so that a future
version could deliver notifications to the right person. This is why our App Store
privacy disclosures list a device identifier and a user identifier — the
identifiers exist even though no notification is ever sent.

Deleting your account removes the association. Deleting the app removes the
identifier from your device.

## Service providers
We use a small number of processors:

| Provider | What it does | What it receives |
|---|---|---|
| **Supabase** | Database, sign-in, AED photo storage | Account record, AED pins and photos, Community content, approximate location (~11 m grid) used to run the nearby-AED search |
| **Cloudflare** | Workers AI screening of Community text | The submitted text only |
| **OneSignal** | Push infrastructure (dormant — see Notifications) | Device identifier, and your user id once signed in |
| **Sentry** | Anonymized crash and error reports | Diagnostic data, with identity, request, and location context removed before sending |

These processors act on our instructions. We do not sell your data, and we have no
affiliates — no company under common ownership or control with us receives any of
it.

## How long we keep things
- **Emergency contacts** — on your device only, until you delete them or remove the app. Never on our servers.
- **Account and profile** — until you delete your account.
- **AED pins and photos** — as long as the pin is useful to the community; anonymized, not deleted, when you delete your account.
- **Community posts and comments** — as above: retained and anonymized.
- **Moderation records** — as long as needed for Community safety.
- **Location used for searching** — approximate (~11 m grid), used to answer your request and not stored as a location history.
- **Crash and error reports** — kept for a limited period under Sentry's retention schedule, then deleted.

## Security
Data in transit is encrypted with HTTPS/TLS. Emergency contacts are held in your
device's encrypted keystore. Server data sits behind per-user access rules that
restrict each account to its own records, and privileged keys are used only in
server-side functions, never shipped in the app.

No system is perfectly secure, and we don't claim otherwise.

## International transfers
Our providers operate globally, and Cloudflare and OneSignal in particular process
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
We don't sell your data, we don't store your phone number on our servers, we don't
build a history of your movements, and the CPR metronome and voice guidance work
fully offline without sending anything anywhere.

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
