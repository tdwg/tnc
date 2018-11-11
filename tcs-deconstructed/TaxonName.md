# TaxonName

Label      | TaxonName
-----------|-------------------------------------------------------
Definition | An object that represents a single scientific biological name that either is, or appears to be, governed by one of the biological codes of nomenclature. These are not taxa. Taxa, whether accepted or not, are represented by TaxonConcept objects. Vernacular names are also dealt with under taxon concepts.

## Properties

### id

Label      | id
-----------|-------------------------------------------------------
Type       | xs:NMToken
Repeatable | No

### isAnamorphic

Label      | isAnamorphic
-----------|-------------------------------------------------------
Definition | Some fungal names under ICBN are termed anamorphic. This is because they have asexual types and aren't available for use for teleomorphic or holomorphic taxa. Use this flag to indicate that the name is anamorphic.
Type       | xs:boolean
Repeatable | No

### nomenclaturalCode

Label      | nomenclaturalCode
-----------|-------------------------------------------------------
Definition | The nomenclatural code that governs the construction and use of this name. This is a TCS signature field.
Type       | [NomenclaturalCodesEnum](NomenclaturalCodesEnum.md)
Repeatable | No

### Simple

Label      | Simple
-----------|-------------------------------------------------------
Definition | A full (non-atomized) name, including nomenclatural citation (authors/year in the form mandated by the relevant code). The name should be normalized (removing optional infrageneric or infraspecific hierarchy, author given only for the lowest nomenclatural rank) human readable and unique representation of the nomenclatoral name object. Where available, this should be generated from the canonical name and authorship plus Name extensions. In combination with the ID this constitutes the lowest abstraction a of name. Any other information is optional.
Type       | xs:string
Repeatable | No

### Rank

Label      | Rank
-----------|-------------------------------------------------------
Definition | The taxonomic rank of this name. Either as a string or as a code for a recognise rank or both. The code attribute is a TCS signature field.
Type       | [TaxonomicRank](TaxonomicRank)

### CanonicalName

Label      | CanonicalName
-----------|-------------------------------------------------------
Definition | Canonical name enforcing strict inclusion of only nomenclatural information - _not_ taxonomic information with the exception of the necessary placements within Genus or Species.
Type       | [CanonicalName](CanonicalName.md)

### CanonicalAuthorship

Label      | CanonicalAuthorship
-----------|-------------------------------------------------------
Definition | Authorship of the name, optionally atomized.
Type       | [CanonicalAuthorship](CanonicalAuthorship/md)

### Year

Label      | Year
-----------|-------------------------------------------------------
Definition | The year of publication of the name as it would appear in the publication. This is the publication year for THIS name combination not for the basionym should this be a comb nov. This is a TCS signature field.
Type       | xs:gYear

### MicroReference

Label      | MicroReference
-----------|-------------------------------------------------------
Definition | Specifies any minor reference parts connected to the name publication e.g. page number.
Type       | xs:string

### Typification

Label      | Typification
-----------|---------------------------------------------------------
Definition | -
Type       | [\[Typification\]](Typification.md)
Repeatable | No


### SpellingCorrectionOf

Label      | SpellingCorrectionOf
-----------|-------------------------------------------------------
Definition | The current name is a spelling correction of the name that is pointed to.
Type       | [NomenclaturalNoteType](NomenclaturalNoteType.md)
Repeatable | Yes

### Basionym

Label      | Basionym
-----------|-------------------------------------------------------
Definition | The current name is a recombination (comb nov) of the name pointed to and the name pointed to is not, itself, a recombination.
Type       | [NomenclaturalNoteType](NomenclaturalNoteType.md)
Repeatable | No

### BasedOn

Label      | BasedOn
-----------|-------------------------------------------------------
Definition | The current name is the validation of a that was not fully published before. Covers the use of ex in botanical author strings. ICBN Art. 46.4: e.g. if this name object represents G. tomentosum Nutt. ex Seem. then the pointer should point to G. tomentosum Nutt.
Type       | [NomenclaturalNoteType](NomenclaturalNoteType.md)
Repeatable | No

### ConservedAgainst

Label      | ConservedAgainst
-----------|-------------------------------------------------------
Definition | The current name is conserved against the name pointed to. ICBN: Conservation is covered under Article 14 and Appendix II and Appendix III (this name is nomina conservanda). ICZN: Conservation is covered under Article 23.9 (this name is nomen protectum and the target name is nomen oblitum).
Type       | [NomenclaturalNoteType](NomenclaturalNoteType.md)
Repeatable | Yes

### LaterHomonymOf

Label      | LaterHomonymOf
-----------|-------------------------------------------------------
Definition | Current name has same spelling as target name but was published later and has priority over it (unless conserved or sanctioned). See ICBN: Article 53, ICZN: Chapter 12, Article 52.
Type       | [NomenclaturalNoteType](NomenclaturalNoteType.md)
Repeatable | No

### Sanctioned

Label      | Sanctioned
-----------|-------------------------------------------------------
Definition | With reference to fungi. ICBN: Articles 13.1d and 15. ICZN: No equivalent term for animals.
Type       | [NomenclaturalNoteType](NomenclaturalNoteType.md)
Repeatable | No

### ReplacementNameFor

Label      | ReplacementNameFor
-----------|-------------------------------------------------------
Definition | Current name is replacement for target name. Also called 'Nomen Novum' or 'avowed substitute' ICBN: Article 7.3 ICZN: Article 60.3.
Type       | [NomenclaturalNoteType](NomenclaturalNoteType.md)
Repeatable | No

### PublicationStatus

Label      | PublicationStatus
-----------|-------------------------------------------------------
Definition | Note concerning the publication status of the name. e.g. whether it is validly published. THIS SHOULD NOT BE USED TO IMPLY WHETHER THE NAME IS CONSIDERED TO REPRESENT AN ACCEPTED TAXON. An accepted taxon can only be represented as a TaxonConcept.
Type       | [NomenclaturalNoteType](NomenclaturalNoteType.md)
Repeatable | No

### ProviderLink

Label      | ProviderLink
-----------|-------------------------------------------------------
Type | xs:string

### ProviderSpecificData

Label      | ProviderSpecificData
-----------|-------------------------------------------------------
Definition | Mechanism to allow for the extension of the schema for specific applications.
