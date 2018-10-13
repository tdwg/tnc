# CanonicalName

Label      | CanonicalName
-----------|-------------------------------------------------------
Definition | Canonical name enforcing strict inclusion of only nomenclatural information - _not_ taxonomic information with the exception of the necessary placements within Genus or Species.

## Properties

### Simple

Label      | Simple
-----------|-------------------------------------------------------
Definition | A label containing the canonical name without authors. For the purposes of a TCS signature this field should contain nothing but the text strings representing the name itself with no indication of rank or any other qualifiers.
Type       | xs:string
Repeatable | No

### Uninomial

Label      | Uninomial
-----------|-------------------------------------------------------
Definition | Family, genus, infrafamilial or suprafamilial name
Type       | xs:string
Repeatable | No

### Genus

Label      | Genus
-----------|-------------------------------------------------------
Definition | The name of the genus. If this name is below the rank of genus then this may also be reference to a TaxonName that contains the name of the genus.
Type       | [ReferenceType](ReferenceType.md)
Repeatable | No

### InfragenericEpithet

Label      | InfragenericEpithet
-----------|-------------------------------------------------------
Type       | xs:string
Repeatable | No

### SpecificEpithet

Label      | SpecificEpithet
-----------|-------------------------------------------------------
Definition | The specific epithet for the name. If this is subspecific taxon then this may be a link to another TaxonName that contains the species.
Type       | xs:string
Repeatable | No

### InfraspecificEpithet

Label      | InfraspecificEpithet
-----------|-------------------------------------------------------
Type       | xs:string
Repeatable | No

### CultivarNameGroup

Label      | CultivarNameGroup
-----------|-------------------------------------------------------
Definition | The name of the Cultivar, Cultivar Group, grex, convar or graft chimera. Under the ICNCP. Just include here the string of the name. i.e. omit the single quotes around cultivar names, the word Group that denotes cultivar group and the + sign used in chimeras. These symbols can be added in later on the basis of the rank of the name. The user of Group for example is language dependant.
Type       | xs:string
Repeatable | No
