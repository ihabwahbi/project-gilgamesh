## Drawer Organiser — MVP Build Brief (24–48 hr “Pilot” version)

### 1) What this is (one sentence)

A **MyGov-style hub for ADC Part 2 candidates**: one login → community + OSCE case rooms + study partner matching, with strict “no exam content” rules.

### 2) The MVP goal

Ship a **working pilot** that proves:

* Candidates can sign up and use the platform safely
* The community features work (rooms, posting, basic moderation)
* Study partner matching works (the “killer feature” for early traction)

Everything else is “Phase 2+”.

---

## 3) Non-negotiables (must-have rules)

1. **No exam content policy** baked into UI + ToS checkbox on signup

   * Clear footer on all pages: “No exam content. Educational guidance only.”
2. **Privacy & security first**

   * Email verification
   * Rate limiting on login/signup
   * Basic anti-spam (captcha optional)
3. **MVP must be deployable** (real URL, SSL, database, backups)
4. **Mobile-friendly** (most candidates will use phones)

---

## 4) User roles (simple)

* **Candidate (default)**: can join rooms, post, comment, DM (optional), create study partner profile.
* **Mentor (flagged)**: same as candidate + badge (no special perms in MVP unless easy).
* **Admin**: moderate posts, ban users, manage rooms, view reports.

*(Don’t overcomplicate permissions on day one.)*

---

## 5) Core MVP features (Phase 1)

### A) Auth + Profiles

* Signup/login (email + password)
* Profile fields:

  * Display name (can be anonymous handle)
  * City/State (Australia + “Overseas” option)
  * Exam stage (Written / Practical / OSCE / Waiting results)
  * Availability (days/times)
  * Study goals (free text)
  * Privacy toggle: show/hide from public matching

### B) OSCE Rooms (48 case rooms) — Reddit-lite

* Pre-created **rooms** (seed list can be placeholders now; exact 48 later)
* Inside each room:

  * Posts (title + body)
  * Comments
  * Upvote/downvote optional (nice-to-have)
* Global feed page: latest posts across rooms
* Reporting: “Report post” button

### C) Study Partner Matching (MVP version)

* Search/filter candidates by:

  * Location (state/city)
  * Exam stage
  * Availability
* “Request to connect”:

  * Either DM system (simple inbox) **OR** “share contact” request flow (safer)
* Reviews/ratings: **Phase 2** (skip unless trivial)

### D) Moderation basics

* Admin dashboard:

  * List users
  * List posts
  * View reports
  * Delete post/comment
  * Ban user (soft ban is fine)

---

## 6) Nice-to-have (only if time)

* Tagging posts (“Medical history”, “Communication”, “Emergency”, “Ethics”)
* Mentor badge + “mentor-verified” post marker (careful: don’t create liability)
* Simple onboarding walkthrough modal (3 screens)

---

## 7) Explicitly OUT of scope for MVP (do not build now)

* Payments/subscriptions (Stripe)
* Course provider directory + capacity meter + waitlists
* Marketplace buy/sell
* News page + verification workflows
* Points/badges system
* Video hosting / session scheduling
* OSCE trends index (crowdsourced stats)

These will kill speed if you touch them.

---

## 8) Suggested tech stack (fast + sane)

Pick whatever Ehab is fastest in, but for speed:

* **Next.js + Supabase** (Auth + Postgres + Storage)
  OR
* **Django + Postgres** (if he’s a backend wizard and wants control)
* Deploy: **Vercel** (Next) or **Render/Fly.io** (backend)

---

## 9) Data model (minimum tables)

* `users` (auth id, role, handle, location, stage, availability, privacy)
* `rooms` (name, slug, description)
* `posts` (room_id, user_id, title, body, created_at)
* `comments` (post_id, user_id, body, created_at)
* `reports` (type, target_id, reason, reporter_id, status)
* `connections` (requester_id, receiver_id, status)

---

## 10) UI pages (MVP)

* `/` Landing (what it is + rules + CTA signup)
* `/signup` `/login`
* `/feed` Global feed
* `/rooms` list of rooms
* `/rooms/[slug]` room page
* `/posts/[id]` post page
* `/match` partner matching search
* `/profile` edit my profile
* `/admin` moderation dashboard (admin only)
* Static: `/terms` `/privacy` `/rules`

---

## 11) Acceptance checklist (so you know it’s “done”)

* I can signup, verify email, login/logout
* I can edit profile and toggle privacy
* I can view rooms, create post, comment
* I can search study partners and send a connection request
* Admin can delete a post and ban a user
* Policy footer exists on all pages + signup checkbox exists

---

## 12) Content seed (I will supply, unless he wants placeholders)

* Room names list (48 OSCE cases)
* Rules text (no exam content, respectful conduct, no doxxing, etc.)
* Landing page copy (short)

---

## 13) Blunt warning (so Ehab doesn’t accidentally build the wrong thing)

If he tries to build **“the full platform”** in 24 hours, he’ll ship a pretty carcass. The MVP must be **community + matching** only. That’s the proof-of-value.