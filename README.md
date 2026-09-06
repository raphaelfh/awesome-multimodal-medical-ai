# awesome-multimodal-medical-ai

A curated list of multimodal medical AI. Tools, agents, papers and datasets spanning medical imaging, clinical text/EHR, genomics, and multimodal fusion models.

**Access:** 🟢 Open (direct download) · 🟡 Registration (free account or click-through terms) · 🔴 Application (formal request, data use agreement or committee review)

## Contents

- [Datasets](#datasets)
  - [Population-Scale Biobanks](#population-scale-biobanks)
  - [Brain & Mental Health](#brain--mental-health)
  - [Cancer Imaging](#cancer-imaging)
- [Repositories & Platforms](#repositories--platforms)
- [Find by Modality](#find-by-modality)
- [Contributing](#contributing)

## Datasets

### Population-Scale Biobanks

| Dataset | Modalities | Scale | Access |
| :-- | :-- | :-- | :-- |
| **[UK Biobank](https://www.ukbiobank.ac.uk/)**<br><sub>Genomics, biomarkers and EHR linkage with multi-organ imaging</sub> | `MRI` `ultrasound` `DEXA` `genomics` `biomarkers` `EHR` | ~500,000 adults<br><sub>100,000 imaged (target met 2025)</sub> | 🔴 Application<br><sub>access fee</sub> |

### Brain & Mental Health

| Dataset | Modalities | Scale | Access |
| :-- | :-- | :-- | :-- |
| **[ABIDE](https://fcon_1000.projects.nitrc.org/indi/abide/)**<br><sub>Multi-site autism benchmark with rich phenotypic data</sub> | `rs-fMRI` `sMRI` `phenotype` | 1,112 subjects / 17 sites (I)<br><sub>1,114 / 19 sites (II)</sub> | 🟢 Open |
| **[ADNI](https://adni.loni.usc.edu/)**<br><sub>Longitudinal Alzheimer's biomarker cohort, running since 2004</sub> | `MRI` `PET` `genomics` `CSF/plasma` `cognitive` | 4 phases<br><sub>ADNI 1 / GO / 2 / 3 / 4</sub> | 🔴 Application<br><sub>DUA via LONI IDA</sub> |
| **[Cam-CAN](https://opendata.mrc-cbu.cam.ac.uk/projects/camcan/)**<br><sub>Adult lifespan sample pairing MRI with MEG and cognition</sub> | `sMRI` `fMRI` `MEG` `cognitive` | ~700 subjects<br><sub>ages 18–87</sub> | 🔴 Application |
| **[COBRE](https://fcon_1000.projects.nitrc.org/indi/retro/cobre.html)**<br><sub>Compact schizophrenia classification baseline</sub> | `rs-fMRI` `sMRI` `phenotype` | 146 subjects<br><sub>72 patients / 74 controls</sub> | 🟢 Open |
| **[Healthy Brain Network](https://data.healthybrainnetwork.org/main.php)**<br><sub>Pediatric transdiagnostic biobank with deep phenotyping</sub> | `MRI` `EEG` `eye-tracking` `actigraphy` `genomics` `clinical` | 10,000+ target<br><sub>ages 5–21; 3,000+ with EEG</sub> | 🔴 Application<br><sub>data use agreement</sub> |
| **[Human Connectome Project](https://www.humanconnectome.org/)**<br><sub>Reference maps of healthy brain connectivity</sub> | `sMRI` `fMRI` `dMRI` `MEG` `behavioral` `genomics` | 1,206 young adults<br><sub>7T and MEG for subsets</sub> | 🟡 Registration<br><sub>🔴 for family/genetic data</sub> |

### Cancer Imaging

| Dataset | Modalities | Scale | Access |
| :-- | :-- | :-- | :-- |
| **[The Cancer Imaging Archive](https://www.cancerimagingarchive.net/)**<br><sub>De-identified cancer imaging linked to clinical and genomic data</sub> | `CT` `MRI` `PET` `pathology` `genomics` `clinical` | Per cancer-type collection<br><sub>NCI-funded</sub> | 🟢 Open<br><sub>🔴 some collections</sub> |

## Repositories & Platforms

Aggregators worth browsing directly. Several datasets above are distributed through them.

| Platform | Modalities | Highlights | Access |
| :-- | :-- | :-- | :-- |
| **[1000 Functional Connectomes / INDI](https://fcon_1000.projects.nitrc.org/)**<br><sub>Umbrella initiative for open rs-fMRI sharing</sub> | `rs-fMRI` `sMRI` `DTI` `phenotype` | 1,200+ datasets / 33 sites<br><sub>hosts ABIDE, COBRE, ADHD-200, CoRR</sub> | 🟢 Open |
| **[OpenNeuro](https://openneuro.org/)**<br><sub>BIDS-validated sharing for imaging and neurophysiology</sub> | `MRI` `PET` `MEG` `EEG` `iEEG` | Versioned public datasets<br><sub>browser, CLI or S3 download</sub> | 🟢 Open<br><sub>most datasets CC0</sub> |
| **[PhysioNet](https://physionet.org/)**<br><sub>Physiological signals and critical-care clinical records</sub> | `ECG` `EEG` `waveforms` `clinical` | MIT-hosted<br><sub>includes the MIMIC databases</sub> | 🟢 Open<br><sub>🔴 credentialed tier</sub> |

## Find by Modality

- **Imaging (MRI/CT/PET):** [ADNI](#brain--mental-health) · [Cam-CAN](#brain--mental-health) · [HCP](#brain--mental-health) · [HBN](#brain--mental-health) · [TCIA](#cancer-imaging) · [UK Biobank](#population-scale-biobanks) · [OpenNeuro](#repositories--platforms)
- **Neurophysiology (EEG/MEG/iEEG):** [Cam-CAN](#brain--mental-health) · [HBN](#brain--mental-health) · [HCP](#brain--mental-health) · [OpenNeuro](#repositories--platforms) · [PhysioNet](#repositories--platforms)
- **Genomics:** [ADNI](#brain--mental-health) · [HBN](#brain--mental-health) · [HCP](#brain--mental-health) · [TCIA](#cancer-imaging) · [UK Biobank](#population-scale-biobanks)
- **Clinical records / EHR:** [PhysioNet](#repositories--platforms) · [TCIA](#cancer-imaging) · [UK Biobank](#population-scale-biobanks)
- **Digital pathology:** [TCIA](#cancer-imaging)
- **Free to start today (🟢):** [ABIDE](#brain--mental-health) · [COBRE](#brain--mental-health) · [FCP/INDI](#repositories--platforms) · [OpenNeuro](#repositories--platforms) · [PhysioNet](#repositories--platforms) · [TCIA](#cancer-imaging)

## Contributing

<details>
<summary>Checklist before opening a pull request</summary>

Suggestions are welcome. Check that the resource:

1. Is genuinely about multimodal medical AI, not general-purpose machine learning.
2. Has a working, canonical link that points to the resource itself rather than to an aggregator page.
3. Is not already listed, directly or as part of a repository already listed here.
4. Follows the table format in use: name and one-line description, modality tags, scale, and access level.

Rows are ordered alphabetically within each table, and any new entry should also be added to [Find by Modality](#find-by-modality).

</details>

## License

[MIT](LICENSE)
