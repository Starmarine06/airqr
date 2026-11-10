# AirQR

Send a file from one device to another with no network between them. One screen shows a stream of QR codes, the other device's camera reads them.

No Wi-Fi, no Bluetooth, no cable, no account. If one device can see the other's screen, the file gets across.

## Use it

```
git clone https://github.com/Starmarine06/airqr
cd airqr
node bin/cli.js
```

That serves the app at `http://localhost:8000` and opens your browser. The page has two panels. On the sending device, pick a file under Sender and press Start Transmitting. On the receiving device, open the same page, use Receiver, and point the camera at the sender's screen.

The whole app is one `index.html`, so you can also open that file directly.

Needs Node 10 or newer. MIT license.
