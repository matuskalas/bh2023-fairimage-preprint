---
title: 'Enhancing the image analysis community in Galaxy'
title_short: 'Image analysis with Galaxy'
tags:
  - Imaging
  - Image analysis
  - Image processing
  - Interdisciplinary
  - Life sciences
  - Earth sciences
  - Galaxy
authors:
  - name: Leonid Kostrykin
    affiliation: 1,2
    orcid: 0000-0003-1323-3762
  - name: Tatiana Woller
    affiliation: 3
    orcid: 0000-0002-6958-6498
  - name: Matúš Kalaš
    affiliation: 4
    orcid: 0000-0002-1509-4981
  - name: Bugra Özdemir
    affiliation: 5
    orcid: 0000-0001-9823-0581
  - name: Rafael Andrade Buono
    affiliation: 3
    orcid: 0000-0002-6675-3836
  - name: Yi Sun
    affiliation: 6
    orcid: 0000-0002-7636-0200
  - name: Anup Kumar
    affiliation: 7
    orcid: 0000-0002-2068-4695
  - name: Nadia Goué
    affiliation: 8
    orcid: 0000-0003-2750-1473
  - name: Bjoern Gruening
    affiliation: 7
    orcid: 0000-0002-3079-6586
  - name: Beatriz Serrano-Solano
    affiliation: 5
    orcid: 0000-0002-5862-6132
  - name: Anne Fouilloux
    affiliation: 9
    orcid: 0000-0002-1784-2920
affiliations:
  - name: Biomedical Computer Vision Group, Heidelberg University, BioQuant, IPMB, 69120 Heidelberg, Germany
    index: 1
  - name: ELIXIR Germany, Institute of Bio- and Geosciences (IBG-5) – Computational Metagenomics, Forschungszentrum Jülich GmbH, 52425 Jülich, Germany
    index: 2
  - name: Vlaams Instituut voor Biotechnologie, Datacore, Technologiepark-Zwijnaarde 75, 9052 Gent; ELIXIR Belgium
    index: 3
  - name: ELIXIR Norway, and Department of Informatics, University of Bergen, Norway
    index: 4
  - name: Euro-BioImaging ERIC Bio-Hub, European Molecular Biology Laboratory (EMBL) Heidelberg, Meyerhofstraße 1, 69117 Heidelberg, Germany
    index: 5
  - name: European Molecular Biology Laboratory (EMBL) Heidelberg, Meyerhofstraße 1, 69117 Heidelberg, Germany
    index: 6
  - name: Department of Computer Science, University of Freiburg, Georges-Köhler-Allee 106, 79110 Freiburg, Germany
    index: 7
  - name: Université Clermont Auvergne, AuBi platform, F-63000 Clermont-Ferrand, France 
    index: 8
  - name: Simula Research Laboratory, Oslo, Norway
    index: 9
date: 7 April 2024
cito-bibliography: paper.bib
event: BH23EU
biohackathon_name: "BioHackathon Europe 2023"
biohackathon_url:   "https://biohackathon-europe.org/"
biohackathon_location: "Barcelona, Spain, 2023"
group: Project 16 - Enhancing the image analysis community in Galaxy 
# URL to project git repo --- should contain the actual paper.md:
git_url: https://github.com/beatrizserrano/bh2023-preprint
# This is the short authors description that is used at the
# bottom of the generated paper (typically the first two authors):
authors_short: Leonid Kostrykin, Tatiana Woller, \emph{et al.}
---


<!--

The paper.md, bibtex and figure file can be found in this repo:

  https://github.com/journal-of-research-objects/Example-BioHackrXiv-Paper

To modify, please clone the repo. You can generate PDF of the paper by
pasting above link (or yours) in

  http://biohackrxiv.genenetwork.org/

-->

# Introduction

The 2023 edition of [BioHackathon Europe](https://biohackathon-europe.org/) took place in Barcelona in November last year, where a group of people interested in image data analysis gathered around the project nr. 16, **_"Enhancing the image analysis community in Galaxy"_**.

Although the [Galaxy platform](http://galaxyproject.org) [@citesAsAuthority:extends:Galaxy] has a strong presence in omics fields like genomics and proteomics, it has yet to establish itself in the imaging community fully. This would be of great value to the scientific communities working with image data, as Galaxy provides free and open, democratised access to extensive computational resources, via common user-friendly interfaces (GUI and API), and with built-in provenance for transparency and reproducibility, fostering FAIR scientific workflows [@citesAsSourceDocument:galaxyFAIR]. However, at the moment, **efforts** to integrate tools and create workflows for image analysis in Galaxy **are scattered** across research fields and locations.

This project's vision is to join those efforts and go beyond, by creating **interdisciplinary image analysis resources**. By fostering collaboration among scientists and enthusiasts from different fields, we aim to create a dynamic community that focuses on image data management and analysis, both within and outside of life sciences. Our goal is to provide both professional and citizen scientists, from all domains of science (_e.g._ life and Earth sciences, materials science, astronomy, archaeology, or arts), with free access to state-of-the-art, high-performance image analysis.

The initiative started in the summer of 2023 when the group gathered around a newly-created **Expert Group on _FAIR Image Data Workflows_** within [Euro-BioImaging](https://www.eurobioimaging.eu/), the European Research Infrastructure offering open access to (bio-)imaging technologies, training, and data services. Additionally, it aims to tap into the capabilities of [Simula Research Laboratory](https://www.simula.no/). This Norwegian non-profit research organisation addresses crucial scientific and engineering problems with a societal impact, focusing on five primary ICT (Information and Communication Technologies) research areas: communication systems, cryptography, scientific computing, software engineering, and machine learning. Together, these entities will foster the development of a community dedicated to crafting FAIR computational workflows specifically tailored for image analysis.

### Project goals

For the BioHackathon 2023, we set a number of multifaceted goals:

- Gather all the existing resources for image data management and analysis in Galaxy (_e.g._, tools available in the [Galaxy ToolShed](https://toolshed.g2.bx.psu.edu/) [@usesDataFrom:citesAsAuthority:toolshed], training materials published in the [Galaxy Training Network](https://training.galaxyproject.org/) [@usesDataFrom:citesAsAuthority:gtn], and workflows collected in the [WorkflowHub](https://workflowhub.eu/) [@usesDataFrom:citesAsAuthority:workflowhub]).
- Create a list of tools widely used in the image analysis field that are not yet integrated into Galaxy.
- Annotate the existing image analysis tools that are lacking annotations with [EDAM](https://bioportal.bioontology.org/ontologies/EDAM) [@citesAsAuthority:extends:edam] and especially the [EDAM Bioimaging](https://bioportal.bioontology.org/ontologies/EDAM-BIOIMAGING) ontology [@citesAsAuthority:usesDataFrom:extends:edamBioimaging; @usesDataFrom:edamBioimagingAlpha06].
- Create a community-of-practice page in the [Galaxy Community Hub](https://galaxyproject.org/).
- Establish community practices and decide on regular interactions.


# Results

In this section, we discuss the achievements within the BioHackathon, aligning them with the project goals. We explore the progress made addressing conventions, tool renaming, tool annotation, and the identification of tools not available in Galaxy, together with image data management and image analysis tools.

## Landscape analysis of image analysis and image processing tools in Galaxy

The current state of image analysis and image processing tools within Galaxy, as of October 13, 2023, reveals an extensive and diverse landscape. A comprehensive overview provides valuable insights into the existing ecosystem and areas that need to be enhanced.

### Tool Statistics

![Distribution of tools across repositories](https://hackmd.io/_uploads/B1RQLDUHT.png)

- **Tool count**: The _"Imaging"_ category on Galaxy Europe lists 101 tools.
- **Contributors**: Approximately 23 contributors have added and maintained these tools.
- **Repositories**: The tools are distributed across 5 different GitHub repositories, presenting a need for structuration and organization.
- **Categorization challenges**: Some tools with relevance to image analysis are found in the "Interactive" category, indicating a potential need for reclassification and structure clarification.

### Big pile of tools — needing structure

Following the gathering and identification of this extensive number of tools, we identified potential obstacles that could be hindering their FAIRness.

#### Example 1: Inconsistent tool naming schemes

Within the tool repository, there was a noticeable diversity in naming styles, with tools adopting various conventions such as the title case, sometimes capitalized, abbreviated, using camel case, _etc._ Some examples of this diversity are listed below: 

- Title Case: _Anisotropic Diffusion_, _Count Objects_, …
- Capitalized: _Binary To Points_, …
- Abbreviated: _Binary 2 Label_, …
- Camel Case: _ColorToGray_, _ConvertObjectsToImage_, …
- Regular: _Convert image_, _Find edges_, _Filter segmentation_, …
- Verb-forms vs. Nouns: _Split objects_, _Mahotas-features_, …

During the BioHackathon, we reached an agreement on a recommended naming scheme for tools, to facilitate finding these tools (see section [Conventions](#Conventions)).

#### Example 2: Low-level vs. high-level tools

The distinction between low-level and high-level tools highlights the diverse needs of the Galaxy user community. Advanced users, with a good understanding of image analysis, benefit from the flexibility and control offered by low-level tools. On the other hand, users with varying levels of expertise, including those less familiar with image analysis, find high-level tools to be more accessible and efficient. This duality in tool design acknowledges the heterogeneous user base within the Galaxy community. 


#### Example 3: Tools with unclear goals

The purpose of some tools can be unclear (_e.g._ _Gate Finder_, _Concatenate images_, _Compose two raw transformations_, _Add shadow effect_, ...), have typos in their documentation (_labeled_ vs. _labled_) or are unrelated to imaging (_GeneSeqToFamily preparation_), emphasizing the importance of defining the purpose of each tool clearly in its metadata.

Enhancing consistency in tool names and descriptions will contribute to a more user-friendly experience.


#### Example 4: Duplicated or similar tools

Some tools within the Galaxy ecosystem have similar purposes but often originate from different tool suites (_e.g._ _CellProfiler_ or _ImageJ_). Using prefixes or other consistent schemes for indication of the tool suites should facilitate identification and enhance user navigation.

#### Example 5: Lack of tool interoperability

Incompatibilities between tools were identified, particularly concerning input formats and inconsistent tool IDs. For example, tools like _Count Objects_ historically accepted only TIFF inputs, while others, like _Concatenate images_ exclusively accepted binary images without apparent justification. To enhance user experience and interoperability, a suggestion was made for tools to support formats such as TIFF and PNG universally. 

#### Example 6: Different versions of the same tool

Occasionally, the Galaxy tool panel may feature duplicated versions of the same tool, even if their functionalities have undergone alterations. There are different reasons for this, from typos to the way tool names are displayed in the tool panel. 

## Conventions
We acknowledge the existence of the [IUC recommendations](https://galaxy-iuc-standards.readthedocs.io/en/latest/) for tool names but decided on a somewhat different pattern,
1. to avoid too long tool names due to the inclusion of tool suits, 
2. to comply with the fact that many Galaxy tools in our community are thin tool wrappers around established tools (_e.g._, tool suites or other Conda packages), while 
3. many others implement their main functionality directly within the wrapper.

The conventions described below have a few limitations (see section [Discussion](#Discussion)).

### Naming
Generally, the name of Galaxy tools in our community should be expressive and concise, while stating the purpose of the tool as precisely as possible. Consistency of the namings of Galaxy tools is important to ensure they can be found easily. To maintain consistency, we consider phrasing names as imperatives a good practice, such as “Analyze particles” or “Perform segmentation using watershed transformation”. An acknowledged exception from this rule is the names of tool wrappers of major tool suites, where the name of a tool wrapper should be chosen identically to the module or function of the tool which is wrapped (_e.g._, “MaskImage” in CellProfiler).

### Tool description 
If a Galaxy tool is a thin tool wrapper (_e.g_, part of a major tool suite), then the name of the wrapped tool (and only the name of the wrapped tool, subsequent to the term “with” as in “with Bioformats”) should be used as the description of the tool (further examples include “with CellProfiler”, “with ImageJ2”, “with ImageMagick”, “with SpyBOAT”, “with SuperDSM”). This ensures that the tool is found by typing the name of the wrapped tool into the “Search” field on the Galaxy interface. The tool description should be empty if a tool is either not part of a major tool suite, or the main functionality of the tool is implemented in the wrapper.

### Annotations 
We point out that there is a global list of precedential annotations with [Bio.tools](https://bio.tools/) identifiers [@citesAsAuthority:usesDataFrom:biotools] in Galaxy, which may outweigh the annotations made in the XML specification of a Galaxy tool (and thus the annotations of a tool reported within the web interface of Galaxy might be divergent). However, since the precedential annotations are subject to possible changes and to avoid redundant work, we do not aim to reflect those in our specifications (those which we make in the XML specifications of Galaxy tools).


## Tool annotation

The annotations of tools within the Galaxy Image Community involve the use of the EDAM ontology and Bio.tools. To recognize the role of [BioImage Informatics Index (BIII)](https://biii.eu/) as the registry of tools, workflows, training, and example data for bioimage analysis [@citesAsAuthority:usesDataFrom:bioimageWorkflows], we agreed to use also BIII identifiers in Galaxy, taking into account the BIII's use of annotations with EDAM Bioimaging.

To fully reflect this decision, we included a new metadata field in the Galaxy tool wrappers that enables the annotation of tools with BIII IDs (see [PR](https://github.com/galaxyproject/galaxy/pull/16952)).

We annotated all the tools with Bio.tools IDs, EDAM concepts, and BIII IDs, and adhered to the agreed conventions in the following pull requests:

- https://github.com/BMCV/galaxy-image-analysis/pull/71
- https://github.com/bgruening/galaxytools/pull/1346 
- https://github.com/goeckslab/tools-mti/pull/53
- https://github.com/galaxyproject/tools-iuc/pull/5572
- https://github.com/usegalaxy-eu/usegalaxy-eu-tools/pull/641

Thanks to these annotations and in collaboration with Project 25 _" Increasing the findability, visibility, and impact of Galaxy tools for specialised scientific Communities"_ [@usesMethodIn:obtainsSupportFrom:project25], we gathered a list of tools that are of interest for the imaging community.

We also started the discussion to facilitate the Bio.tools annotations when wrapping a tool for Galaxy using the [Galaxy Language Server](https://github.com/galaxyproject/galaxy-language-server) (see [issue](https://github.com/galaxyproject/galaxy-language-server/issues/250)).

## Data management tools

Improving data management is crucial when it comes to improving the image analysis experience in Galaxy. During the BioHackathon, we worked on adding support for the [Zarr format](https://zarr.readthedocs.io/en/stable/spec.html#specifications) ([PR](https://github.com/usegalaxy-eu/galaxy/pull/203)), and a beta version of OME-Zarr ([PR](https://github.com/galaxyproject/galaxy/issues/16862)) [@citesAsAuthority:usesMethodIn:OMEzarr], with plans for adding metadata information and checks in the future. This will also facilitate adding support for other community-driven standards, such as [NCZarr](https://www.unidata.ucar.edu/blogs/developer/en/entry/netcdf-zarr-data-model-specification) and [GeoZarr](https://github.com/zarr-developers/geozarr-spec).

Tools were added to convert NetCDF to NCZarr, and various proprietary image file formats to OME-Zarr ([PR](https://github.com/NordicESMhub/galaxy-tools/pull/64)), addressing specific image analysis data formats for better data handling in Galaxy.

In addition, a tool to fetch image data directly from the [BioImage Archive (BIA)](https://www.ebi.ac.uk/bioimage-archive/) has been implemented ([PR](https://github.com/bgruening/galaxytools/pull/1345)), and tools for data conversion have been included ([PR](https://github.com/BMCV/galaxy-image-analysis/pull/72)).

## AI-powered image analysis

The integration of AI-powered image analysis in Galaxy involved leveraging models from the [BioImage Model Zoo (BMZ)](https://bioimage.io/#/) [@citesAsAuthority:usesDataFrom:BMZ] and conducting an analysis of [ZeroCostDL4Mic](https://github.com/HenriquesLab/ZeroCostDL4Mic) dependencies. 

We explored the possibility of consuming models from the [BMZ](https://bioimage.io/#/) in Galaxy, with specific examples for live cell segmentation and cellular nucleus segmentation boundary models. 

## Community

We updated the Galaxy subdomain [imaging.usegalaxy.eu](https://imaging.usegalaxy.eu) to contain the list of training materials related to imaging ([PR](https://github.com/usegalaxy-eu/website/pull/1165)). We also agreed on renaming our community to “image community”, thus also renaming the subdomain to [image.usegalaxy.eu](https://image.usegalaxy.eu).


# Discussion

The project has made good progress in gathering existing image analysis tools, creating a list of tools to integrate, and adding annotations to tools that needed them.

## Future work

Looking ahead, we plan to continue this work by collaborating closely with the Galaxy, EDAM (Bio-)imaging, and BioImage Model Zoo communities. The long-term goal is to create a solid community that supports the creation and reuse of reproducible and FAIR image analysis workflows, amongst diverse scientific disciplines.

### Community development

We welcome anyone interested, from experienced Galaxy tool developers and image analysts to those who are new to the field, to join our community (info@eurobioimaging.eu) and monthly meetings on the third Wednesday of the month at 4 pm CE(S)T. 

### Improving conventions 
We are aware of the following limitations of our conventions for tool naming, tool descriptions, and annotation (see section [Conventions](#Conventions)), which we seek to address in the future:

1. If a Galaxy tool has a Bio.tools identifier included in its XML specification, then its EDAM operation annotation can be inherited from the Bio.tools record. The EDAM operations in Bio.tools might be precedential over the EDAM operations given in the XML specification of a Galaxy tool. However, depending on the evolving community guidelines, the precedence could also be the opposite.
2. Our primary motivation for prominently exposing the name of the wrapped tool in the tool description has been to account for the fact that tools with similar functionality (and hence similar names) exist across different tool suites. However, they can also exist across different plugins within the same tool suite (such as ImageJ2). To account for that, we might want to take the suggested scheme one step further and include the name of the corresponding plugin in the tool description (as in “with ImageJ2, bUnwrapJ”).

# Acknowledgements

This work was developed as part of BioHackathon Europe 2023.
We thank the contributions from Project 25 [@usesMethodIn:obtainsSupportFrom:project25].
This work was supported by [ELIXIR](https://elixir-europe.org), the research infrastructure for life science data.
The authors utilised the language model ChatGPT developed by OpenAI to assist in structuring and drafting this text.


# References
