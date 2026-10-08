# Study design, provenance, and implementation access

This is a public methodological summary of analysis release **v1.2.0**, not a new preregistration and not an executable reproduction package. The original decisions, amendments, implementation, and run records are preserved in the separate private repository. The public summary was prepared on **2026-10-08** from private snapshot `dc2d24c8e7ffb6cfa4b2b29800a6b8a3a60ee631`.

## Scope and comparison

The study compares flat ΛCDM with flat CPL w0waCDM on identical data within each comparison. It first reproduces reference results, then measures sensitivity to supernova selections, covariance scenarios, and the Dovekie release. It uses BAO alone, BAO plus compressed CMB, and three separate supernova combinations. It does not stack overlapping supernova compilations into one independent sample.

BAO constrain dimensionless distance ratios relative to the acoustic ruler. The BAO-only branch allows the overall ruler scale to vary. The CMB branches use DESI's three-variable Gaussian compression and an approximate acoustic-scale calculation, with the disclosed P8 calibration. They do not evaluate the full Planck/ACT CMB likelihood. Supernova offsets are treated as nuisance quantities; no SH0ES absolute-distance calibration is added.

## Data provenance

| Input | Version or selection used | Primary source |
|---|---|---|
| DESI DR2 BAO | `bao_data` v2.6; 13 observables and their covariance across seven redshift slices | [Official BAO products](https://github.com/CobayaSampler/bao_data/tree/v2.6/desi_bao_dr2) and [DESI DR2 paper](https://arxiv.org/abs/2503.14738) |
| Compressed CMB | DESI Appendix A compression of acoustic angle and physical densities; full-precision official-chain values | [DESI DR2 paper](https://arxiv.org/abs/2503.14738) |
| Pantheon+ | Data-release commit `c447f0f`; baseline zHD > 0.01, 1590 rows; released STAT+SYS covariance | [Official release](https://github.com/PantheonPlusSH0ES/DataRelease) |
| Original DES-SN5YR | Tag v1.2; 1829 entries; released systematic covariance with published diagonal uncertainties | [Official release](https://github.com/des-science/DES-SN5YR/tree/v1.2) and [DES-SN5YR cosmology paper](https://arxiv.org/abs/2401.02929) |
| Union3 | 22-node compressed distance product and covariance; `sn_data` commit `61d9643` | [Pinned Cobaya input](https://github.com/CobayaSampler/sn_data/tree/61d96434cafc2770928322c38e5a750e686368ae/Union3) and [original release](https://github.com/rubind/union3_release) |
| Dovekie | DES release commit `c9a4fcaf`; 1820 entries | [Pinned release](https://github.com/des-science/DES-SN5YR/tree/c9a4fcafc4cbd19bd750dee47fc76194a45c181f) and [DES reanalysis paper](https://arxiv.org/abs/2511.07517) |

Pinned file hashes and selection records remain in the private archive. The separate 1580-entry Pantheon+ covariance-check sample excludes SH0ES calibrators to match the chosen reference; it is not the 1590-row baseline above. Counts refer to catalogue entries, which need not correspond one-to-one to unique physical supernovae.

## Decisions made before and after results

The original study recorded parameter ranges, reference windows, numerical checks, seeds, and supernova selections before the corresponding runs. Subsequent sensitivity extensions likewise have dated protocols. This statement has two material qualifications:

- **P8 was introduced after a failure.** The original analytic BAO+CMB result fell outside its acceptance window. Acoustic-scale corrections were calibrated on official chains and recorded before rerunning the comparison. This is a disclosed post-failure calibration, not blind preregistration.
- **The matched-supernova extension has a non-blind reference stage.** Its reproduction stage and later catalogue-column check have different evidential status. Calling every stage blind would be inaccurate.

This public summary preserves these distinctions. Preparing it did not constitute a fresh rerun or an independent certification of the archived calculations.

## Sensitivity comparisons

The original low-redshift tests require z > 0.1, remove CfA and CSP while retaining Foundation, restrict to the DES survey where applicable, or require z > 0.025. Models are refitted after selection. Removing a population changes the available information as well as any possible systematic contribution; the resulting change cannot identify the cause on its own.

The v1.1 extension uses Gaussian catalogue simulations for a covariance check, survey-removal refits, and matched-supernova differences between releases. The v1.2 extension varies the supernova covariance alone, then separately replaces the original DES release with Dovekie at a fixed analysis pipeline. Neither extension replaces the original baseline with a preferred adjusted result.

The report uses the reference two-extra-parameter χ²-to-Gaussian convention for Nσ. Its validity depends on that approximation and the model assumptions. It is distinct from a posterior probability, a model-evidence calculation, or proof of a physical mechanism. Alternative catalogue branches share observations and must not be treated as independent confirmations.

## Audit trail retained privately

The archive contains the original specifications and amendments, data manifest, historical failures, and numerical records. Reported baseline numbers are drawn from `m5_fits_corrected.json`; selection results from `m7_cuts.json`; Foundation comparisons from `m12_loo.json`; covariance scenarios from `m16_v4.json`; and Dovekie comparisons from `m17_dovekie.json`. The original results document records the mock and matched-catalogue analyses and their uncertainty limitations. These identifiers locate records for authorized reviewers; no implementation or executable material is included in this public repository.

## Request reproduction access

Use a [code access request](https://github.com/Flasher1717/desi-w0wa-results/issues/new?title=Code%20access%20request) to describe:

- Your research or review question and intended use.
- The results you want to reproduce and the materials you need.
- An optional professional identity or affiliation.

Public issues are visible to everyone. Do not include passwords, tokens, private datasets, identity documents, or other sensitive information. The project owner reviews access individually; filing a request does not automatically grant access.

## Attribution

Téo Alletz owns the project and its research decisions. Claude / Anthropic provided historical AI assistance; Codex / OpenAI reviewed the reported findings and prepared this public summary. These assistance credits do not imply endorsement or peer review by those organizations or by the observational collaborations.
