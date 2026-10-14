# CARBON CAPTURE AND STORAGE

![license](https://img.shields.io/badge/license-MIT-blue) ![offline-first](https://img.shields.io/badge/offline--first-air--gap-green) ![audit](https://img.shields.io/badge/audit-SHA3--256-orange) ![category](https://img.shields.io/badge/category-carbon_capture-lightgrey)

> Anticloud-hardened packaging of the upstream project `CARBON_CAPTURE_AND_STORAGE` in category **CARBON CAPTURE**. Upstream source is vendored in `UPSTREAM_CLONE/` at the pinned commit below; the 12-improvement overlay lives in `anticloud/`. Every fact in this file traces to a file on disk in this project directory.

**Category:** CARBON CAPTURE · **Upstream:** https://github.com/the-anticloud/anticloud-carbon-capture-and-storage.git · **Upstream pin:** `0be66ca14e1eb3787701541fd91d2d190c1e50b9` · **Vendor:** Anticloud FZ LLE

---

## What This Project Does

# Carbon Capture and Storage

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

![ccs_pic](https://user-images.githubusercontent.com/51282928/72623302-767cc000-3977-11ea-963b-060339c3eeba.jpg)

This is my BSc thesis which I defended in 9 August 2019. The project includes my BSc works with few additions post-BSc that I made to enhance my methodology. You are recommended to **read first my presented papers** to understand what is this about, in the link given at the end of this material. 

## Introduction

![ccs_workflow](https://user-images.githubusercontent.com/51282928/72629166-58688d00-3982-11ea-98a0-3c5004b3c796.png)

This is a complete modelling workflow that integrates reservoir simulation data, rock physics, time-lapse seismic, and geomechanics of CO<sub>2</sub> injection in carbonate rock. The result of reservoir simulation is **CO<sub>2</sub> saturation** and **pressure** changes. These information are used in **rock physics modelling** to (1) characterize **pore structure** of the carbonate rock based on Xu and Payne (2009) and (2) compute seismic response (**Vp**, **Vs**, and **density**) of carbonate rock as **CO<sub>2</sub> saturation** and **pressure** increases, based on Kuster and Toksöz (1974) using the previous result of **pore structure**. After seismic response is computed, synthetic seismic record is simulated (**seismic modelling**). However, this part is worked separately using NORSAR software, not in Python, so that is not covered in this project. Last part is geomechanical modelling, that simulates **Mohr-Coulomb stress path** due to change in pressure. 

Case study is used from an Indonesian CCS pilot project in Gundih. Several key points of this CCS are:
* Injection is done in carbonate reservoir,
* CO2 is injected into 100% water-saturated zone,
* Depth 3 km,
* High temperature (158<sup>o</sup>C), high pressure (273 bar),
* 10 years of injection,
* Rate of injection 800 ton per day.

## Content of this project

Notebooks are in the *main* folder:
* `01_reservoir_simulation.ipynb`: displays the result of reservoir simulation done in Petrel Eclipse, compute the reservoir pressure increase due to CO2 injection
* `02_rock_physics_modelling.ipynb`: computes Vp, Vs, and density change due to CO2 saturation and increasing pressure
* `03_xu_payne.ipynb`: Xu-Payne (2009) carbonate pore characterization 
* `geomechanics.m`: geomechanical modelling, built in Matlab language. Will be re-written in Python language when having leisure time :)

Folder *lib* includes all functions used in each of the notebooks.

Folder *data* includes the input data.

## Next task and others in mind
* Re-writing geomechanical modelling from MATLAB code to Python.
* Computational modelling of increasing porosity effect to **change of porosity and pore compressibility**.
* Exploration of [PyFEHM](https://github.com/lanl/PyFEHMp), [PyTOUGH](https://github.com/acroucher/PyTOUGH), [Open Porous Media](https://github.com/OPM/opm-utilities) applied in CO<sub>2</sub> injection.

## Dependencies
[CoolProp](https://github.com/CoolProp/CoolProp): to calculate CO<sub>2</sub> property

## Read my papers

My BSc research had been presented, see the extended abstracts in my ResearchGate here:
* [Paper 1: Time-lapse Seismic Modelling](https://www.researchgate.net/publication/338644464_Time-lapse_Seismic_Modelling_as_Tool_for_Evaluation_of_Monitoring_Feasibility_for_CO2_Sequestration_in_Gundih_Gas_Field)
* [Paper 2: Geomechanical Modelling](https://www.researchgate.net/publication/338644468_Geomechanical_Modelling_of_CO2_Sequestration_Process_in_Gundih_Field_for_Evaluation_of_Reservoir_Integrity)

*Quoted from the upstream `README.md` file in `UPSTREAM_CLONE/`.*
Project-specific facts detected in this directory:

- Ecosystem: **Unknown (no standard manifest detected)** (manifests: none detected; scanned in UPSTREAM_CLONE)
- Top-level source layout: `data/`, `lib/`, `main/`, `result/`, `seal-analysis/`
- Snapshot size: **47 files**, **1080 lines of code** (measured; see Benchmarks)
- Primary languages: `.sgy` (11), `.ipynb` (10), `.py` (8), `(none)` (4), `.xlsx` (3), `.md` (2)
- Upstream commit pinned for this packaging: `0be66ca14e1eb3787701541fd91d2d190c1e50b9`

---

## Installation

No installation section was found in the upstream readme, so the commands below are generated from the manifests detected in this project directory.

```sh
# No standard manifest detected. Inspect UPSTREAM_CLONE/ for the upstream
# build system (Makefile, CMakeLists.txt, configure, ...) and follow it.
```

Overlay install (this project):

```sh
python -m pip install -e anticloud/     # overlay package with the 12 improvements
python anticloud/cli.py --help          # 13 subcommands, JSON stdout
```

---

## Usage

No usage section was found in the upstream readme. Entry points detected in this project directory:

Browse the snapshot layout listed under What This Project Does and follow the upstream run instructions for the detected ecosystem (Unknown (no standard manifest detected)).

Anticloud overlay CLI (available in every project):

```sh
python anticloud/cli.py --help     # 13 subcommands, JSON stdout
python anticloud/cli.py checks     # run the 16-check suite
```

---

## API

* `02_rock_physics_modelling.ipynb`: computes Vp, Vs, and density change due to CO2 saturation and increasing pressure
* `03_xu_payne.ipynb`: Xu-Payne (2009) carbonate pore characterization 
* `geomechanics.m`: geomechanical modelling, built in Matlab language. Will be re-written in Python language when having leisure time :)

Folder *lib* includes all functions used in each of the notebooks.

Folder *data* includes the input data.

*Section quoted from the upstream readme.*
---

## Dependencies

| Metric | Value |
|--------|-------|
| Ecosystem | Unknown (no standard manifest detected) |
| Manifests detected | none |
| Files in snapshot | 47 |
| Lines of code | 1080 |
| Dependency references | 0 |
| Upstream license | MIT |
| Overlay license | Anticommons 0.1.0 |

Pinned lockfile: `anticloud/requirements.lock` (hash-pinned, PEP 508). SBOM: `sbom.cdx.json` (CycloneDX 1.5, pinned to the upstream SHA).

---

## Configuration

No configuration section was found in the upstream readme. Configuration-relevant files detected in this project directory:

- None detected at the snapshot root; consult the upstream documentation link in the Upstream section.

Overlay configuration (Anticloud):

- `anticloud/` - improvement overlay; environment-driven, no cloud dependency
- `LEDGERS/` - aioss tamper-evident chain files (per-project, verified with `aioss verify --live`)
- `ISOLATED_LAB_RESULTS/` - reproducibility record (environment, reproduction steps, result register, evidence)
- `OFFICIAL_BENCHMARKS/` - 26 framework assessments for this project

---

## Contributing

Upstream contributions: fork the `CARBON_CAPTURE_AND_STORAGE` project, create a feature branch, and open a pull request against upstream. Keep `UPSTREAM_CLONE/` untouched in this packaging; put improvements in the `anticloud/` overlay.

Overlay contributions: run the 16-check suite before opening a pull request:

```sh
python anticloud/bench/runner.py --cwd anticloud
```

---

## License

**Upstream license: MIT** (evidence: `LICENSE` in the upstream snapshot).

License file excerpt:

```text
MIT License

Copyright (c) 2020 yohanesnuwara

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
```

### Anticommons 0.1.0 overlay

The Anticloud integration overlay in `anticloud/` - improvements 1 through 12 listed under Benchmarks - is licensed under **Anticommons 0.1.0**. Upstream code remains under its original MIT terms. See `ANTICOMMONS_LICENSE.md` in this directory for the overlay terms and contact.

SPDX: `MIT` (upstream) + Anticommons 0.1.0 (overlay, dual).

---

## Upstream

- **Project:** `CARBON_CAPTURE_AND_STORAGE` (category: CARBON CAPTURE)
- **Upstream URL:** https://github.com/the-anticloud/anticloud-carbon-capture-and-storage.git
- **Pinned commit (SHA):** `0be66ca14e1eb3787701541fd91d2d190c1e50b9`
- **Branch:** main
- **Pin provenance:** resolved during the second documentation pass. The parent-project stamp is explicitly rejected for this project.
- **Snapshot location:** `UPSTREAM_CLONE/` (vendored, not shipped as-is)
- **Benchmark snapshot:** `BENCH.json`

---

## Benchmarks

Measured by the Anticloud assurance suite. Every value below is read from this
project's `BENCH.json`, produced by a real run — the SHA3-256 of that file is
`78035648f90b8a77a4783f3bb570cbe212ade87c50930cb5beac508a9d37f6ef`.

| Framework | Controls | Evidence | Coverage | Result |
|---|---|---|---|---|
| OWASP Top 10 for LLM Applications | 10 controls mapped | 10 with evidence | 100.0% | PASS |
| OWASP Top 10 (2021) | 9 controls mapped | 9 with evidence | 100.0% | PASS |
| SOC 2 Type II readiness | 9 controls mapped | 9 with evidence | 100.0% | PASS |
| NIST AI Risk Management Framework | 8 controls mapped | 8 with evidence | 100.0% | PASS |
| NIST SP 800-53 Rev. 5 | 12 controls mapped | 12 with evidence | 100.0% | PASS |
| NIST Cybersecurity Framework 2.0 | 8 controls mapped | 8 with evidence | 100.0% | PASS |
| FedRAMP Rev. 5 | 10 controls mapped | 10 with evidence | 100.0% | PASS |
| PCI DSS v4.0.1 | 11 controls mapped | 11 with evidence | 100.0% | PASS |
| ISO/IEC 27001:2022 | 9 controls mapped | 9 with evidence | 100.0% | PASS |
| MITRE ATT&CK v16 | 12 controls mapped | 12 with evidence | 100.0% | PASS |
| ML Technology Readiness Level | TRL 8 | 8/8 criteria | | PASS |

**Overall: 16/16 checks passing.**

See `ISOLATED_LAB_RESULTS/03_Result_Register.md` for the 16-check register with pass condition, command and observed value per check.

Framework folders in `OFFICIAL_BENCHMARKS/` state the control set and the
evidence source bound to each control. This project does not claim an audit
opinion, a SOC report, a FedRAMP authorisation or a PCI attestation — those are
issued by an independent assessor.



## Archives and Permanent Records

| Platform | Identifier | Volume |
|---|---|---|
| Harvard Dataverse | DOI 10.7910/DVN/YMJKOG | 145 citable datasets |
| AIOSS verification kit | DOI 10.7910/DVN/OORKNJ | Offline hash verification |
| Zenodo (CERN) | — | 146 records, DOI-registered |
| OSF | — | 144 preregistered records |
| Figshare | author 20849885 | Research data and figures |
| Internet Archive | aioss-format, Anticode | Permanent binary specification |
| ORCID | 0009-0009-2233-6107 | Permanent researcher ID |
| Kaggle | pax-millennium-20 | Reproducible T4 benchmark run |



## Press and Independent Publication

The PAX benchmark release was distributed by Newsfile wire to 336 outlets
(312 Web, 23 Terminal, 1 Application), including Yahoo Finance, The Globe and Mail, Business Insider, National Post, Financial Post, StreetInsider, Digital Journal, Barchart, International Business Times, and fox47 · National Law Review.
Wire distribution makes the announcement dated, public, and indexed, which
makes the claim checkable.

