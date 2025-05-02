---
jupytext:
  cell_metadata_filter: -all
  formats: md:myst
  text_representation:
    extension: .md
    format_name: myst
    format_version: 0.13
    jupytext_version: 1.10.3
kernelspec:
  display_name: Python 3
  language: python
  name: python3
---
(impacts-env-chapitre)=
# Impacts environnementaux

<table>
  <tr>
  </tr>
</table>

Tout au long de ce cours, nous avons discuté de différentes techniques de neuroimagerie pour étudier les variations structurelles et fonctionnelles cérébrales et nous les avons comparées principalement en termes de leurs principes physiques et physiologiques, de la flexibilité expérimentale offerte. Par contre, nous n’avons pas discuté de l’impact environnemental associé à la recherche en neuroimagerie. Ce chapitre vise à offrir une perspective différente pour comparer ces techniques en regardant spécifiquement les coûts énergétiques et environnementaux aux travers des différentes étapes de recherche.

Les objectifs du cours sont les suivants:
- Identifier et discuter de l'impact environnemental des différentes étapes de recherche.
- Fournir une comparaison des différentes techniques en termes de coûts énergétiques et environnementaux.
- Identifier et discuter de différentes solutions pour mitiger ces coûts.

## Impacts environnementaux tout au long du processus de recherche

Les rapports d’évaluation du GIEC (Groupe d’experts intergouvernemental sur l’évolution du climat) compilant les résultats d’études scientifiques actuelles sur le climat résument les impacts des activités humaines, principalement via l’émission de gaz à effet de serre, sur  le réchauffement climatique et les conséquences sanitaires, sociales et économiques ([AR6 Synthesis Report: Climate Change 2023](https://www.ipcc.ch/report/ar6/syr/downloads/report/IPCC_AR6_SYR_FullVolume.pdf)). En 2019, les Fonds de Recherche du Québec (FRQ), un organisme subventionnaire public au niveau provincial, ont publié un [plan d’action](https://frq.gouv.qc.ca/app/uploads/2021/04/plan-action-responsabilite-environnementale_vf.pdf) pour sensibiliser la communauté scientifique aux pratiques écoresponsables et durables en recherche, reconnaissant les impacts tant négatifs que positifs que le recherche peut générer au niveau environnemental.

```{figure} ./reproductibilite/research-cycle.jpg
---
width: 800px
name: research-cycle-fig
---
Cycle de découvertes en recherche. Figure par [scriberia](https://info.scriberia.com/contact-us) dans le cadre du livre [The Turing way](https://the-turing-way.netlify.app) sous licence [CC-BY 4.0](https://creativecommons.org/licenses/by/4.0/), DOI: [10.5281/zenodo.3332807](https://doi.org/10.5281/zenodo.3332807).
```

La {numref}`research-cycle-fig`, que vous avez déjà vu durant le chapitre [Reproductibilité et controverses](reproductibilite), dépeint les différentes étapes de la méthode scientifique intégrant les principes de science ouverte. Dans cette section, nous allons nous concentrer sur les coûts environnementaux associés à la cueillette de données, au prétraitement et à l’analyse de données, ainsi qu’à l’infrastructure numérique nécessaire au partage, à la préservation et à la réutilisation des données de recherche.

### Cueillette de données

```{admonition} Contenu de la section
:class: tip
:name: acquisition-tip
Sensibiliser les étudiantes et étudiants à l’impact environnemental associé à l’acquisition de données de neuroimagerie. Cette section abordera principalement l’IRM, faute d’information sur le coût énergétique des autres modalités… L’article de Chaban et al. (2024) est une bonne référence à utiliser pour décortiquer les différents facteurs affectant la consommation énergétique de l’IRM. Si possible, discuter de ces facteurs pour la TEP (p.ex., consommation énergétique du cyclotron).
```

```{admonition} Encadrés à inclure
:class: tip
:name: encadre-acq-tip
1- Comment mesure-t-on le coût environnemental ?
2- Tableau comparatif du coût énergétique des différentes techniques de neuroimagerie.
```

```{admonition} Références
:class: tip
:name: refs-acq-tip
Chaban et al. (2024). Environmental sustainability and MRI: challenges, opportunities, and a call for action. https://doi.org/10.1002/jmri.28994
Hernandez et al. (2025). Reducing the Energy Consumption of Magnetic Resonance Imaging and Computed Tomography Scanners: Integrating Ecodesign and Sustainable Operations. https://doi.org/10.1097/RCT.0000000000001700
Leswick et al. (2025). Enhancing Environmental Sustainability in Diagnostic Radiology: Focus on CT, MRI, and Nuclear Medicine. https://doi.org/10.1177/08465371251327143
Merkle et al. (2023). The Impact of Modern Imaging Techniques on Carbon Footprints: Relevance and Outlook. https://doi.org/10.1016/j.euf.2023.09.009
Roletto et al. (2024). The environmental impact of energy consumption and carbon emissions in radiology departments: a systematic review. https://doi.org/10.1186/s41747-024-00424-6 
Signorile et al. (2024). Comparative analysis of energy expenditure and costs in neuroimaging. https://doi.org/10.1016/j.jns.2024.123001
Vosshenrich & Heye (2023). Small Steps toward a More Sustainable and Energy-efficient Operation of MRI. https://doi.org/10.1148/radiol.230874
Woolen et al. (2023). Ecodesign and Operational Strategies to Reduce the Carbon Footprint of MRI for Energy Cost Savings. https://doi.org/10.1148/radiol.230441  
```

### Infrastructure numérique en recherche

```{admonition} Contenu de la section
:class: tip
:name: infrastruc-tip
Introduire les étudiantes et étudiants aux différentes composantes de l’infrastructure numérique en recherche, et les sensibiliser aux coûts énergétiques associés, particulièrement sur les composantes matérielles (discuter davantage de la composante logicielle de l’infrastructure numérique dans la section Prétraitement et analyse des données). Discuter de l’espace de stockage requis pour les données de neuroimagerie.
```

```{admonition} Références
:class: tip
:name: refs-infrastruc-tip
Samuel & Lucivero (2020). Responsible open science: Moving towards an ethics of environmental sustainability. https://doi.org/10.3390/publications8040054
The Turing Way Community. (2022). The Turing Way: A handbook for reproducible, ethical and collaborative research (1.0.2). Zenodo. https://book.the-turing-way.org/ethical-research/activism/activism-env-impact
```

### Prétraitement et analyse de données

```{admonition} Contenu de la section
:class: tip
:name: preproc-tip
Discuter des différents facteurs pouvant impacter le coût énergétique associé au prétraitement des données et à l’analyse des données.
```

```{admonition} Références
:class: tip
:name: refs-preproc-tip
Souter et al. (2024). Measuring and reducing the carbon footprint of fMRI preprocessing in fMRIPrep. https://doi.org/10.1002/hbm.70003
Souter et al. (2023). Ten recommendations for reducing the carbon footprint of research computing in human neuroimaging. https://doi.org/10.1162/imag_a_00043
```

## Des solutions

```{admonition} Contenu de la section
:class: tip
:name: solutions-tip
Discuter de certaines solutions pour réduire l’impact environnemental de la recherche en neuroimagerie par rapport aux étapes du processus de recherche précédemment discutées (cueillette des données, stockage des données, analyse de données).
```

```{admonition} Références
:class: tip
:name: refs-solutions-tip
Souter et al. (2024). Measuring and reducing the carbon footprint of fMRI preprocessing in fMRIPrep. https://doi.org/10.1002/hbm.70003
Souter et al. (2023). Ten recommendations for reducing the carbon footprint of research computing in human neuroimaging. https://doi.org/10.1162/imag_a_00043
The Turing Way Community. (2022). The Turing Way: A handbook for reproducible, ethical and collaborative research (1.0.2). Zenodo. https://book.the-turing-way.org/ethical-research/activism/activism-env-impact
```


## Conclusions

## Exercices
