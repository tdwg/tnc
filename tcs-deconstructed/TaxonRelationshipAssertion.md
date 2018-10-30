# TaxonRelationshipAssertions

Label      | TaxonRElationshipAssertion
-----------|-------------------------------------------------------
Definition | Relationships between two concepts which are not part of the original definition of either of these concepts; possibly by a third party.

## properties

### type

Label      | type
-----------|-------------------------------------------------------
Definition | Any of an enumerated list of possible taxonomic relationships that may be expressed between two TaxonConcepts.
Type       | xs:string ([\[RelationshipTypeEnum\]](RelationshipTypeEnum.md))

### id

Label      | id
-----------|-------------------------------------------------------
Definition | Unique identifier (key) of the element. It can be local to the data set or a GUID in which case it can be resolved to a location on the internet where the record is stored.
Type       | xs:token

### AccordingTo

Label      | AccordingTo
-----------|-------------------------------------------------------
Definition | Information about the authorship of the asserted relationship.
Type       | [AccordingToType](AccordingToType.md)

### FromTaxonConcept

Label      | FromTaxonConcept
-----------|-------------------------------------------------------
Definition | Starting point of the directed relationship. A reference to a TaxonConcept.
Type       | ReferenceType

### ToTaxonConcept

Label      | ToTaxonConcept
-----------|-------------------------------------------------------
Definition | End point of the directed relationship. A reference to a TaxonConcept.
Type       | ReferenceType
