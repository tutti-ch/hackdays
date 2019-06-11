---
hackname: email-tracking
quicksummary: Track all emails between tutti users, deliver stats from it
resource: true
archived: false
categories: [hack]
---

# email-tracking

On outgoing emails, rewrite _from_ to `encrypt(from, ad_id)`@users.tutti.ch.
On incoming emails to users.tutti.ch, rewrite _to_ to `decrypt(split(to, @)).from`.
Keep stats. As a first feature (in addition to hiding emails) track average reply
latency, display it on li (typically replies within N hours).
