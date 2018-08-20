# Names for Biodiversity Workshop

## Introduction

Recent work on names is fragmented into individual and isolated project efforts. There are now more terms than concepts, more definitions than terms. Many, more-or-less, similar vocabularies, alternative frameworks and non-interoperable, application systems.

This may well be the natural process of evolution but we do need to make time now to discuss synthesis and a more collaborative approach to development of a workable standard for names. Can we work together to fill the gaps, and to resolve the competing requirements of aggregation and science, data and knowledge, product and research, Code-compliance and interoperability.

## Purpose

To raise awareness of the importance of names to biodiversity informatics and to re-invigorate a more collaborative phase of standards development with names within the TDWG umbrella.

This workshop will aim for consensus around the idea that we can work together within TDWG to evolve a pragmatic replacement for the existing names standards, and a map to get us there.

## Goals

1.  Reconvene the [Taxonomic Names and Concepts Interest Group](https://www.tdwg.org/community/tnc/)
    - Membership
    - GitHub, [tdwg/tnc](https://github.com/tdwg/tnc)
    - Standards maintenance.
2.  Agreement on a plan for a replacement of the **Taxonomic Concept Transfer Schema (TCS)** that:
    - is compliant with the TDWG [Standards Documentation Standard](https://github.com/tdwg/vocab/tree/master/sds) and [Vocabulary Maintenance Standard](https://github.com/tdwg/vocab/tree/master/vms).
    - provides for the needs of the various types of users and use cases of Taxonomic Names in the biodiversity informatics space
    - as much as possible synthesises and takes benefit of the work that has been done in the TDWG community so far.

##  Uses / Stakeholders

- Simple checklists, aggregators: GBIF, ALA, CoL
- Species Information Systems
- Floras, Faunas etc.
- Systems that capture historical (as well as current) name usages: NSL, APNI, AFD
- Systems that try to capture phylogenetic relationships

## Current standards

- [Taxonomic Concept Transfer Schema (TCS)](https://www.tdwg.org/standards/tcs/)
-	[Darwin Core](https://www.tdwg.org/standards/dwc/)

> #### Resources
> - **TCS 1.01 Schema Documentation** can be found at http://tdwg.github.io/tcs/schema/1.01/
> - **Darwin Core** terms can be found at http://tdwg.github.io/dwc/terms/

## Issues

- Expectation reversal, but:
  - Taxa **change**
    - AFD = taxonomic (opinion) product, not a Nomenclator, not a taxon store.
      @rdmpage:  WTF
    - Taxonomic Names are stable.
    - Inappropriate use of taxon.
- No “Names” standard.
  - Darwin Core RDF Guide recommends separate vocabulary.
  - Ad hoc Darwin Core extensions.
  - Inappropriate use of the taxonomic concept concept.
  - Essential controlled vocabularies lacking.
- Taxonomic Concept (TCS)
  - Seems too esoteric:  
    - Not used, or
    - used anyway.
  - Application schema
    - Interchange of literature based concept definitions.
  - Difficult to distill, harder to extend.
  - Syntax (XML) → path to RDF … JSON.
  - Over engineered for normal usage:)
  - Relationship object
    - Path to RDF, JSON-LD
  - > How does tcs:TaxonConcept relate to dwc:Taxon?
  - > How does tcs:TaxonConcept relate to NameUsage and nsl:Instance?
- Darwin Core ambiguous
  - Overloaded definitions
  - Many interpretations.
  - Overloaded usage.
  - Classification terms.
  - Ranks.
  - Path to RDF …
- Many different application profiles
  - Simple vocabulary required.
- A Domain Model?
  - Agreement on definitions
  - Classes
  - Code compliance
- ???

## Previous Work

- **Bisby**
- APNI
- Berlin Model
- IPNI
- ITIS, CoL
- Flora of Australia
- Tropicos
- LinneanCore (**SDD**)
- **DwC**, **ABCD**
- **TCS**
- TDWG ontology
- ALA-NSL (2008)
- txn:deVriese
- GBIF Checklist
- **DwC RDF**
- Nomen
- WFO
- OpenBiodiv
- BCO
- ColPlus
- TaxRef
- +++

## Strategy / Way Forward?

- **A new standard or update/replace/extend existing standards?**

- **Restart with Linnean Core**
  - A Basic vocabulary for the interchange and use of Taxonomic Names and “names”.
  - Darwin Core  extensions >  NFB  < TCS.
  - Controlled vocabularies!
  - Recommend classes.
  - Guidelines.

- **Darwin Core**
  - leave “convenience” terms and internal links.
  - remove external links (id terms) ?
  - Add new terms?
  - [Darwin Core RDF Guide](http://rs.tdwg.org/dwc/terms/guides/rdf/index.htm#2.6_Darwin_Core_ID_terms_and_RDF)

- **A Domain Model or List?**
  - Normative or Guide?
  - API specification for:
  - Name
  - Instance (name occurrence)
  - Usage ( potential/taxonomic concept)
  - Taxon
  - Taxonomic Tree ?
  - Arrangement

## What are we looking for in a Name standard/vocabulary?

(Core competencies / Functional Requirements / Use cases)

- Generic metadata model
  - Vocabularies
- Full Code support
  - ICN, ICZN, ...
  - Code maintenance
    - Domain owners?
- Interoperability
  - Every name
  - Every instance (name usage)
  - Every relationship
  - Every point of view
  - Every version
  - Every syntax
  - Every application profile
  - Common interchange format
  - Support for publication
  - Extensible
- Obey the the TDWG laws for standards and vocabularies
- Independent of serialization
- Concise vocabulary
- RDF support
- Application Profiles
- Simple enough for …
