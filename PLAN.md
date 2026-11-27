# Build for Bharat (Scaler × Wispr Flow): Team Solaris plan

## Context

You and Priyanshu (team **Solaris**) are entered in Scaler × Wispr Flow's "Build for Bharat / India Runs on Voice" hackathon: voice-first tools for India, ₹30 L across 15 teams (₹7 L, ₹5 L and ₹3 L for the top three, then ₹1.25 L each for 4th to 15th, plus Flow Pro, and a Singapore trip and Wispr interview listed as perks; the site notes prize details are still unconfirmed). You asked me to go through everything, set up GitHub (your profile plus a project repo), and plan for the best result. This plan uses the public pages and your live dashboard as of 27 Nov, about 20:10 IST.

**The situation in one line:** Round 2 (the build) opened today and closes 30 Nov, but it stays locked for us until Round 1 passes, and Round 1 stays locked until Wispr verifies your Flow sign-in, which can take up to 24 hours. Every hour Round 1 stays unsubmitted comes out of a three-day build.

### Where we stand
- Registered. Team Solaris is you and Priyanshu Kumar Senapati; you chose to stay at two. The team locks at the first Round 1 submit.
- Round 1: 0 of 3 done. All three activities are locked until Flow is verified. Flow 1.6 is installed and running on this Mac (downloaded 19:47 today).
- Masterclass (25 Nov, Rahul Mathur of DeVC, "From idea to prototype") is marked complete; the recording is "available soon".
- GitHub gd23456: 8 public repos, no profile README, no bio, nothing pinned.
- Keys: Sarvam, plus Gemini/Groq/OpenAI on free tiers, and a paid Anthropic key. Tools: gcloud (project `voyance-demo-2fb3b5`, which already has the ₹100 budget alert), Node, Python 3.11, ffmpeg. Docker is not installed.

### Dates
| When | What |
|---|---|
| 27 Nov, 23:59 IST | Registration closes (we're in) |
| 27–30 Nov | Round 2 build window; it opens for us when Round 1 passes |
| **29 Nov, 23:59** | Round 1 closes: Idea, then Prompt, then Impact, each quality-checked before the next unlocks |
| **30 Nov** | Submit the build (time of day not published). Per the dashboard: codebase on their Docker template, live link, public video walkthrough, idea deck |
| 2 Dec | Live link must still work. Round 2 results and finale shortlist |
| 13 Dec | Finale on campus: build and demo in person to Wispr leadership, AI founders and investors |

Judging criteria are published per round when it unlocks, so we don't have Round 2's yet. The pages contradict each other on some dates (Round 1 close 26 vs 29 Nov, build submit 29 vs 30 Nov), so we work to the earlier date wherever that's cheap.

## How we win
1. **Shrink the gate.** All three Round 1 answers finished and tested tonight, so submitting takes 15 minutes the moment either of you is unlocked. Round 1 is one response per team, so whoever unlocks first submits. If still locked at 12:00 tomorrow, escalate.
2. **Treat Round 1 as points, not a formality.** It shows a score out of 100, prizes go to the highest total score, and the check is likely AI-graded. Answer every part of each question under its own label, with one named user, one place, one language, sourced numbers, and the same persona and metrics across all three activities.
3. **Build everything the problem statement doesn't change before we see it:** a voice kit (speak, transcribe, understand, act, speak back) live on Cloud Run, an accuracy-eval harness, and video and deck skeletons. When the statement arrives we only write domain logic.
4. **Look for the Round 2 statement early.** Teams already through Round 1 can see it; check the Discord (https://discord.gg/ppB3sFzDBV) announcements tonight.
5. **Win a shared problem statement on execution.** Most teams will ship a chatbot with a mic button. We ship: no typing needed anywhere; real code-mixed speech (Hinglish, Kannada-English) plus one low-resource language (Odia); accuracy and latency measured in a table; 3–5 real people tried it, with quotes; "try a sample" buttons so a judge who doesn't speak Kannada still sees it work.
6. **Speak to this jury.** Wispr is a voice company and the finale panel is founders and investors. Lead with the team's record (three shipped voice-for-Bharat projects and Indic speech-recognition research), show cost per conversation in rupees, and show the build happening by voice with Flow.

## Schedule

### Tonight, 27 Nov
- **You, now (10 min):** in Flow, confirm you're signed in with the email you registered with, and dictate a few sentences so the account shows use. Redeem `FLOW4SCALER` (1 month Pro, free) so the free plan's word cap can't stop you mid-build. Join the Discord and look for the Round 2 statement, Docker template, criteria and exact deadline.
- **You to Priyanshu:** install Flow, sign in with his registered email, check his dashboard. Agree that whoever unlocks first submits Round 1.
- **Me:** three idea cards (below). You two talk the chosen one through with Flow for 10 minutes; I turn that into full drafts of all three activities, then run the Prompt draft through an AI app builder to prove it produces a working prototype. You do a final read-aloud edit with Flow.
- **Me, while you decide:** GitHub profile draft, shown to you before anything goes public.
- **Me:** start the voice kit backend and a throwaway Cloud Run deploy.

### Sat 28 Nov
- Submit Round 1 the moment it unlocks; fix any "needs changes" straight away.
- 12:00 and still locked: you send the support email I draft (wispr.support@scaler.com) and post in Discord.
- Voice kit: frontend (I'll ask which design skill you want first, as on Voyance), eval harness, fake-microphone browser test, live on Cloud Run.
- Record 30–40 eval clips: both of you, three languages, quiet and noisy.
- Watch the masterclass's idea-evaluation and testing segments if the recording is up.
- The moment Round 2 unlocks: the first-two-hours playbook below, then the hero flow end to end.

### Sun 29 Nov
- Hero flow working on the live link by midday. Second language. Error paths: silence, wrong language, noise. Confirm-before-acting by voice.
- 3–5 real people try it (a shopkeeper, a relative, campus staff), recorded with consent.
- Evening: eval table, README, deck draft. Round 1 must be completely done today whatever else happens.

### Mon 30 Nov: submission day
- 12:00 feature freeze. 13:00–15:00 record the video; 15:00–17:00 edit and caption it; finish the deck.
- Submit by about 18:00, earlier if Discord gives a cutoff. Open every link logged out on a phone.

### 1–2 Dec
- No feature deploys. Watch the live link until results.

### 3–13 Dec, if shortlisted
- Investor pitch (who pays, distribution, unit economics), a bank of judge questions with answers, a demo that survives bad Wi-Fi (hotspot plus sample clips), two rehearsals, and a short list of features to build on site.

## Round 1: what I'll draft

Three idea cards; you and Priyanshu pick one.

| | Idea | Who has the problem | Why speaking is the way | Builds on |
|---|---|---|---|---|
| A | ASHA voice register (Healthcare) | ASHA workers recording home visits across registers and apps | Visits happen on foot with hands busy, in the local language; typed forms are slow | Neralu's ASHA escalation, Indic ASR |
| B | Kirana voice orders (Small business) | Kirana owners taking orders by voice note and phone call | Customers already order by voice; typing an order list in a regional script is slow | Karigar AI |
| C | Read-aloud fluency check (Education) | Class 1–3 teachers checking each child's reading for NIPUN Bharat | Reading aloud is the assessment itself | indic-bridge (Whisper LoRA) |

Each card is checked against the rubric before you choose: severity, how often it happens, why voice, India-specific insight, can it be prototyped from a prompt, can impact be measured, and team credibility.

How the three answers are built:
- **Activity 1, Idea:** who has the problem (one named persona, place, language), the moment it hurts, why speaking is the way, and what the product does, each under its own label.
- **Activity 2, Prompt:** a build-ready prompt: goal, user, the voice flow step by step, screens, data with sample entries in the local language, rules, in-browser speech for the prototype, accessibility, acceptance tests, out of scope. Tested in an AI app builder before submitting.
- **Activity 3, Impact:** primary and secondary beneficiaries with sourced sizes, what changes for them, three measurable indicators and how a two-week pilot would collect them, and one risk with its mitigation.
- Every number gets a source (Census, NFHS, ASER, NHM and similar). Word limits aren't visible until it unlocks, so each answer also gets a trimmed version.

## Round 2: the build

### Voice kit (tonight and tomorrow, independent of the statement)
One container listening on `$PORT`, so it drops into whatever Docker template they give:
- `app/` FastAPI: `/api/stt` (Sarvam speech-to-text with language auto-detect; Whisper on Groq or OpenAI as fallback), `/api/turn` (Claude structured output: reply plus action JSON), `/api/tts` (Sarvam Bulbul; the browser's own speech as fallback), `/healthz`. Per-IP rate limit and a maximum clip length, because the Anthropic key is paid and the link is public.
- `web/` React, Vite and TypeScript: one large mic button (hold or tap), live captions, a language chip, read-back with confirm or cancel by voice, "try a sample" clips, typing only as an accessibility fallback.
- `eval/`: labelled clips scored for character and word error rate per language, task success and median latency.
- `e2e/`: Playwright with Chrome's fake microphone fed from WAV files, so the voice flow is tested without a person.
- `deploy/cloudrun.sh`: free-tier settings (0 to 1 instances, 512 MiB, CPU throttling).

Reused, not rewritten:
- `~/Neralu/backend/app/transcribe.py`: the Sarvam `saaras:v4` call and its provider registry become the speech-to-text adapter.
- `~/indic-bridge/src/normalize.py` (`normalize_text`) and `~/indic-bridge/src/evaluate.py` (`score_all`, `script_validity`, `per_utterance_errors`): scoring for Indic transcripts.
- `~/voyage/deploy/cloudrun.sh`, `~/voyage/Dockerfile`, `~/voyage/e2e/playwright.config.ts`: deploy, container and browser-test setup.
- Karigar's rule: the full flow still completes with no network or key (sample mode), so a demo never dead-ends.

Claude through the official Python SDK, with structured outputs and refusal fallback enabled. Default model `claude-opus-5-5` at low effort. `claude-haiku-5-5` is about 40 times cheaper and faster; you choose after we time both on 20 real utterances. Set a spend limit in the Anthropic console before the link goes public.

### First two hours after the statement unlocks
1. Copy the statement, criteria, rules, template link and exact deadline into `PS.md`.
2. Decode it in 20 minutes: one user, one moment, why voice, one measurable outcome. Map every criterion to a moment in the demo.
3. Write the hero flow as one sentence: "<user> says <utterance, language> and <outcome> happens within N seconds."
4. Deploy the template untouched within the first hour, so a live link exists from the start; then move the voice kit in.
5. Write down what we won't build, split the lanes, build.

### Deliverables
- **Codebase:** on their template. README with demo link, video, screenshots, architecture diagram, three-command setup, `.env.example`, eval table, limitations, AI-use note, and "built by voice with Wispr Flow". No keys in git.
- **Live link:** Cloud Run over HTTPS (the mic needs it), sample clips, no login, tested on iPhone Safari and Android Chrome, up until 2 Dec.
- **Video, 2–3 minutes, on YouTube:** a real user and the problem; the live demo by voice in two languages with captions; how it works and the accuracy numbers; impact and what's next; ten seconds of us building by voice with Flow.
- **Deck, about 10 slides, made as an artifact and exported to PDF or PPTX:** problem, user, why voice, demo, how it works, evidence, impact (from Round 1 Activity 3), business and distribution, cost per conversation, roadmap, team.

## GitHub

### Your profile (gd23456)
- A new public repo `gd23456/gd23456` with a README: a one-line positioning ("software people use by speaking, in the languages India speaks"), "Now building: Solaris, Build for Bharat 2026", selected work with factual one-liners only (indic-bridge; Karigar AI for SIH 2026; Kshana, 88 ms per image on an iPhone 15; Neralu, Hack4SDG 2026 finale, as contributor), toolbox, and contact. No stats widgets and no invented numbers.
- A bio set through `gh api`. Six pins, which you click in "Customize your pins" because GitHub has no API for them: solaris, indic-bridge, SIH2026, cv-hackathon, Neralu, and voyage if it's public.
- I show you the README and bio first. Nothing goes public without your yes.

### Project repo
- `gd23456/solaris`, private, created once the template is known: from the template if it's a GitHub template, otherwise with the template as the first commit. Priyanshu (`Priyanshu-senapati`) added as a collaborator. Made public at submission, on your yes.
- Local copy at `~/solaris` with its own `git init`. Your home folder is a git repo, so I check the repo root before every git command. Strategy notes and Round 1 drafts stay local-only via `.git/info/exclude`.

## Lanes
- **You:** product and voice: web UI, speech in and out, deploy, eval, video edit, GitHub.
- **Priyanshu:** engine: domain logic and rules for the statement, data, API; deck research and numbers; user tests.
- **Both:** the idea pick, eval recordings, video voiceover, final checks.
- **Me:** drafts, code alongside both lanes, sourced research, checklists.

## Decisions I'll ask at the time
- Claude model for the app, after timing Opus 5.5 against Haiku 5.5.
- Whether the public repo's commits carry a Claude co-author line (cv-hackathon and voyage had none).
- Cloud Run in `voyance-demo-2fb3b5` (already budget-guarded) or a new project.
- Installing Docker (OrbStack) or building only on Cloud Build.
- Which design skill to use for the frontend.

## Risks and fallbacks
| Risk | Fallback |
|---|---|
| Flow verification takes the full 24 hours | Priyanshu submits if he unlocks first; support email and Discord at 12:00 on 28 Nov |
| A Round 1 answer comes back "needs changes" | Trimmed versions already written; revise in minutes |
| Round 2 shrinks to about two days | Voice kit and deploy ready beforehand; one hero flow only |
| Free-tier rate limits while judges test | Cached speech for fixed lines; fallback speech-to-text; sample mode works offline |
| The public link runs up the paid Anthropic key | Key stays on the server; per-IP limit; capped output tokens; console spend limit |
| The mic fails on a judge's phone | HTTPS; tested on iOS and Android; sample clips need no mic |
| Their Docker template doesn't fit our stack | The kit is one container on `$PORT`; we adapt to the template, never the reverse |
| Unknown cutoff time on 30 Nov | Submit by 18:00; check Discord for the exact time |

## Verification
- **Round 1:** each activity shows a pass on the dashboard and the Round 2 card unlocks.
- **Voice kit:** unit tests on the structured output and rules; `eval/` prints error rates per language (indic-bridge scoring) and task success; the fake-microphone Playwright run passes end to end; the Cloud Run URL works on iPhone Safari and Android Chrome; cold start timed.
- **Submission:** every link opened logged out on a phone; the video plays without sign-in; the README renders; Cloud Run logs show judges' requests succeeding through 2 Dec.
- **Profile:** github.com/gd23456 opened logged out shows the README and pins, and no private details.

## Next moves (on hold until the idea is refined)
1. Save this hackathon to memory.
2. Three idea cards with sourced numbers in `~/solaris/round1/ideas.md`.
3. GitHub profile README and bio draft for your review.
4. Full Round 1 drafts for the idea you pick; the prompt tested in an AI app builder.
5. Voice kit backend and a throwaway Cloud Run deploy.
6. Optional: publish this plan as a private page you can share with Priyanshu.
