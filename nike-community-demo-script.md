# Nike Member Community: demo script

File: `nike-community.html` (single page, open in any browser, state saved in the browser).
Reset anytime with **↺ Restart** (top right). Total run time: about 12 minutes.

All Nike content is illustrative. Detection, video and "send to admin" are simulated in the prototype (see the last section for what a real build needs).

---

## 0. Setup (30 sec)
- Open the file. Top bar shows **View as: Member**. You are **Alex Chen**, rank and points are in the top bar.
- Say: "Next-gen customers arrive from ChatGPT or Google already wanting proof from real people. Community is how a brand earns that trust, and how it catches AI-generated noise."

## 1. Arrive from ChatGPT (1 min)
- Entry screen: a runner asked ChatGPT why Nike Run Club runs are not syncing to Apple Health.
- Point out the three generic causes, then the call to action to the Nike Member Community.
- Say: "The AI answer is generic. The next question is always 'has this worked for real people?'"
- Click **Open the community**. (Switch the source chip to Google or Help Center to show other entry points.)

## 2. Landing and the Agent answer (2 min)
- Alex's question sits in the chat. The **Agent** answers from the knowledge base.
- Click the format tabs: **Text**, **Podcast**, **Diagram**.
- Click **Video**: press **Play**. Show pause, seek bar, **1× / 1.5× / 2×**, **CC**, and the four step chips. The label says AI-generated until staff review, plus the sources it was built from.
- Let it reach the end. Click **Yes, it worked**: question marked resolved, points awarded, Nike sees a deflected case.
- Say: "Video is generated from approved knowledge and labelled until a human verifies it."

## 3. Expert match and connections (2 min)
- **Expert Match** shows peers matched by topic (Tasha Obi, Dev Anand).
- Click **Add connection**, edit the note, **Send request**. It shows **Request sent**, then accepts itself after about 2 seconds.
- Open **Connections** in the sidebar: accept Leo Park's incoming request, then **Message** him. Send a message, a reply arrives. Click **Huddle** to show the huddle banner, then **Leave**.
- Say: "Peer connections turn a help site into a network. Real audio and live presence come from Slack in a real build."

## 4. Trust: responses, validation, AI flags (3 min)
- In **Trending for you**, click **See responses** on the sync question: each reply has a trust label.
  - **Community-validated** (3 or more helpful votes), **Validated by Nike**, **AI-written**, **AI-flagged**, **Unvalidated**.
- Click **🔍 Check if AI-generated** on any post or **🔍** on any reply: percentage, verdict and the signals found.
- Open the Pegasus sizing question (**Open**). The AI reply says all models run true to size and is flagged. As a member it is **hidden while Nike checks it**.
- Use the thread filter chips: **All answers / Validated / AI & flagged**.
- Click **👍 Helpful** on a reply (once per reply). **🚩 Report as AI-generated** on a member reply sends it to staff.
- Post a reply that says "Certainly! I hope this helps." with the AI box unticked: it is flagged automatically and earns no points. Tick **I used AI to help write this** and it is labelled instead.
- Find the question from **PromoBot** (filter **AI-posted**): a brand-new account posting a listicle-style prompt. It shows **Posted by AI · under review**, earns no points, and is off the leaderboard.
- Post your own question with AI wording to show auto-flagging, or tick **I used AI to write this question** to show the disclosed label.
- Say: "Members can see exactly what is human, validated, AI-written or flagged."

## 5. Ask a new question (30 sec)
- Type "size for wide feet?": the knowledge base answer appears before posting (deflection).
- Post it: +2 points, the feed updates.

## 6. Feedback and ideas (1 min)
- **Ideas & feedback**: submit an idea, vote on others (▲). Ideas reaching 100 votes auto-route to Product.
- Shipped items show **You said, we did**.

## 7. Gamification (1 min)
- Always visible: rank and points in the top bar, **Your standing** and progress to the next badge in the right rail, mini leaderboard, **Recent activity**.
- **Leaderboard** page: podium, ranking, click a person for their profile with Message, Huddle, Add connection.
- Points rules: +10 helping resolve, +5 resolving, +3 feedback, +2 posting, +1 idea votes. AI answers and flagged posts earn nothing.
- On a thread, click **✅ This fixed it** (on your own question that has replies) and watch helpers get points.

## 8. Switch to Nike staff (3 min)
- Top bar: **View as → Nike staff (admin)**.
- **Admin insights**:
  1. **AI-flagged answers**: approve or remove flagged replies, mark flagged questions human-verified or remove as spam.
  2. **Most-asked questions**: the questions members ask most. **Send to admin** puts it in the admin queue.
  3. **Knowledge gaps**: questions with no verified answer. **Draft KB article**, then **Review and publish**. After publishing, the Agent answers it from the knowledge base and a member typing it sees the answer.
  4. **Product and service feedback**: ranked by votes, **Route to Product**, set status (Under review, Planned, Shipped).
- On any thread: **✓ Validate** a member reply. It becomes a verified answer and the author earns +5.
- **Video studio**: render settings, pipeline (script, scenes, voiceover, render), render the sizing video, **Verify and publish** to remove the AI-generated label.
- Switch back to Member to show the label change.

## Closing line
"Community gives the AI answer proof, catches AI-generated noise, finds what our knowledge base is missing, and turns customer feedback into product input."

---

## Using this in a customer community help site

**What this prototype is:** a clickable UI with seeded data and simulated behaviour. It is not connected to any back end.

| Prototype piece | Simulated today | Real build |
|---|---|---|
| Entry from ChatGPT / Google | Static screen | Referrer detection plus a landing page that carries the user's question and the generic answer. |
| Agent answer | Fixed knowledge base text | Agent grounded on the knowledge base and verified community posts, with citations, excluding flagged posts. |
| Troubleshooting video | Animated mock screens | Video generation service fed by approved articles, with staff review before the label changes. |
| Expert match | Keyword match | Match on topics, past solved answers and availability. |
| Connections, messaging, huddles | In-page state and canned replies | Slack or Experience Cloud messaging and calls. |
| AI check | Wording heuristic | A detection service plus account signals (age, posting pattern). Always a human decision. |
| Leaderboard and badges | Local points | Points service tied to member profiles. |
| Admin insights | Computed from page data | Reports on real posts, search and case data, with a queue into the admin and product tools. |

**Suggested rollout on a help site**
1. **Phase 1, read and trust:** show community answers with trust labels next to knowledge base articles; AI answers cite them. No posting yet.
2. **Phase 2, ask and answer:** members post, community validation and staff validation live, AI disclosure and flagging on.
3. **Phase 3, loop back:** most-asked and knowledge-gap reports to the admin, article drafting, idea voting routed to product.
4. **Phase 4, network:** connections, expert match, leaderboard rewards, video generation.

**Metrics to track:** deflection (questions resolved without a case), share of answers validated, AI-flagged rate and review time, knowledge gaps closed per month, ideas shipped, and traffic arriving from chat assistants.

**Decisions to make first:** who validates answers (staff, trusted members, both), how AI-written content is disclosed, what happens to flagged content, and what members earn points for.

---

## Embedding in the customer's branding

**Principle:** the community should look like the customer's site, not like a Slack or Salesforce product. The trust labels (validated, AI-written, AI-flagged) stay consistent in meaning but take the brand's styling.

### Three levels of branding
| Level | What the customer controls | Effort |
|---|---|---|
| 1. Theme | Logo, colors, fonts, corner radius, hero image, button style | Low. Design tokens only. |
| 2. Layout and content | Navigation names (for example "Run Club" instead of "Community"), which sections show (ideas, leaderboard, video), badge names and artwork, point rules | Medium. Configuration. |
| 3. Embedded experience | Runs inside the customer's own header, footer, login and domain (for example `help.brand.com/community`) | Higher. Needs site integration. |

### Level 1: what to expose as tokens
In this prototype the look comes from a few CSS variables and a hero gradient at the top of the file:
- `--org` (primary action color), `--grn` (success and validated), `--blue` (links and selection), `--aub` / `--aub2` (the dark navigation).
- The hero gradient, brand name in the top bar and welcome text.
- Badge names (Newcomer, Helper, Gear Guru, Pace Setter) and the "Nike staff" label.

A real build turns these into a brand settings page: logo, primary and secondary color, font, badge names and art, staff label, and tone for AI-written text.

**Keep fixed, not brandable:** the meaning of the trust labels and the "AI-generated" disclosure. Customers can restyle them, not remove them. That is what makes the community credible.

### Level 3: how it sits in the customer's site
1. **Same domain and shell.** Serve it under the customer's help site path so the header, footer, search and cookie banner are theirs.
2. **Single sign-on.** Members sign in with the customer's existing account, so the profile, purchase history and Run Club data link to the same identity. Public readers see answers without logging in; posting needs login.
3. **Search and agent entry.** The help site search and the site's AI assistant both pull from community answers (validated only) and link back with citations.
4. **Chat-referred traffic.** Pages need clean, indexable answers so ChatGPT or Google can cite them, with schema markup for questions and accepted answers. This is how the "arriving from ChatGPT" journey in the demo starts.
5. **Components, not an iframe, where possible.** Embed as components inside the site so styling inherits from the page. An iframe is the quick start but the styling, deep links and accessibility are harder.
6. **Staff roles.** Map the customer's support team and community leaders to the staff and validator roles; the "Nike staff" label becomes the customer's own.

### Brand-specific things to agree with each customer
- Voice and naming: member, runner, fan, customer. Leaderboard names and badge art.
- Rewards: points only, or also real perks. Point rules and any limits.
- Moderation: who validates, response-time targets, what happens to flagged content, and how AI disclosure is worded.
- Legal and privacy: display names, public versus members-only content, data retention, and regional rules.
- Accessibility and languages: contrast of brand colors against the label styles, captions on videos, and translations.

### Demo tip
To show branding live, duplicate the file and change the brand name, the `--org` color, the hero gradient and the badge names. The same flows work for any brand. A natural next step is a small theme switcher in the prototype (Nike, a bank, an airline) to show the same community in three brandings.

---

## Update: setup first, then community features

**Tab ① Set up with Claude** (`portal-setup.html`, Salesforce Setup look). Type one sentence, e.g. "Set up a community for Adidas, blue, no video, flag after 5", or click **Quick setup**. Claude fills a 7-step path (Site, Brand, Agent & knowledge, Features, Moderation & trust, Access & growth, Review). Click **Activate**, then **Open community**: name, colour, menu and flag threshold follow the setup. **↺ Restart both** clears it.

Community features: categories and tags with Latest/Top, trust levels TL0-TL4 (flagging and polls unlock at 20 pts), badges (bronze/silver/gold) on the Leaderboard page, flag reasons, AI topic summary, polls, chat channels, notifications, markdown and attach. Simulated: attachments, chat replies, summary text, SSO/SEO/2FA toggles (setup records them, nothing enforces them).

**Repeated questions loop.** In setup, Claude asks how to handle repeated questions: highlight to admin, draft a KB article and add to product feedback (automatic), highlight only, or off, plus the threshold (25/50/100/200 members). In the community, switch to Nike staff, open **Admin insights**: the **Repeated questions** card lists the highlighted questions, a KB draft is ready to review and publish, and a "Fix needed" item appears in product feedback. Simulated: the KB draft text and the counts.
