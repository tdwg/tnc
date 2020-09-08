# Use cases

Use cases and/or desiderata of interest to the TNC interest group, for discussion. 
A subset of these are also of specific interest to the TCS 2 task group.

These use cases were initially pulled out of [issue #1](https://github.com/tdwg/tnc/issues/1).  
Subsequent additions came from the 'requirements/use cases' folder in google drive.

## @deepreef, 06 Sep. 2018

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
- What other names are considered as subjective synonyms of a scientific name/what other name is a scientific name considered a subjective synonym of, according to a specified Meta-Authority?
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

### @jgerbracht, 18 Sep. 2018

Some more Use Cases

As a data consolidator.
- Do these 2 pieces of information, from different data providers, refer to the same circumscribed taxon. (Taxonomic Concept)?
- What is the name for this Taxon given an authority/publish date?
- I want to 'discover' and access datasets which unambiguously refer to a specific circumscribed taxon. i.e. H. sapiens which includes neanderthalensis vs excludes neanderthalensis

As a data provider
- Publish taxon related data, such as observations, which are not easily misunderstood or misapplied. i.e. I want to publish my data so that it's difficult to inappropriately consolidate with other datasets based on differing taxon concepts.

As a taxonomy publisher
- I need to 'mint' new Taxon Concept identifiers.
- I need reliable methods to determine if a specific Taxon Concept already exists, so I don't mint duplicates.
- I need to publish the 'Clements' checklist with Taxon Concept identifiers and provide a persistent landing page for TC definitions.
- As Taxon Concepts become obsolete, I need to still provide the basic information of a concept, i.e. TNU and circumscription.

### @jliljeblad, 17 Jun. 2020

#### Problems

Several systems/databases which have been invested in extensively and we do not want to abandon. Some are global and need to be managed in a larger context. Others are regional and have both national funding and cover special national needs (legislation, etc.). How can we continue regionally and at the same time pool our resources and share data, both to humans as well as machines (automatically)?

- XML and RDF as a barrier for not so knowledgeable biologists? CSV is preferred.
- Well defined and finalized standard. Can be strongly validated. Not a moving target.
- Not embraced by major players like GBIF and EOL.

#### General use cases
- Contribute to an Extended Catalogue of Life when building a taxonomic backbone
  - CoL+ project interprets some checklists and builds one taxonomic backbone to which all checklists can be mapped
- Access taxonomic information about “the same” taxon in other systems/databases, both by humans and machines
  - Matching service to find out what is “the same” in different systems/databases
  -	Automate the process as much as possible
  -	Have one or several GSDs pool their data which can then be accessed by a local system
- Access other information about “the same” taxon in other systems/databases, both by humans and machines
  -	Observations/Distribution
  -	Ecology
  -	Morphology and molecules
  -	Conservation: IAS risk assessment, conservation measures
- Management of impact of taxonomic changes on internal systems in the same way?
  -	Observations
  -	Morphology/identification
  -	Media
  -	Ecology/Conservation
  -	Analysis
- Describing properties of a taxon
  -	Hierarchical classification/relationships
  -	Taxon concept circumscription
  -	Nomenclature and nomenclatural acts
  -	Taxonomic status (consensus)
  -	Tracking changes of all of the above properties

#### Real world use cases

- It must be possible to use the standard for both name based and taxon based checklists without any major issues. For the majority (?) of lists the name hasn’t changed, so an identifier based on the name is stable for now.
- Possible to track historical changes using statuses and time stamps.
Not only RCC5 relationships but also add in a directionality. A has been replaced by B, which is otherwise congruent A=B. A and B has been merged into C, which represents an extended concept = includes A and B.

### GBIF Range Map, @jgerbracht, 17 Jun. 2020

Using GBIF data to generate accurate range maps of a species when the people involved are not taxonomic experts.  Somehow, the GBIF datasets (from multiple sources) must include enough information about the taxon for each ‘observation’ so that each GBIF record, regardless of datasource, can be reliably combined with all other records which refer to the exact same circumscribed taxon and be completed accurately by non-taxonomists.  Unfortunately, names are all to commonly used to combine these data.    

Download all GBIF data for _Circus cyaneus_
- Download includes over 31,000 records from eBird which all occur in Europe and Asia and 1 North American record.   
- Download includes over 70,000 records from North America from 608 other datasources.

Use these downloaded data to generate a range map for _Circus cyaneus_

Unless the person creating the maps understands the taxonomic history of which concepts have had the name _Circus cyaneus_ applied to them, they will generate a range map based on the combination of multiple taxonomic concepts believing they are generating a map for a single taxonomic concept.   

To create an ‘accurate’ range utilizing as much of the GBIF data as is appropriate, the person must follow these steps today.  Lets assume the map they wish to create for C. cyaneus is the concept according to the latest IOC checklist. 

1.	Determine what other scientific names have been applied to C. cyaneus
2.	Download GBIF data for all the possible scientific names. 
3.	Determine the authority and authority version for each record downloaded (some can be determined for an entire datasource, others can be different within a datasources and many records may not have this information and need to be removed.  
4.	 For every single authority and authority version (which may be 100s), determine if the concept for each record is congruent to the latest IOC concept.  This step requires a DEEP understanding of every authority and how it has applied names to concepts and how those have changed from version to version.
5.	Remove all records that cannot be accurately applied to the latest IOC concept of C. cyaneus.    
6.	Create the map.  

While this is an obvious case where the taxonomic concepts are so different that the ‘oddity’ in the data should be noticed by non-taxonomists, there are many examples similar to _Circus cyaneus_ where the geographic differences are much more subtle.

### World Flora Online — @WUlate, 18 Jun. 2020

1.  The World Flora Online (WFO) handles a consensus Taxonomy and requires an exchange format that allows them to receive new information on endemic plants from different providers.  For example: the National Species List (NSL) Infrastructure from Australia, the Brazilian Flora 2020, the Catalogue of Madagascar, the Flora de Colombia, etc..

    In this use case, to include them in WFO, Anne provides him with the list of names in endemic Australian families from their National Species List (NSL), currently stored as a set of profiles in the eFlora platform hosted by the Atlas of Living Australia.  The exchange format should consider that some of the names may have a different “usage” than what the World Flora Online could have received already from other sources.  William needs to assign a WFO-ID code (an identifier that is globally unique) to names provided, if this is a “new” taxon, a new WFO-ID should be assigned.  The information associated (authors, taxonomic status, classification, publication) may need to be updated or included for those names.  Eventually, the Taxonomic Expert Network (TEN) that deals with the group of each name will determine its classification and update accordingly.  The list should be sent back to Anne so she can keep the WFO-ID codes assigned, this way the updates are incorporated and not overwritten nor duplicated.


2.  The World Flora Online (William) needs to exchange its consensus Taxonomic Backbone with the Catalogue of Life (Markus) to incorporate it into CoL, so they will eventually distribute it to GBIF preserving, at all times, the reference to the sources of the names, the corresponding IPNI ID(s) and the classification.

3.  William would like to make the species descriptive information from the World Flora Online (WFO) using the Plinian Core unratified TDWG standard (as soon as it gets ratified) which currently borrows terms from the TCS Standard and needs to be updated to use the new (TCS 2.0) corresponding IRIs to update it.

### Use case - ASU BioKIC, @jar398, 18 Jun. 2020

In brief, the Automated Taxonomic Concept Reasoning and Learning (ATCRL) project at the ASU Biodiversity Knowledge Integration Center (BioKIC) is working on tools that operate on alignments between checklists (or between checklists and taxonomies, or between taxonomies). An alignment is essentially a set of RCC-5 articulations between the entries in the respective checklists. The tools generate, reason about, and report on checklist alignments. They therefore require an interchange format for alignments.

The ‘taxon concepts’ in the checklists may be different so the tools use names not to identify taxa, but as partial evidence of some relationship between taxa. Each checklist may have its own way to refer to ‘taxon concepts’, usually some kind of internal identifier with a variety of associated properties including relationships to other ‘taxon concepts’ in the same checklist, as well as names, ranks, data such as geographic range, nomenclatural information, and so on. All these properties provide evidence for or against candidate articulations.

It would be possible for ATCR to invent an idiosyncratic format tuned for use by its tools, but a format with broader community acceptance has a number of advantages. These include a lower documentation burden, a lower education burden on users, and a lower implementation burden on other projects that might want to generate or consume these alignments (‘interoperate’). A standard format will also encourage investment of time and resources by organizations, such as NatureServe, that see themselves as benefiting from using taxonomic concepts but need to demonstrate adherence to general community standards.

We expect that the road toward a complete standard format for alignments will be long, with standard bibliographic references perhaps the most difficult aspect. But much can be done in the absence of a complete standard; we can match ‘taxon concepts’ in many ways other than by having a standard way to refer to them. At worst, articulations can be determined manually, in which case an interchange format to capture these hard-won articulations is that much more important.

TBD: Figure out whether/why TCS 1.0 fails for this application. …

TBD: Figure out whether this use case is covered under the TNC interest group and the nascent task group, or if it is something different

### @afuchs1, 24 Jun. 2020
Use Cases - Australian National Species List

As a data consolidator:

- I want the details of a ‘new’ taxonomic name when it is published including new combinations, authorship of the name, the full bibliographic citation, a link to the digital version of the taxonomic work, nomenclator’s registration number and the nomenclatural status based on the appropriate codes (ICN, ICZN etc), synonyms within the works (including basionyms etc) and types cited.
- I want the details of a revision of a taxon in a taxonomic work, the full bibliographic citation, and synonyms within the works
- In a taxonomic work I would like to extract the understanding of the taxon in comparison to previous taxonomic works (ie. in this work how is it being treated differently)
- For a taxonomic work I would like to identify it is applicable to Australia
- For a taxonomic name I want to know what taxonomic work established that name (protologue)
- For a name in a taxonomic work I want to search BHL and/or publishers to establish a link to the digital version of the work.
- As a repository of Australian taxa I would like to establish links to global respositories or products such as the World Flora Online, Catalogue of Life etc 

As a data publisher:

- I want to deliver a current classification for Australia to occurrence aggregators that includes 
The classification name, classification according to, the version of the classification, citable link to the version, all taxon concepts accepted by this classification within a taxonomic hierarchy
- For each accepted taxon concept within the classification
-- The taxonomic name (with and without authorship), the taxonomic work accepted by this classification,  concepts within the classification and their rank, a citable link to the accepted taxon concept within the classification, a link to the protologue, placement of the taxon concept in the classification, synonyms of the taxonomic name, according to, 
- I want to deliver the differences between one published version of an accepted classification and another so that consumers can apply the differences (WA census requirement)





