# kukkuone-hatchery-mobile

**Placeholder. No app is built here.**

The Hatchery experience ships inside
[kukkuone-partner-mobile](https://github.com/KukkuOne/kukkuone-partner-mobile),
together with the other four counterparty roles, behind a workspace switcher.

## Why one app rather than five

These five roles are one kind of software: publish a catalog or an offer,
receive an order, agree terms, record a dispatch or a pickup, settle. They
share a spine, and the overlap between them is real — a trading partner who
also lifts, a hatchery that also trades — which is exactly what the switcher
is for. Five binaries would ask those people to juggle installs, and would
cost five store listings, five review queues and five release pipelines before
any of them had a user.

Farming is the one genuine exception and has its own app,
[kukkuone-farmer-mobile](https://github.com/KukkuOne/kukkuone-farmer-mobile):
a system of record filled in several times a day on a farm, offline, in
Telugu. Different software for a different job.

## When this repo would be used

If Hatchery outgrows the shared app — its own release cadence, device permissions
the others do not need, or an audience the combined app confuses — it gets
carved out here. That split is cheap: `lib/roles.ts` in the partner app
already states each role's tabs and screens. Merging apps back together is not
cheap, which is why the split is deferred rather than made up front.

Until then, work on Hatchery happens in the partner app.
