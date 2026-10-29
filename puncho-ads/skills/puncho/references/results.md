### 6. Results

`sync_insights` pulls into `MetricDaily`; `get_attribute_rollup` is the payoff
query. Two honesty rules:

- **Meta's numbers move for about 72 hours** as conversions attribute. Never
  treat day-0 numbers as final, and re-sync a trailing window.
- **The rollup is one project's.** Blending attribute performance across
  brands is actively misleading — a hook that wins for one audience says
  nothing about another — so `get_attribute_rollup` is always scoped to a
  project. `adAccountId` narrows further, for a project that runs through
  several accounts.

The rollup has spend and impression floors for a reason. A combination that
converted once on $6 is noise, and the floors exist so the loop does not
confidently amplify it. If every row is below the floor, the honest answer is
"not enough spend to say yet" — say that rather than ranking noise.

Every row carries 95% intervals and an `evidence` of `NOT_ENOUGH_DATA`,
`DIRECTIONAL` or `CLEAR`. Cost per result is per conversion: the event the
campaign optimises for (a registration, a lead), a purchase only where that is
the goal. Report the interval with the number ("21 a result, could be 14 to
38", in the account's currency) and call only `CLEAR` a winner; a group of
fewer than three ads is never `CLEAR`. The winning attributes generation is
shown are the groups cheaper than the blend, and a `DIRECTIONAL` one is
leaning, not proven.

To learn one thing per batch, give the brief a `testVariable` in
`create_brief`: the batch then varies that attribute and holds the rest, and
`store_specs` warns when it doesn't. `get_test_verdict` reads the result and
the spend still needed; `get_batch_lift` says whether each batch beat the last.

### 7. The calendar

Read `get_calendar` at the start of a session. Its `days` are what happened
(spend, launches, decisions, renders), read from rows that already exist, and
its `entries` are what was planned, each with a progress state. Lead with what
needs the human: a flight that is `due` (its start passed and nothing launched),
an organic post that was `missed`, anything `overran` or `failed`.

`plan_calendar_entry` puts a plan on it, always as PLANNED:

- **Events** are dates in the brand's world: a hackathon, a registration
  deadline. Put them on when the human mentions them, then plan around them.
- **Flights** are approved concepts planned to run between two dates. A flight
  launches nothing. When one comes due, propose the launch the usual way
  (section 5); the date passing is not a yes.
- **Organic posts** are one concept and a caption, for a human to schedule on
  the board. The caption is every word of the post outside the image, so it
  meets the same bar as ad copy: load `ad-copy` and write it in the brand's
  voice.

`update_calendar_entry` edits or cancels a plan. It refuses a post a human has
scheduled; if that post needs changing, say so and let them unschedule it.

You cannot schedule, unschedule or publish a post, and there is no tool for it:
a post goes out under the brand's name, like an approval. Never tell the human a
post is scheduled or published unless `get_calendar` shows that status.
