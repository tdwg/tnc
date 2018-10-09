### Specimen

Label      | Specimen
-----------|-------------------------------------------------------
Type       | Class
Definition | Specimen and location                                              

### Publication

Label      | Publication
-----------|-------------------------------------------------------
Type       | Class
Definition | Details of the data source




### TaxonConcept

Label      | TaxonConcept
-----------|-------------------------------------------------------
Type       | Class
Definition | Representation of a TaxonConcept. Various types of concept can be represented, including a reference to the GUID of an existing Concept.

#### id

Label      | id
-----------|-------------------------------------------------------
Type       | Property (attribute)
Definition | Unique identifier (key) of the element. It can be local to the data set or a GUID in which case it can be resolved to a location on the internet where the record is stored.



#### type
- **Type**: attribute
- **Definition**: The optional enumerated type of the Concept may reflect which data elements are provided.
- **Vocabulary**: original  | revision | incomplete | aggregate | nominal

Label      | type
-----------|-------------------------------------------------------
Type       | Property (attribute)
Definition | The optional enumerated type of the Concept may reflect which data elements are provided.
Vocabulary | original  &#124; revision &#124; incomplete &#124; aggregate &#124; nominal

#### form

Label      | form
-----------|-------------------------------------------------------
Type       | Property (attribute)
Definition | Flag as to sexual form or parentage. List of options may extend in future but are mutually exclusive.
Vocabulary | anamorph &#124; teleomorph &#124; hybrid

#### Name

Label      | Name
-----------|-------------------------------------------------------
Type       | Property
Definition | A non-unique handle to the concept. This can represent the name as published.


#### TaxonRelationships

Label      | TaxonRelationships
-----------|-------------------------------------------------------
Type       | Property
Definition | Container for taxonomic assertion records.


### TaxonRelationshipAssertion

Label      | TaxonRelationshipAssertion
-----------|-------------------------------------------------------
Type       | Class
Definition | Relationships between two concepts which are not part of the original definition of either of these concepts; possibly by a third party.

#### RelationshipType

Label      | RelationshipType
-----------|-------------------------------------------------------
Type       | Property
Definition | Any of an enumerated list of possible taxonomic relationships that may be expressed between two TaxonConcepts.

#### RelationshipTypeVocabulary

Term       | Definition
-----------|-------------------------------------------------------
is congruent to     | Set Relationship: The extent of Concept 1 is (essentially) identical to Concept 2
is not congruent to | Set Relationship: The extent of Concept 1 is not identical to Concept 2.
includes            | Set Relationship: Concept 2 is a subset of Concept 1.
does not include    | Set Relationship: Concept 2 is not a subset of Concept 1.
excludes            | Set Relationship: Concept 1 does not overlap or include Concept 2.
is included in      | Set Relationship: Concept 1 is a subset of Concept 2.
is not included in  | Set Relationship: Concept 1 is not a subset of Concept 2.
overlaps            | Set Relationship: Concepts 1 and 2 share members/children in common.
does not overlap    | Set Relationship: Concepts 1 and 2 have no members/children in common.
|
is child taxon of   | Hierarchical Relationship: Concept 1 is a member of lower taxonomic rank of Concept 2.
is parent taxon of  | Hierarchical Relationship: Taxon Concept 1 includes Concept 2 as a lower-ranked member.
|
is anamorph of      | Concept 1 is the asexual or mitotic reproductive stage in a pleomorphic life cycle in which Concept 2 is the teleomorph or meiotic reproductive stage.
is teleomorph of    | Concept 1 is the teleomorph or meiotic reproductive stage in a pleomorphic life cycle in which Concept 2 is the asexual or mitotic reproductive stage.
|
is second parent of | Hybrid Relationship: Concept 1 is genetic parent (2) of Concept 2.
is female parent of | Hybrid Relationship: Concept 1 is genetic mother of Concept 2.
is first parent of  | Hybrid Relationship: Concept 1 is genetic parent (1) of Concept 2.
is male parent of   | Hybrid Relationship: Concept 1 is genetic father of Concept 2.
is hybrid parent of | Hybrid Relationship: Concept 1 is genetic parent of Concept 2.
is hybrid child of  | Hybrid Relationship: Concept 2 is a genetic parent of Concept 1.
|
is ambiregnal of    | Concepts have only a single scientific name. This name is governed by a single nomenclatural code. If an organism falls into two codes (not a desirable or frequent situation) then two TaxonConcepts should be created and linked with this relationship. e.g. a concept for the organism as an animal and a concept of it as a plant. It is unlikely this will be widely used as a taxonomist would typically have a single view of which kingdom a organism is in. Also note that ambiregnal is used to imply different nomenclatural codes but there is not a precise relationship between codes and kingdoms.
|
is vernacular for   | The current concept is used as a vernacular concept, at least in part, for the target concept. This kind of relationship should not be used to express any form of set relationship (e.g. overlaps, is congruent with, includes). Consider using vernacular type relationships along with set type relationships to avoid any ambiguity.
has vernacular | The target concept is used as a vernacular concept, at least in part, for the current concept. This kind of relationship should not be used to express any form of set relationship (e.g. overlaps, is congruent with, includes). Consider using vernacular type relationships along with set type relationships to avoid any ambiguity.
|
has synonym         | The target concept is considered a synonym of the current concept. This is an ambiguous relationship. It can mean: 1) a nomenclatural relationship where all that is implied is that the type of the target concept is included in the current circumscription. This is more precisely expressed as a SpecimenCircumscription (for heterotypic synonyms) or as TaxonName basionym relationships (for homotypic synonyms) 2) a concept relationship where some part of (or all of) the target concept is included in the current circumscription. This is more precisely expressed using the set relationships such as 'is congruent to'. This is intended for handling legacy data.


#### FromTaxonConcept

Label      | FromTaxonConcept
-----------|-------------------------------------------------------
Type       | Property
Definition | Starting point of the directed relationship. A reference to a TaxonConcept.

#### ToTaxonConcept

Label      | ToTaxonConcept
-----------|-------------------------------------------------------
Type       | Property
Definition | End point of the directed relationship. A reference to a TaxonConcept.

#### AccordingTo

Label      | AccordingTo
-----------|-------------------------------------------------------
Type       | Property
Definition | Information about the authorship of the asserted relationship.
