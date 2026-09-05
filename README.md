# Little SF clock

A small public clock for [Little SF](https://little-sf.david-eden.chatgpt.site). It requests a server wake-up approximately every five minutes. GitHub schedules can be delayed.

The application alone decides whether to advance: its continuous mode is off by default. The clock uses a short-lived GitHub OIDC identity restricted to this repository, workflow and main branch. It has no settings permission or access to the model key. No Site secret is stored in GitHub. No application source or user data is kept in this repository.

The wake-up job can request only its temporary identity; it has no repository write permission. A separate weekly maintenance check updates the operation heartbeat at most once every 28 days, so the public schedule remains active. Standard public GitHub runners are used; no paid runner, cache or artifact is configured.
