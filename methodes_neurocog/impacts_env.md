---
jupytext:
  formats: md:myst
  text_representation:
    extension: .md
    format_name: myst
kernelspec:
  display_name: Python 3
  language: python
  name: python3
---
(impacts-env-chapitre)=
# Impacts environnementaux

## Objectifs

Tout au long de ce cours, nous avons discuté des avantages et des limitations de différentes techniques de neuroimagerie pour étudier les variations structurelles et fonctionnelles cérébrales. Ce chapitre offre une perspective différente: discuter des coûts énergétiques et environnementaux liés aux différentes étapes de recherche. Certains de ces coûts sont spécifiques de la technique utilisée, alors que d'autres s'appliquent à l'ensemble d'entre elles.

Les objectifs du cours sont les suivants:
- Identifier et discuter de l'impact environnemental des différentes étapes de recherche.
- Identifier et discuter de différentes solutions pour réduire cet impact.

## Impacts environnementaux tout au long du processus de recherche

Les rapports d’évaluation du GIEC (Groupe d’experts intergouvernemental sur l’évolution du climat) compilant les résultats d’études scientifiques actuelles sur le climat résument les impacts des activités humaines, principalement via l’émission de gaz à effet de serre ([AR6 Synthesis Report: Climate Change 2023](https://www.ipcc.ch/report/ar6/syr/downloads/report/IPCC_AR6_SYR_FullVolume.pdf)) {cite:p}`ipcc2023`. Le rapport de 2023 souligne qu’il faut atteindre des émissions nettes de CO2 nulles pour limiter le réchauffement climatique global d’origine humaine à 1.5°C comparativement au niveau pré-industriel. Autrement, les conséquences irréversibles risquent de s’accroître au niveau environnemental (p. ex. perte d’habitats et de biodiversité), sanitaire (p. ex. augmentation de la propagation de maladies vectorielles), social (p. ex. certaines populations sont plus vulnérables aux conséquences climatiques) et économique (p. ex. l’augmentation des évènements météorologiques extrêmes peut mener à la destruction des terres et des infrastructures).

En tant que chercheur·euse·s, il est important de reconnaître l’impact que nous avons sur la crise climatique. En 2019, les Fonds de Recherche du Québec (FRQ), un organisme subventionnaire public au niveau provincial, ont publié un [plan d’action](https://frq.gouv.qc.ca/app/uploads/2021/04/plan-action-responsabilite-environnementale_vf.pdf) pour sensibiliser la communauté scientifique aux pratiques écoresponsables et durables en recherche, reconnaissant les impacts tant négatifs que positifs que la recherche peut générer au niveau environnemental. Malgré ces efforts, les impacts environnementaux dans le processus de recherche en neuroimagerie demeurent peu discutés au sein de la communauté scientifique et dans le curriculum universitaire.

```{figure} ./reproductibilite/research-cycle.jpg
---
width: 800px
name: research-cycle-fig-impact-env
---
Cycle de découvertes en recherche. Figure par [scriberia](https://info.scriberia.com/contact-us) dans le cadre du livre [The Turing way](https://the-turing-way.netlify.app) sous licence [CC-BY 4.0](https://creativecommons.org/licenses/by/4.0/), DOI: [10.5281/zenodo.3332807](https://doi.org/10.5281/zenodo.3332807).
```

La {numref}`research-cycle-fig-impact-env` dépeint les différentes étapes de la méthode scientifique intégrant les principes de science ouverte. Avant de discuter des coûts environnementaux associés à chaque étape, de la cueillette de données à la réutilisation des données de recherche, nous allons brièvement voir comment il est possible d’estimer l’empreinte environnementale des activités de recherche. À la fin du chapitre, nous allons proposer quelques pistes de solutions et de réflexions pour réduire cette empreinte.

### Calculer l'impact environnemental

Il existe plusieurs indicateurs qui nous permettent d’évaluer de manière plus complète l’impact environnemental des différentes activités humaines, tels que l’impact sur le réchauffement global, l’acidification des sols et de l’eau, la pollution de l’eau et l’utilisation d’eau douce {cite:p}`schollhammer2024`. Ces facteurs nous rappellent la complexité de l’impact que nous pouvons avoir sur notre environnement. Au cours de ce chapitre, nous allons principalement nous concentrer sur les émissions de gaz à effet de serre, et plus spécifiquement sur la quantité d’équivalent CO2 émis. Cet indicateur est couramment utilisé pour estimer l’empreinte carbone des différentes activités de recherche.

```{admonition} Équivalent CO2
:class: tip
:name: eqCO2-tip
La quantité de gaz à effet de serre émis par les différentes étapes du processus de recherche peut être exprimée en équivalent dioxyde de carbone (éqCO2). Cette métrique permet de prendre en compte le potentiel de réchauffement planétaire (PRP) qui diffère selon le type de gaz à effet de serre. Par exemple, le méthane a un PRP 25 fois plus grand que le dioxyde de carbone. Donc, pour calculer la quantité de gaz à effet de serre, on peut appliquer cette formule:
éqCO2 = (masse_Gaz1 x PRP_Gaz1) + ... + (masse_Gazn x PRP_Gazn)
```

```{admonition} L'empreinte carbone
:class: tip
:name: empreintecarbone-tip
L’empreinte carbone correspond à la quantité totale de gaz à effet de serre générée directement ou indirectement par un individu, une organisation, un événement ou un produit. Cela représente indirectement la contribution de ces instances au réchauffement climatique.
```

Pour les équipements de recherche spécifiquement, il est possible de se baser sur une méthode appelée analyse du cycle de vie (ACV ou Life Cycle Assessment) pour évaluer leur impact environnemental sur l’ensemble ou sur une partie de leur cycle de vie. Il existe deux types d’analyse du cycle de vie: l’ACV attributionnelle (Attributional Life Cycle Assessment) et l’ACV conséquente (Consequential Life Cycle Assessment) {cite:p}`schaubroeck_relevance_2023`.

L’ACV attributionnelle est associée à l’impact d’un produit ou d’un service tel qu’il existe, en considérant les différentes étapes de son cycle de vie. Cela pourrait comprendre l’extraction et la fabrication des matériaux nécessaires pour développer un appareil jusqu’à sa fin de vie (p. ex. recyclage ou élimination). Cette méthode pourrait par exemple être utilisée si nous voudrions comparer l’impact environnemental associé à deux différents modèles d’IRM (p. ex. Siemens Trio 3T vs Philips Ingenia Elition 3T).

L’ACV conséquente fournit une information quant à l’impact environnemental direct ou indirect conséquent à une décision potentielle. Ce type d’analyse se concentre donc sur les impacts additionnels ou évités de l’utilisation ou non d’un produit. L’ACV conséquente serait pertinente si nous voudrions estimer par exemple l’impact environnemental d’inclure une session supplémentaire d’acquisition IRM dans notre étude plutôt qu’une seule {cite:p}`mcalister2024`. Dans ce cas, nous ne prendrions pas en compte l’impact associé à la fabrication de l’appareil, simplement l’usage potentiel à venir.

L’ACV est parfois rendue disponible par les fabricants. Il existe également une base de données regroupant l’ACV pour différents produits et procédés utilisés dans le système de santé ([HealthcareLCA](https://healthcarelca.com/) {cite:p}`drew_healthcarelca_2022`). Donc, au-delà du coût environnemental associé à l’utilisation directe d’un appareil, nous pouvons également tenir compte des étapes intermédiaires de fabrication et de maintenance des équipements de recherche.

### Cueillette de données

Dans cette section consacrée à la collecte de données, nous allons utiliser les données recueillies via l’IRM comme étude de cas pour illustrer à quoi pourrait ressembler une analyse du cycle de vie et mieux comprendre quels sont les facteurs influençant l’impact environnemental d’un projet collectant des données IRM (IRM T1, IRM de diffusion ou IRM fonctionnelle).

Nous pouvons décomposer le coût environnemental de l’IRM à travers trois composantes qui peuvent être analysées avec l’ACV:
- Matériaux utilisés pour la fabrication de l'appareil
- Consommation d'hélium liquide
- Consommation énergétique

#### Matériaux

Pour réaliser une ACV attributionnelle, il faudrait prendre en compte l’impact environnemental associé aux matériaux nécessaires pour fabriquer un IRM. Un appareil IRM est composé principalement de métaux (environ 75%) et de plastique (environ 14%)([Global Electronics Council - Tableau 2](https://globalelectronicscouncil.org/wp-content/uploads/medical-imaging-equipment-state-of-sustainability-research.pdf)) {cite:p}`fessler_state_2022`. En effet, l’aimant de l’IRM est fabriqué à partir d’un alliage de niobium et de titanium et de cuivre, alors que les composantes électroniques de l’appareil utilisent d’autres métaux comme le palladium, le tantalum, la gallium, le germanium et l’indium. Ces composantes proviennent de l’exploitation minière et du traitement physique ou chimique de ces métaux. Ces activités requièrent généralement beaucoup d’eau et d’énergie et produisent des émissions de GES et des résidus miniers qui doivent être entreposés dans des installations spécialisées en raison des risques de contamination du sol et de l’eau.

#### Hélium liquide

La majorité de l’empreinte environnementale associée à la collecte de données d’IRM est liée à l’utilisation d’hélium liquide. En effet, dans le chapitre [Imagerie par résonance magnétique](https://methodes-cogneuro.github.io/irm.html), nous avons brièvement mentionné la nécessité d’utiliser de l’hélium liquide pour refroidir l’aimant supraconducteur de l’appareil IRM. Mais l’approvisionnement en hélium liquide ne vient pas sans coût environnemental et financier ! En effet, l’hélium est une ressource non-renouvelable provenant de l’extraction de gaz naturel. La {numref}`approvisionnement-helium-fig` résume les étapes du processus d’approvisionnement en hélium liquide.

```{figure} ./impacts_env/helium.png
---
width: 800px
name: approvisionnement-helium-fig
---
Approvisionnement en hélium: des profondeurs de la terre jusqu’aux centres de neuroimagerie. Le gaz naturel est d’abord extrait de formations géologiques qui se trouve dans les profondeurs de la Terre et dans les fonds marins par processus de forage. Le gaz naturel est ensuite acheminé dans un centre de traitement de traitement pour séparer dans un premier temps l’hélium gazeux des autres composants du gaz naturel, puis pour liquéfier l’hélium et le transporter à des distributeurs dans contenants cryogéniques (volume de plus de 40000 L). Les distributeurs s’occupent de ré-empaqueter l’hélium liquide dans des Dewar (volume de 50 - 500 L), des sortes de gros thermos, et de les transporter aux centres de neuroimagerie {cite:p}`chrz_helium_2010` {cite:p}`hu_review_2025`. Cette figure a été créée à partir de ressources provenant de [Flaticon.com](https://www.flaticon.com/).
```

Les émissions de CO2 provenant du processus d’extraction, de purification et de liquéfaction de l’hélium sont estimées à 5.97 tonnes métriques pour 3000 L d’hélium {cite:p}`stein_sp0242_2018`. En ajoutant le transport, les émissions de CO2 s’élèvent à 6.74 tonnes métriques par année. Or, l’aimant de l’IRM doit être plongé en tout temps dans un volume variant entre 1200 L  et 2000 L d’hélium liquide, selon la force de l’aimant et les modèles d’IRM. De plus, une certaine quantité d’hélium s’évapore régulièrement, ce qui nécessite des remplissages périodiques pour les appareils n’incluant pas de système sans évaporation. En effet, les nouveaux aimants sont munis de systèmes sans évaporation («zero boil-off» ou «low boil-off») qui permettent de capturer l’hélium gazeux et le recondenser en hélium liquide réduisant de manière importante les besoins en remplissage {cite:p}`mahesh_mri_2016`.

```{admonition} Étude de cas: l’appareil IRM à l’Unité de Neuroimagerie Fonctionnelle
:class: tip
:name: helium-UNF-tip
L’aimant IRM de l’Unité de Neuroimagerie Fonctionnelle (UNF) a fêté ses 20 ans en 2024 ! Voyons quelle est l'empreinte environnementale de l’IRM liée à son utilisation d’hélium liquide depuis tout ce temps. L’appareil IRM à l’UNF est muni d’un réservoir d’hélium liquide de 1200L. Ce réservoir doit être rempli de trois à quatre fois par année en raison de l’évaporation de l’hélium. Chaque remplissage compte pour 500L d’hélium. Avec les chiffres mentionnés précédemment, il est possible de calculer les émissions carbone selon la formule suivante:
Émissions carbone = volume initial (L) * 0.0022 (tonne de CO2/L) + volume de remplissage par année (L / an) * nombre d’année d’opération (an) * 0.0022 (tonne de CO2/L)
Donc en date de 2025, les émissions de CO2 associées à l'approvisionnement et l’utilisation de l’hélium liquide à l’UNF tourneraient autour de 71.94 et 95.04 tonnes métriques, soit l’équivalent de 36 à 47 vols aller-retour Montréal-Paris (équivalences estimées selon [le calculateur d’émissions de CO2 myclimate](https://co2.myclimate.org/en/flight_calculators)). À noter que les chiffres utilisés pour le calcul ci-haut supposent une relation linéaire entre le volume d’hélium liquide et les émissions de CO2.
```

Il est important de noter que cet enjeu est également applicable à la magnétoencéphalographie (MEG) qui consomme environ 2500 L d’hélium liquide par année {cite:p}`baillet2024`. Heureusement, il est possible d’utiliser des systèmes de récupération de l’hélium, réduisant les émissions de gaz à effet de serre associées à la production d’hélium liquide ainsi qu’à son transport. Le plateforme de MEG à l'UdeM dispose d'ailleurs d'un tel système. 

#### Consommation énergétique

Une autre source d’émissions de CO2 associée à l’acquisition de données IRM provient de la consommation énergétique des scanners. En effet, 60% à 70% de la consommation énergétique des appareils IRM est allouée au refroidissement continu de l’aimant. La quantité exacte de kilowattheures (kWh) nécessaire dépend du type d’aimant et de la force de l’aimant {cite:p}`gratzel_von_gratz_mri_2023`. D’autres facteurs influencent la consommation énergétique globale, notamment le mode de fonctionnement du scanner (i.e., éteint, inactif, prêt à scanner, actif). Par exemple, lorsque l’IRM est en mode actif, sa consommation énergétique est environ 2.5 fois plus élevée que lorsque l’appareil est en mode prêt à scanner et 3 fois plus élevé que lorsqu’il est en mode inactif {cite:p}`chaban_environmental_2024`. Comme mentionné dans le chapitre IRM, les bobines de gradient sont parmi les composantes les plus énergivores lors de l’acquisition d’images. De plus, certaines séquences, comme la DWI utilisée en IRM de diffusion, exigent davantage d’énergie que d’autres séquences. En général, la consommation énergétique est directement proportionnelle à la durée totale d’acquisition. Finalement, le modèle d’appareil IRM peut également influencer cette consommation.

Pour estimer l’impact environnemental associé à un scan IRM via l’ACV conséquente, il est possible de considérer uniquement l’énergie consommée pour ce scan spécifiquement, en soustrayant la consommation de l’appareil s’il n’avait pas été utilisé {cite:p}`mcalister_carbon_2022`. Cependant, dans le cas de l’ACV attributionnelle, il faudrait déterminer quelle part de l’impact total lié à l’utilisation de l’IRM peut être attribuée à un seul scan. Il faudrait alors non seulement prendre en compte le temps d’opération actif, mais aussi les phases inactives de l’appareil.

```{admonition} Consommation énergétique et source d’électricité
:class: tip
:name: consommation-source-tip
Pour évaluer adéquatement la consommation énergétique associée à l’utilisation d’un appareil IRM, il est important de considérer les sources d’électricité utilisées. En effet, l’intensité carbone de la production d’électricité, c’est-à-dire la quantité de CO2 émis par unité d’énergie générée, dépend des sources d’électricité qu’une région utilise {cite:p}`schollhammer2024`.  Par exemple, en 2021, la majorité de l’électricité produite au Québec provenait de sources renouvelables (99.6%), alors que 0.4% provenait du pétrole et du gaz naturel. Avec ces sources d’énergie, les émissions de GES associés à ce secteur étaient estimées à 0.3 Mt d’éq CO2. Par contre, 85% de l’énergie produite en Alberta provenait de sources d’énergie non-renouvelable en 2021. En 2022, les GES émis par le secteur de l’énergie albertain s’élevaient à 19.4 Mt d’éq CO2 {cite:p}`gouvernement_du_canada_e_2024`.
```

### Prétraitement, analyse et préservation des données

Étant donné la complexité des analyses et la taille des données, les projets de recherche en neuroimagerie reposent souvent sur une infrastructure numérique pour répondre aux besoins computationnels. Cette demande doit être supportée par des centres de données, qui fournissent les infrastructures nécessaires pour entreposer et effectuer le prétraitement et l’analyse de ces données. Ces infrastructures, bien qu’essentielles, consomment beaucoup d’énergie. À l’échelle mondiale, le secteur des technologies de l’information et de la communication génère entre 1.4% et 3.9% des émissions globales de CO2, notamment en raison de la demande électrique nécessaire pour faire fonctionner, maintenir et refroidir les serveurs de données {cite:p}`freitag_real_2021` {cite:p}`habibi_khalaj_energy_2016` {cite:p}`malmodin_ict_2024`.

```{admonition} Infrastructure numérique en recherche
:class: tip
:name: infrastructure-tip
L’infrastructure numérique réfère aux composantes matérielles (p.ex., centres de données, ordinateurs, composants non-durables comme les minerais/métaux, etc.) et informatiques (p.ex., logiciels) nécessaires à la gestion des données et des ressources computationnelles pour prétraiter et analyser les données.
```

Nous avons parlé dans les cours précédents des différentes étapes de prétraitement à appliquer aux données de neuroimagerie avant de pouvoir effectuer nos analyses (p. ex. recalage dans un espace de référence, correction du mouvement, etc). Plusieurs paramètres de prétraitement doivent être choisis par les chercheuses et chercheurs et ces choix influencent la consommation énergétique requise pour compléter cette étape. Souter et collègues (2024) ont analysé l’impact carbone de différentes options de prétraitement avec le logiciel fMRIPrep et ont proposé une liste de recommandations pour diminuer cet impact, sans pour autant diminuer la qualité des images obtenues {cite:p}`souter_measuring_2024`.

```{admonition} Impact du moment de la journée sur l’intensité carbone
:class: tip
:name: jour-nuit-tip
Le moment de la journée durant lequel nous effectuons le prétraitement ou l’analyse de nos données peut impacter l’intensité carbone de la tâche selon où nous nous trouvons dans le monde. Par exemple, les sources d’énergie au Royaume sont un mélange d’énergie renouvelable et non-renouvelable. La proportion d’énergie renouvelable n’est pas assez élevée pour répondre à la demande lors des périodes d’utilisation élevée d’énergie, et donc les sources d’énergie à forte intensité carbone doivent être utilisées ([https://carbonintensity.org.uk](https://carbonintensity.org.uk)). Si vous vous trouvez dans une région qui fonctionne de manière similaire, il est recommandé de lancer ses analyses lors des périodes de faible achalandage énergétique pour réduire l’impact carbone de son étude (pour avoir accès à ces informations, voir [https://app.electricitymaps.com/](https://app.electricitymaps.com/)).
```

Outre les choix de paramètres, le choix du logiciel utilisé pour réaliser le prétraitement et les analyses des données contribue aussi à l’impact carbone. Souter et collègues (2025) ont montré qu’il pouvait y avoir jusqu’à un facteur de 30 entre les émissions de CO2 associées à différents logiciels {cite:p}`souter_comparing_2025`. Dans tous les cas, les émissions de CO2 étaient plus élevées pour le prétraitement comparativement à l’analyse des données (analyse statistique au niveau du groupe).

La taille totale des fichiers générés varie également beaucoup entre les logiciels, ce qui peut affecter l’impact carbone lié au stockage des données. Par exemple, le logiciel fMRIPrep peut produire jusqu’à 5.55 GB de données par sujet, alors que les fichiers habituellement utilisés pour des analyses subséquentes ne représentent que 0.23 GB {cite:p}`souter2023`. La consommation d’énergie associée au stockage des données dépend du type de serveur. Par exemple, dans l’article de Smith et collègues (2025), la consommation d’énergie de leur serveur s’élevait à 19 KWh/TB/an {cite:p}`smith_doctoral_2025`. Si nous prenons en compte qu’un jeu de données standard en IRMf comprend 40 participant·e·s, alors la consommation énergétique requise pour stocker nos données prétraitées est de 4.12 KWh / an. Si ce serveur est situé au Québec, les émissions de GES liées au stockage de notre jeu de données serait de 142.14 g d'éq CO2 / an (34.5 g éq CO2 / KWh × 4.12 KWh / an) {cite:p}`levasseur2021`. Par contre, si ce serveur se situe en Alberta, cette valeur s’élèverait à 2224.8 g d’éq CO2 / an (540 g éq CO2 / KWh × 4.12 KWh / an) (Emission Factors and Reference Values - Tableau 5.1 {cite:p}`canada_greenhouse_gas_2024`). Pour des jeux de données d’envergure comme celui du Human Connectome Project, la taille totale des fichiers compte pour 80 TB {cite:p}`dataladhandbook`. Cela équivaudrait à 216.1 kg éq CO2 / an si ces données étaient stockées sur un serveur au Québec et 820.8 kg éq CO2 / an sur un serveur en Alberta !

### Présentation des résultats de recherche

Maintenant que nous avons acquis nos données et que nous les avons analysées, il est venu le temps de présenter nos résultats ! Ce partage de connaissances se fait soit via la présentation des résultats lors de conférences, soit sous forme de publications dans des journaux scientifiques.

Pendant la pandémie de la Covid-19, plusieurs conférences scientifiques se sont déplacées en ligne (p. ex., ISMRM 2020 et 2021, OHBM 2020 et 2021, SfN 2021). Malheureusement, ce format ne semble pas avoir persisté. De nombreuses conférences internationales ont repris en présentiel, obligeant donc à une grande proportion des participant·e·s à se déplacer en avion. Or, le secteur de l’aviation pourrait à lui seul contribuer à un réchauffement global cumulé d’environ 0.1 °C d’ici 2050 {cite:p}`klower2021`. Ce chiffre peut paraître assez faible a priori, mais sachant qu'il est impératif de limiter le réchauffement global à 1.5°C selon les recommandations du GIEC alors que nous étions déjà à 1.28°C en moyenne en 2024 {cite:p}`nasa2024`, cet impact est loin d’être négligeable.

Mais quelle est la contribution des conférences scientifiques sur les émissions de GES liés à l’aviation ? Il a été estimé que les émissions de GES associées au voyagement pour se rendre à la conférence de la Society for Neuroscience (environ 30000 participant.·e·s annuellement) s’élevaient à 22000 tonnes de CO2 en 2014 {cite:p}`nathans_2016`. Epp et collègues (2023) ont fait cet exercice dans le contexte des conférences de l’Organization for Human Brain Mappings (OHBM) (voir Tableau 1) {cite:p}`epp_2023`. Leur analyse montre que l’empreinte carbone de la conférence de 2019 à Rome, à elle seule, était équivalente à l’empreinte carbone totale de 50000 personnes vivant dans un pays à faible revenu sur une période de 1 an. Par contre, cet impact varie selon la localisation de la conférence. Par exemple, bien que la conférence de 2019 ait attiré près de 1000 participant·e·s de plus qu’en 2015, cette dernière a généré environ 2000 tonnes supplémentaires d’éq CO2, en raison d’un plus grand nombre de vols long (>1500 km) ou super long (>8000 km). Si l’on reprend l’exemple de la conférence de 2019, même si 45.6% des participant·e·s ont effectué un vol super long pour se rendre à la conférence, leur contribution aux émissions d’éq CO2 s’élève à 88.5% des émissions totales estimées.

| **Location**   | **Année** | **Présence** | **Tonnes éq CO2** |
| ----------- | :-----: | :--------: | :--------: |
| Honolulu  | 2015  | 2897     | 14277         |
| Vancouver | 2017  | 2775     | 8326          |
| Singapour | 2018  | 2038     | 10200         |
| Rome      | 2018  | 3886     | 12254         |

Tableau 1. Estimation de la quantité d’éq CO2 pour différentes conférences OHBM {cite:p}`epp_2023`.

## Des solutions

Maintenant que nous nous sommes sensibilisés à l’impact environnemental lié à la collecte, le prétraitement, l’analyse, la préservation et la présentation de données de recherche, il est temps de parler des solutions ! Dans cette section, nous allons voir qu’il est possible d’agir dans différentes sphères d’influence, de notre recherche à notre institution en passant par notre vie académique. Bien que nous allons prendre chacune de ces sphères séparément, il est important de mentionner qu’elles s'influencent mutuellement.

### Dans notre recherche

#### S'interroger

La première étape d’une étude scientifique commence par l’idéation du projet de recherche, c’est-à-dire la formulation de la question de recherche et l’élaboration du protocole expérimental en fonction de ce qui a été fait précédemment dans la littérature ({numref}`research-cycle-fig`). Cette étape pourrait/devrait comprendre une réflexion concernant la pertinence globale du projet de manière plus exhaustive.

Autrement dit, le manque de connaissances ne justifie pas toujours, à elle seule, la réalisation d’une nouvelle étude. Nous pourrions donc nous demander si les retombées scientifiques, sociales ou cliniques potentielles d’un projet justifient les coûts environnementaux et financiers associés. Même s’il n’existe pas d’outils nous permettant de faire cette évaluation coût-bénéfice, il est tout de même possible d’entamer certaines réflexions dès l’idéation de notre projet.

Il existe déjà plusieurs pratiques permettant d’augmenter les bénéfices de notre recherche. Par exemple, si nous cherchons à développer un plan d’intervention auprès d’une population spécifique, il serait essentiel de collaborer étroitement avec des individus de cette population pour s’assurer que l’on mesure des variables pertinentes et que le plan d’intervention proposé est réalistiquement implémentable dans leur réalité. Il est également possible de mettre en place différentes stratégies pour maximiser la valeur des données recueillies. Par exemple, nous pourrions élaborer un plan de partage de données incluant la plateforme utilisée, un format standard utilisé pour organiser les données, ainsi que la documentation nécessaire à leur réutilisation. Pour diminuer les coûts environnementaux, nous pourrions considérer dès l'élaboration de notre projet s’il serait possible d’utiliser des données déjà existantes, quelle serait la durée minimale d’acquisition nécessaire et le type d’équipement le plus approprié. Par contre, cette réflexion est rendue difficile en raison du manque d’information concernant le coût énergétique associé à certains choix expérimentaux.

#### Mesurer et rapporter

Dans le but de bien comprendre l’échelle des impacts environnementaux de la recherche au sein de notre communauté, il est important de mesurer ces impacts au niveau de nos projets de recherche et de rapporter ces résultats. Cela peut nous permettre d’identifier les étapes générant le plus d’émissions d’éq CO2 et réfléchir à des solutions pour les réduire. Cela peut également nous permettre d’identifier les équipements pour lesquels ces informations ne sont pas disponibles, et demander aux fabricants de les fournir (p. ex. via l’analyse du cycle de vie de leurs produits).

Certains outils sont déjà disponibles pour estimer l’impact carbone de nos activités de recherche. Au niveau de l’équipement utilisé pour la collecte de données, nous avons déjà discuté de l’analyse du cycle de vie qui est parfois fournie par les fabricants. La base de données [HealthcareLCA](https://healthcarelca.com/) est également pertinente pour les services, les équipements et les produits utilisés dans le domaine de la santé. Au niveau du prétraitement des données IRMf, le logiciel fMRIPrep inclut une fonctionnalité pour estimer la consommation énergétique et les émissions carbones liées au pipeline (voir la [documentation de fMRIPrep](https://fmriprep.org/en/stable/api.html#fmriprep.config.execution.track_carbon)). Au niveau des analyses, il est possible d’intégrer des outils de suivi d’émissions carbone comme [CodeCarbon](https://github.com/mlco2/codecarbon), CarbonTracker {cite:p}`anthony_2020` ou encore [GreenAlgorithms](https://calculator.green-algorithms.org/) (pour une liste plus exhaustive, voir [https://ohbm-environment.org/carbon-tracker-toolboxes/](https://ohbm-environment.org/carbon-tracker-toolboxes/)). Pour estimer les émissions liées au voyagement, des outils comme [myclimate](https://co2.myclimate.org/en/flight_calculators) peuvent être utilisés.

Ces informations peuvent être rapportées de différentes manières dans un article scientifique par exemple sous une section dédiée (p. ex. voir la section Environmental Impact Statement dans l’article de Souter et collègues (2024) {cite:p}`souter_measuring_2024`) ou sous forme de bilan carbone en annexe. Cela peut également être inclus dans les mémoires et les thèses, ou même sur nos affiches scientifiques. Si ces informations étaient plus fréquemment rapportées, cela pourrait permettre aux chercheuses et chercheurs de faire des choix plus éclairés lors de la conception de leur étude. Par exemple, cela pourrait influencer le choix de la séquence d’acquisition, des paramètres de prétraitement et des analyses réalisées. Cependant, pour maximiser l’utilité, il est préférable de rapporter ces informations de manière standardisée pour pouvoir adéquatement comparer les résultats entre différentes études. Par exemple, le [Scientific CO2nduct](https://scientific-conduct.github.io/) propose un exemple de tableau standardisé à inclure dans les publications scientifiques pour partager de manière transparente l’empreinte carbone d’une étude scientifique.

#### Faire des choix écoresponsables

Au-delà de la quantification de l’impact carbone, il est déjà possible d’utiliser les informations accessibles pour faire des choix éclairés lors de la conception de nos projets de recherche. Par exemple, les données sur l’ACV peuvent être utilisées pour faire des choix éco-responsables au niveau de l’achat d’équipement (p. ex. choisir des équipements avec une faible ACV), de leur maintenance (p. ex. prioriser la réparation plutôt que l’achat de nouveaux équipements) et de leur usage.

Il serait également possible de mutualiser les ressources entre les laboratoires de recherche plutôt que de dupliquer le matériel et les dépenses ! Par exemple, un laboratoire ayant acquis des tablettes électroniques pour leur cueillette de données pourrait les rendre accessibles à d’autres laboratoires. Le [Registre des Infrastructures et des Équipements (RIÉ)](https://rie.umontreal.ca/accueil/) à l’Université de Montréal est un bon exemple de plateforme supportant le partage d’équipement de recherche en biologie, biophysique et biochimie.

Au niveau de la consommation énergétique au niveau du prétraitement et de l’analyse des données IRMf. Nous avons déjà discuté des études de Souter et collègues (2024 et 2025) proposant certaines pistes de solutions pour diminuer l’impact carbone du prétraitement des données via fMRIPrep ou via l’utilisation d’autres logiciels (SPM et FSL). En ce qui concerne les analyses, [The Turing Way Community](https://book.the-turing-way.org/ethical-research/activism/activism-env-impact) propose des stratégies de réduction de l’impact environnemental, comme l’amélioration de l’efficacité du code, l’évitement de tâches non nécessaires, l’utilisation de centres de données verts. Réduire la quantité de données en éliminant les fichiers redondants et inutilisés permet également de diminuer la demande énergétique associée à la préservation de données (voir [fMRIPrepCleanup](https://github.com/NickESouter/fMRIPrepCleanup) pour un exemple).

```{admonition} Science (ou)verte !
:class: tip
:name: science-ouverte-tip
Les pratiques de science ouverte incluent notamment le partage de données et le partage de code. Le partage des données permet de limiter l’acquisition redondante de données qui, comme nous l’avons vu au début de la section, peut être très coûteuse au niveau énergétique. De plus, si ces données sont partagées dans des formats standardisés, cela peut favoriser l’utilisation des données et éliminer le besoin de conversion de format. Cependant, il est important de choisir une plateforme de partage de données utilisant des serveurs ayant un faible impact environnemental. Par exemple, la plateforme Open Science Framework (OSF) qui utilise Google Cloud. Les centres de données de Google sont parmi les plus efficaces en termes de consommation énergétique ([https://datacenters.google/operating-sustainably/](https://datacenters.google/operating-sustainably/)).
```
### Dans nos institutions

#### S'impliquer

En tant qu’étudiant·e·s ou chercheur·euse·s, nous avons l’opportunité de nous impliquer à différents niveaux, que ce soit dans des comités étudiants, au niveau départemental, au niveau de notre centre de recherche, ou au niveau de nos communautés scientifiques. Renseignez-vous sur les initiatives écologiques dans votre université, impliquez-vous, ou créez un comité vert s’il n’y en a pas.

Si vous vous impliquez dans l’organisation de divers événements (p. ex. les journées scientifiques), supportez l'implémentation de choix écologiques, que ce soit au niveau du choix des chercheur·euse·s invité·e·s, du choix du traiteur, de la gestion des déchets, etc. Offrez la possibilité de participer en ligne si possible. En plus de limiter le transport, cela permet également à votre événement d’être plus inclusif en réduisant les coûts pour les participant·e·s et en offrant une option qui offre plus de flexibilité aux personnes ayant différentes contraintes dans leur horaire (p. ex. parents avec de jeunes enfants) ou une mobilité réduite. Il existe plusieurs ressources en ligne pour faire des choix plus éclairés lorsqu’il s’agit d’organiser des événements écoresponsables (p. ex. [le Guide de l’événement écoresponsable de l’Université de Montréal](https://durable.umontreal.ca/fileadmin/durable/documents/Even-ecoresponsables/guide-evenement-ecoresponsable-udem-complet.pdf)).

```{admonition} Ombre climatique
:class: tip
:name: ombre-climatique-tip
L’ombre climatique réfère à l’impact climatique total de nos actions, au-delà de notre empreinte carbone {cite:p}`pattee_2024`. Ce concept prend donc en compte l’impact que l’on a plus généralement sur les autres et la société. L’ombre climatique de notre institution pourrait comprendre ses investissements dans les énergies fossiles et non simplement l’empreinte carbone associée à l’usage et au maintien de ses infrastructures. Notre ombre climatique au niveau de notre vie académique pourrait par exemple inclure l’inclusion de rapport carbone dans nos mémoires et nos thèses pour rapporter l’empreinte carbone de notre recherche, ou bien encore prendre le temps de discuter au sein de nos laboratoires des enjeux environnementaux auxquels nous faisons face.
```

### Dans notre vie académique

#### Voyager moins, voyager mieux

Favoriser les conférences régionales et les conférences à faible impact carbone. Il existe plusieurs formats de conférences qui permettent de réduire les coûts environnementaux, comme les conférences en ligne, les conférences hybrides, les conférences multi-sites et les conférences bisannuelles {cite:p}`epp_2023`. Avant de vous inscrire à une conférence, vérifiez également si le comité organisateur a partagé une liste des pratiques écoresponsables entourant l’organisation de cet événement (p. ex. s’il est possible de se rendre à la conférence à vélo ou en utilisant le transport en commun).

#### Engagement et communication scientifique

Le rôle de chercheur·euse·s offre un statut privilégié pour discuter des enjeux environnementaux au niveau des pratiques scientifiques, mais également pour accéder et comprendre la littérature scientifique pertinente. Utilisez les plateformes qui vous sont disponibles pour mettre de l’avant ces enjeux, que ce soit en affichant l’impact carbone de votre étude sur votre affiche scientifique, lors d’une présentation orale, ou au sein de votre laboratoire. Normaliser ces discours peut mener à des changements de mentalité propices à des actions collectives.

### La (fausse ?) promesse de l'IA

Avec les prouesses de l’intelligence artificielle (IA), il serait raisonnable de croire que cette technologie pourrait nous permettre de résoudre, du moins en partie, la crise climatique de manière générale, mais également en ce qui nous concerne dans ce chapitre, c’est-à-dire pour tenter de réduire l’empreinte carbone de la recherche en neuroimagerie. Il pourrait donc être possible de se concentrer sur une application de l’IA visant à minimiser l’impact environnemental associé aux différentes étapes du processus de recherche, par exemple, en optimisant une séquence d’acquisition IRMf pour limiter la durée des scans ou pour sélectionner une séquence moins énergivore, ou encore pour sélectionner des algorithmes plus verts pour analyser ce type de données {cite:p}`lannelongue_green_2021` {cite:p}`lorenz_2016`.

Par contre, il est important de reconnaître les impacts négatifs de l’IA et de responsabiliser l’utilisation que nous en faisons. La balance entre les impacts positifs de l’IA et ses impacts négatifs, particulièrement sur le plan environnemental, est complexe. Les émissions de gaz à effet de serre liées à l’intelligence artificielle proviennent de sources diverses, notamment le stockage des données, l’entraînement, l’ajustement et l’utilisation de modèles d’apprentissage profond. L’impact environnemental de ces étapes est d’autant plus exagéré par la poursuite de l’intelligence artificielle générale et par la croyance que plus c’est mieux: plus de données, des modèles plus larges, et plus de temps et de ressources computationnelles mèneraient au développement de modèles plus performants {cite:p}`krizhevsky_imagenet_2012` {cite:p}`varoquaux_2025` {cite:p}`bhardwaj_2025`. Ces pratiques accroissent le rythme d’expansion des centres de données et l’intégration des super-ordinateurs qui dépendent principalement des énergies fossiles pour fonctionner en continu 24 heures sur 24, 7 jours sur 7 {cite:p}`tec_2025`. Entre 2020 et 2023, Les émissions opérationnelles des quatre principaux acteurs dans le domaine de l’IA (Amazon, Microsoft, Alphabet (Google) et Meta) ont augmenté de 150% en moyenne {cite:p}`itu_greening_2025`. De plus, les infrastructures et les centres de données requièrent également d’être refroidis, ce qui nécessite l’utilisation d’eau douce. Au-delà de l’impact environnemental, cette consommation de ressources entraîne d'importants enjeux humains et sociaux considérant le développement de centres de données dans des zones confrontés à un stress hydrique.

Heureusement, plusieurs centres de données transitionnent vers des pratiques écoresponsables, en intégrant des équipements à meilleure efficacité énergétique, des techniques de refroidissement permettant de réduire la consommation énergétique ou encore en introduisant de plus en plus des sources d’énergie renouvelables {cite:p}`gugul_2023`. Les centres de données/de calcul haute performance (high performance computing; HPC) ayant la meilleure efficacité énergétique figurent sur la [liste GREEN500](https://www.top500.org/lists/green500/) {cite:p}`sharma_2006`. D’ailleurs, en juin 2025, le superordinateur dédié à la recherche canadienne, Rorqual, y était listé en 73e position {cite:p}`green500_2025` !

```{admonition} L'IA verte
:class: tip
:name: ia-verte-tip
L’IA verte constitue un changement de paradigme dans le domaine de l’intelligence artificielle en proposant de nouvelles manières d’évaluer les modèles d’IA. Au lieu d’uniquement considérer la performance prédictive (accuracy) comme métrique d’évaluation, l’IA verte soutient l’inclusion de métriques visant à mesurer l’efficacité computationnelle {cite:p}`schwartz_2019`.
```

## Conclusions

Ce chapitre vous a offert un aperçu de l’impact environnemental associé à chaque étape du processus scientifique. Plusieurs concepts ont été introduits pour mieux comprendre comment calculer et rapporter l’impact environnemental de notre recherche.

## Exercices

Le format des exercices de ce chapitre diffère de celui des chapitres précédents puisqu’il n’y a pas de bonne ou de mauvaise réponse. Ces exercices servent plutôt à susciter des réflexions à propos du contenu de ce chapitre.

```{admonition} Exercice 1
:class: note
a. Quels gestes pourriez-vous envisager pour réduire l’impact environnemental dans votre recherche, dans vos institutions ou dans votre vie académique ?
b. Quels gestes seraient les plus accessibles ? Lesquels seraient les plus difficiles à réaliser ? Pourquoi ?
```

```{admonition} Exercice 2
:class: note
Est-ce que l’impact environnemental devrait être considéré lors de l’approbation éthique d’une étude scientifique ?
```

```{admonition} Exercice 3
:class: note
Selon vous, dans l’écosystème de recherche, quels acteurs ont le plus de pouvoir pour faire évoluer les pratiques de recherche pour inclure davantage les enjeux environnementaux ?
```

```{admonition} Exercice 4
:class: note
À quoi pourrait ressembler un projet de recherche en neuroimagerie qui intègre des considérations environnementales à toutes les étapes de recherche ?
```

## Contributrices

🤔 Contenu | 💻 Code | 🧩 Quizz | 👀 révision du texte
::::{grid}

:::{grid-item}
![Lune Bellec](https://avatars.githubusercontent.com/u/1670887?v=4?s=100)
[Lune bellec](https://github.com/lunebellec) 👀
:::

:::{grid-item}
![Dylan Sutterlin Guindon](https://avatars.githubusercontent.com/u/70554831?v=4?s=100)
[Dylan Sutterlin Guindon](https://github.com/dylansutterlin)
👀
:::

:::{grid-item}
![Marie-Eve Picard](https://avatars.githubusercontent.com/u/77584086?v=4?s=100)
[Marie-Eve Picard](https://github.com/me-pic)
🤔🧩👀
:::

:::{grid-item}
[Aline Moussard]()
👀
:::

::::
