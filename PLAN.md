# Build for Bharat (Scaler × Wispr Flow): Team Solaris plan

## Context

You and Priyanshu (team **Solaris**) are entered in Scaler × Wispr Flow's "Build for Bharat / India Runs on Voice" hackathon. The theme is voice-first tools for India. The prize pool is ₹30 L across 15 teams: ₹7 L, ₹5 L and ₹3 L for the top three, then ₹1.25 L each for 4th to 15th, plus Flow Pro, with a Singapore trip and a Wispr interview listed as perks. The site notes that prize details are still unconfirmed. This plan uses the public pages and your live dashboard as of 27 Nov, about 20:10 IST. It was updated on 28 Nov with the team's change proposals (see the last section).

**The situation in one line:** Round 2 (the build) opened on 27 Nov and closes 30 Nov. It stays locked for us until Round 1 passes, and Round 1 stays locked until Wispr verifies your Flow sign-in, which can take up to 24 hours. Every hour Round 1 stays unsubmitted comes out of a three-day build.

### Where we stand
- Registered. Team Solaris is you and Priyanshu Kumar Senapati; you chose to stay at two. The team locks at the first Round 1 submit.
- Round 1: 0 of 3 done. All three activities are locked until Flow is verified. Flow 1.6 is installed and running on your Mac (downloaded 27 Nov, 19:47).
- Masterclass (25 Nov, Rahul Mathur of DeVC, "From idea to prototype") is marked complete; the recording is "available soon".
- GitHub: the private repo `gd23456/solaris` holds this plan, and Priyanshu is invited with write access. Your profile gd23456 has 8 public repos, no profile README, no bio and nothing pinned.
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

Judging criteria are published for each round when it unlocks, so we don't have Round 2's yet. The pages contradict each other on some dates: Round 1 closes on 26 or 29 Nov, and the build is due on 29 or 30 Nov. **Ask the organisers for the exact build cutoff** on Discord or at wispr.support@scaler.com. Until they answer, have a version ready to submit by 29 Nov 23:59, the earliest date shown publicly, and do the final submission on 30 Nov.

## How we win
1. **Shrink the gate.** All three Round 1 answers are finished and tested before Round 1 unlocks, so submitting takes 15 minutes the moment either of you gets in. Round 1 is one response per team, so whoever unlocks first submits. If it's still locked at 12:00 on 28 Nov, escalate.
2. **Treat Round 1 as points, not a formality.** It shows a score out of 100, prizes go to the highest total score, and the check is likely AI-graded. Answer every part of each question under its own label. Use one named user, one place, one language and sourced numbers, and keep the same persona and metrics across all three activities.
3. **Build everything the problem statement doesn't change before we see it.** That means a voice kit (speak, transcribe, understand, act, speak back) live on Cloud Run, an accuracy-eval harness, and video and deck skeletons. When the statement arrives, we only write domain logic.
4. **Look for the Round 2 statement early.** Teams already through Round 1 can see it, so check the Discord (https://discord.gg/ppB3sFzDBV) announcements.
5. **Ship one focused workflow that does four things well:**
   - **Natural Indian speech:** the languages, accents and code-mixing the statement's users actually speak.
   - **Understand before acting:** notice missing or ambiguous information and ask about it.
   - **Complete a real task:** validated domain logic and a saved result, not just a chat reply.
   - **Prove reliability:** task completion, recognition quality, latency and real-user results, all measured.

   Most teams will ship a chatbot with a mic button. We also add "try a sample" buttons, so a judge who doesn't speak the language still sees it work.
6. **The LLM interprets; code decides.** The model only turns speech into structured fields. Plain code validates those fields, asks for confirmation and executes. Model output never writes data or triggers an action on its own.
7. **Speak to this jury.** Wispr is a voice company, and the finale panel is founders and investors. Lead with the team's record: three shipped voice-for-Bharat projects and Indic speech-recognition research. Show cost per task in rupees, and show the build happening by voice with Flow.

## Schedule

### Milestones
| Milestone | Done when |
|---|---|
| **M1 Baseline** | The organisers' template runs locally and on the live link, `docs/PROBLEM_STATEMENT.md` is written, and both of you can explain the exact problem in one sentence |
| **M2 End to end** | A judge can go from speech to a saved result on the live link |
| **M3 Submitted** | Every deliverable opens from a fresh logged-out session, no secrets or internal notes are exposed, and proof of submission is saved |

If the confirmed deadline differs from the dates below, move the dates but keep the milestones in the same order.

### 27 Nov, night
- **You (10 min):**
  - In Flow, confirm you're signed in with the email you registered with, and dictate a few sentences so the account shows use.
  - Redeem `FLOW4SCALER` (1 month Pro, free) so the free plan's word cap can't stop you mid-build.
  - Join the Discord and look for the Round 2 statement, the Docker template, the criteria and the exact deadline.
- **You to Priyanshu:** install Flow, sign in with his registered email and check his dashboard. Whoever unlocks first submits Round 1.
- **Me:**
  - Write three idea cards (below). You two talk the chosen idea through with Flow for 10 minutes.
  - Turn that into full drafts of all three activities. Run the Prompt draft through an AI app builder to prove it produces a working prototype.
  - You do a final read-aloud edit with Flow.
- **Me, while you decide:** a GitHub profile draft, shown to you before anything goes public.
- **Me:** start the voice kit backend and a smoke deploy to the `solaris` Cloud Run service.

### Sat 28 Nov
- Submit Round 1 the moment it unlocks, and fix any "needs changes" straight away.
- At 12:00, if it's still locked: you send the support email I draft (wispr.support@scaler.com), post in Discord, and ask for the exact build cutoff.
- Voice kit: frontend (I'll ask which design skill you want first, as on Voyance), eval harness, fake-microphone browser test, live on Cloud Run.
- Record 30–40 eval clips: both of you, in the two target languages, quiet and noisy.
- Watch the masterclass's idea-evaluation and testing segments if the recording is up.
- The moment Round 2 unlocks: run the first-two-hours playbook below and reach **M1**, then build the hero flow end to end.

### Sun 29 Nov
- **M2** by midday: the hero flow works on the live link.
- After that: the second language, the failure cases (table below), and confirm-before-acting by voice.
- 3–5 real people try it (a shopkeeper, a relative, campus staff), recorded with consent.
- **By 23:59, have a version ready to submit** (live link, README, rough video, deck draft) in case the cutoff turns out to be 29 Nov. Round 1 must also be completely done today, whatever else happens.

### Mon 30 Nov: submission day
- 12:00: feature freeze.
- 13:00–15:00: record the video. 15:00–17:00: edit and caption it, and finish the deck.
- Submit by about 18:00, or earlier if the organisers give an earlier cutoff, then reach **M3**.

### 1–2 Dec
- No feature deploys. Watch the live link until results.

### 3–13 Dec, if shortlisted
- An investor pitch covering who pays, distribution and unit economics.
- A bank of likely judge questions with answers.
- A demo that survives bad Wi-Fi (hotspot plus sample clips).
- Two rehearsals.
- A short list of features to build on site.

## Round 1: what I'll draft

**Status 28 Nov:** Round 1 is unlocked. The team picked **A, the ASHA home visit** (product name *Bheti*). Paste-ready answers are local-only in `round1/` (`1_idea.txt`, `2_prompt.txt`, `3_impact.txt`).

**How the dashboard grades it** (from the site's own activity rules):
| Activity | Points | Limit | Graded on |
|---|---|---|---|
| 1. Idea | 0 (pass/fail) | 50–500 words | One everyday task, its voice-only version, and users in India. Fails on gibberish, duplication, copied questions, off-topic text, or being too general |
| 2. Prompt | 50 | 1,000 words | Theme fit 25%, completeness 25%, clarity and specificity 20%, buildability 15%, originality 15%. **The accepted prompt is final** |
| 3. Impact | 25 | 1,000 words | Theme fit 25%, impact 25%, specificity and reasoning 20%, adoption feasibility 15%, originality 15% |

Activities unlock one after another. Sign up for Wispr Flow before submitting Activity 3 to stay eligible for the Round 1 prizes.

**These three ideas are for Round 1 only.** Round 1 has to be submitted before the Round 2 statement is visible, so it needs one idea now. The Round 2 product follows the official statement, whatever we pick here.

| | Idea | Who has the problem | Why speaking is the way | Builds on |
|---|---|---|---|---|
| A | ASHA voice register (Healthcare) | ASHA workers recording home visits across registers and apps | Visits happen on foot with hands busy, in the local language; typed forms are slow | Neralu's ASHA escalation, Indic ASR |
| B | Kirana voice orders (Small business) | Kirana owners taking orders by voice note and phone call | Customers already order by voice; typing an order list in a regional script is slow | Karigar AI |
| C | Read-aloud fluency check (Education) | Class 1–3 teachers checking each child's reading for NIPUN Bharat | Reading aloud is the assessment itself | indic-bridge (Whisper LoRA) |

Before you choose, each card is checked against these questions: how severe the problem is, how often it happens, why voice, what's specific to India, whether it can be prototyped from a prompt, whether impact can be measured, and whether the team is credible on it.

How the three answers are built:
- **Activity 1, Idea:** who has the problem (one named persona, place and language), the moment it hurts, why speaking is the way, and what the product does, each under its own label.
- **Activity 2, Prompt:** a build-ready prompt covering:
  - goal and user
  - the voice flow, step by step
  - screens
  - data, with sample entries in the local language
  - rules
  - in-browser speech for the prototype
  - accessibility
  - acceptance tests
  - what's out of scope

  It's tested in an AI app builder before submitting.
- **Activity 3, Impact:** primary and secondary beneficiaries with sourced sizes, what changes for them, three measurable indicators and how a two-week pilot would collect them, and one risk with its mitigation.
- Every number gets a source (Census, NFHS, ASER, NHM and similar). Word limits aren't visible until Round 1 unlocks, so each answer also gets a trimmed version.

## Round 2: the build

### Voice kit (built before the statement, works for any statement)
One container listening on `$PORT`, so it drops into whatever Docker template the organisers give. One clear pipeline, no multi-agent setup.

**The journey**
1. The user starts a voice turn by holding or tapping the mic.
2. The app records the clip and uploads it.
3. Speech-to-text runs, and the app shows the transcript and the detected language.
4. The LLM extracts fields into a strict schema.
5. Code checks required fields, formats, ranges and ambiguity.
6. If something is missing or unclear, the app asks one short question about just that.
7. The app reads back the key details and asks for confirmation before anything consequential.
8. The action runs once (a request ID makes retries safe) and is saved.
9. The app shows and speaks a completion receipt with a reference ID.
10. The user can correct or undo, where the domain allows it safely.

**States:** `idle`, `recording`, `uploading`, `transcribing`, `understanding`, `needs_clarification`, `awaiting_confirmation`, `executing`, `speaking`, `completed`, `error`.

**Languages**
- Two language experiences first, chosen from the statement's users (for example Hindi-English and Kannada-English). Odia only once those two pass the eval.
- Language is detected automatically, with a manual language picker as fallback.
- The original transcript is kept beside the normalised values. Numbers, quantities, dates and names are normalised without changing their meaning.
- Low confidence or a missing field triggers a question, never an action.
- Check that text-to-speech supports every language we claim. Its language list can differ from speech-to-text's.

**Providers**
- **Speech-to-text:** Sarvam `saaras`. At most one fallback (Whisper via Groq or OpenAI), and only if testing shows it earns its place.
- **Text-to-speech:** Sarvam Bulbul, with the browser's own speech as fallback.
- **LLM:** Claude through the official Python SDK, with structured outputs and refusal fallback. Time Haiku 5.5 and Opus 5.5 on 20 real utterances (accuracy, latency, cost), then pick, and use the stronger model only where tests show a clear gain. Set a spend limit in the Anthropic console before the link goes public.

**Storage:** Firestore's free tier, in the same GCP project. Each task gets one record: ID, timestamps, status, fields, validation and confirmation status, error code and timings. Never use container disk, because a Cloud Run restart wipes it. Store the minimum, keep no raw audio unless it's needed and consented to, and write down a retention rule.

**Failure handling**
| Case | Behaviour |
|---|---|
| Background noise | Ask the user to repeat or move somewhere quieter |
| No speech detected | Show a clear prompt to speak |
| Unsupported language | Offer the language picker |
| Low-confidence transcript | Ask for confirmation or a repeat |
| Missing required field | Ask one focused question |
| Ambiguous value | Show what we understood so the user can correct it |
| Speech or LLM timeout | Show a retry state, keeping whatever progress is safe |
| Provider down | Offer the clearly labelled sample mode |
| Duplicate request | Detect it and don't execute twice |
| Invalid action | Explain the problem; write nothing invalid |

**Sample mode:** clearly labelled. It runs the same UI and workflow on fixed sample inputs, and it never pretends that a live provider or a real action succeeded. It works with no network and no key (Karigar's rule), so a demo never dead-ends.

**Interface**
- A large, accessible mic with a waveform.
- Clear listening, processing, speaking and error states.
- The transcript appears after each clip; no fake streaming captions.
- An editable transcript and confirmation card, and native-language feedback.
- A completion receipt with a reference ID.
- "Try a sample" for judges, and a compact eval panel.
- States for a denied or unavailable microphone.
- Keyboard access with visible focus.
- Tested on iPhone Safari and Android Chrome. Typing is only an accessibility fallback.

**Deploy:** one Cloud Run service, `solaris`, used for both the early smoke test and the final app. Free-tier settings: 0 to 1 instances, 512 MiB, CPU throttling. Per-IP rate limit and a maximum clip length, because the Anthropic key is paid and the link is public.

**Layout** (adapted to the organisers' template; their required files come first):
```text
app/api/        voice.py, transcription.py, actions.py
app/core/       orchestrator.py, intent.py, validation.py, confirmation.py
app/providers/  sarvam.py, asr_fallback.py, tts.py
app/storage/    Firestore access
web/src/        components/, pages/, services/
eval/           dataset/, metrics.py, report.md
tests/          unit/, e2e/ (Playwright with Chrome's fake microphone fed from WAV files)
docs/           PROBLEM_STATEMENT.md, architecture.md, user-testing.md
deploy/         cloudrun.sh
Dockerfile, .env.example, .gitignore, README.md
```

**Reused, not rewritten:**
- `~/Neralu/backend/app/transcribe.py`: the Sarvam `saaras:v4` call and its provider registry become `app/providers/sarvam.py`.
- `~/indic-bridge/src/normalize.py` (`normalize_text`) and `~/indic-bridge/src/evaluate.py` (`score_all`, `script_validity`, `per_utterance_errors`): scoring for Indic transcripts in `eval/metrics.py`.
- `~/voyage/deploy/cloudrun.sh`, `~/voyage/Dockerfile` and `~/voyage/e2e/playwright.config.ts`: deploy, container and browser-test setup.

**Leave out** unless the statement needs them: multi-agent orchestration, vector databases, an analytics dashboard, several speech providers, fully offline AI, and more than one deployment.

### First two hours after the statement unlocks
1. Copy the statement, judging criteria, required features, technical limits, submission format, template link and exact deadline into `docs/PROBLEM_STATEMENT.md`. Confirm whether the Docker template is mandatory.
2. Decode it in 20 minutes: one user, one moment, why voice, one measurable outcome. Map every criterion to a moment in the demo.
3. Write the hero flow as one sentence: "<user> says <utterance, language> and <outcome> happens within N seconds."
4. Deploy the template untouched within the first hour, so a live link exists from the start, then move the voice kit in.
5. Agree on the request and response schemas, write down what we won't build, split the lanes and start building.

### Evaluation
| Metric | What it measures |
|---|---|
| Word and character error rate | Transcription quality (indic-bridge scoring) |
| Language detection accuracy | Whether the spoken language was identified correctly |
| Intent and field accuracy | Whether the request was understood, and names, quantities and dates came out right |
| Task completion rate | Share of valid requests completed |
| Correction rate | How often users had to fix something |
| Median and P95 latency | Typical and slow-end response time |
| Cost per successful task | Rupees per completed task |

The test cases cover:
- quiet and noisy rooms
- different speeds, speakers and accents
- code-mixed speech
- incomplete or interrupted requests
- similar-sounding names or numbers
- missing or ambiguous fields
- invalid or out-of-range values

State the test set's size and limits plainly; a few dozen clips don't prove accuracy for a whole population. Record consent for user tests, and don't keep personal audio we don't need.

### Deliverables
- **Codebase:** on their template. The README has:
  - the demo link, video and screenshots
  - an architecture diagram and a three-command setup
  - `.env.example`
  - the eval report and the limitations
  - an AI-use note, and "built by voice with Wispr Flow"

  No keys in git.
- **Live link:** Cloud Run over HTTPS (the mic needs it), with sample mode and no login. Tested on iPhone Safari and Android Chrome, and up until 2 Dec.
- **Video:** 2–3 minutes, on YouTube.
- **Deck:** about 10 slides, made as an artifact and exported to PDF or PPTX. It covers the problem, the user, why voice, the demo, how it works, the evidence, the impact (from Round 1 Activity 3), business and distribution, cost per task, the roadmap and the team.

**The demo story** (video and live pitch):
1. The user and the problem, from the official statement.
2. Natural speech in a supported language, or code-mixed.
3. The transcript and the extracted fields on screen.
4. A clarification question, or a correction.
5. Confirmation before acting.
6. The real saved result.
7. The spoken completion with its reference.
8. Measured results and limitations.

Flow appears as how we built it (ten seconds of us building by voice), not as a feature of the product.

**Submission checklist**
- [ ] The codebase follows the official Docker template and rules.
- [ ] Repo access matches what the organisers require.
- [ ] The live URL works without developer credentials.
- [ ] API keys stay on the server, never in the browser.
- [ ] The video is publicly accessible.
- [ ] The deck matches the live product.
- [ ] Metrics and claims match actual test results.
- [ ] Known limitations are written down honestly.
- [ ] The submission confirmation is saved.

## GitHub

### Your profile (gd23456)
- A new public repo `gd23456/gd23456` with a README containing:
  - a one-line positioning: "software people use by speaking, in the languages India speaks"
  - "Now building: Solaris, Build for Bharat 2026"
  - selected work, with factual one-liners only: indic-bridge; Karigar AI for SIH 2026; Kshana, 88 ms per image on an iPhone 15; and Neralu, Hack4SDG 2026 finale, as a contributor
  - a toolbox and contact details

  No stats widgets and no invented numbers.
- A bio, set through `gh api`.
- Six pins: solaris, indic-bridge, SIH2026, cv-hackathon, Neralu, and voyage if it's public. You click these yourself in "Customize your pins", because GitHub has no API for pins.
- I show you the README and bio first. Nothing goes public without your yes.

### Project repo
- `gd23456/solaris` is private and holds this plan. Priyanshu (`Priyanshu-senapati`) has write access. When the template is known, it comes in as the first code commit.
- Local copy at `~/solaris`, with its own git repo. Your home folder is also a git repo, so I check the repo root before every git command. Round 1 drafts stay local-only via `.git/info/exclude`. Commits here carry no Claude co-author line.
- **Before it goes public:**
  - scan the full git history for secrets (gitleaks)
  - remove `PLAN.md` and other internal notes
  - publish only material meant for judges

  If the organisers require a public repo earlier, their rule wins.

## Lanes
| Work | Owner | Support |
|---|---|---|
| Frontend and voice UX | Gourab | Priyanshu reviews the API integration |
| Speech-to-text and text-to-speech providers | Gourab | Priyanshu reviews |
| API, orchestrator, LLM field extraction | Priyanshu | Gourab tests the full interaction |
| Domain rules, validation, storage | Priyanshu | Gourab checks the user journey |
| Accuracy evaluation | Gourab | Priyanshu labels clips |
| User tests | Priyanshu | Gourab recruits people and takes notes |
| Deploy | Gourab | Priyanshu verifies independently |
| Video | Gourab | Priyanshu checks the technical claims |
| Deck numbers | Priyanshu | Gourab reviews |
| Final checks and submission | Both | Each checks the other's work |

Agree the request and response schemas early, and hold two short integration checkpoints a day. **Me:** drafts, code alongside both lanes, research with sources, and checklists.

## Decisions I'll ask at the time
- Cloud Run in `voyance-demo-2fb3b5` (already budget-guarded) or a new project.
- Installing Docker (OrbStack), or building only on Cloud Build.
- Which design skill to use for the frontend.

## Risks and fallbacks
| Risk | Fallback |
|---|---|
| Flow verification takes the full 24 hours | Priyanshu submits if he unlocks first; support email and Discord at 12:00 on 28 Nov |
| A Round 1 answer comes back "needs changes" | Trimmed versions are already written; revise in minutes |
| We build a strong answer to the wrong problem | `docs/PROBLEM_STATEMENT.md` first; every criterion mapped to a demo moment before building |
| Round 2 shrinks to about two days | Voice kit and deploy ready beforehand; one hero flow only |
| The real cutoff is 29 Nov, or earlier than 18:00 on 30 Nov | A submittable version by 29 Nov 23:59; ask the organisers for the exact time |
| Data is lost when Cloud Run restarts | Firestore, never container disk |
| Free-tier rate limits while judges test | Cached speech for fixed lines; one fallback speech-to-text provider; labelled sample mode |
| The public link runs up the paid Anthropic key | Key stays on the server; per-IP limit; capped output tokens; console spend limit |
| The mic fails on a judge's phone | HTTPS; tested on iOS and Android; sample mode needs no mic |
| Their Docker template doesn't fit our stack | The kit is one container on `$PORT`; we adapt to the template, never the reverse |

## Definition of done
The build is ready only when all of these hold:
- [ ] It starts with the required Docker workflow.
- [ ] A user can complete the primary workflow from voice to a real saved result.
- [ ] The user can inspect and correct the transcript and the key fields.
- [ ] Missing or ambiguous information leads to a question, not a guess.
- [ ] Consequential actions need explicit confirmation.
- [ ] Duplicate requests don't create duplicate actions.
- [ ] Provider failures lead to recovery the user can understand.
- [ ] It works on at least one mobile browser and one desktop browser.
- [ ] A labelled test set and an evaluation report exist.
- [ ] The live link, video, deck and repo are reachable by judges.
- [ ] The build matches the official Round 2 statement.

## Verification
- **Round 1:** each activity shows a pass on the dashboard, and the Round 2 card unlocks.
- **Voice kit:**
  - unit tests on the schema, validation and confirmation rules
  - `eval/` prints the metrics above for each language
  - the fake-microphone Playwright run passes end to end
  - the Cloud Run URL works on iPhone Safari and Android Chrome
  - cold start is timed
- **Submission:** every link is opened logged out on a phone, the video plays without sign-in, the README renders, and Cloud Run logs show judges' requests succeeding through 2 Dec.
- **Profile:** github.com/gd23456, opened logged out, shows the README and pins, and no private details.

## Next moves (on hold until the idea is refined)
1. Three idea cards with sourced numbers, in `~/solaris/round1/ideas.md` (local-only).
2. The GitHub profile README and bio draft, for your review.
3. Full Round 1 drafts for the idea you pick, with the prompt tested in an AI app builder.
4. The voice kit backend, and a smoke deploy to the `solaris` Cloud Run service.

## Changes from the proposals (28 Nov)
**Taken:**
- one focused workflow, where the LLM interprets and code validates and acts
- the 10-step journey and the 11 states
- the language rules, and Firestore storage with an audit trail
- the failure table and the labelled sample mode
- the fuller evaluation, the demo story, the submission checklist and the definition of done
- the repo-safety steps, the milestone exit criteria and the repo layout

**Declined or changed, and why:**
- **Reading the Round 2 statement on 27 Nov:** it can't happen. The statement unlocks only after Round 1 passes, so the Round 1 gate stays first.
- **Holding off on the idea until the statement is known:** Round 1 needs one idea now, before the statement is visible. Holding off applies only to the Round 2 product.
- **Ending the schedule on 29 Nov:** the logged-in dashboard says 30 Nov. We hedge with a submittable version by 29 Nov 23:59 and ask the organisers for the exact cutoff.
- **Managed SQL:** Cloud SQL has no free tier, so we use Firestore's free tier, in line with zero spend.
- **Priyanshu owning speech recognition and evaluation:** accuracy evaluation stays with Gourab, who built the indic-bridge scoring. Priyanshu takes LLM extraction, domain rules and storage.
- **A fast, cheap model by default:** we time Haiku 5.5 and Opus 5.5 on 20 real utterances first, then pick.
- **"Consider making the repo private":** it already is.
- **`PLAN.md` in the final repo:** it comes out before the repo goes public, because it holds strategy and the GCP project name.
