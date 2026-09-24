# Meetup Contact Kit

A small, inspectable handoff for meeting people in person: one URL, a QR code, a contact card, a few useful links, and a human follow-up. No account, newsletter, CRM, or backend is required.

[See Brian's live example](https://gorzelic.net/meet) · [Read how he uses it](https://gorzelic.net/meet/setup)

## Use it

1. Copy `index.html` and `contact.vcf` to a folder you can host over HTTPS.
2. Replace the sample name, description, email, and links. Keep the page short.
3. Publish the folder on a host you control. Check both files in a browser.
4. Make a QR code for the page URL, not for the contact-card file. For example, with `qrencode`: `qrencode -t SVG -o event-qr.svg 'https://your-domain.example/meet'`.
5. Print the QR at high contrast and test it from another phone on cellular data. If you use an NFC tag, write the same HTTPS URL to it.
6. Use [CHECKLIST.md](CHECKLIST.md) before the event. Follow up only with people who agreed to continue the conversation.

You can download the ZIP from [the setup page](https://gorzelic.net/meet/setup) without a GitHub account. For an AI-assisted version, copy the starter prompt there or upload [ADAPT_WITH_AI.txt](ADAPT_WITH_AI.txt) to ChatGPT, Claude, or another assistant. Those links open a new chat; they do not transfer a file or prompt automatically. Review every generated claim and test every integration. The prompt is a starting point, not a substitute for working software.

## What this template does

The sample page has a `.vcf` contact download, direct email link, and space for a few work links. It is plain HTML and CSS. There is no tracking script, server, database, automatic email, or contact capture form.

Brian's live `/meet` implementation uses a separate Next.js site. Its event pages can count page visits and selected clicks with Umami when a website ID and tracker URL are configured. The portable template does not inherit that tracking. If you add analytics to your copy, disclose it and test the deployed page and dashboard before claiming it works. A click count is not a count of qualified leads.

If you add a form later, decide what data you truly need, tell visitors how you will use it, protect it against abuse, and verify delivery end to end. A successful browser animation does not prove an email was delivered. An attendee scanning your code has not consented to a mailing list.

## Files

- `index.html` — responsive sample landing page
- `contact.vcf` — editable vCard 4.0 sample
- `ADAPT_WITH_AI.txt` — prompt that asks an AI assistant to tailor the setup without inventing results or integrations
- `CHECKLIST.md` — event-day checks and follow-up discipline

The public example is Brian Gorzelic's implementation; this repo is the portable pattern. It intentionally excludes his private event notes, prospect research, credentials, email configuration, and contact records.

MIT licensed. Built to start conversations, not collect a room without its permission.
