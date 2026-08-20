# Exploring the Data — Virtual Cell Challenge 2026

This is a provisional sequence, not a fixed publication schedule.

### Exploring the Data I — Dataset construction, preprocessing, and coverage

Focus:

* How the challenge data were generated.
* How they were preprocessed.
* Independent preprocessing.
* General dataset statistics.
* Coverage per perturbation.
* Coverage per cell line.
* Sequencing depth / counts / detected genes.
* Imbalance and obvious anomalies.

### Exploring the Data II — Contamination

Focus:

* Evidence for ambient / cross-perturbation contamination.
* Decontamination using Trashpanda or related methods.
* How decontamination changes apparent perturbation structure.
* Clearly distinguish public methods/results from any confidential or employer-derived material.

### Exploring the Data III — Response

Focus:

* Which cells appear to respond to perturbation?
* Mixscape or related responder/nonresponder approaches.
* Response strength and heterogeneity.
* Whether average perturbation effects hide distinct response classes.

### Possible subsequent directions

#### Inhomogeneity

* Do individual perturbations induce multiple qualitatively different outcomes?
* Can those outcomes be separated from technical variation?
* Should perturbation models predict distributions rather than means?

#### Perturbation consistency

* How reproducible is a perturbation across cells?
* Across donors / batches / contexts where applicable?
* Are some perturbations much more internally coherent than others?

#### False negatives / label errors

Investigate whether some cells appear biologically consistent with a perturbation despite lacking the expected label.
