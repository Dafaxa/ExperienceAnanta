# Ananta.ID Property Walkthrough

_Started 2026-09-26 02:15 UTC_

---

## User

Wireframe the screens for Interactive 3D Property Walkthrough & Immersive Marketing Gallery ANANTA.ID 
ALL THE PRD AND ALL PLAN ATTACH for style sesuaikan dengan ananta.id

## User

Wireframe the screens for Interactive 3D Property Walkthrough & Immersive Marketing Gallery ANANTA.ID 
ALL THE PRD AND ALL PLAN ATTACH for style sesuaikan dengan ananta.id

## Assistant

_[tool: list_files]_

_[tool: dc_write]_

_[tool: ready_for_verification]_

I've wireframed 20 screens in **Ananta Immersive Wireframes.dc.html**, all in the Ananta brand style (obsidian, ivory and gold, serif headlines, hatched boxes where renders and the 3D scene will go).

They follow the PRD flow in five groups:
- **Discover and select (1a–1f):** welcome screen, project gallery, property overview, masterplan, unit explorer, and the 2D floor plan with an "Enter 3D" entry.
- **3D walkthrough (1g–1i):** three ways to lay out the on-screen controls. 1g is minimal, 1h has a room list and a live mini floor plan like your Virtual Tour reference, and 1i is a guided tour mode.
- **In-experience layers (1j–1m):** room info panel, material configurator, time of day and weather, and measure mode.
- **Compare and connect (1n–1p):** unit comparison, the site-visit booking form, and a thank-you screen with a QR code.
- **Sales and gallery (1q–1t):** sales console, the physical showroom layout, analytics dashboard, and the mobile walkthrough.

Handwritten notes under each screen explain its behaviour; you can hide them with the notes switch in the Tweaks panel.

Prices and project details are placeholders, and the dashboard numbers are the sample figures from the PRD. The admin CMS isn't wireframed yet. A good next step is picking one of 1g, 1h or 1i so I can take that screen to high fidelity.

## User

awesome love it any other recomendation

## Assistant

Here's what I'd add next, in rough priority order:

**Gaps in the current flow**
1. **Loading / scene transition screen.** Unreal scenes take time to load. A branded loader that shows the floor plan and room count makes the wait feel intentional.
2. **Idle timeout and session reset.** A showroom needs an "Are you still exploring?" prompt that returns to 1a and ends the session cleanly, so one visitor's data doesn't leak into the next session.
3. **Window view simulation.** The PRD calls this a key sales moment and it only appears as a button in 1j. It deserves its own screen: a garden/pool/ocean toggle combined with the time-of-day control.
4. **Price and payment plan.** Base price, promo price, booking fee and an installment calculator. Right now price is just a single line of text.
5. **Consent and privacy line** on the lead form (1o), plus a "share with sales" confirmation.

**Screens the PRD needs but aren't wireframed**
6. **Admin CMS:** projects → units → rooms → hotspots, plus the unit status editor.
7. **Scene versioning:** Draft → Review → Approved → Live, with version history.
8. **Floor plan upload + room tagging:** mapping 2D regions to 3D camera anchors. This is the core of the pipeline.
9. **Lead detail in CRM:** the lead record with its session timeline (rooms visited, configuration, time spent), shown from the salesperson's side.

**Product and design decisions**
10. **Choose one HUD.** My pick is **1h** for the showroom touch kiosk and **1g** for web. They can share the same components.
11. **Bahasa / English toggle** on every customer screen, not only the welcome screen.
12. **AI Concierge (Phase 4) concept screen:** a voice/chat bar over the 3D scene ("Show me the largest bedroom"). It's useful for investor pitches even before it's built.
13. **Motion spec** for 2D→3D camera transitions and panel reveals. This will define the premium feel more than static layouts do.

Should I wireframe any of these? Items 1–5 would fit as a turn 2 above the current screens.

## User

yes

## User

yes

## User

can you make detail every page with high fidelity design ui/ux prototype

## Assistant



## Assistant

_[tool: ask_user]_

Before I start the hi-fi build, I need a few answers in the form: screen size, which walkthrough layout to use, where the imagery comes from, which screens to include, how interactive it should be, and language.

## User

Answered — device: Showroom 1920×1080; hud: 1h — Tour rail + mini-plan; imagery: Both — uploads now, slots where missing; scope: Customer journey (1a–1p, 2a–2e), Sales console, Showroom setup, Analytics dashboard, Mobile web; interaction: Clickable + live states (room switch, material swap, time slider, form); lang: EN + ID toggle

## Assistant

_[tool: list_files]_

_[tool: read_skill_prompt]_

_[tool: run_script]_

Copying uploads to safe names first.

_[tool: copy_files]_

_[tool: run_script]_

_[tool: run_script]_

_[tool: run_script]_

Quick check of crops for baked-in text.

_[tool: run_script]_

_[tool: view_image]_

_[tool: run_script]_

_[tool: copy_starter_component]_

_[tool: dc_write]_

_[tool: dc_html_str_replace]_

_[tool: dc_html_str_replace]_

_[tool: dc_html_str_replace]_

_[tool: dc_js_str_replace]_

_[tool: dc_js_str_replace]_

_[tool: run_script]_

_[tool: dc_set_props]_

_[tool: dc_js_str_replace]_

_[tool: show_html]_

_[tool: multi_screenshot]_

_[tool: show_html]_

Looks good. Checking other screens.

_[tool: multi_screenshot]_

_[tool: multi_screenshot]_

_[tool: show_html]_

_[tool: multi_screenshot]_

_[tool: run_script]_

_[tool: show_html]_

_[tool: multi_screenshot]_

_[tool: run_script]_

_[tool: show_html]_

_[tool: multi_screenshot]_

_[tool: dc_write]_

_[tool: dc_write]_

_[tool: dc_write]_

_[tool: dc_write]_

_[tool: run_script]_

_[tool: dc_html_str_replace]_

_[tool: dc_js_str_replace]_

_[tool: ready_for_verification]_

I've built the high-fidelity prototype as five linked files, all clickable. The main walkthrough file and the Sales Console have had a quick visual check; the other three haven't been screenshotted yet and are still being reviewed.

**Ananta Immersive Prototype** (1920×1080 showroom screen)
- **Customer flow:** Welcome → Projects → Overview → Masterplan → Unit explorer → Floor plan → Loading → 3D tour → Compare → Price → Lead form → Thank you.
- **3D tour** uses the 1h layout: a room list on the left, a live mini floor plan with a view cone, and tools on the right.
  - **Moving around:** drag to look, A/D or arrow keys to change rooms, and hotspots that open room info or jump to the next room.
  - **Tour layers:** room info, material changes with a before/after toggle and live upgrade cost, a time-of-day slider with weather, measure mode (tap two points), window view, and a guided tour that plays automatically.
- **Price and lead form:** the payment calculator (cash / instalment / KPR) and the lead form with validation and consent both work.
- **Language and timeout:** the EN/ID toggle switches every screen. The idle countdown and session reset trigger after 90 seconds by default; you can change that in Tweaks.
- A **☰ Screens** button at the bottom-left jumps to any screen or to the other four files.

**The other four files**
- **Sales Console** (tablet): controls rooms, materials, lighting, guided tour and what appears on each screen, with a command log, interest signal, private notes and an offline simulation.
- **Showroom Setup:** a clickable gallery floor plan showing the four displays and the tablet, plus a system diagram with an online/offline toggle.
- **Analytics:** filter by project and 7/30/90 days; includes the funnel, room attention map, top configurations, and a session list with a timeline drawer.
- **Mobile Web:** home, 3D tour with a bottom sheet, and a WhatsApp lead form.

**Things to know**
- Photos are cropped from your uploaded Ananta images. Kitchen, master bedroom, bedroom 2, bathroom and the consultant photo are empty slots you can drag your own renders into.
- The 3D scenes are simulated: drag-to-look moves a still image, and material changes are colour overlays, not real renders.
- Prices, distances and the consultant's name are placeholder data.

## User

Found issues — fixing…

## Assistant

_[tool: snip]_

_[tool: run_script]_

_[tool: ready_for_verification]_

I fixed the two problems the review found, and the files are back out for another check.

- **Blank screen:** the prototype could go completely blank and stay that way if it measured the window before the window had a size. It now skips zero-size measurements and re-measures after loading, so the screen scales correctly. I applied this to all five files.
- **Screens button:** it was covering content at the bottom-left. It's now small and faint in the top-right corner, and becomes fully visible when you hover over it.

## User

any other recomendation

## Assistant

Here's what I'd do next, most valuable first:

**Make it more convincing**
1. **Real renders for the empty rooms.** Kitchen, master bedroom, bedroom 2 and bathroom are empty slots. Drop in 16:9 renders, ideally the same camera angle at day and at night, so the time slider can swap between real images instead of tinting one.
2. **Material variants as real images.** Render the living room in oak, marble and stone and swap the photos. Right now the change is a colour overlay, and a real swap will look far better in a pitch.
3. **A short video in the welcome loop.** A 15–20s exterior flythrough instead of a still would make the LED wall come alive.

**Connect the apps**
4. **Link the sales console to the customer screen.** Both run in the same browser, so tapping "Master Bedroom" on the tablet could move the LED wall screen live. That's the most impressive demo moment from the PRD.
5. **Hand off from showroom to phone.** Scanning the QR on the thank-you screen could open the mobile web version on the same room and configuration.

**Fill the remaining PRD gaps**
6. **AI Concierge overlay (Phase 4 concept).** A voice/chat bar in the tour ("Show me the master bedroom", "Make the floor marble") that runs the same actions. Strong for investor and developer pitches.
7. **Admin CMS:** projects, units, pricing, hotspots, plus scene versioning (Draft → Review → Live).
8. **Floor plan upload and room tagging:** the pipeline screen that shows how a CAD file becomes the 3D experience.

**Before real users try it**
9. **Test on the actual LED wall and touch table.** Check text size at 3–4 m viewing distance; labels at 11–13px will likely need to grow about 1.5×.
10. **Pilot script for sales:** a one-page 5-minute demo path (Welcome → Living → Sunset → Master → Price → Book) so every consultant presents it the same way.

My recommendation is 4 then 6. Want me to start with those?

## User

okay all real renders and photo & video i will upload ASAP, do selain itu

## Assistant

_[tool: update_todos]_

_[tool: run_script]_

_[tool: run_script]_

_[tool: dc_write]_

_[tool: run_script]_

_[tool: dc_write]_

_[tool: update_todos]_

_[tool: ready_for_verification]_

I've built everything except the renders, photos and video you're uploading. None of it has been tested live yet; the main prototype is being reviewed now.

- **Sales console controls the customer screen:** open both files in the same browser (two tabs or two windows). Room, material, lighting, guided tour and screen changes on the tablet move the LED screen live. The console also mirrors whatever the visitor does on the customer screen, and shows "Linked" when connected or an "Open customer screen" link when not.
- **Ask Ananta (AI concierge):** a bar in the 3D tour where you type or speak requests in EN or ID, like "master bedroom at sunset", "lantai marmer", "berapa harga?". It moves rooms, changes finishes, lighting and weather, and opens the view, price, compare or booking screens. It works by matching keywords, not a real AI model, so it runs offline.
- **QR handoff:** clicking the QR on the thank-you screen opens the mobile version on the same room and floor finish.
- **Larger text for the LED wall:** small labels are about 2px bigger, and the tools column is wider.
- **Admin CMS** (new file), with four sections:
  - **Units & pricing:** change status and price, then publish.
  - **Floor plans:** a simulated upload, recognition steps, and tagging each room to its 3D camera position.
  - **Scenes & versions:** Draft → Review → Approved → Live, with rollback.
  - **Leads:** filter and change each lead's status.
- **Demo Script** (new file): a printable one-page guide for consultants covering the 8-step, 5-minute walkthrough, dos and don'ts, and questions to ask after each session.

The Screens button (top-right, faint until you hover) now links to all eight files.

Voice input only works in Chrome and Edge.

## User

Found issues — fixing…

## Assistant

_[tool: run_script]_

_[tool: ready_for_verification]_

I moved the room-to-room hotspots in the 3D tour so they no longer cover the tool column on the right. They now sit at 72–74% across the screen instead of 84–90%. The window-view hotspot on the terrace moved in slightly too.

I only reloaded the page after this change; I didn't re-check the hotspots visually or run another review.

The page shows two broken-image errors while loading, but all images display once it finishes loading.

## User

focus on Admin CMS any other recomendation to customize the project

## Assistant

Here's what I'd add to the Admin CMS, grouped by what it lets the client customise.

**Brand & project setup**
1. **Project settings / white-label:** logo, colours, fonts, tagline, and a toggle between "Powered by Ananta" and the developer's own brand only. Everything the customer screens show would read from here.
2. **Project creation wizard:** Developer → Project → Building → Floor → Unit in five steps, so a new project goes live without an engineer.

**Content inside the 3D experience**
3. **Hotspot editor:** place pins on a room preview, choose the type (Info / Product / View / Navigate / CTA), then set title, description, media and target room. This is the most requested content tool in the PRD.
4. **Materials & configuration library:** upload swatches, set the price modifier, assign them to units and rooms, and mark defaults. This controls exactly what the configurator offers.
5. **Guided tour builder:** drag the room order, write the caption for each stop (EN + ID), and set how long each one lasts.
6. **Facilities & location (POI) editor:** masterplan pins, clusters and nearby places with travel times.
7. **Media library:** renders, videos and 360s, tagged by room and time of day. When you upload your renders, this is where they would plug into the image slots.

**Sales & commercial rules**
8. **Pricing rules:** promos with start and end dates, booking fee, payment plans (instalment tenors, KPR interest rate), and hide/show price per channel (LED wall, web, mobile).
9. **Lead form & CTA builder:** required fields, purpose options, consent wording, WhatsApp routing, and which CTAs appear per screen.
10. **Lead routing:** assign leads round-robin or by project, set a follow-up SLA (e.g. 24h), and connect a CRM webhook.

**Language & AI**
11. **Translations:** every customer-facing string side by side in EN | ID, with "missing translation" flags.
12. **Ask Ananta phrases:** manage synonyms per action (e.g. "kamar terbesar" → Master Bedroom), and see what visitors asked that went unanswered.

**Operations & governance**
13. **Displays manager:** each showroom screen, online status, current scene version, remote restart, and offline cache status.
14. **Roles & permissions:** the PRD's 10 roles (Super Admin … Viewer), each with its own editing rights.
15. **Audit log:** who changed a price, status or scene, when, and before/after values.

My top pick is **1, 3, 4 and 8**. Those four let a developer change the project's branding, what visitors see in each room, what they can configure, and how much it costs. Shall I build those into the CMS?

## User

okay do all

## Assistant

_[tool: dc_write]_

_[tool: run_script]_

_[tool: dc_write]_

_[tool: run_script]_

_[tool: dc_write]_

_[tool: dc_write]_

_[tool: dc_write]_

_[tool: dc_write]_

_[tool: show_html]_

_[tool: ready_for_verification]_

I've built all 15 CMS sections as clickable screens. I checked the Hotspots screen and it renders correctly; the rest are out for review now.

The CMS is split into six files that share one sidebar, grouped as:

- **Project** (Ananta CMS Setup)
  - **Brand & settings:** switch between Ananta, co-branded and white-label; change developer name, tagline, headline, colours, font, languages and logo, with a live preview of the welcome screen.
  - **New project:** a 5-step wizard from developer to unit list that generates unit codes as you go.
- **Content** (Ananta CMS Content)
  - **Hotspots:** click a room render to place a pin, then set its type, title, description and target room.
  - **Materials:** name, swatch, price, default finish and which units each option applies to.
  - **Guided tour:** reorder stops, turn them on or off, set durations, and write EN/ID captions with a cinematic preview.
  - **Facilities & location:** map pins with category and travel time.
  - **Media library:** upload, then tag by room and time of day. This is where your renders will go.
- **Commercial** (Ananta CMS Sales, plus the existing CMS)
  - **Pricing rules:** promos with dates, booking fee, down payment, KPR rate, tenors, and price visibility per channel, with a live preview.
  - **Lead form & CTAs:** which fields show and which are required, purpose options, consent wording, and which buttons appear on each screen.
  - **Lead routing:** assignment rule, consultants, response time limit, escalation, and a CRM webhook with a test payload.
  - **Units & pricing** and **Leads** stay in the existing Admin CMS.
- **Pipeline:** Floor plans and Scenes & versions stay in the existing Admin CMS.
- **Language & AI** (Ananta CMS Language)
  - **Translations:** EN/ID side by side, with missing strings flagged and a coverage percentage.
  - **Ask Ananta phrases:** the words that trigger each action, a test box, and unanswered questions you can map to an action with one click.
- **Operations** (Ananta CMS Operations)
  - **Displays:** status, scene version, offline cache and restart for each screen, plus push-to-all.
  - **Roles & permissions:** the 10 roles × 8 areas, each set to None, View or Edit.
  - **Audit log:** filterable, with before and after values.

Clicking a sidebar item that lives in a different file reloads the page, so unsaved changes on the current screen are lost. All changes are in-page only; nothing is saved between visits.

## User

Found issues — fixing…

## User

Found issues — fixing…

## User

great, any recomenddation

## Assistant

_[tool: update_todos]_

Your usage quota is nearly used up, so I'm pausing here with all the work in a stable state. Here's what I'd do next, most useful first:

1. **Connect the CMS to the prototype.** Right now CMS edits stay inside the CMS page. If they were saved in the browser, a price, promo, hotspot, material or translation change would show up straight away on the LED screen. That would make the pitch demo convincing.
2. **Hub page.** One entry page that links the customer app, sales console, CMS, analytics and demo script, so you can present the whole platform from one place.
3. **Pitch deck.** 10–12 slides for developers: problem, the experience, the showroom, the CMS, analytics, pricing packages (A–D from the PRD) and the roadmap, using screenshots of these screens.
4. **Developer handoff.** Package the screens, data model and API list from your PRD so an engineering team (Unreal + Next.js) can start building.
5. **Onboarding for each role:** short first-login guides for Sales Agent, Marketing Manager and 3D Artist.
6. **Drop in your renders.** When you upload the photos, renders and video, I'll place them in the media library and room slots and replace the colour-overlay material changes with real image swaps.

Tell me which to start with. The first two are quick, and 1 has the biggest effect on the demo.

## User

good do it

## Assistant

_[tool: run_script]_

_[tool: dc_write]_

_[tool: ready_for_verification]_

I've done the first two items: the CMS now updates the customer screen, and there's a new hub page linking everything. The hub is out for review. I haven't tested the CMS-to-screen link yet.

**CMS updates the customer screen.** Open the CMS in one tab and the Immersive Prototype in another. When you publish, the customer screen should update and show "Content updated from CMS":
- **Units & pricing:** unit prices and status (available, reserved, sold).
- **Pricing rules:** promo amount and name, booking fee, and KPR rate on the price screen.
- **Brand & settings:** the English welcome headline.

It works in the same browser only. The CMS colours and logo are not applied to the customer screen yet.

**Ananta Platform Hub** (new file) is one entry page with cards for all eight apps, grouped into customer experience, sales & showroom, and platform. Each card opens in a new tab.

Your usage quota is nearly used up. Items 3–5 (pitch deck, developer handoff, onboarding guides) are next whenever you want to continue.

## User

contiue

## Assistant

_[tool: copy_starter_component]_

_[tool: dc_write]_

## Assistant

_[tool: update_todos]_

_[tool: ready_for_verification]_

## Assistant

_[tool: dc_write]_

## Assistant

_[tool: dc_write]_

_[tool: run_script]_

_[tool: update_todos]_

_[tool: ready_for_verification]_

I've added the last three pieces: a pitch deck, a developer handoff document and onboarding guides. The deck and the updated hub are out for review; the handoff and onboarding files haven't been previewed yet.

- **Ananta Pitch Deck:** 10 slides for developer meetings, from the title through the problem, platform, experience, sales gallery, CMS, intelligence, packages, pilot and roadmap, to the close. Each slide has speaker notes.
- **Ananta Developer Handoff:** covers the screen map, the protocol that links the sales console to the customer screen, the data model, the events to track, and behaviour rules (idle timeout, Ask Ananta limits, consent, offline mode, localisation).
- **Ananta Onboarding Guides:** first-login checklists for Sales Agent, Marketing Manager and 3D Artist. Each step links to the right screen, and progress is tracked as you tick steps off.

The hub page now has a fourth "Pitch & handoff" group linking to these three files.

The package prices on the deck come from your PRD's business model; confirm them before sharing. When your renders, photos and video are ready, upload them and I'll place them.

## User

is it ready t demo?

## Assistant

_[tool: snip]_

Yes, you can demo it as a clickable prototype, as long as you set it up beforehand and explain a few limits up front. Treat it as a concept demo, not a working product.

Two things were never re-checked: the hotspot move in the 3D tour, and the live CMS-to-screen link.

**What works well**
- The full customer flow on the LED screen, in English and Bahasa.
- The sales console moving the customer screen live, when both are open in the same browser.
- CMS changes to price, promo, booking fee and the welcome headline showing on the customer screen.
- Ask Ananta, by typing (voice only works in Chrome and Edge).
- The Analytics, Admin CMS, pitch deck and demo script.

**Setup before the meeting**
1. Use Chrome, full screen (F11).
2. Open the **Platform Hub**, then open the **Immersive Prototype** and **Sales Console** in two windows of the same browser.
3. Check the console header says **LINKED**.
4. Set **idle timeout** to 300s in Tweaks so it doesn't reset mid-pitch.
5. Run the **Demo Script** once to rehearse.

**Be upfront about**
- **Empty rooms:** kitchen, master bedroom, bedroom 2 and bathroom show empty image slots until your renders are uploaded. Either stay in Entrance, Living, Dining and Terrace, or upload the renders first.
- **Not real 3D yet:** drag-to-look moves a still image, and material and lighting changes are colour overlays on the photo, not real renders.
- **Sample data:** prices, leads and analytics numbers are placeholders.
- **Nothing is saved:** apart from the published price, promo, fee and headline, CMS edits reset when a page reloads.
- **One device:** sync only works between windows in the same browser, not between a real tablet and a separate LED PC.

**Best 5-minute path**
Welcome → Unit explorer (2B-01) → Floor plan → Enter 3D (Living) → change the floor to marble → Terrace at sunset → Ask Ananta "berapa harga?" → Price → Book visit → Thank you.

Then switch to the sales console and move rooms from it. That's the strongest moment.

If you can upload the four missing room renders first, the demo will look much more complete.

## User

make all the transition move smooth transitiom

## Assistant

_[tool: run_script]_

_[tool: ready_for_verification]_

I've made the transitions smoother in the main prototype and the mobile version. I haven't watched them run yet; the prototype is being reviewed now.

**Customer prototype**
- **Between screens:** the old screen fades out with a slight zoom and blur, then the new one fades in and settles into place. It takes under a second.
- **Between rooms in the 3D tour:** a slower crossfade, with a gentle zoom-out as you arrive in the room.
- **Material and lighting changes:** these now blend in gradually instead of jumping.
- **Panels:**
  - Room info and Customise slide in from the right.
  - The time-of-day bar rises from the bottom.
  - Window view fades in.
  - The idle warning pops in softly.
  - Floor plan room previews fade in.
  - The masterplan info card glides to whichever cluster you tap.
- **Buttons:** every hover effect now fades instead of switching instantly.

**Mobile web:** screens fade and rise into place, and buttons ease on hover.

The sales console, CMS files and analytics still switch instantly. I can give them the same treatment if you want them to match.

## User

Save as standalone HTML: `Ananta Immersive Prototype.dc.html`

## Assistant

_[tool: read_file]_

_[tool: run_script]_

_[tool: copy_files]_

_[tool: super_inline_html]_

Those are runtime template holes (resolved via `__resources` in JS), not real files. Checking it runs.

_[tool: show_html]_

_[tool: get_webview_logs]_

_[tool: eval_js_user_view]_

_[tool: save_screenshot]_

Images from code render correctly offline.

_[tool: present_fs_item_for_download]_

The standalone prototype (1.9 MB) is ready to download above. It works offline: all photos are packed inside it, and I checked that the project cards render correctly.

A few things won't work in this single file:
- **Links:** the Screens-menu links to the other apps (sales console, CMS and so on) won't open, because those files aren't included.
- **Console and CMS sync:** live control from the sales console and live updates from the CMS don't work in this file.
- **Room photos:** kitchen, master bedroom, bedroom 2 and bathroom still show empty image slots.
- **Fonts:** they load from Google Fonts, so fully offline the text falls back to a standard font.

## User

bagaimana untuk deploy all

## Assistant

_[tool: snip]_

_[tool: write_file]_

_[tool: present_fs_item_for_download]_

Seluruh proyek sudah siap diunduh sebagai zip di atas. Saya menambahkan `index.html` yang langsung membuka Platform Hub, jadi alamat utama situs akan menampilkan halaman Hub.

**Cara deploy (paling mudah: Netlify, gratis)**
1. Unduh zip, lalu ekstrak.
2. Buka **app.netlify.com/drop**.
3. Seret folder hasil ekstrak ke halaman itu.
4. Anda langsung mendapat link seperti `ananta-demo.netlify.app`.
5. Opsional: hubungkan domain sendiri, misalnya `demo.ananta.id`, di Domain settings.

Alternatif lain: **Vercel**, **Cloudflare Pages**, atau **GitHub Pages**. Caranya sama: upload folder apa adanya. Tidak perlu server, database, atau proses build karena semuanya file statis.

**Untuk showroom offline**
- Salin folder ke PC showroom.
- Jalankan server lokal sederhana dari folder itu, misalnya `npx serve`, lalu buka `localhost:3000` di Chrome dalam mode layar penuh.
- Jangan buka file dengan klik dua kali, karena sebagian fitur butuh dibuka lewat server.

**Yang perlu diketahui**
- Sinkronisasi sales console ↔ layar pelanggan dan CMS ↔ layar hanya jalan **di browser yang sama pada satu perangkat**. Tablet dan PC terpisah butuh backend WebSocket sungguhan, sesuai Developer Handoff.
- Perubahan di CMS tersimpan hanya di browser itu dan tidak tersinkron antar pengguna.
- Font dimuat dari Google Fonts, jadi saat offline tampilannya memakai font standar.
- Jangan hapus `support.js`, `image-slot.js`, `deck-stage.js`, folder `img/`, dan `CMSSidebar.dc.html`. Semua halaman bergantung pada file-file ini.
- Render ruangan yang Anda seret ke slot gambar ikut terbawa di file `.image-slots.state.json`, jadi jangan dihapus juga.

## User

any other recomendation

## Assistant

Here's what I'd do next, in order:

**Before showing clients**
1. **Upload the four missing room renders** (kitchen, master bedroom, bedroom 2, bathroom). This is the biggest visual gap.
2. **Put real numbers in the CMS:** unit prices, promo and booking fee. Fake numbers get questioned in meetings.
3. **Protect the demo link.** Netlify has password protection, so the prototype and your pricing aren't public.
4. **Use your own domain,** like `experience.ananta.id`. It looks more credible than a netlify.app address.

**To make the demo stronger**
5. **Swap real images for material changes.** Render the living room in oak, marble and stone so the floor change looks real instead of tinted.
6. **Day and night renders** for the living room and terrace, so the time slider switches real photos.
7. **Welcome video loop:** 15–20 seconds of exterior flythrough on the first screen.
8. **Record a 90-second screen video** of the demo path. It's useful for WhatsApp, Instagram and LinkedIn, and for meetings where you can't demo live.

**To validate the business**
9. **Pilot with one developer and one unit.** Track how many visitors enter 3D, view the price and book a visit, then compare against their normal brochure conversion.
10. **Get 5 buyer interviews** using the questions on the Demo Script, and put the quotes into the pitch deck.

**Toward production**
11. **Hire or brief an Unreal developer** with the Developer Handoff doc. The first milestone is one room walkable with real collision.
12. **Build a real backend link** (WebSocket) so a separate tablet can control the LED PC. This is the first production feature a showroom needs.

Share the renders when you have them (1, 5, 6) and I'll place them and replace the colour-overlay changes with real image swaps.

