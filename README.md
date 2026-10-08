# DESI DR2 dark-energy refit: public results

This repository publishes the findings and methodological limitations of a personal cosmology project by Téo Alletz. The analysis compares flat ΛCDM with the evolving-dark-energy CPL model, using DESI DR2 BAO, a compressed CMB constraint, and alternative supernova compilations.

The concrete result is a measured sensitivity profile: the preference changes with the supernova release, low-redshift selection, and covariance treatment. This work does not establish evolving dark energy, identify the cause of a catalogue difference, or validate Janus or a mirror universe.

## Main findings

| Comparison | Result in this analysis |
|---|---|
| BAO + compressed CMB + original DES-SN5YR | 3.837σ preference for CPL |
| Same combination, requiring supernova redshift z > 0.1 | 1.464σ |
| Same pipeline with the Dovekie supernova release | 2.838σ |
| Effect of removing Foundation, original / Dovekie release | −1.335σ / −0.683σ |

These are formal significance equivalents under the stated statistical convention, not probabilities that a physical theory is true. The CMB calculation includes a disclosed calibration introduced after an initial validation failure. See the complete qualifications in [REPORT.md](REPORT.md) and [PROTOCOL.md](PROTOCOL.md).

## Read the work

- [Results, limitations, and primary references](REPORT.md)
- [Study design, data provenance, and access policy](PROTOCOL.md)

This publication summarizes analysis release **v1.2.0**. The implementation and its history are maintained separately in a private repository; this repository contains reports and figures only.

## Request implementation access

Open a [code access request](https://github.com/Flasher1717/desi-w0wa-results/issues/new?title=Code%20access%20request) with a short description of your project, intended use, and reproduction needs. A professional identity or institutional affiliation is optional. Do not post credentials, private datasets, identification documents, or other sensitive information in a public issue. Access is reviewed individually by the repository owner.

## Credits

- **Téo Alletz:** project owner and research decisions.
- **[Claude Code / Anthropic](https://github.com/claude):** historical AI assistance with the analysis and documentation.
- **[Codex / OpenAI](https://github.com/codex):** review of the reported findings and preparation of this public report.

These credits describe assistance. They do not imply institutional affiliation, endorsement, or peer review by Anthropic, OpenAI, DESI, or DES.
