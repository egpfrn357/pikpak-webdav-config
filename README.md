# PikPak WebDAV Setup: How to Enable, Connect, and Mount Your Cloud Drive on Windows, Mac, and Mobile — Client Recommendations, Read-Only Limits, and Premium Requirements Explained

If you've been searching for "PikPak WebDAV setup," you're probably trying to do one specific thing: get the files sitting in your PikPak cloud drive to show up as a regular folder on your computer, in your media player, or inside an app like VidHub or Infuse — without manually downloading everything first. That's exactly what WebDAV is for, and PikPak rolled the feature out specifically so people could do this.

The catch is that the setup isn't quite as plug-and-play as people expect, and there are a few prerequisites (membership status being the big one) that trip people up before they even get to the connection screen. This guide walks through what WebDAV actually does for a PikPak account, how to switch it on, how to connect from different devices, and what its current limitations are — plus where the membership requirement fits into all of this.

## What WebDAV Actually Does for Your PikPak Account

WebDAV (Web Distributed Authoring and Versioning) is a protocol that lets a remote storage location behave like a local folder. Instead of opening the PikPak app every time you want a file, you connect once with a WebDAV address, username, and password, and from then on your PikPak drive shows up inside whatever software supports the protocol — a file manager, a media center app, a network drive on Windows, or a "Connect to Server" mount on a Mac.

According to PikPak's own help documentation, the feature was added so users could access their cloud storage files through third-party applications and use various WebDAV-compatible client software to browse, play, and download their stored files. That's the whole point: PikPak's own apps are good for *adding* files via torrent/magnet/social links, but WebDAV is what lets other software *read* what's already there.

## Before You Start: The Premium Requirement

This is the part that catches a lot of people off guard. WebDAV on PikPak is currently available to members only, and it's a read-only implementation for now — PikPak has stated that due to development costs, it currently supports only read operations and does not support write, copy, or move operations, with more functionality planned for later.

So if you're on the free tier and the WebDAV toggle either isn't doing anything or isn't visible at all, that's expected behavior, not a bug. You'll need an active Premium subscription before the rest of this guide will actually work for you.

## Step-by-Step: Enabling WebDAV in PikPak

The official process is short, and it's the same regardless of which device you eventually plan to connect *from* (the toggle itself is done once, inside the PikPak app or web drive):

1. Open the **PikPak Web Drive** (or app) and go to **Settings**.
2. Navigate to **Experimental Features**.
3. Toggle on the **WebDAV** option.
4. PikPak will generate a unified WebDAV connection address, along with a username and password — these act as your login credentials for any WebDAV client.

> Treat that address and password like any other account credential. PikPak itself notes you should keep this information secure and avoid sharing it, since anyone with it can browse your files.

If you don't already have a Premium account active, this is the point where it's worth signing up — 👉 [start a PikPak account with a bonus through this invite link](https://mypikpak.com?invitation-code=74098243) before you go further, since the WebDAV toggle won't unlock anything useful on a free account.

## Connecting to PikPak via WebDAV from Different Devices

Once you have the address/username/password trio, the actual connection step depends on what you're connecting *from*. Here's how it breaks down across common setups people search for:

### Windows
Windows doesn't have a great native WebDAV client for media use, so most people use a dedicated mounting tool. **RaiDrive** is the one most commonly recommended for PikPak specifically — you add a new WebDAV connection inside RaiDrive, paste in the PikPak-issued address, username, and password, and it appears as a mapped drive letter in File Explorer.

### macOS
Finder has built-in WebDAV support: **Go → Connect to Server**, paste the PikPak WebDAV address, and authenticate with the username/password. It'll mount like any network share.

### Media Center / Streaming Apps
This is actually the most popular reason people look this up — they don't want a mapped drive, they want their PikPak library to show up inside a media player. Apps like **VidHub** support adding PikPak as a WebDAV source directly inside their "Add File Source" menu, which is useful if you're already centralizing multiple cloud drives (PikPak, Aliyun, 115, etc.) in one resource management interface.

### Advanced / Self-Hosted Setups
There's also a small ecosystem of community-built bridge tools (open-source projects that wrap the PikPak API in a local WebDAV server) aimed at people who want to use **rclone** or a NAS system rather than PikPak's native WebDAV endpoint directly. These are unofficial, third-party tools, not built or maintained by PikPak — useful if you're comfortable running a small self-hosted service, but worth weighing against the official method if you'd rather not add another moving part to your setup.

## Known Limitations to Plan Around

Before you build a workflow around this, it's worth knowing the rough edges that show up consistently in PikPak's own documentation and in user reports:

- **Read-only access.** You can browse, stream, and pull files down — you can't upload, rename, move, or delete through the WebDAV connection itself.
- **Client compatibility varies.** Because different WebDAV clients implement the protocol differently, you may run into compatibility quirks depending on which app you're connecting with.
- **Premium-gated.** As covered above, this isn't a feature free accounts can use at all right now.

None of these are dealbreakers for the most common use case (streaming saved videos into a media player), but they matter if you were hoping to use PikPak's WebDAV mount as a general-purpose synced drive.

## Picking the Right PikPak Plan

Since WebDAV requires Premium, it's worth understanding how PikPak's plans are actually structured before you subscribe. PikPak runs two parallel pricing tracks rather than one flat global price: **Global Premium**, aimed at a list of roughly 30 developed markets (the US, Canada, Japan, the UK, Germany, and others), and **Regional Premium**, a reduced-price tier for everywhere else. PikPak automatically determines which tier applies based on your IP address, device language, and SIM country code — you don't choose it manually, and pricing on the checkout page reflects whichever tier you're assigned.

Both tiers unlock the same feature set (WebDAV, full 10TB storage, original-quality playback); the differences are price and, in some cases, peak download speed. Premium itself can be billed monthly, semi-annually, or annually, and additional storage beyond the base 10TB can be purchased separately for accounts that need more room.

| Plan | Storage | WebDAV Access | Billing Cycle | Typical Price Range* | Get It |
|---|---|---|---|---|---|
| Free | 6GB | ❌ Not available | — | $0 |  [Create a free account](https://mypikpak.com?invitation-code=74098243) |
| Premium — Regional | 10TB | ✅ Read-only | Monthly / Semi-Annual / Annual | Lower-cost tier for non-listed countries |  [Check current price & subscribe](https://mypikpak.com/drive/payment?invitation-code=74098243) |
| Premium — Global | 10TB | ✅ Read-only | Monthly / Semi-Annual / Annual | Higher-cost tier for the ~30 listed developed markets, includes top download speed priority |  [Check current price & subscribe](https://mypikpak.com/drive/payment?invitation-code=74098243) |
| Additional Storage Add-on | +10TB increments | ✅ (extends existing Premium) | Annual | Add-on priced separately from base Premium |  [View storage add-ons](https://mypikpak.com/drive/payment/storage?invitation-code=74098243) |

*PikPak detects your country automatically and displays the exact local price and currency only at checkout, so the figures above are intentionally a range rather than a fixed number — open the link above to see what applies to your account.

Both Premium tiers are billed through the same purchase flow, which is why the table above points Regional and Global rows to the same checkout link — PikPak's system assigns the correct tier and rate for you rather than letting you pick a separate URL for each.

## Getting a Bit More Out of Sign-Up

If you're creating a new account anyway to get WebDAV working, it's worth going through an invitation code rather than a blank registration. PikPak's referral system applies a registration code at signup and, per PikPak's own help center, ties bonus premium days to that process — the exact bonus shown depends on the current promotion, so it's best to check what's displayed at sign-up. 👉 [Register using invite code 74098243](https://mypikpak.com?invitation-code=74098243) to apply it automatically rather than typing it in manually later.

## Frequently Asked Questions

**Does the free plan support WebDAV at all?**
No. PikPak's documentation is explicit that the feature is members-only, so you'll need an active Premium subscription (Global or Regional) before the toggle does anything useful.

**Can I write or upload files through the WebDAV connection?**
Not yet. The current implementation is read-only — you can browse, stream, and download, but uploads, moves, and deletions need to happen inside the PikPak app itself.

**Why does my WebDAV client behave differently than someone else's?**
PikPak has acknowledged that compatibility varies by client implementation. If one app behaves oddly, it's worth trying a different WebDAV client (RaiDrive vs. a media center app vs. Finder, for example) before assuming the connection details are wrong.

**Is purchasing Premium through a third-party reseller risky?**
PikPak's own help center allows for buying redemption codes through its official Gift Card Service Center or authorized distributors, but explicitly warns that buying outside those approved channels can carry account-suspension risk. The safest route is subscribing directly on PikPak's own payment page.

**What's the difference between Global and Regional Premium besides price?**
Mainly price and peak download speed allowance — Global Premium guarantees the higher speed tier regardless of location, while Regional Premium is priced lower but capped at a slightly lower max speed per file in the listed developed-country regions.

## Wrapping Up

WebDAV turns PikPak from "an app you have to open" into a drive your other software can read directly — which is genuinely useful once it's connected, even with the read-only restriction. The setup itself is just four steps inside PikPak's settings; the part that actually requires planning is making sure you're on a Premium plan first, since that's the real gatekeeper here, not the WebDAV toggle itself.

If you're setting this up for the first time, registering through an invite link costs nothing extra and may apply a sign-up bonus automatically: 👉 [Get started with PikPak here](https://mypikpak.com?invitation-code=74098243).

*This article includes a referral link; using it may earn the author a commission at no extra cost to you.*
