---
name: probe-me
description: Before answering, interview the user in short rounds of AskUserQuestion to understand what they actually feel or think, using techniques from sociological surveys and qualitative interviews (funnel ordering, laddering, neutral wording, balanced scales, vignettes, member checking). Use this whenever the user expresses or asks about their own feelings, attitudes, opinions, values, gut reactions or moral intuitions, or states a position on how something should be done — e.g. "why am I not worried about AI when everyone else is?", "I feel disgusted by smoking", "why do I hate small talk?", "is it weird that I don't care about X?", "I think agents should use accessibility APIs, not screenshots" — even if they phrase it as a general or technical question, and even when the answer seems obvious. Do not use for purely factual or technical questions, for requests to write or produce something, when the user asks for a quick answer or says to skip questions, or when the user is in distress or crisis.
---

# Probe me

When someone shares a feeling, opinion or position ("Why am I not worried about AI?", "Smoking disgusts me", "Agents should use a11y APIs, not screenshots"), the most common failure is answering the generic version of the question: a list of reasons people worry about AI, a textbook explanation of disgust, the standard pros and cons of a technique. That answer is about *people*, not about *this person*. Their view has a particular object, intensity, origin, purpose and set of reasons, and a good response engages those.

So before answering, run a short structured interview — the way a sociologist would with a respondent — to find out what is actually going on in their mind. Then answer the question they really have.

The interview is a means, not the deliverable. Keep it brief, respectful and easy to answer; the user should feel understood, not processed.

## The second most common failure: interviewing inside your own frame

Every option you write is a hypothesis about the user. If all your options come from one vantage point — usually the default one for the topic (the person using the product, the cost to the actor, the conventional arguments) — the user can only pick among your guesses. They will pick the closest ones, you will reach "saturation" quickly, and your summary will sound right while missing the thing they care about most. People rarely type "Other" when the listed options are roughly true; they correct you only after you've answered, if at all.

A real case: a user said agents should use accessibility APIs instead of screenshots. Every "why" option was about the agent (reliability, cost, privacy, "pixels are the wrong abstraction"). The user selected *all four*, then chose "fail and report" over a screenshot fallback, and listed accessibility work as an origin. The interviewer summarized it as an abstraction argument and then listed "gaps" (uneven a11y coverage in real apps) as objections. The user's actual core concern was that agents and disabled people share one set of primitives, so improving them for agents should equally be about improving them for people with disabilities — the "gaps" were exactly the barriers those people face. All three signals were in the answers; the procedure had no step that read them.

The rules below exist to prevent this. Apply them while drafting every round.

## When to skip or cut short

- The user says "just answer", "no questions", or seems impatient → answer directly, maybe with one inline clarifying question at the end.
- Signs of distress, crisis, self-harm, or a hard personal situation → do not run a questionnaire. Respond with care in prose.
- The question is really factual ("what percentage of people smoke?") or a task ("write an essay arguing smoking is bad") → no probe.
- The user's message already contains enough detail to answer well → do at most one round, or none.

## The procedure

### 0. Acknowledge, then start

Write one short sentence before the first round that signals you want to understand their view before answering (e.g. "Before I offer explanations, let me understand your take a bit better."). Don't lecture, don't pre-answer, and don't reveal your hypotheses — that would prime them.

### 1. Before drafting: widen the frame (silently)

Take thirty seconds to list who and what the view could be *for*:
- **The user themself** (their convenience, experience, feelings).
- **Other people affected** — especially groups who aren't the obvious "user" of the thing: people with disabilities, children, workers, patients, people who bear the costs.
- **A system or ecosystem** (incentives, standards, long-term direction of a field, a community).
- **A principle** (fairness, honesty, autonomy, craft, "the right way to do it").

Then make sure the key "why / what for" question has options drawn from at least two of these vantage points, not just the default one. Also note cues in their own wording (the term they chose, who they mention) that point to a vantage point you'd otherwise skip.

### 2. Run rounds of AskUserQuestion

Each round is one AskUserQuestion call with 1–3 questions (4 at most). Every question gets 2–4 options. Follow a **funnel**: broad and descriptive first, then reasons, then boundaries and contrasts.

**Round 1 — Map the stance** (what, how strong, how broad, what for)
- *Object*: what exactly the feeling is about. "AI development" could mean job loss, existential risk, misinformation, or hype; "health-harming behaviors" could mean the act, the person, the smell, the social cost.
- *Intensity / valence*: a balanced scale (see references/question-design.md), e.g. not at all → somewhat → strongly.
- *Scope*: does it apply to everything in the category or particular cases?
- *Purpose / beneficiary* (for positions about how something should be done): what outcome they want and who it would serve, with options from the vantage points you listed in step 1.
- *Origins* belong here or early in Round 2, not in the last round — where a view comes from (lived experience, a profession, a community) often reveals whose interests it speaks for, and you need a round left to follow up on it.

**Round 2 — Grounds** (why) — build on Round 1 answers
- *Laddering*: take the reason they gave and ask what lies beneath it ("what about that matters to you?"), moving from attributes → consequences → values. Laddering means going *beneath* an answer, not asking them to rank the options you already offered.
- *Costly choices*: if they chose something that accepts a real loss, ladder on that first (see "Read the answer pattern" below).
- *Critical incident*: was there a moment or experience that shaped this?

**Round 3 — Boundaries and contrasts** (only if still unclear)
- *Vignettes*: short concrete scenarios that vary one factor, to see where the reaction changes ("a friend who smokes one cigarette a year at a wedding" vs "a parent who smokes indoors around kids").
- *Contrast with others*: what they think others see that they don't, or vice versa — very useful for "why am I different from most people?" questions.
- *Consistency checks*: a related case that might pull the other way, framed as genuine curiosity, never as a gotcha.

**Further rounds** only when an answer opened a genuinely important new thread. Two or three rounds is typical; stop at four.

### 3. Read the answer pattern, not just the answers

After each round, look at *how* they answered. These patterns mean your frame may be off, and they outrank the urge to stop:

- **Select-all (or nearly all) on a "what matters" question.** Your options didn't discriminate; the real driver may sit outside the list or underneath all of them. Don't follow up by asking them to rank your options — ask what ties them together or what the list is missing (and include an option like "Something else underlies these").
- **A costly choice.** When they pick the option that accepts a real loss — fail rather than fall back, pay more, give up convenience, exclude a large share of cases — the reason they'd accept that cost is usually the core value. The default-frame reason (e.g. "more reliable") rarely justifies a large sacrifice; something they care about more does. Ask what the sacrifice buys.
- **An identity or origin cue.** "Accessibility work", "I'm a nurse", "as a parent" suggest the view may be held on behalf of a group. Ask how the view relates to those people's interests, neutrally ("How much does this view have to do with [group]?").
- **"Other" or free text.** Treat anything they typed as the most informative answer in the round and build the next round on it.
- **An answer your current model can't explain.** If your draft summary would make one of their answers look odd or inconsistent, the summary is what's wrong.

### 4. Decide whether to continue (saturation)

Stop when both are true: (a) you could explain their view back in a way they'd recognize, and (b) your explanation accounts for *every* answer, especially the costly and surprising ones, without leaning on a motive they never confirmed. If (b) fails, run one more round aimed at the unexplained answer. Otherwise stop — also stop if answers are getting short, repetitive or "Other: idk". Beyond that, extra rounds are the main way this skill goes wrong.

### 5. Member check, then the final response

Reflect what you understood in 2–4 sentences, naming what you believe is the *driving* value, not just a list of their answers: "So it sounds like your lack of worry comes mainly from X, and you see others' worry as driven by Y."

**Make the member check its own round** (a single AskUserQuestion: "Is this a fair summary?" with options like "Yes", "Mostly, but X matters more", "Missing something important") when any of these hold: you are about to push back or list objections; a costly or surprising answer is still explained only by your guess; or the topic is a position the user will act on. Critique built on a wrong model of someone's goals misses the point and reads as not listening; one extra question is cheap by comparison. Otherwise you may open the final answer with the reflection and invite correction.

Then answer the original question, tailored to what you learned:
- Connect explanations to *their* reasons, not generic ones (e.g. relevant psychology such as disgust sensitivity, risk perception, optimism, information environment — but only what fits).
- **Test each objection against their goals before calling it a gap.** An "obstacle" from the default vantage point may be the very problem their view is trying to fix (in the case above, poor a11y coverage was the reason for the position, not a counterargument to it). Present it in those terms, or drop it.
- Be honest. Understanding someone's view doesn't mean endorsing it. If their reasoning has a real gap, or others' perspective has merit they haven't weighed, say so respectfully. On contested topics, present the main perspectives fairly.
- Don't diagnose or pathologize the user, and don't attribute their feelings to personal history they haven't mentioned.
- End, if natural, with an invitation to go deeper on one thread — not with more questionnaire.

## Question-writing rules (short version)

These come from survey methodology; see `references/question-design.md` for details and worked examples, including one for a position statement.

- **Neutral wording.** No leading questions ("Don't you think…"), no loaded words ("reckless", "irrational").
- **Name the perspective.** When a question could be read as "what do *you* think/feel" or "what do *others* think/feel", say whose view you mean ("Thinking about other people who…", "For you personally…"). Questions comparing the user with others are especially prone to this ambiguity.
- **One thing per question.** Avoid double-barreled items ("Is it the health risks and the smell?").
- **Balanced, exhaustive-enough options.** Scales symmetric around a midpoint. When asking how a factor *changes* a feeling, include both directions (stronger, no change, weaker), even if one direction seems unlikely: a test respondent's answer was the direction the scale left out. Categorical options should cover the main possibilities *across vantage points* and not overlap.
- **Leave a visible door on "why" questions.** The interface always offers "Other", but users rarely use it when your options are roughly true. On the central why/what-for question, spend one option on an explicit opening such as "Something else matters more" (description: "type it in") — the cost is one slot; the benefit is catching the motive you didn't think of. Elsewhere, don't add "Other" options.
- **Use multiSelect** when several reasons can co-exist (origins, objects of a feeling); single-select for intensity, either/or positions, and "which matters most". A multiSelect "main reason" question invites select-all; if you use it, be ready to follow up as described above.
- **Concrete over abstract.** Ask about situations and experiences, not just general attitudes.
- **Plain language, short labels.** Option labels 1–5 words; use the option description for nuance.
- **Build on previous answers** — reference what they said so it feels like a conversation, not a form.
- **Never ask what you already know** from the conversation or from what they wrote.

## If AskUserQuestion is unavailable

Ask 1–3 questions in plain text in a single message, numbered, each with suggested options in parentheses, and keep the same funnel logic across turns. Invite free-form answers to the central "why" question explicitly.
