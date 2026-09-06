# awesome-multimodal-medical-ai

A curated list of multimodal medical AI. Tools, agents, papers and datasets spanning medical imaging, clinical text/EHR, genomics, and multimodal fusion models.

## Contents

- [How to Read the Entries](#how-to-read-the-entries)
- [Datasets](#datasets)
  - [Population-Scale Biobanks](#population-scale-biobanks)
  - [Brain & Mental Health](#brain--mental-health)
  - [Cancer Imaging](#cancer-imaging)
- [Repositories & Platforms](#repositories--platforms)
- [Contributing](#contributing)

## How to Read the Entries

Every entry gives the resource, one sentence on what it is and why it matters,
then the modalities it covers and how you get access:

- **Open** — direct download, no account required.
- **Registration** — free account or click-through data use terms.
- **Application** — formal request, data use agreement or committee review.

## Datasets

### Population-Scale Biobanks

- **[UK Biobank](https://www.ukbiobank.ac.uk/)** — Deep-phenotyped cohort of ~500,000 UK adults linking genomics, blood and urine biomarkers and lifestyle data to hospital, cancer-registry and mortality records, with multi-organ imaging completed for 100,000 of them.
  *Modalities:* MRI (brain, cardiac, abdominal), ultrasound, DEXA, genomics, biomarkers, EHR · *Access:* Application (approved research, access fee)

### Brain & Mental Health

- **[ABIDE](https://fcon_1000.projects.nitrc.org/indi/abide/)** — Autism benchmark aggregating resting-state fMRI, structural MRI and phenotypic data; ABIDE I pools 1,112 scans from 17 sites and ABIDE II adds 1,114 subjects from 19 sites, with some longitudinal follow-up.
  *Modalities:* rs-fMRI, structural MRI, phenotypic/clinical · *Access:* Open
- **[ADNI](https://adni.loni.usc.edu/)** — Longitudinal Alzheimer's study running since 2004 that pairs serial MRI with amyloid, tau and FDG PET, genetics, CSF and plasma biomarkers and repeated cognitive testing across its ADNI 1/GO/2/3/4 phases.
  *Modalities:* MRI (structural, diffusion, functional), PET, genomics, CSF/plasma biomarkers, cognitive · *Access:* Application (data use agreement via LONI IDA)
- **[Cam-CAN](https://opendata.mrc-cbu.cam.ac.uk/projects/camcan/)** — Cross-sectional adult lifespan sample of ~700 people aged 18–87 with structural and functional MRI, resting and task MEG, and cognitive scores spanning attention, emotion, action, language and memory.
  *Modalities:* structural MRI, fMRI, MEG, cognitive/behavioural · *Access:* Application
- **[COBRE](https://fcon_1000.projects.nitrc.org/indi/retro/cobre.html)** — Compact schizophrenia benchmark with resting-state fMRI, anatomical MRI and phenotypic data for 72 patients and 74 healthy controls (ages 18–65), widely reused as a psychiatric-classification baseline.
  *Modalities:* rs-fMRI, structural MRI, phenotypic/clinical · *Access:* Open
- **[Healthy Brain Network (HBN)](https://data.healthybrainnetwork.org/main.php)** — Child Mind Institute biobank of children and adolescents aged 5–21 for transdiagnostic mental-health and learning-disorder research, combining imaging, neurophysiology and wearables with deep clinical phenotyping.
  *Modalities:* MRI, EEG, eye-tracking, actigraphy, voice/video, genomics, clinical phenotyping · *Access:* Application (data use agreement)
- **[Human Connectome Project (HCP)](https://www.humanconnectome.org/)** — Reference maps of healthy brain connectivity, with 1,206 young adults scanned at 3T (structural, task and resting fMRI, diffusion MRI) plus 7T and MEG for subsets, alongside behavioural and genetic measures; Lifespan and disease-focused studies extend the same protocols.
  *Modalities:* structural MRI, fMRI, diffusion MRI, MEG, behavioural, genomics · *Access:* Registration (open terms); Application for restricted family and genetic data

### Cancer Imaging

- **[The Cancer Imaging Archive (TCIA)](https://www.cancerimagingarchive.net/)** — NCI-funded archive of de-identified cancer imaging organized into disease-specific collections, many of them linked to clinical outcomes, genomics and expert annotations, which makes it a common starting point for radiogenomics work.
  *Modalities:* CT, MRI, PET, digital pathology, genomics, clinical/outcomes, annotations · *Access:* Open (some collections require a data use agreement)

## Repositories & Platforms

- **[1000 Functional Connectomes Project / INDI](https://fcon_1000.projects.nitrc.org/)** — Umbrella data-sharing initiative distributing resting-state fMRI (and later DTI) from more than 30 sites, and the host for several phenotypically rich collections including ABIDE, COBRE, ADHD-200 and CoRR.
  *Modalities:* rs-fMRI, structural MRI, DTI, phenotypic/clinical · *Access:* Open
- **[OpenNeuro](https://openneuro.org/)** — Free platform for validating and sharing BIDS-formatted brain data across MRI, PET, MEG, EEG and iEEG, with versioned public datasets downloadable from the browser, CLI or S3.
  *Modalities:* MRI, PET, MEG, EEG, iEEG · *Access:* Open (most datasets under CC0)
- **[PhysioNet](https://physionet.org/)** — MIT-hosted archive of physiological signals and clinical data, including ECG, EEG and waveform databases and the MIMIC critical-care records, with open tooling and a credentialed tier for sensitive clinical data.
  *Modalities:* ECG, EEG, physiological waveforms, clinical records, imaging · *Access:* Open, with a credentialed tier for restricted databases

## Contributing

Suggestions are welcome. Before opening a pull request, check that the resource:

1. Is genuinely about multimodal medical AI, not general-purpose machine learning.
2. Has a working, canonical link that points to the resource itself rather than to an aggregator page.
3. Is not already listed, directly or as part of a repository already listed here.
4. Follows the entry format above: one sentence on what it is and why it matters, plus its modalities and access level.

Entries are ordered alphabetically within each section.

## License

[MIT](LICENSE)
