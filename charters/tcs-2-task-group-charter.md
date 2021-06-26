# TCS 2 Task Group Charter

### 1. Summary

The TCS 2 Task Group will bring TCS up to date with the Vocabulary Maintenance Standard and provide the necessary documentation according to the Standards Documentation Standard by early 2022.

### 2. Convener

Niels Klazenga – Royal Botanic Gardens Victoria / Atlas of Living Australia

### 3. Core members

- Johan Liljeblad – SLU Swedish Species Information Centre
- Campbell Webb – University of Alaska Museum of the North
- Jeff Gerbracht – Cornell Lab of Ornithology
- Greg Whitbread – Taxamatics
- William Ulate – Missouri Botanical Garden
- Anne Fuchs - Centre for Australian National Biodiversity Research

### 4. Motivation and scope

The purpose-built TDWG standard for exchanging taxonomic data, the [Taxon Concept Schema (TCS)](https://github.com/tdwg/tcs/blob/master/TCS101/UserGuidev_1.3.pdf), is an XML Schema, so requires data to be in XML format. The XML Schema is also seen as overly complicated, hard to validate and not extensible, and is seen as primarily a document specification for delivering a data set. The alternative, the [Darwin Core Taxon class](https://dwc.tdwg.org/terms/#taxon), on the other hand is a bit too flexible and does not do enough to discourage exchange of incorrect or incomplete data. It also implies classes that are not defined, for example for scientific names and references, and is therefore unsuitable for exchange of data in, for example, RDF.

Despite its shortcomings, the basic data model of TCS is considered well thought-through and works for many people. The Taxon Name and Taxon Concept parts of the [TDWG LSID Ontology](https://github.com/tdwg/ontology/tree/master/ontology/voc), which are based on TCS, are being used, but are not a standard. We believe that, if we recast TCS to an extensible TDWG vocabulary, according to the Vocabulary Maintenance Specification, it will meet the needs of all use cases and will find wide acceptance.

The focus of the Task Group will be on structure, rather than content. While many terms need better definitions and notes, we do not expect significant changes to the meaning of terms.

### 5. Goals, outputs, and outcomes

The goal of the Task Group is to create a new version of TCS that is up to date with the [Vocabulary Maintenance Standard](https://github.com/tdwg/vocab/tree/master/vms) and [Standards Documentation Standard](https://github.com/tdwg/vocab/tree/master/sds) and will elevate TCS to the state Darwin Core and Audubon Core are in.

Outputs of the task group will be:

- Specification of terms and definitions with usage, notes and mapping to the previous version and other specifications
- Controlled vocabularies for terms that require or would benefit from them
- Additional documentation.

The intended outcome is a TDWG standard for exchange of taxonomic and nomenclatural data that will find wide acceptance in the community and works well with other TDWG standards.

### 6. Strategy and/or framework

The framework for revisions to existing TDWG standards is provided by the [Vocabulary Maintenance Specification](https://github.com/tdwg/vocab/blob/master/vms/maintenance-specification.md).

The [Term list document](https://docs.google.com/document/d/1bcfjhh0ztmXKz7P9G0ni7vYZc3MtH4LLxlCZjswF2k4) that resulted from the review of TCS 1.1 and other relevant specifications that took place between TDWG 2018 and TDWG 2019 will form the basis for version 2 of TCS. Some refinement will be necessary, but significant changes or additions are out of scope. The task group will further triage by focusing on terms and controlled vocabularies that are necessary and/or straightforward. Terms and/or controlled vocabularies for which use cases are not clear yet, but that are likely to require a lot of time from the task group, will be marked as potential future enhancements to the standard at the discretion of the maintenance group.

Following the lead of the Collection Description and Attribution interest groups, GitHub issues have been created for all terms and project boards have been created for classes and controlled vocabularies. The intention is to have a master document (or documents) and move issues across the boards via commits to the master document. The task group will have monthly meetings.

We intend to invite feedback from important stakeholders like Catalogue of Life and Plazi at various times during the development of the specification, possibly by inviting them to review pull requests. This is separate from the expert review that is part of the TDWG process for ratification of standards and changes to standards.

We aim to complete the specification by TDWG 2021 at the end of September and the entire standard including additional documentation well before TDWG 2022.

### 7. Becoming involved

All the work of the task group will take place in the TCS 2 GitHub repository and a shared Google Drive folder. All documents will be available for viewing and commenting by anyone in the community at any time. People who are interested in participating in the task group are encouraged to contact the convener or a core member.

### 8. History/context

The Taxon Concept Schema (TCS) was developed by the then Taxon Names and Concepts subgroup of TDWG and was ratified at TDWG 2005 in Saint Petersburg and released as TCS 1.01. Like its contemporaries, the Access to Biological Collections Data (ABCD) and Structured Descriptive Data (SDD) standards, TCS is an XML Schema and has not kept up with changing requirements for TDWG standards. In 2009, TDWG ratified the Darwin Core standard, which is a vocabulary of terms and definitions and therefore much more flexible than TCS. Darwin Core has a Taxon class, which is now widely used for the exchange of taxonomic data, for which TCS was made, but which has its shortcomings as well. At the Taxon Names and Concepts interest group (TNC) workshop at TDWG 2018 in Dunedin, it was decided that the TNC should undertake a revision of TCS. Between TDWG 2018 and TDWG 2019, the TNC did a review of TCS, also looking at the Darwin Core Taxon class, the TDWG Taxon Name and Taxon Concept LSID Ontologies, as well as other specifications, which resulted in a working document that will form the basis for this task group’s work.

### 9. Resources

- [Task Group’s GitHub repository](https://github.com/tdwg/tcs2): a new GitHub has been created for the Task Group. The [working document](https://docs.google.com/document/d/1bcfjhh0ztmXKz7P9G0ni7vYZc3MtH4LLxlCZjswF2k4) has been split up in separate issues for each term, so that each term has its own discussion thread. We have also created projects for each class and vocabulary.
- [TNC Interest Group repository](https://github.com/tdwg/tns): discussions in the last three years have mostly taken place in the issues in this repository. If people want to propose new terms that are not in the TCS 2 repository yet, it is best to do that in the TNC repository.
- [TCS 1 repository](https://github.com/tdwg/tcs): this repository contains the XML Schema, schema documentation and user guide of TCS 1.
- TDWG [Taxon Name](https://github.com/tdwg/ontology/blob/master/ontology/voc/TaxonName.rdf) and [Taxon Concept](https://github.com/tdwg/ontology/blob/master/ontology/voc/TaxonConcept.rdf) LSID Vocabularies. These ontologies, converted to Turtle, are also available in the [TNC repository](https://github.com/tdwg/tnc/tree/master/tcs-docs).
- [Darwin Core Taxon class](https://dwc.tdwg.org/terms/#taxon) and the section on description of a taxonomic entity in the [Darwin Core RDF Guide](https://dwc.tdwg.org/rdf/#274-description-of-a-taxonomic-entity-normative).
- Hawksworth, D.L. (2017), Terms Used in Bionomenclature. The naming of organisms (and plant communities). GBIF. &lt;https://www.gbif.org/document/80577/terms-used-in-bionomenclature-the-naming-of-organisms-and-plant-communities&gt;. This work contains a lot of the definitions we need for terms dealing with taxon names, based on all the different nomenclatural code.
