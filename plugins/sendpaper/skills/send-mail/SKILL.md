---
name: send-mail
description: Send a real printed postcard or letter to a US address with Sendpaper. Use when the user asks to mail, post, or send a physical postcard, card, letter, note or notice to someone.
---

# Sending physical mail with Sendpaper

1. Collect, and read back to the user before creating anything:
   - recipient name and full US address (street, city, two-letter state, ZIP)
   - the user's own name and return address (required; it is printed on the piece)
   - the wording. Draft it for them if asked, but show it before sending.
2. Choose the product: `create_postcard` (4x6 default, 6x9 for photos or longer notes, message up to 600 characters) or `create_letter` (up to ~3 pages of plain text). Call `get_pricing` if the user asks about cost.
3. For a postcard front, use an https image URL the user provided, or a short `front_headline` with a `front_theme`.
4. Pass an `idempotency_key` (e.g. a slug of recipient + date) so retries never create duplicates.
5. Show the user the `preview_url` and the `checkout_url` from the response. Say plainly that nothing is mailed until they pay, and that a person reviews every piece first.
6. Use `get_order` to report status later. Use `cancel_order` only for unpaid orders.

Never invent an address. Refuse threatening, harassing, fraudulent or obscene mail.
