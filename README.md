# AirQR

Send files from one of your devices to another, straight from the browser. No account, no upload, no cable.

**Open it: https://starmarine06.github.io/airqr/**

## Pairing code (the default)

1. On the device that has the file, open the page and drop the file in **Send**. A 6-digit code appears.
2. On the other device, open the same page, type the code under **Receive** and press Receive.
3. The file downloads on the second device. Both sides show when it's done.

The file travels directly between the two browsers over an encrypted WebRTC connection. It is never stored on a server. A pairing service ([PeerJS](https://peerjs.com/)) only introduces the two browsers to each other, so both devices need internet for the handshake. Files up to 200 MB are checked with SHA-256 on arrival, larger ones by size.

No camera needed on either side. Send several files at once if you like.

Things to know:

- Keep the sending tab open until it says done.
- A code works for one receiver. Press **New code** to send again.
- The received file is held in memory before it's saved, so very large files (several GB) depend on how much RAM the receiving browser has.
- A strict office firewall can stop two browsers reaching each other.

## QR and camera (no network at all)

The second tab is the original AirQR. One screen shows a stream of QR codes and the other device's camera reads them. Nothing goes over Wi-Fi, Bluetooth or the internet, so it works between machines that can't talk to each other any other way. It's slow, and the receiving device needs a camera.

On the sending device, pick a file under Sender and press Start Transmitting. On the receiving device, open the same tab, use Receiver, and point the camera at the sender's screen.

## Run it locally

```
git clone https://github.com/Starmarine06/airqr
cd airqr
node bin/cli.js
```

That serves the app at `http://localhost:8000` and opens your browser. The whole app is one `index.html`.

Needs Node 10 or newer. MIT license.
