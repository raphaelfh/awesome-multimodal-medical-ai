# awesome-multimodal-medical-ai

A curated list of multimodal medical AI. Tools, agents, papers and datasets spanning medical imaging, clinical text/EHR, genomics, and multimodal fusion models.

**Access** (datasets and platforms): 🟢 Open (direct download) · 🟡 Registration (free account or click-through terms) · 🔴 Application (formal request, data use agreement or committee review)

## Contents

- [Datasets](#datasets)
  - [Population-Scale Biobanks](#population-scale-biobanks)
  - [Brain & Mental Health](#brain--mental-health)
  - [Cancer Imaging](#cancer-imaging)
- [Repositories & Platforms](#repositories--platforms)
- [Libraries & Frameworks](#libraries--frameworks)
- [Tools](#tools)
- [Papers](#papers)
  - [Surveys & Field Overviews](#surveys--field-overviews)
  - [Generalist & Vision-Language Models](#generalist--vision-language-models)
  - [Domain Foundation Models](#domain-foundation-models)
  - [Multimodal Fusion for Prognosis](#multimodal-fusion-for-prognosis)
  - [Genomics & Multi-omics](#genomics--multi-omics)
  - [Radiology & Report Generation](#radiology--report-generation)
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

## Libraries & Frameworks

Code you import into your own pipeline.

| Library | Modalities | Built on | License |
| :-- | :-- | :-- | :-- |
| **[CLAM](https://github.com/mahmoodlab/CLAM)**<br><sub>Weakly-supervised attention-MIL for whole-slide classification from slide-level labels</sub> | `pathology` | PyTorch | GPLv3 |
| **[MedCAT](https://github.com/CogStack/MedCAT)**<br><sub>Extracts clinical concepts from free text and links them to SNOMED-CT or UMLS</sub> | `clinical notes` | spaCy | Elastic 2.0<br><sub>not an OSI licence</sub> |
| **[medspaCy](https://github.com/medspacy/medspacy)**<br><sub>spaCy components for clinical text: sectioning, context and negation detection</sub> | `clinical notes` | spaCy | MIT |
| **[MONAI](https://monai.io/)**<br><sub>The default framework for medical imaging deep learning (NVIDIA, NIH, KCL)</sub> | `MRI` `CT` `PET` `pathology` | PyTorch | Apache-2.0 |
| **[nnU-Net](https://github.com/MIC-DKFZ/nnUNet)**<br><sub>Self-configuring segmentation that adapts to a new dataset without manual tuning</sub> | `MRI` `CT` | PyTorch | Apache-2.0 |
| **[PyHealth](https://github.com/sunlabuiuc/PyHealth)**<br><sub>Makes no datatype assumption, so signals, notes, labs, codes and images combine in one pipeline</sub> | `EHR` `signals` `notes` `imaging` `codes` | PyTorch | MIT |
| **[TIAToolbox](https://github.com/TissueImageAnalytics/tiatoolbox)**<br><sub>End-to-end whole-slide pipelines: reading, stain normalization, segmentation, inference</sub> | `pathology` | PyTorch | BSD-3-Clause |
| **[TorchIO](https://github.com/TorchIO-project/torchio)**<br><sub>3D preprocessing, augmentation and patch sampling for volumetric medical images</sub> | `MRI` `CT` | PyTorch | Apache-2.0 |

## Tools

Applications you run, rather than libraries you import. Together they cover the annotation loop that produces training data.

| Tool | Modalities | Highlights | License |
| :-- | :-- | :-- | :-- |
| **[3D Slicer](https://www.slicer.org/)**<br><sub>Desktop platform for medical image analysis and visualization</sub> | `MRI` `CT` `PET` `DICOM` | Segmentation, registration, 3D rendering<br><sub>large extension ecosystem</sub> | BSD-style |
| **[MONAI Label](https://github.com/Project-MONAI/MONAILabel)**<br><sub>AI-in-the-loop annotation server that learns from the labels you make</sub> | `MRI` `CT` `pathology` | Plugs into 3D Slicer, OHIF and QuPath<br><sub>the connective tissue between the other three</sub> | Apache-2.0 |
| **[OHIF Viewer](https://github.com/OHIF/Viewers)**<br><sub>Zero-footprint web DICOM viewer and application framework</sub> | `DICOM` | Runs in the browser<br><sub>connects to a DICOMweb server</sub> | MIT |
| **[QuPath](https://qupath.github.io/)**<br><sub>Reference open-source application for whole-slide image analysis</sub> | `pathology` | Scriptable and batchable<br><sub>6,000+ citations</sub> | GPLv3 |

## Papers

Grouped by subfield, newest first within each group. `Code` links to official weights or implementation where one exists.

### Surveys & Field Overviews

Start here if you are new to the field.

| Paper | Modalities | Venue | Code |
| :-- | :-- | :-- | :-- |
| **[Multimodal Foundation Models for Medical Imaging](https://www.medrxiv.org/content/10.1101/2024.10.23.24316003v1.full)**<br><sub>Systematic review plus practical implementation guidelines</sub> | `imaging` `text` | medRxiv 2024 | — |
| **[Foundation models for generalist medical artificial intelligence](https://www.nature.com/articles/s41586-023-05881-4)**<br><sub>Moor et al. set out the GMAI paradigm: one model flexibly interpreting many modality combinations</sub> | `imaging` `EHR` `labs` `genomics` `text` | Nature 2023 | — |
| **[Multimodal biomedical AI](https://doi.org/10.1038/s41591-022-01981-2)**<br><sub>Acosta et al., the survey that defined the field and still the best map of it</sub> | `imaging` `EHR` `genomics` `wearables` | Nature Medicine 2022 | — |

### Generalist & Vision-Language Models

| Paper | Modalities | Venue | Code |
| :-- | :-- | :-- | :-- |
| **[Towards Generalist Biomedical AI](https://arxiv.org/abs/2307.14334)**<br><sub>Med-PaLM M handles clinical text, imaging and genomics in one model without per-task finetuning</sub> | `imaging` `text` `genomics` | arXiv 2023 | — |
| **[LLaVA-Med](https://arxiv.org/abs/2306.00890)**<br><sub>Curates instruction-following data from PubMed to adapt LLaVA to biomedicine in under a day</sub> | `imaging` `text` | NeurIPS 2023 | [microsoft/LLaVA-Med](https://github.com/microsoft/LLaVA-Med) |
| **[BiomedCLIP](https://arxiv.org/abs/2303.00915)**<br><sub>Contrastive pretraining on 15M figure-caption pairs scraped from PubMed</sub> | `imaging` `text` | NEJM AI 2025<br><sub>arXiv 2023</sub> | — |

### Domain Foundation Models

| Paper | Modalities | Venue | Code |
| :-- | :-- | :-- | :-- |
| **[Virchow](https://www.nature.com/articles/s41591-024-03141-0)**<br><sub>Clinical-grade pathology model aimed specifically at rare cancer detection</sub> | `pathology` | Nature Medicine 2024 | — |
| **[UNI](https://www.nature.com/articles/s41591-024-02857-3)**<br><sub>Self-supervised on 100M images from 100k+ slides, with no organ, grade or molecular labels</sub> | `pathology` | Nature Medicine 2024 | [mahmoodlab/UNI](https://github.com/mahmoodlab/UNI) |
| **[CONCH](https://www.nature.com/articles/s41591-024-02856-4)**<br><sub>Vision-language pathology model, so a pathologist can search slides by describing a morphology</sub> | `pathology` `text` | Nature Medicine 2024 | [mahmoodlab/CONCH](https://github.com/mahmoodlab/CONCH) |
| **[RETFound](https://www.nature.com/articles/s41586-023-06555-x)**<br><sub>Retinal images predicting systemic disease, including heart failure and myocardial infarction</sub> | `retinal imaging` | Nature 2023 | [openmedlab/RETFound_MAE](https://github.com/openmedlab/RETFound_MAE) |

### Multimodal Fusion for Prognosis

| Paper | Modalities | Venue | Code |
| :-- | :-- | :-- | :-- |
| **[MedFuse](https://arxiv.org/abs/2207.07027)**<br><sub>Tackles the asynchronous, missing-modality reality of clinical data instead of assuming paired inputs</sub> | `chest X-ray` `EHR time-series` | MLHC 2022 | [nyuad-cai/MedFuse](https://github.com/nyuad-cai/MedFuse) |
| **[PORPOISE](https://www.cell.com/cancer-cell/fulltext/S1535-6108%2822%2900317-8)**<br><sub>Pan-cancer survival from whole-slide images fused with molecular profiles, with interpretability</sub> | `pathology` `genomics` `transcriptomics` | Cancer Cell 2022 | [mahmoodlab/PORPOISE](https://github.com/mahmoodlab/PORPOISE) |
| **[MCAT](https://openaccess.thecvf.com/content/ICCV2021/html/Chen_Multimodal_Co-Attention_Transformer_for_Survival_Prediction_in_Gigapixel_Whole_Slide_ICCV_2021_paper.html)**<br><sub>Co-attention between histology and omic tokens for gigapixel survival prediction</sub> | `pathology` `genomics` | ICCV 2021 | — |

### Genomics & Multi-omics

| Paper | Modalities | Venue | Code |
| :-- | :-- | :-- | :-- |
| **[A technical review of multi-omics data integration methods](https://academic.oup.com/bib/article/26/4/bbaf355/8220754)**<br><sub>Traces the path from classical statistics to deep generative approaches</sub> | `multi-omics` | Briefings in Bioinformatics 2025 | — |
| **[Multimodal deep learning for single-cell multi-omics integration](https://academic.oup.com/bib/article/24/5/bbad313/7256792)**<br><sub>Review focused on the single-cell case, where modalities are hardest to align</sub> | `single-cell` `multi-omics` | Briefings in Bioinformatics 2023 | — |
| **[Multi-omics integration through deep learning for disease diagnosis and prognosis](https://www.frontiersin.org/journals/genetics/articles/10.3389/fgene.2023.1199087/full)**<br><sub>Review organized by clinical use rather than by architecture</sub> | `multi-omics` `clinical` | Frontiers in Genetics 2023 | — |

### Radiology & Report Generation

| Paper | Modalities | Venue | Code |
| :-- | :-- | :-- | :-- |
| **[LLaVA-Rad](https://arxiv.org/abs/2403.08002)**<br><sub>Deliberately lightweight and open-access, with automated report evaluation</sub> | `chest X-ray` `text` | arXiv 2024 | — |
| **[RadFM](https://arxiv.org/abs/2308.02463)**<br><sub>Handles 2D and 3D scans, multi-image inputs and interleaved vision-language cases</sub> | `CT` `MRI` `X-ray` `text` | arXiv 2023 | — |
| **[CheXzero](https://www.nature.com/articles/s41551-022-00936-9)**<br><sub>Expert-level zero-shot pathology detection learned from unannotated reports alone</sub> | `chest X-ray` `text` | Nature BME 2022 | [rajpurkarlab/CheXzero](https://github.com/rajpurkarlab/CheXzero) |

## Find by Modality

Datasets and platforms by data type. Libraries and tools carry their own modality tags, and papers are already grouped by subfield above.

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
4. Follows the table format in use for the section it joins: name and one-line description, modality tags, then the columns that section uses.

Rows are ordered alphabetically, except papers, which run newest first within their subfield. New datasets and platforms should also be added to [Find by Modality](#find-by-modality).

</details>

## License

[MIT](LICENSE)
