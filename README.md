# KiwiHacks Beacons

Tiny Astro redirect site for beacon/referral links:

```text
https://signup.kiwihacks.org/[REF_CODE]
```

Visitors are redirected to:

```text
https://kiwihacks.fillout.com/nova?ref=[REF_CODE]&Referral+Code=[REF_CODE]
```

## Fillout setup

In the Fillout form, add a URL parameter named `ref`, then set the default value for the **Referral Code** field from that URL parameter. Fillout stores URL parameters in submissions by default, so the beacon code is also available as `ref`.

## Deploying on Vercel

Deploy this folder as an Astro static site and point `signup.kiwihacks.org` at the Vercel project. `vercel.json` rewrites arbitrary paths like `/ABC123` to the Astro page, where the referral code is read and forwarded to Fillout.

## Development

```sh
npm install
npm run dev
```

Build with:

```sh
npm run build
```
