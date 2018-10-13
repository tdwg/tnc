# TaxonomicRank

Enumerated codes to express the rank of a taxon (scientific organism name) in a taxonomic hierarchy. The list is intended to be interoperable between name providers for bacteria, viruses, fungi, plants, and animals. It is not assumed that in each taxonomic group all ranks have to be used. Individual applications may select appropriate subsets (which may be based on information given inside the enumerated values, see Specifications/BioCode-, Botany-, Zoology-, and BacteriaStatus). The enumeration attempts to strike a balance between listing all possible rank terms, and remaining comprehensible. For example, the "infra-" ranks specifically mentioned in BioCode have been included (although very rarely used), but the additional intermediate zoological ranks (micro, nano, pico, etc.) are not included. Whether the selection of infraspecific ranks (some informal ranks, esp. from bacteriology, may be missing!) probably needs some discussion. However, it is believed that this list may help to start developing data sets that can easily be integrated across the barriers of Language and taxonomic traditions.</p>
<p>Not included in the list are the botanical "notho-" ranks, which are used to designate hybrids (nothospecies, nothogenus). It is assumed they can be generated from separate information that the taxon is a hybrid. ICBN Â§4.4 states: "The subordinate ranks of nothotaxa are the same as the subordinate ranks of non-hybrid taxa, except that nothogenus is the highest rank permitted".

The following publications have been consulted to determine the number of type terms that should be included and to prepare the semantic definitions:

* The Berlin Taxonomic Information Model, MoReTax view (Berendsohn &amp; al., http://www.bgbm.org/scripts/ASP/BGBMModel/Catalogues.asp?Cat=MT)
* DiversityTaxonomy model version 0.7 (G. Hagedorn &amp; T. Grafenhan 2002, http://160.45.63.11/Workbench/Taxonomy/Model/InformationModels.html)
* ABCD version 1.44, types HigherTaxonRankType and RankAbbreviationType, by W. Berendsohn, reviewed by D. Hobern
* TaxCat2 - Database of Botanical Taxonomic Categories by Jorg Ochsmann, IPK Gatersleben; http://mansfeld.ipk-gatersleben.de/TaxCat2/default.htm

A separate enumeration and several ranks have been added to the original list to better accommodate names from ICNCP. (RDH).

Many thanks for review and help go to Dr. Walter Gams.

Note: the list of all ranks is implemented as a union of all following rank subsets. Note that although BioCode has been used to define the partition into subsets, the ranks are not limited to BioCode but should be an interoperable superset of ranks used in Virology, Bacteriology, Botany and Zoology.

## TaxonomicRankAboveSuperfamilyEnum

Subset of ranks; equivalent to BioCode "suprafamilial". This rank group includes all ranks higher than superfamily (class, phylum/division, kingdom, domain)

Value | Description | Examples
-|-|-
infraord | infraorder |
subord | suborder | Magnolineae, Catarrhini
ord | order | Magnoliales, Primates
superord | superorder | Magnolianae
infracl | infraclass |
subcl | subclass | Magnoliidae, Eutheria
cl | class | Magnoliopsida, Mammalia
supercl | superclass |
infraphyl_div | infraphylum (= infradivision) |
subphyl_div | subphylum (= subdivision) | Magnoliophytina, Vertebrata
phyl_div | phylum (= division) | Magnoliophyta, Chordata
superphyl_div | superphylum (= superdivision) |
infrareg | infrakingdom |
reg | kingdom | Plantae, Animalia
superreg | superkingdom | Eukaryota
dom | domain | Archaea (= Archaeobacteria), Bacteria (= Eubacteria), Eukarya (= Eukaryota)
taxsupragen | suprageneric taxon of undefined rank -- This value indicates that the rank of a name is unknown. Compare "incertae sedis" which is commonly used as a replacement for a taxon to group all taxa whose position in the classification or phylogenetic tree is uncertain |

## TaxonomicRankFamilyGroupEnum

Subset of ranks; equivalent to BioCode "family group", i.e. infrafamily to superfamily

Value | Description | Examples
-|-|-
infrafam | infrafamily |
subfam | subfamily | Magnolioideae
fam | family | Magnoliaceae, Hominidae
superfam | superfamily | Magnoliacea

## TaxonomicRankFamilySubdivisionEnum

Subset of ranks; equivalent to BioCode "subdivision of a family", i.e. ranks between genus group and family group

Value | Description | Examples
-|-|-
infratrib | infratribe |
subtrib | subtribe |
trib | tribe |
supertrib | supertribe |

## TaxonomicRankGenusGroupEnum

Subset of ranks; equivalent to BioCode "genus group", i.e. infragenus to genus

Value | Description | Examples
-|-|-
infragen | infragenus |
subgen | subgenus |
gen | genus | Magnolia, Homo

## TaxonomicRankGenusSubdivisionEnum

Subset of ranks; equivalent to BioCode "subdivision of a genus", i.e. all ranks between genus and species group (i.e. not including subgenus and species)

Value | Description | Examples
-|-|-
aggr | species aggregate (= species group, species complex) -- A loosely defined group of species. Zoology: "Aggregate - a group of species, other than a subgenus, within a genus. An aggregate may be denoted by a group name interpolated in parentheses." -- The Berlin/MoreTax model notes: "[these] aren't taxonomic ranks but cirumscriptions because on the one hand they are necessary for the concatenation of the fullname and on the other hand they are necessary for distinguishing the aggregate or species group from the microspecies." Compare subspecific aggregate for a group of subspecies within a species! |
taxinfragen | infrageneric tax. of undefined rank -- A name that appears between a genus name and a species epitheton and is not clearly marked as series or section, or other may be assigned to this rank until the true rank can be assigned by a taxonomic expert. |
subser | subseries |
ser | series |
subsect | subsection |
sect | section |

## TaxonomicRankSpeciesGroupEnum

Subset of ranks; equivalent to BioCode "species group", i.e. only species and subspecies

Value | Description | Examples
-|-|-
subsp_aggr | subspecific aggregate (= group, complex) -- A loosely defined group of subspecies. Zoology: "Aggregate - a group of subspecies within a species. An aggregate may be denoted by a group name interpolated in parentheses." |
ssp | subspecies | Pinus nigra subsp. nigra, Homo sapiens sapiens
sp | species | Taxus baccata, Homo sapiens

## TaxonomicRankBelowSubspeciesEnum

Subset of ranks; equivalent to BioCode "infra-subspecfic", i.e. below the species group

Value | Description | Examples
-|-|-
cand | candidate -- Candidatus' rank is proposed in bacteriology for putative taxa, which could not yet be studied sufficiently to warrant the creation of a name with a known rank. (Murray, R.G.E. &amp; Schleifer, K.H.: Taxonomic notes: a proposal for recording the properties of putative taxa of procaryotes. Int. J. Syst. Bacteriol., 1994, 44, 174-176). |
taxinfrasp | infraspecific tax. of undefined rank -- Undefined ranks (using either no rank identifier in botany, or using greek letters or symbols like stars, crosses) occur in very old publications. Most frequently these are to be interpreted as varieties, but occasionally they are forms or subspecies (see Stearn, W.T. 1957: Species plantarum (Facsimile); Introduction. 1. London, p. 90-95, 160-161, 163). The interpretation of these cases requires taxonomic knowledge that may not be available at the time when data are parsed. Such lack of knowledge can be expressed using this rank identifier. |
fsp | special form -- The ICBN does not formally cover formae specialis (art. 4, note 3). However, because of the economic importance of pathogenic f. sp., and since it is common practice to handle them as if the code would apply (i. e. priority usually observed, name quoted with author), they are included here. |
subsubfm | subsubform |
subfm | subform |
fm | form -- Form, race, variety are not subject to regulation in zoology; see ICZN Article 1.3.4 |
subsubvar | sub-sub-variety |
subvar | sub-variety |
var | variety -- Form, race, variety are not subject to regulation in zoology; see ICZN Article 1.3.4 | Pinus nigra var. caramanica (= "P. nigra subsp. nigra var. caramanica"), Taxus baccata var. variegata
pv | patho-variety |
bv | biovariety |
infrasp | infraspecies |

## TaxonomicRankCultivatedPlants

Subset of ranks used spefically for cultivated plants

Value | Description | Examples
-|-|-
cv | cultivar -- The epithet is usually output in single quotes and may contain multiple words, see ICBN Â§28. | Taxus baccata 'Variegata', Juniperus ×pfitzeriana 'Wilhelm Pfitzer', Magnolia 'Elizabeth' (= a hybrid, no species epithet).
convar | convar -- Used in cultivated plants (ICNCP), but deprecated, see 'Some notes on problems of taxonomy and nomenclature of cultivated plants' by J. Ochsmann, http://www.genres.de/IGRREIHE/IGRREIHE/DDD/22-08.pdf |
grex | grex -- a rank equivalent to cultivar group used principly for artificial hybrid swams in Orchidaceae |
cvgroup | cultivar group |
graftchimaera | graft-chimaera |
denomclass | Denomination classes are constructs under ICNCP for defining the scope within which a cultivar or Group epithet must be unique. |
