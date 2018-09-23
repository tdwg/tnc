# Use cases

Pulled out of issue #1 for starters:

##@deepreef, 06 Sep. 2018

OK, then maybe one way to establish use cases is to enumerate some questions we would like to ask about organisms in nature, specifically related to taxa and their names (starting with the pedantic ones and moving on to more general ones):

**Nomenclature**
- In what publication was a scientific name first established?
- Is a scientific name available/validly published in the sense of the Code?
- Is a scientific name a homonym (either within a Code or across Codes)?
- What spelling variants have been used for a scientific name?
- What objective (Code-governed) synonyms exist for a scientific name?
- Where is the type specimen for a scientific name?

**Taxonomy**
- What other names has a scientific name been regarded as a subjective synonym of?
- What other names have been regarded as a subjective synonym of a given scientific name?
- Is a scientific name considered valid according to a specified Meta-Authority?
- What other names are considered as subjective synonyms of a scientific name/what other name is a scientific name    considered a subjective synonym of, according to a specified Meta-Authority?
- How stable has the subjective synonymy or validity of a scientific name been over time?
- How do the circumscriptions of the same scientific name by two different authorities compare to each other?
- How many type specimens (and of what names) are included within a particular circumscription?
- What other circumscriptions are congruent with/include/are included in/overlap with a particular circumscription?

**Classification**
- What different genera has a species epithet been combined with?
- What parent taxon has a child taxon been included within?
- What child taxa have ever been included within a parent taxon?
- What child taxa are included within a parent taxon according to a specified Meta-Authority?
- How stable has the classification for a given taxon been over time?

**Biodiversity**
- What taxon name is an Organism (specimen/occurrence) currently identified as?
- What taxon names has an Organism ever been identified as?
- What is the currently accepted scientific name of a particular Organism, according to a specified Meta-Authority?
- What Organisms (with their respective occurrence metadata, such as locality, etc.) are currently identified to a scientific name or regarded as falling within a taxon circumscription, according to a specified Meta-Authority?
- [....]

In my mind, use cases involve sets of these questions to allow us to traverse from a given set of inputs to a given set of outputs.  

For example, a use case might be:
- "Give me a list of all species and associated occurrences recorded for a given geographic region, including both the accepted name according to the most recent Catalog of Life, as well as the names that the occurrences are currently identified as."

Another might be:
- "For a given scientific name, let me know what homonyms exist, and for each homonym give me the current status and classification of the name according to different Meta-Authorities, a complete list of all names that have ever been regarded as a synonym (either junior or senior) as well as all known spelling variations and combinations."

To fulfill these use cases, we'd need to be able to answer several of the questions above.

I don't know if this is the right strategy to identify how best to proceed on this discussion and its desired outcome, but it seems to me that enumerating questions of this sort both builds the foundations for addressing Use Cases (or, perhaps, enumerating the Use Cases allow us to figure out what questions we need to answer to fulfill them), and allows us to be more specific about what entities we need to define, and what properties for each entity we need to capture.

#### @jgerbracht, 18 Sep. 2018

Some more Use Cases

As a data consolidator.
- Do these 2 pieces of information, from different data providers, refer to the same Taxonomic Concept?
- What is the name for this Taxon Concept given an authority/publish date?
- I want to 'discover' and access datasets which unambiguously refer to a specific Taxonomic Concept. i.e. H. sapiens which includes neanderthalensis vs excludes neanderthalensis

As a data provider
- Publish taxon related data, such as observations, which are not easily misunderstood or misapplied. i.e. I want to publish my data so that it's difficult to inappropriately consolidate with other datasets based on differing taxon concepts.

As a taxonomy publisher
- I need to 'mint' new Taxon Concept identifiers.
- I need reliable methods to determine if a specific Taxon Concept already exists, so I don't mint duplicates.
- I need to publish the 'Clements' checklist with Taxon Concept identifiers and provide a persistent landing page for TC definitions.
- As Taxon Concepts become obsolete, I need to still provide the basic information of a concept, i.e. TNU and circumscription.
