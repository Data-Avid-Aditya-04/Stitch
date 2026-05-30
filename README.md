# Stitch

**Door-to-door multi-modal trip planner for India.**

Stitch helps you plan a real, complete journey — from your exact starting point to your exact destination — by stitching together the right mix of cab, auto, train, bus and flight. You see the full trip on one screen, with honest time and cost estimates, then book each leg on the partner you trust (Uber, Ola, Skyscanner, RedBus, IRCTC).

Live at: **[stitch-d42g.vercel.app](https://stitch-d42g.vercel.app)**

---

## What Stitch does differently

Most travel apps stop at airport-to-airport or station-to-station. They tell you a flight is "2 hours" — but skip the 1-hour cab to the airport, the 1.5 hours of check-in, and the 45-minute cab on the other side. Stitch shows you the **real door-to-door journey**:

- **Exact locations, not just cities.** "Hewlett Packard, Electronic City" → "Goregaon West, Mumbai" — Stitch knows the difference between starting in Electronic City vs. Whitefield and picks the right airport, station, or pickup point accordingly.
- **The full journey, stitched.** Cab to station → train → cab from station. One screen, total time, total cost.
- **Smart group pricing.** Tickets multiply per person; cabs and autos share up to capacity. 3 people in one auto is 1 auto, not 3.
- **Real train data.** Train names, numbers, and schedules from public records (2023), with a dropdown to pick the train that fits your departure time. Live confirmation on IRCTC.
- **Honest estimates.** Prices and times are clearly labelled as estimates. Stitch never invents fake clock times — it shows what it knows and points you to the partner for the live price.

---

## How it works

1. **Enter your real "from" and "to"** — search any address, building, or landmark in India.
2. **Choose when, how many travellers, what to avoid** — "Leave around morning, 3 people, no flights."
3. **See all the routes Stitch can stitch** — sorted by best, fastest, or cheapest.
4. **Open any journey to see the full breakdown** — every leg, every wait, every cost.
5. **Tap "Book"** — Stitch hands off to Uber, Skyscanner, RedBus or IRCTC with your route pre-filled. You book and pay on the partner directly.

Stitch is a **planner**, not a booking site. It earns a referral commission when you book on a partner (eventually — affiliate setup is in progress). Your payment, your booking, your refund — all with the partner. Stitch never touches your money or holds your ticket.

---

## Tech (kept deliberately simple)

- **Single-file vanilla JavaScript** — no build step, no framework
- **Live location search** via OpenStreetMap Nominatim (free, no API key)
- **Nearby station / airport / stop discovery** via OpenStreetMap Overpass API
- **Real train schedules** from the [datameet/railways](https://github.com/datameet/railways) dataset (CC0 public domain) and the bhavyarajdev Kaggle dataset (October 2023)
- **Hosted on Vercel**, source on GitHub, deploys on every commit

That's it. No backend, no database, no login. The whole app is `index.html` and one JSON data file.

---

## Honest limitations

Stitch is built by a solo founder on a zero budget. We are honest about what that means:

- **Prices are estimates**, not live quotes. Live prices come from partners.
- **Train schedules are based on 2023 public records.** Major routes and trains are accurate; exact times may have drifted slightly. Always confirm on IRCTC before booking.
- **Vande Bharat trains added after 2023** are not in the dataset yet.
- **Flights and buses don't have live timings** — partners show those during booking.
- **No login, no profile, no history** — every search is fresh. We don't store your data.

Where Stitch doesn't have data, it says so honestly and points you to the right partner.

---

## Roadmap

- **Now:** Stitch as an honest planner with real data wherever possible
- **Next:** Affiliate partnerships (Cuelinks aggregator → Skyscanner, RedBus) for legitimate live data and revenue
- **Later:** Paid train-data API for live timings; SEO route guides for organic traffic

---

## Built by

[Aditya Geda](https://github.com/Data-Avid-Aditya-04) — a college student in Bengaluru who got tired of opening five apps to plan one trip.

Feedback, bug reports, route suggestions: open an issue here on GitHub.

---

*Stitch is independent and not affiliated with Uber, Ola, Skyscanner, RedBus, IRCTC, or Indian Railways.*
