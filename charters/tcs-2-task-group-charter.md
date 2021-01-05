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

### 4. Motivation and scope

The purpose-built TDWG standard for exchanging taxonomic data, the Taxon Concept Schema (TCS), is an XML Schema, so requires data to be in XML format. The XML Schema is also seen as overly complicated, hard to validate and not extensible, and is seen as primarily a document specification for delivering a data set. The alternative, the Darwin Core Taxon class, on the other hand is a bit too flexible and does not do enough to discourage exchange of incorrect or incomplete data. It also implies classes that are not defined, e.g. for scientific names and references, and is therefore unsuitable for exchange of data in, for example, RDF.

Despite its shortcomings, the basic data model of TCS is considered well thought-through and works for many people. The Taxon Name and Taxon Concept parts of the TDWG LSID Ontology, which are based on TCS, are being used by taxonomic and nomenclatural systems, but are not a standard. We believe that, if we recast TCS to an extensible TDWG vocabulary, according to the Vocabulary Maintenance Specification, it will meet the needs of all use cases and will find wide acceptance.

The focus of the Task Group will be on structure, rather than content. While many terms need better definitions and notes, we will only make changes to the meaning of terms when required.
While not in scope for the Task Group, the ability to exchange references in a standard way is essential for the success of the standard and will be incorporated in TCS 2 if other activities of the TCS Maintenance Group or outside the group deliver it in time.

### 5. Goals, outputs, and outcomes

The goal of the project is to create a new version of TCS that is up to date with the Vocabulary Maintenance Standard and Standards Documentation Standard.

Outputs of the task group will be:

- Specification of terms and definitions with usage, notes and mapping to the previous version and other specifications
- Controlled vocabularies for terms that require/would benefit from them
- Additional documentation.

The intended outcome is a TDWG standard for exchange of taxonomic and nomenclatural data that will find wide acceptance in the community and works well with other TDWG standards.

### 6. Strategy and/or Framework

The Term list document that resulted from the review of TCS 1.1 and other relevant specifications that took place between TDWG 2018 and TDWG 2019 will form the basis for version 2 of TCS. Some refinement will be necessary, but significant changes or additions are out of scope for this Task Group. For changes to TCS that are in scope, but are felt might still be controversial or poorly understood, the Task Group will consult with the community at an early stage. Well before release we aim at publishing a paper in BISS on the rationale behind the changes to the standard.
We expect that it will take the task group 12 months to complete the specification and another six months to complete the additional documentation.

We intend to invite reviewers from important stakeholders like Catalogue of Life and Plazi to provide feedback at various times during the development of the specification.This is separate from the TDWG review process that will take place when the draft standard is completed.

The organisational and procedural framework for developing and ratifying TDWG standards is specified by the ratification process given in the TDWG Process.

### 7. Becoming Involved

All the work of the task group will take place in the TNC GitHub repository and a shared Google Drive folder. All documents will be available for viewing and commenting by anyone in the community at any time. People who are interested in participating in the task group are encouraged to contact the convener or a core member.

### 8. History/Context

The Taxon Concept Schema (TCS) was developed by the then Taxon Names and Concepts subgroup of TDWG and was ratified at TDWG 2005 in Saint Petersburg and released as TDS 1.01. Like its contemporaries, the Access to Biological Collections Data (ABCD) and Structured Descriptive Data (SDD) standards, TCS is an XML Schema and has not kept up with changing requirements for TDWG standards. In 2009, TDWG ratified the Darwin Core standard, which is a vocabulary of terms and definitions and therefore much more flexible than TCS. Darwin Core has a Taxon class, which is now widely used for the exchange of taxonomic data, for which TCS was made, but which has its shortcomings as well. At the Taxon Names and Concepts interest group (TNC) workshop at TDWG 2018 in Dunedin, it was decided that the TNC should undertake a revision of TCS. Between TDWG 2018 and TDWG 2019, the TNC did a review of TCS, also looking at the Darwin Core Taxon class, the TDWG Taxon Name and Taxon Concept LSID Ontologies, as well as other specifications, which resulted in a working document that will form the basis for this task group’s work.

### 9. Resources

- Task Group’s GitHub repository: https://github.com/tdwg/tnc
- Use cases
- TCS 1.01: https://github.com/tdwg/tcs
- Project boards: https://github.com/tdwg/tnc/projects
