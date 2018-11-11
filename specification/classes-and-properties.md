# Classes and properties

### TaxonomicName

- nameComplete
- uninomial
- genusPart
- infragenericEpithet
- specificEpithet
- infraspecificEpithet
- nomenclaturalCode
- cultivarNameGroup
- rank
- rankString
- authorTeam
- authorship
- basionymAuthorship
- combinationAuthorship
- year
- basionymFor
- hasBasionym
- typificationString
- typifiedBy
  - typeName
  - typeOfType
  - trypeSpecimen
- hasAnnotation
  - type
  - subjectTaxonName
  - objectTaxonName
  - code
  - ruleConsidered
  - note


### TaxonomicNameUsage

- **taxonConceptLabel**
- accordingTo [[1]](#footnote-1)
- accordingToString
- hasName
- nameString
- circumscribedBy (/DataSet/TaxonConcepts/TaxonConcept/SpecimenCircumscription) [[2]](#footnote-2)
- describedBy (/DataSet/TaxonConcepts/TaxonConcept/CharacterCircumscription) [[2]](#footnote-2)
- hasInformation
- hasRelationship
- primary

### TaxonConceptRelationshipAssertion

- fromTaxon
- relationshipCategory
- toTaxon


<a id="footnote-1">[1]</a> The attribution is really weak in TCS. I would like to have a **Reference** ([dcterms:BibliographicResource](http://dublincore.org/documents/2012/06/14/dcmi-terms/#terms-BibliographicResource)?) class, so that a **TaxonomicNameUsage** is clearly an intersection between a **TaxonomicName** and a **Reference** (I stole some words from Greg's mouth). [NK, 2018-11-10]

<a id="footnote-2">[2]</a> The translation from the TCS *Specimen Circumscription* and *Character Circumscription* is rather poor. I am wondering if anybody ever has used or would use these terms, or that we could leave them out. [NK, 2018-11-10]
