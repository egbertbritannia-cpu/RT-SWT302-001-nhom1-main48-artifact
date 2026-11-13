# Main48 supplementary methods notes

These notes retain details moved from Research Methodology during the
11 November 2026 editorial shortening. They introduce no new measurements,
analysis decisions or validation results. They accompany the supplementary methods and results published in this repository.

## Transport and retained operational records

Download processes have a 600-second limit. Download failures trigger a
60-second backoff; size and SHA-256 checks allow reuse of verified files.
The dispatcher checks existing submission identities before resubmission,
and transfer retries do not rerun measurements. Historical bootstrap records
and attempts remain archived. The main text retains the limit of one
documented, same-configuration infrastructure measurement retry with a new
attempt record, no automatic measurement retry and no overwriting.

Sources: `results/expansion-main48-v1-2026-11-09/README.md`, `budget-lock.json`,
`dispatcher-repair-v3.json` and the archived worker snapshot. The separate
`results/main48-pipeline-audit-v1-2026-11-10/` reports observed events with
distinct launch, shard, measurement and resampling denominators.

## Post hoc assessment of inference

After reviewing main48 results, procedures for equality of group correlations
were assessed under candidate models for scope/package structure. One used
common bootstrap weights within packages to construct intervals for all
30 group-by-seed correlations. In each of nine null settings, the proportion
of simulated datasets whose intervals simultaneously contained all 30 true
correlations was below the 95% target. This post hoc assessment did not
establish a valid population test. Purposive scope selection and dependence
within projects/packages leave the population weighting and dependence model
unjustified. The manuscript therefore retains descriptive estimates and ranges;
the simulation assessment does not confer confirmatory status on main48.

## Helper audit counting and aggregation

The post hoc audit checks generated regression-test source and helper/test
bytecode against recorded hashes for all 480 scope–seed pairs. It counts invoke
instructions targeting packaged helper classes in generated test methods,
including static calls, instance calls and constructors. These are retained
direct call sites, not runtime executions or indirect callbacks. Static-method
counts were independently computed from source and bytecode and agreed for
all 480 pairs; this is an implementation cross-check, not independent human
adjudication.

AI-assisted source inspection distinguishes input/fixture construction,
output/state observation and observer setup, checked against configured
observer lists. Each scope's footprint includes distinct directly called
helper methods and the complete source units containing them. Source lines
exclude comments and blanks but include shared code unused by that scope.
Declared-method counts exclude constructors, class initializers and synthetic
methods. Call sites divided by generated test-method count are calculated
within each seed, summarized by the median over all ten seeds per scope,
and then summarized over 16 scopes per group. No Java measurement is rerun.

Scope tables, hashes, method roles and the scripts remain in
`results/main48-helper-audit-v1-2026-11-10/` and the existing local
`main48-helper-audit-v1.zip`. These notes do not alter that archive.
