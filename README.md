# main48 numerical-analysis artifact

This repository distributes the frozen analysis artifact for *Branch Coverage
and Raw Mutation Scores across Java API Groups*: 48 purposively selected API
scopes from four Java project releases, measured at ten seeds (480 paired
scope–seed observations).

## Download the pinned release

- [Analysis archive v2](https://github.com/egbertbritannia-cpu/RT-SWT302-001-nhom1-main48-artifact/releases/download/main48-analysis-v2/main48-analysis-supplement-v2.zip)
- [SHA-256 checksum](https://github.com/egbertbritannia-cpu/RT-SWT302-001-nhom1-main48-artifact/releases/download/main48-analysis-v2/main48-analysis-supplement-v2.zip.sha256)
- [Release and verification notes](https://github.com/egbertbritannia-cpu/RT-SWT302-001-nhom1-main48-artifact/releases/tag/main48-analysis-v2)

Archive SHA-256:

```text
44ed1106492fb7bc710fb1f79d045d1c31df5f9b669bd36707cad65db7f8cc57
```

The ZIP contains 2,048 payload files and a per-file SHA-256 manifest. Extract
it into an empty directory and retain its `scripts/` and `results/` structure.
The README inside the ZIP is the complete reproduction guide.

## Included evidence

- Frozen membership, paired input counts, key selection and analysis plans.
- JaCoCo XML, PIT XML, measurement configuration and result records for all
  480 scope–seed pairs, with original hashes.
- Canonical calculation and verification scripts, stored point summaries
  and descriptive resampling arrays.
- The retained-counterexample-key post hoc comparison.
- RQ2 perturbation-dose summaries and the PIT 1.30.0 source evidence used to
  distinguish KILLED-only scores from detected fractions.
- A verification wrapper that uses a separate scratch copy rather than
  overwriting the bundled frozen outputs.

## Reproduction scope

This archive supports numerical reanalysis and checks against recorded XML.
It does not contain release JARs, generated suites or suite bytecode needed
to repeat the Java measurements. Repeated seeds are repeated measurements
of the same scopes. Resampling ranges are descriptive; no population null
hypothesis decision is claimed. The original single-operator and mutant-
identity limitations remain in force.

The main study repository remains private. This public artifact repository
is a separate distribution; its creation does not make the study repository
public or disclose its full working tree.
