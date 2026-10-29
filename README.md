# Alliance Builder

A mobile-friendly, one-page group game built with vanilla HTML, CSS, and JavaScript.

## Play live on your own phones

1. Open the **website**.
2. One person selects **Host a live room · QR join**.
3. Other people scan the QR code (or open the link / enter the 12-character code).
4. Everyone enters their **own real name**, without example or placeholder players.
5. The host starts a round once there are at least 4 players.
6. Each person privately reveals just their **partner(s) and shared task** on their own phone.
7. When time is up, the host can reshuffle or edit settings.

The host's tab must stay open for the live room.

## Offline option

Choose **Play together on one device (offline)** to enter names locally and pass a phone around for private reveals. No scripts, servers, accounts, or internet access are required for this mode.

## Features

- 54 editable short tasks: conversation, physical-light, creative, or mixed.
- Random pairings; avoid repeats from the previous round when possible.
- Optional trio or one randomly sitting-out person for odd player counts.
- 90-second, 2-minute, 3-minute, or 5-minute rounds.
- Hide/show mission; personal "We did it" checkmark.
- Host-controlled new rounds and editing.
- WebRTC data connections through PeerJS for live rooms. Only each person's mission is transmitted to their phone.
- QR codes generated on the host's browser with the qrcode-generator library.

## GitHub Pages

In the repository, open **Settings → Pages**, choose **Deploy from a branch**, select **main** and **/(root)**, and save.

Then visit **https://tbenitz.github.io/alliance-builder/**.

## Network notes

Online multiplayer requires internet to load the PeerJS/QR libraries and contact public PeerJS signaling infrastructure. Some strict NATs and firewalls can prevent direct peer connections; there is no dedicated TURN relay. Names and assignments are not stored in an online database. Offline mode continues to work without external resources.

## Structure

`index.html` is the complete game. All gameplay styling and logic are inside that one file. Only online multiplayer dynamically loads external browser libraries.
