# TradeBlade — privacy policy

This repository exists for one reason: App Store Connect requires a privacy
policy at a **public** URL, and the TradeBlade source repository is private.
It holds the published page and nothing else — no app code.

**Published at:** https://jakenpk-boop.github.io/tradeblade-privacy/

## Do not edit index.html here

`index.html` is generated. The wording lives in the app, in
`TradeBlade/PrivacyPolicy.swift` (`PrivacyText`), so that the policy shown in
Settings → About and the policy on the web cannot drift apart — a test in the
app repo fails if they do.

To change the policy:

1. Edit `PrivacyText` in the TradeBlade repo, and bump `lastUpdated`.
2. Run `Scripts/publish-privacy.sh` there. It regenerates the page and pushes
   it here.

Editing this file by hand would make the website disagree with the app, which
is the exact problem the setup is designed to prevent.
