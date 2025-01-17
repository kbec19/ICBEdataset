
  - [The International Crisis Behavior Events
    (ICBe)](#the-international-crisis-behavior-events-icbe)
  - [The Paper:](#the-paper)
  - [The Data:](#the-data)
  - [The Authors:](#the-authors)
  - [Citation:](#citation)
  - [Replication Code and Analysis](#replication-code-and-analysis)
      - [Self Contained Package](#self-contained-package)
  - [RMarkdown files](#rmarkdown-files)
      - [Replication Data](#replication-data)
      - [Replication Paper](#replication-paper)
  - [Data inputs:](#data-inputs)
      - [ICBe preparation](#icbe-preparation)
      - [External datasets](#external-datasets)
      - [License](#license)

<!-- README.md is generated from README.Rmd. Please edit that file -->

[![CC
BY-NC-SA 4.0](https://img.shields.io/badge/License-CC%20BY--NC--SA%204.0-lightgrey.svg)](http://creativecommons.org/licenses/by-nc-sa/4.0/)

## The International Crisis Behavior Events (ICBe)

This is a github repository for the International Crisis Behavior Events
(ICBe) dataset. Submit any issues regarding the dataset, paper, or
github repository using [the issues
tab](https://github.com/CenterForPeaceAndSecurityStudies/ICBEdataset/issues/new/choose).

## The Paper:

[Introducing the ICBe Dataset: Very High Recall and Precision Event
Extraction from Narratives about International
Crises](https://github.com/CenterForPeaceAndSecurityStudies/ICBEdataset/blob/master/replication_paper/IntroducingICBe_DouglassEtAl_2021_BetaDraft_bookdown.pdf).

The [ArXiv pre-print](https://arxiv.org/abs/2202.07081) was posted on
February 15, 2022.

## The Data:

The agreed datasets are the final dataset used in much of the paper and
figures. It includes our best efforts at cleaning the data and
reconciling intercoder agreement. The dataset is available in long and
wide format. The data is also available in .tsv format in the same
folders.

  - [ICBe\_V1\_long\_agreement.Rds](https://github.com/CenterForPeaceAndSecurityStudies/ICBEdataset/blob/master/replication_data/out/ICBe_V1_wide_agreed.Rds)
      - All coded values and information about how often they were
        selected by coders.  
  - [ICBe\_V1\_long\_agreed.Rds](https://github.com/CenterForPeaceAndSecurityStudies/ICBEdataset/blob/master/replication_data/out/ICBe_V1_long_agreed.Rds)
      - `ICBe_V1_long_agreement.Rds` filtered down only to those codings
        that were agreed upon (see Algorithm 1 in paper).
  - [ICBe\_V1\_wide\_agreed.Rds](https://github.com/CenterForPeaceAndSecurityStudies/ICBEdataset/blob/master/replication_data/out/ICBe_V1_wide_agreed.Rds)
      - `ICBe_V1_long_agreed.Rds` in wide form where each row is an
        event.

The coding and cleaning process are described in the paper with
additional information and details about the variables in the codebook.
- [ICBEdataset
Codebook](https://docs.google.com/document/d/1aJkweohbfIWtNpJw1CmXbeIiK6czbJ5iPyKwiYP1YlU/edit?usp=sharing)

## The Authors:

[Rex W. Douglass](http://www.rexdouglass.com), [Thomas Leo
Scherer](http://tlscherer.com/), [J. Andrés
Gannon](https://jandresgannon.com/), [Erik
Gartzke](http://erikgartzke.com/), [Jon
Lindsay](https://www.jonrlindsay.com/), [Shannon
Carcelli](https://www.shannoncarcelli.com/), Jonathan Wilkenfeld, David
M. Quinn, Catherine Aiken, Jose Miguel Cabezas Navarro, Neil Lund, Egle
Murauskaite, and Diana Partridge.

## Citation:

For any use of the dataset or paper, please cite:

Douglass, Rex W., Thomas Leo Scherer, J. Andrés Gannon, Erik Gartzke,
Jon Lindsay, Shannon Carcelli, Jonathan Wiklenfeld, David M. Quinn,
Catherine Aiken, Jose Miguel Cabezas Navarro, Neil Lund, Egle
Murauskaite, and Diana Partridge. 2022. “Introducing the ICBe Dataset:
Very High Recall and Precision Event Extraction from Narratives about
International Crises.” arXiv:2202.07081 \[cs, stat\].
<http://arxiv.org/abs/2202.07081>.

## Replication Code and Analysis

### Self Contained Package

All of the files used to create the datasets, tables, figures.

## RMarkdown files

### Replication Data

  - 01\_compile\_saves\_and\_align
      - compiles the original coding files into
        `./replication_data/in/icb_coder_crisis_sentence_event.Rds`. The
        original coding files are not on the public repository. Public
        users will load `icb_coder_crisis_sentence_event.Rds` directly.
      - aligns codings from multiple GUI versions on similar source
        sentences
      - creates `./replication_data/temp/ICBe_V1_long_unclean.Rds.Rds`
        (not included in online repo)
  - 02\_format\_and\_clean
      - applies cleaning dictionaries to create
        `./replication_data/temp/ICBe_V1_long_clean.Rds` and
        `./replication_data/temp/ICBe_V1_long_clean.Rds` (not included
        in online repo)
  - 03\_aggregation
      - applies aggregation algorithm to create
        `./replication_data/out/ICBe_V1_long_agreement.Rds`,
        `./replication_data/out/ICBe_V1_long_agreed.Rds`,
        `./replication_data/out/ICBe_V1_wide_agreed.Rds`.

### Replication Paper

  - CaseStudy196
      - creates Cuban Missile Crisis comparison table
        `/tables/CaseStudy196_ft.Rds`.
  - CaseStudy426
      - creates DRC Civil War comparison table
        `/tables/CaseStudy426_ft.Rds`.
  - ICBEdataset\_figure\_metro\_maps
      - creates the metroplot Rds files in `/figures/metro_plots/.`.
  - ICBEdataset\_figure\_semantic\_embeddings
      - creates the figure `/figures/p_semantic_embeddings.png` and the
        `/tables/codings_wide_agreed_embeded_stratified_sample_ft.Rds`
        and
        `/tables/codings_wide_agreed_embeded_stratified_sample_ft_smaller.Rds`
  - ICBEdataset\_paper\_appendixICBCrises
      - creates `/tables/ft_crisis_text_counts.Rds`.
  - ICBEdataset\_paper\_appendixVerbMeanings
      - creates `/tables/verbs_sentence_wordnet_top_ft.Rds`
  - ICBEdataset\_paper\_figure\_prep
      - creates the metroplot pngs in `/figures/.`.
  - ICBEdataset\_paper\_litreviewtable
      - creates the table `/tables/litreview_ft.Rds`.
  - ICBEdataset\_paper\_PlotInterCoderAgreement
      - creates the figure `figures/p_percent_chose_tag_by_concept.png`

## Data inputs:

### ICBe preparation

  - Cleaning dictionaries: used to clean raw codings for actors,
    actions, locations, and dates
    `/replication_paper/data/in/icb_manual_recording_master_sheet.xlsx`
  - Lit review and tree/leaf codebook:
    `replication_data/in/icbe_litreview_trees_sentences.xlsx` and
    `/replication_paper/data/in/icbe_litreview_trees_sentences.xlsx`
  - Case study tables: `/replication_paper/data/in/CaseStudies.xlsx`

### External datasets

  - [The ICB project](https://sites.duke.edu/icbdata/)
      - System-level (./data/icb1v14.Rds) and Actor-level
        (./data/icb2v14.Rds) datasets
      - Dyadic-Level Crisis Data
        ([source](https://sites.duke.edu/icbdata/data-collections/))
  - [Militarized Interstate Disputes
    (MID)](https://correlatesofwar.org/data-sets/MIDs) version 5.01 at
    the incident level (MIDI 5.01) and incident-participant level (MIDIP
    5.01) converted to Rds.
  - [UCDP Georeferenced Event Dataset (GED) Global
    version 21.1](https://ucdp.uu.se/downloads/index.html#ged_global)
  - cameo.eventcode.txt adapted from [CAMEO Conflict and Mediation Event
    Observations
    Codebook](https://parusanalytics.com/eventdata/cameo.dir/CAMEO.09b6.pdf)
  - [Phoenix Event
    data](https://databank.illinois.edu/datasets/IDB-2796521)
  - [Terrier event data](https://osf.io/4m2u7/files/)
      - too large to include in the github repository
      - to replicate, download the folder ‘largegeolocatedata’ to
        ICBEdata/replication\_paper/data/ignore and decompress
  - [ICEWS
    data](https://dataverse.harvard.edu/dataset.xhtml?persistentId=doi:10.7910/DVN/28075&version=30.0)
      - too large to include in the github repository
      - to replicate, download folder ‘dataverse\_files’ to
        ICBEdata/replication\_paper/data/ignore/ and decompress

### License

This work is licensed under a [Creative Commons
Attribution-NonCommercial-ShareAlike 4.0 International
License](http://creativecommons.org/licenses/by-nc-sa/4.0/).

[![CC
BY-NC-SA 4.0](https://licensebuttons.net/l/by-nc-sa/4.0/88x31.png)](http://creativecommons.org/licenses/by-nc-sa/4.0/)
