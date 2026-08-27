# Technical documentation

Read this file when the draft is technical documentation. README files, code
comments, runbooks, API docs, deploy guides, and error messages.

A reader opens these while something is broken, in a second language, or at two
in the morning. One clear reading matters more than voice.

The rules come from ASD-STE100, the simplified English that aerospace uses for
maintenance manuals. Apply them **in addition to** `SKILL.md`, not instead of
it. A colon reveal is still a colon reveal in a README.

Do not apply this file to essays, posts, letters, or marketing copy. It would
flatten a voice that the rest of the skill exists to protect.

## The rules

**One idea per sentence.** A sentence with two claims joined by "and" or "so"
is two sentences.

> The switch starts off, so a fresh database and a restored backup both come up
> safe.

becomes

> The switch starts off. A fresh database and a restored backup therefore start
> with writes disabled.

**Twenty words.** Twenty for a procedure, twenty-five for description. Count
them. A sentence over the limit is hiding a second idea.

**One instruction per step.** In a numbered procedure, one step is one action.
"Install the site and reload nginx" is two steps.

**One word per idea, every time.** `SKILL.md` bans synonym cycling for style.
This is stricter. Pick the term and repeat it, even when the repetition feels
dull. If the actor is "the person", it is never "somebody", "the user", or "the
caller" later. If a value is "refused", it is never "rejected" or "blocked"
later.

**No metaphors, no idioms.** "The token opens the wrong door" and "a restart is
the wrong speed" both make a reader guess. A reader translating in their head
guesses wrong. Say the mechanism instead.

> A forgotten scope check inside a new tool cannot open the wrong door.

becomes

> The endpoint refuses a token for another tenant before any tool code runs.

**Keep the articles.** "Set the flag in the config file", not "Set flag in
config file". Dropped articles read as telegram English. They slow a non-native
reader down.

**Three words in a noun cluster, at most.** "The release pull request body
template" becomes "the body template for the release pull request".

**Simple tenses.** Present for what is true. Past for what happened. Future for
what will happen. "It will have been migrated" becomes "the migration runs
first".

**Active voice, named actor.** "The write is refused" becomes "The service
refuses the write". Use passive only when the actor is unknown or irrelevant.

**Six sentences per paragraph.** A longer paragraph holds more than one topic.
Split it.

**Say what happens, not what it means.** "This is important for security" gives
the reader nothing to act on. "The endpoint refuses a token for another tenant"
does.

## Checks

Answer each check with pass or fail, after the checks in `eval.md`. If any
check fails, fix the draft and run them again.

1. Does every sentence carry one idea, with no two claims joined by "and" or "so"?
2. Is every sentence twenty words or fewer for a procedure, and twenty-five for description? Count them rather than judging by eye.
3. Does each numbered step hold exactly one action?
4. Is one term used for one idea throughout? Check for a synonym for the same actor, object, or outcome anywhere in the draft.
5. Are metaphors and idioms replaced with the mechanism they stood for?
6. Are the articles kept, rather than dropped for brevity?
7. Is every noun cluster three words or fewer?
8. Are the tenses simple: present for what is true, past for what happened, and future for what will happen?
9. Is the voice active, with a named actor, except where the actor is unknown?
10. Is every paragraph six sentences or fewer?
11. Does the draft say what happens, rather than assert that something matters?
12. Does the What changed section report the number of over-limit sentences before and after?
