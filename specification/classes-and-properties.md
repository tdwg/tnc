# Classes and properties

### TaxonomicName

[code]
- nomenclaturalCode

[rank]
- rank
- rankString

[composition]
- nameComplete
- uninomial
- genusPart
- infragenericEpithet
- specificEpithet
- infraspecificEpithet
- cultivarNameGroup

[authorship]
- authorTeam
- authorship
- basionymAuthorship
- combinationAuthorship

[year]
- year

[typification]
- typificationString
- typifiedBy
  - typeName
  - typeOfType
  - trypeSpecimen

[name relationships]
- basionymFor
- hasBasionym
- hasAnnotation
  - type
    - SpellingCorrectionOf
    - Basionym
    - BasedOn
    - ConservedAgainst
    - LaterHomonymOf
    - Sanctioned
    - ReplacementNameFor
  - subjectTaxonName
  - objectTaxonName
  - code
  - ruleConsidered
  - note


### TaxonomicNameUsage

[composition]
- **taxonConceptLabel**
- accordingTo [<sup>[1]</sup>](#footnote-1)
- accordingToString
- hasName
- nameString

[type]
- primary

[circumscription] [<sup>[2]</sup>](#footnote-2)
- circumscribedBy (/DataSet/TaxonConcepts/TaxonConcept/SpecimenCircumscription)
- describedBy (/DataSet/TaxonConcepts/TaxonConcept/CharacterCircumscription)

[facts (Berlin Model)]
- hasInformation

[relationships]
- hasRelationship


### TaxonConceptRelationshipAssertion

- fromTaxon
- relationshipCategory
- toTaxon


<a id="footnote-1"><sup>[1]</sup></a> The attribution is really weak in TCS. I would like to have a **Reference** ([dcterms:BibliographicResource](http://dublincore.org/documents/2012/06/14/dcmi-terms/#terms-BibliographicResource)?) class, so that a **TaxonomicNameUsage** is clearly an intersection between a **TaxonomicName** and a **Reference** (I stole some words from Greg's mouth). [NK, 2018-11-10]
* I take back the first bit, as I just noticed the TCS Publication class, so now propose to
  have a Publication class with the ID http://purl.org/dc/terms/BibliographicResource [NK, 2018-11-12]

<a id="footnote-2"><sup>[2]</sup></a> The translation from the TCS *Specimen Circumscription* and *Character Circumscription* is rather poor. I am wondering if anybody ever has used or would use these terms, or that we could leave them out. [NK, 2018-11-10]
