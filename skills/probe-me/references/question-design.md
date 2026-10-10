# Question design reference

Read this when drafting probe questions, especially for the first time in a conversation or when a topic is morally charged.

## Contents
1. Methods borrowed from social research
2. Common question pitfalls
3. Scale templates
4. Worked example A — "Why are many people worried about AI but I'm not?"
5. Worked example B — "I feel disgusted with health-harming behaviors like smoking"
6. Worked example C — a position statement: "Computer-use agents should use a11y APIs, not screenshots"

---

## 1. Methods borrowed from social research

| Method | Origin | How it's used here |
|---|---|---|
| Funnel sequencing | Survey design | Broad, easy, descriptive questions first; specific and sensitive ones later. |
| Semi-structured interview | Qualitative research | A planned set of themes (object, intensity, grounds, boundaries) but freedom to follow up on what emerges. |
| Laddering | Means-end chain interviews | Repeatedly ask "what does that give you / why does that matter?" to move from surface reasons to underlying values. Usually 1–2 steps is enough in chat. |
| Probes | Interview technique | Elaboration ("tell me more about…"), clarification ("when you say X, do you mean A or B?"), contrast ("how is that different from…?"). |
| Critical incident technique | Flanagan, applied psychology | Ask whether a specific event or experience shaped the view. |
| Vignettes / factorial surveys | Sociology | Brief scenarios that vary one factor to locate the boundary of a judgment. |
| Likert / semantic-differential scales | Attitude measurement | Measure intensity and direction with balanced options. |
| Theoretical saturation | Grounded theory | Stop when new questions stop yielding new information. |
| Member checking | Qualitative validity | Reflect your interpretation back and let the respondent correct it. |

## 2. Common pitfalls

- **Leading:** "Isn't it frustrating that people ignore the risks?" → "How do you feel when people take health risks?"
- **Loaded:** "Why do you think people are so paranoid about AI?" → "What do you think drives other people's worry about AI?"
- **Double-barreled:** "Does the smell and the health cost bother you?" → ask separately, or use multiSelect.
- **Unbalanced scale:** "Slightly / Very / Extremely disgusted" (no low end) → see templates below.
- **Presuming:** "When did you first notice your disgust?" assumes a moment exists → "Was there a particular experience that shaped this, or has it always been there?"
- **Social desirability:** People under-report stigmatized views. Normalize with neutral framing: "People react to this in many different ways — which is closest to yours?"
- **Acquiescence:** Avoid agree/disagree items where "agree" is the easy default; prefer options that name actual positions.
- **Frame lock:** All options for "why" come from one vantage point (usually the actor's or the default user's), so the respondent can only confirm your hypotheses. Pretest mentally: "If this person cared mainly about someone *else*, or about the long-run system, could they say so here?" If not, replace an option.
- **Ranking a select-all:** The respondent ticked every reason; you then ask which one matters most, from the same list. You get a forced pick, not the driver. Ask instead what connects them or what's missing.
- **Origins last:** Asking where a view comes from in the final round leaves no room to follow up on what it reveals.

## 3. Scale templates (pick 4 points; user can type "Other" for nuance)

- Intensity: Not at all · A little · Moderately · Strongly
- Concern: Not concerned · Mildly · Fairly · Very concerned
- Frequency: Rarely · Sometimes · Often · Almost always
- Certainty: Unsure · Leaning · Fairly sure · Certain
- Position (bipolar, 4-point forces a lean): Strongly X · Somewhat X · Somewhat Y · Strongly Y
- Change (how a factor shifts a feeling — always both directions): Stronger · No difference · Weaker · Unsure. Don't drop "Stronger" just because you expect softening; in testing, the respondent's answer to "does addiction change your disgust?" was the omitted "stronger".

## 4. Worked example A

User: "Why are many people worried about AI development but am I not?"

Round 1 — map the stance
1. "Thinking about OTHER people who say they're worried about AI: what do you think they're mostly worried about?" (multiSelect; an earlier wording, "which concerns come to mind for you?", confused a test respondent about whose concerns were meant) — Jobs and economy · Misinformation/manipulation · Loss of human control · Concentration of power
2. "How would you describe your own outlook on AI development?" — Unconcerned · Mostly relaxed · Mixed feelings · Optimistic/excited

Round 2 — grounds (adapt to round 1)
1. "Which best describes why those concerns don't land for you?" — Seem exaggerated · Will be managed/regulated · Benefits outweigh risks · Not much I can do anyway
2. "Where does most of your sense of AI come from?" (multiSelect) — Using it myself · Working in tech · News and social media · Friends/family

Round 3 — contrast (only if needed)
1. "Is there any AI scenario that *would* worry you?" — Yes, a few · Hard to imagine · Only far-future ones · Not really
2. "What do you think worried people know or feel that you don't?" — Nothing really · More exposure to bad news · Different stakes (e.g. jobs) · Different temperament

Then member check and answer: tie the answer to their stated reasons (e.g. hands-on familiarity reducing perceived threat, optimism bias, differences in personal stakes, information environment), and fairly present what concerned people point to.

## 5. Worked example B

User: "I feel disgusted with significant health-harming behaviors, even for popular ones such as smoking."

Round 1 — map the stance
1. "What does the disgust attach to most?" (multiSelect) — The act itself · The sensory side (smell, mess) · The choice to harm oneself · Effects on others
2. "How strong is it, typically?" — Mild aversion · Noticeable discomfort · Strong disgust · Visceral/physical

Round 2 — grounds and scope
1. "Which other behaviors trigger it?" (multiSelect) — Heavy drinking · Junk food/overeating · Drug use · Mostly just smoking
2. "Does it change how you see the person doing it?" — Not really · Somewhat less respect · Noticeably · It's about the act, not them
3. "Was there an experience that shaped this, or has it always been there?" — Specific experience · Family/upbringing · Learned the facts · Always felt this way

Round 3 — boundaries via vignettes
"Which of these would bother you?" (multiSelect) — An occasional social smoker · A heavily addicted smoker trying to quit · A smoker who never smokes near others · A health-conscious vaper

Then member check and answer: e.g. moral vs. pathogen disgust, how disgust tracks perceived choice and contamination, why popular habits still trigger it — and, honestly, the perspective that addiction limits choice, and the tension between disgust and compassion if it comes up.

## 6. Worked example C — a position statement

User: "I think agentic computer-use should stop relying on screen captures; rather, a11y facilities should be used."

Positions about how something *should* be done hide a purpose and a beneficiary. Before drafting, list the vantage points: the agent's user (reliability, speed, cost), people sharing the same interfaces (screen-reader and switch users), the ecosystem (developer incentives, standards), and principle (the right abstraction). The user wrote "a11y", the accessibility community's term, which is a cue worth testing.

What went wrong in the real session: the "why" question offered only agent-side options; the user ticked all four; the follow-up asked them to rank those same four; origins came in the last round; a costly choice ("fail and report" rather than fall back to screenshots) was never laddered. The final answer then treated poor a11y coverage as an objection, when it was the problem the user wanted solved.

Round 1 — map the stance
1. "If agents moved to accessibility APIs, who would you most want to benefit?" (multiSelect) — People using agents · People using assistive tech · App developers · Something else matters more
2. "How strongly should screenshots be dropped?" — Drop entirely · Rare fallback only · Use both, lean a11y · Mild preference
3. "Where does this view come from?" (multiSelect) — Using agents · Building software · Accessibility work · Reading/discussion

Round 2 — grounds (suppose they chose "Rare fallback" in R1 but later pick "Fail and report")
1. "When an app's accessibility tree is broken, what should the agent do?" — Fall back to screenshots · Fail and report · Ask the user · Depends on stakes
2. If "Fail and report": "Failing means the task doesn't get done. What does that buy, in your view?" — Safer than guessing · Pressure to fix a11y · Keeps agents honest about limits · Something else
3. If "Accessibility work" was an origin: "How much is this view about people who rely on assistive tech?" — Central to it · One reason among several · Mostly separate · Not really

Member check as its own round, before any critique: "So the core of it seems to be that agents and assistive-tech users should share one set of primitives, and agent demand should push those primitives to get better for both — failing loudly is how that pressure works. Fair?" — Yes · Mostly, but… · Missing something important

Then answer: coverage gaps become the shared problem to fix, not an objection; screenshot fallback is weighed as a convenience that removes pressure to fix a11y for disabled users; real tensions (agent needs reshaping a11y semantics away from human needs, the power of OS accessibility permissions, interference with live assistive tech) are raised as risks to the user's own goal.
