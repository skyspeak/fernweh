# 🧳 Trip Planner — trips you'll never take

**Live:** https://skyspeak.github.io/fernweh/

A "dopamine website" for travel: all the thrill of planning a trip, with none of the packing, paying or going. Inspired by South Korea's trend of sites that let you browse delivery menus and fill carts without ever ordering.

## What you can do

- **Pick a destination**: type one, tap a suggestion, or spin the 🎰 slot machine.
- **Dream by season**: choose 🌸 Spring, ☀️ Summer, 🍂 Autumn or ❄️ Winter. Dates land in that season (flipped for southern-hemisphere places), the weather changes, places at their best are marked, and each trip gets a one-season-only moment, like maple illuminations in autumn Kyotoast or fresh powder in winter Queensclown.
- **Fill your Dream Year**: plan one dream trip per season to complete a four-season board in your passport.
- **Get an "AI" itinerary**: a pretend agent "thinks", then builds a day-by-day plan (morning, lunch, afternoon, evening). Heart ❤️ or swap 🔄 any stop.
- **Explore**: tabs for 📍 Attractions, 👀 Sightseeing, ⭐ Top-rated tours, 💎 Hidden gems and 🤝 Private 1:1 excursions.
- **Book tours**: pick a day and time, choose your private guide, add extras. It all costs $0.00.
- **Feel the urgency**: flight prices keep dropping and "14 people are looking at this flight".
- **"Book" the trip**: choose a seat, hold to confirm, get confetti, a boarding pass that boards *never*, and a passport stamp.
- **Confirmation page**: after booking, see every confirmed item (flight, hotel, tours, extras, each day's plan) and send it as a web page by link, email, text, WhatsApp or the share sheet, or save it as a PDF.
- **Share it in fun ways**:
  - ✍️ *Sign it* so the recipient sees who sent it.
  - 🎁 *Surprise mode*: the recipient has to tap a gift three times to unwrap it before they see where they're "going".
  - 🏴‍☠️ *Steal this trip*: recipients can copy a shared trip into their own planner, remix it and book it as theirs. Each re-share adds to a visible trip lineage (Sam → Jo → you?).
  - 💬 *Reactions*: recipients pick a reaction ("😭 Take me with you") and get a short link to send back.
  - 📸 *Postcard*: a 1080×1350 image of the trip for stories and group chats.
- **Passport**: tracks trips planned, money not spent, excursions booked and your Dream Year.

All 11 destinations are parody versions of real places (Kyotoast, Lisbonbon, Reykjaview, Santorinny, Pantsagonia…). Typing the real name, like "Kyoto", takes you to its lookalike. Any other place you type gets a general plan with that name.

## How it works

- One self-contained file: [`index.html`](index.html). No build step, no dependencies, no backend. The only external request is Google Fonts.
- The "AI" is simulated: plans are put together from hand-written content in the page, so it's instant, free and works offline.
- Shared itinerary links carry the whole trip inside the link itself (compressed into the `#trip=` part of the URL; reactions use `#reply=`), so nothing is stored on a server. Anything read from a link is escaped before it's shown.
- Progress (passport stamps, totals, Dream Year, your sign-off name, mute setting) is saved in your browser's `localStorage` and never leaves your device.
- Mobile-first layout, dark mode, sound effects (🔊 to mute), phone vibration and `prefers-reduced-motion` support.

## Run locally

Open `index.html` in a browser, or:

```bash
python3 -m http.server 8000
```

Then visit http://localhost:8000.

Nothing on this site is real, and that's the point. 💛
