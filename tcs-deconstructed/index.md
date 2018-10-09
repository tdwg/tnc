# Index

## [TaxonName](TaxonName.md)

An object that represents a single scientific biological name that either is, or appears to be, governed by one of the biological codes of nomenclature. These are not taxa. Taxa, whether accepted or not, are represented by TaxonConcept objects. Vernacular names are also dealt with under taxon concepts.

Property | Repeatable | Type
-|-|-
id | No | xs:NMToken
[isAnamorphic](TaxonName.md#isanamorphic) | No | xs:boolean
[nomenclaturalCode](TaxonName.md#nomenclaturalcode) | No | [NomenclaturalCodesEnum](NomenclaturalCodeEnum.md)
[Simple](TaxonName.md#simple) | No | xs:string
[Rank](TaxonName.md#rank) | No | [TaxonomicRank](TaxonomicRank)
[CanonicalName](TaxonName.md#canonicalname) | No | [CanonicalName](CanonicalName.md)
[CanonicalAuthorship](TaxonName.md#canonicalauthorship) | No | [CanonicalAuthorship](CanonicalAuthorship/md)
[PublishedIn](TaxonName.md#publishedin) | No | [ReferenceType](ReferenceType.md)
[Year](TaxonName.md#year) | No | xs:gYear
[MicroReference](TaxonName.md#microreference) | No | xs:string
[Typification](TaxonName.md#typification) | No | \[Typification\]
[SpellingCorrectionOf](TaxonName.md#spellingcorrectionof) | Yes | [NomenclaturalNoteType](NomenclaturalNoteType.md)
[Basionym](TaxonName.md#basionym) | No | [NomenclaturalNoteType](NomenclaturalNoteType.md)
[BasedOn](TaxonName.md#basedon) | No | [NomenclaturalNoteType](NomenclaturalNoteType.md)
[ConservedAgainst](TaxonName.md#conservedagainst) | Yes | [NomenclaturalNoteType](NomenclaturalNoteType.md)
[LaterHomonymOf](TaxonName.md#laterhomonymof) | No | [NomenclaturalNoteType](NomenclaturalNoteType.md)
[Sanctioned](TaxonName.md#sanctioned) | No | [NomenclaturalNoteType](NomenclaturalNoteType.md)
[ReplacementNameFor](TaxonName.md#replacementnamefor) | No | [NomenclaturalNoteType](NomenclaturalNoteType.md)
[PublicationStatus](TaxonName.md#publicationstatus) | No | [NomenclaturalNoteType](NomenclaturalNoteType.md)
[ProviderLink](TaxonName.md#providerlink) | No | xs:string
[ProviderSpecificData](TaxonName.md#providerspecificdata) | No | any
