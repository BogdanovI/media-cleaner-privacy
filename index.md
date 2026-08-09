# Privacy Policy for On-Device Media Cleaner

**Last updated:** 9 August 2026

This policy explains what On-Device Media Cleaner ("the app", "we") does with
your information. It applies to the Android app published under the package name
`io.github.bogdanovi.media_cleaner`.

## Summary

The app finds duplicate photos, blurry photos, large media files and messenger
media **entirely on your device**. Your photos and videos are never uploaded,
never transmitted to us, and never sent to any server or AI service.

The one exception to "nothing leaves your device" is advertising: the app shows
ads through Google AdMob, and the Google Mobile Ads SDK collects data as
described in section 4.

## 1. Who is responsible

This app is developed and published by an individual developer.

Contact: ibogdanovdec@gmail.com

## 2. Photos, videos and files

To find duplicates, blurry images and large files, the app reads the photos and
videos in your device's media library (and, on desktop platforms, in folders you
explicitly select).

- All analysis runs locally, in a C++ engine bundled inside the app.
- Image content, file names, file paths, thumbnails and computed image
  fingerprints are held in memory during a scan and written to your device only.
- **None of this is uploaded, shared, or transmitted anywhere.** The app contains
  no server, no account system, and no upload capability.
- When you delete files, deletion happens locally through the Android system.
  Deleted files are handled by Android's own media deletion flow; we never
  receive copies of them.

## 3. Data stored on your device

The app saves a small set of preferences locally (via Android SharedPreferences).
This never leaves the device and is removed when you uninstall the app:

- your chosen language and light/dark theme
- duplicate matching strictness, blur sensitivity thresholds, and the "large
  file" size threshold
- your daily free-deletion counters

We have no access to any of it. Your Premium status is not decided by this local
data — it comes from your Google Play purchase, as described in section 4.

## 4. Advertising (Google AdMob)

The app displays banner ads and optional rewarded ads via **Google AdMob**. To
serve ads, the Google Mobile Ads SDK collects and processes data independently of
us, including:

- your device's **advertising ID** (a resettable identifier)
- device and app information (device model, operating system version, app
  version, coarse language/region settings)
- your **IP address**, from which approximate location may be derived
- ad interaction data (impressions, clicks, rewarded-ad completions)
- ad attribution and interest signals via the Android Privacy Sandbox
  (Topics and Attribution APIs)

This processing is carried out by Google as an independent controller/processor
under its own terms. See:

- Google Privacy Policy: https://policies.google.com/privacy
- How Google uses information from partner apps:
  https://policies.google.com/technologies/partner-sites

We do not receive your advertising ID or your personal data from Google; we only
see aggregate, non-identifying earnings and performance reports.

### Consent in the EEA, UK and Switzerland

If you are in the European Economic Area, the United Kingdom or Switzerland, the
app asks for your consent before serving personalised ads, using Google's
User Messaging Platform (UMP). You may withdraw or change your consent at any
time from the app's settings, under "Ad privacy options". If you decline
personalised ads, you will still see ads, but non-personalised ones.

No ads are requested at all until this consent step has completed.

### Premium

Premium is a one-time purchase that removes ads, lifts the daily delete limit and
unlocks advanced scan settings. Purchases are processed by **Google Play**, and
your entitlement is managed on our behalf by **RevenueCat**, which receives a
pseudonymous app user identifier and your purchase receipt in order to confirm
it. RevenueCat does not receive your name, email address or any of your photos.
See https://www.revenuecat.com/privacy/ for their policy.

We never see or handle your payment details; those stay with Google Play.

## 5. Permissions and why they are needed

| Permission | Why |
| --- | --- |
| `READ_MEDIA_IMAGES`, `READ_MEDIA_VIDEO`, `READ_MEDIA_VISUAL_USER_SELECTED` (and `READ_EXTERNAL_STORAGE` on Android 12 and below) | To read your photos and videos so they can be analysed on-device. This is the app's core function. |
| `POST_NOTIFICATIONS`, `VIBRATE` | To show scan progress and a "scan complete" notification. |
| `FOREGROUND_SERVICE`, `FOREGROUND_SERVICE_DATA_SYNC`, `WAKE_LOCK` | To keep a long scan running when the app is in the background, so it is not killed mid-scan. |
| `RECEIVE_BOOT_COMPLETED` | Declared by the notification and background-task libraries the app uses. The app does not start itself on boot. |
| `INTERNET`, `ACCESS_NETWORK_STATE` | Added by the Google Mobile Ads SDK to load ads. The app itself makes no network requests of any kind. |
| `com.google.android.gms.permission.AD_ID`, `ACCESS_ADSERVICES_AD_ID`, `ACCESS_ADSERVICES_ATTRIBUTION`, `ACCESS_ADSERVICES_TOPICS` | Added by the Google Mobile Ads SDK for advertising identification, ad attribution and Android Privacy Sandbox topics. Used by Google for advertising as described in section 4. |
| `com.android.vending.BILLING` | Added by Google Play Billing so the one-time Premium purchase can be made. |

## 6. Analytics and crash reporting

The app contains **no analytics SDK and no crash reporting SDK**. We do not track
your usage.

If you install the app from Google Play, Google may collect its own standard
crash and usage data as part of the Play platform, independently of us. See
Google Play's privacy terms.

## 7. Children

The app is not directed at children under 13 and we do not knowingly collect
personal data from them.

## 8. Data retention and your rights

Because we do not collect or receive personal data, we hold nothing to retain,
export, or delete. To remove everything the app has stored:

- uninstall the app — all local preferences are deleted with it.

Regarding advertising data held by Google, you can:

- reset or delete your advertising ID in **Android Settings → Privacy → Ads**
- change your consent choices in the app (EEA/UK/Switzerland)
- exercise your GDPR rights (access, rectification, erasure, objection) directly
  with Google via https://policies.google.com/privacy

## 9. Changes to this policy

If this policy changes, the updated version will be published at this same URL
with a new "Last updated" date. Material changes affecting how data is handled
will also be noted in the app's Play Store release notes.

## 10. Contact

Questions about this policy: ibogdanovdec@gmail.com
