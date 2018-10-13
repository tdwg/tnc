# TaxonConcept

Label      | TaxonConcept
-----------|-------------------------------------------------------
Definition | Representation of a TaxonConcept. Various types of concept can be represented, including a reference to the GUID of an existing Concept.

## Properties

### id

Label      | id
-----------|-------------------------------------------------------
Definition | Unique identifier (key) of the element. It can be local to the data set or a GUID in which case it can be resolved to a location on the internet where the record is stored.
Type       | xs:token
Repeatable | No

### type

Label      | type
-----------|-------------------------------------------------------
Definition | The optional enumerated type of the Concept may reflect which data elements are provided.
Type       | xs:string
Repeatable | No
Vocabulary | original &#124; revision &#124; incomplete &#124; aggregate &#124; nominal

### primary

Label      | primary
-----------|-------------------------------------------------------
Definition | If primary='true' the concept is the first level response to a query. If 'false' the concept may be a secondary concept linked directly or indirectly to the definition of a primary concept.
Type       | xs:boolean
Repeatable | No

### form

Label      | form
-----------|-------------------------------------------------------
Definition | Flag as to sexual form or parentage. List of options may extend in future but are mutually exclusive.
Type       | xs:string
Repeatable | No
Vocabulary | anamorph &#124; teleomorph &#124; hybrid

### Name

Label      | Name
-----------|-------------------------------------------------------
Definition | A non-unique handle to the concept. This can represent the name as published.
Type       | ReferenceType
Repeatable | No

### Rank

Label      | Rank
-----------|-------------------------------------------------------
Definition | The taxonomic rank of this concept. Either as a string or as a code for a recognise rank or both.
Type       | [TaxonomicRank](TaxonomicRank.md)
Repeatable | No

### AccordingTo

Label      | AccordingTo
-----------|-------------------------------------------------------
Definition | Information about the authorship of this concept which uses the Name in their sense (i.e. secundum, sensu).
Type       | [AccordingToType](AccordingToType.md)
Repeatable | No

### TaxonRelationship

Label      | TaxonRelationship
-----------|-------------------------------------------------------
Definition | Stores explicit, taxonomic and nomenclatural relationships that are part of the original concept definition.
Type       | TaxonRelationship
Repeatable | Yes

* TaxonRelationship
  * @type
  * ToTaxonConcept

### SpecimenCircumscription

Label      | SpecimenCircumscription
-----------|-------------------------------------------------------
Definition | A set of specimens that are used to define the concept.
Type       | ReferenceType
Repeatable | Yes

### CharacterCircumscription

Label      | CharacterCircumscription
-----------|-------------------------------------------------------
Definition | A set of taxonomic descriptions used to define this concept. May potentially hold descriptions according to the TDWG SDD schema, or any other, format.
Type       | PlaceholderType
Repeatable | Yes

### ProviderLink

Label      | Name
-----------|-------------------------------------------------------
Type       | xs:string
Repeatable | No

### ProviderSpecificData

Label      | ProviderSpecificData
-----------|-------------------------------------------------------
Definition | Mechanism to allow for the extension of the schema for specific applications.
Type       | PlaceholderType
Repeatable | No
