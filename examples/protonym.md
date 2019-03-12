# Protonym

(continued from [issue #34](https://github.com/tdwg/tnc/issues/34))

**Email from @deepreef, 2019-03-09:**

I’ve been dancing around one subtle point, which I should probably explain.  I’ve said that a Protonym is “almost" the same as dwc:originalNameUsageID – because there is a subtle but important difference.  The definition of dwc:originalNameUsageID is “An identifier for the name usage (documented meaning of the name according to a source) in which the terminal element of the scientificName was originally established under the rules of the associated nomenclaturalCode.”  That was actually the original definition of a Protonym as well – which is why dwc:originalNameUsageID was defined that way.  However, after spending a full day discussing it in great detail, and walking through all the implications, we finally came to the conclusion that a better definition for Protonym was “An identifier for the name usage (documented meaning of the name according to a source) in which the terminal element of the scientificName was originally proposed.”  Note the change of “established” to “proposed”, and the removal of “under the rules of the associated nomenclaturalCode”.  Basically, the Protonym is the "chronologically" first usage of a name, but that is not always the usage that “establishes” the name “under the rules of the associated nomenclaturalCode”.  Under both Codes we have pre-Linnean names that were used prior to 1753/1758, and then later “validated” under the rules of the Codes by Linnaeus. Also, in both Zoology and Botany we have cases where a new name is not Code-compliant when it is first proposed, but is later made available/validly published under the respective Code through a subsequent nomenclatural act.  We have several situations for this in Zoology, and my understanding in botany is that all components of a protologue do not always occur within the same publication (i.e., a name may not be validly published when first proposed because not all required elements of the protologue are included, but a subsequent publication completes the protologue and thereby establishes the name as validly published, with authorship derived from the subsequent publication).

This doesn’t represent a problem for the data model, because as I mentioned before, nomenclatural acts (of all kinds, including completion of the protologue) are another layer on top of TNUs.  We coined the term “Nomenclatual Event” to represent each individual element (e.g., type fixation, Latin diagnosis for older botanical names,  etc.), and the name is considered validly published (or “available” in zoology) when all requirements (Nomenclatural Events) have been fulfilled.  In most cases, all of the requisite Nomenclatural Events will be anchored to the Protonym TNU; but they are technically separate things to accommodate situations where names are first proposed in a form that is not validly published/not available, then later validly published/made available in a subsequent publication.

I will try to illustrate this as best I can in the examples.

Aloha,
Rich


**Email from @nielsklazenga, 2019-03-09:**

I see what you mean. In botany we've got invalidly published name. e.g. without description, which can be validated later. Invalid names, however, are often ignored in treatments. We also have names that are validly published, but are illegitimate, because they are homonyms, so a replacement name with the same type can become the basionym.

I think it is easy to make too much of it as this is a matter of definition and doesn't affect the data model, like you say. In any case, I think it would not be good to have, even slightly, different definitions for 'protonym' and 'originalNameUsage', as one is the literal translation of the other.

I don't care about what is literally the "original" name usage. When I order nomenclatural synonyms (that's what we are really talking about, aren't we?), they go in principle in chronological order, but basionyms go first, also when there are illegitimate names that are older, and invalid names come last of all (if I include them at all). I was taught to do it this way and think it is common practice.

We also have to deal with invalid or illegitimate name usages that are never, or not yet, validated or replaced. I would like a term that I can use for these situations as well. Is your issue that the protonym is not necessarily the first usage of a name, or that there might not necessarily be a legitimate usage.

I think we can come up with a sufficiently broad definition, or sufficient qualifications, that we can use the same term in every scenario (as I had the feeling that was sort of the point of the term). So the first legitimate name usage if there is such a thing or the first or only usage if there is not.

Niels


**Email from @deepreef, 2019-03-09:**

> I see what you mean. In botany we've got invalidly published name. e.g. without description, which can be validated later.
> Invalid names, however, are often ignored in treatments. We also have
> names that are validly published, but are illegitimate, because they are homonyms, so a replacement name with the same type can become the basionym.

The concepts in zoology are the same, we just use different terms (e.g., "validly published" = "available", etc.).  

> I think it is easy to make too much of it as this is a matter of definition and doesn't affect the data model, like you say.

Exactly!

> In any case, I think it would not be good to have, even slightly, different definitions for 'protonym'
> and 'originalNameUsage', as one is the literal translation of the other.

I agree that the literal definitions of the terms are essentially the same, but the actual definitions are different.  For various reasons, we need to keep Protonym as the "first usage of the name", independently of whether that first usage was compliant with the relevant Code(s) [I said "Code(s)" because for ambiregnal names, the first Code-compliant usage for the same name may differ under each Code.]  However, the DwC definition of originalNameUsage already exists, and already locks it in as the first Code-compliant usage (i.e., the one from which authorship is derived).  Both concepts are important to the data model, so I think the best path forward is to maintain them as separate terms, keeping their respective current definitions.

> I don't care about what is literally the "original" name usage.

Most taxonomists don't, but the data model does.  It's important to track names that are not validly published/not available, so that they can be identified as such for future taxonomists.

> When I order nomenclatural synonyms (that's what we are really talking
> about, aren't we?), they go in principle in chronological order, but
> basionyms go first, also when there are illegitimate names that are
> older, and invalid names come last of all (if I include them at all).
> I was taught to do it this way and think it is common practice.

Sure, that's fine.  Different taxonomists follow different conventions in how they present and order lists of synonyms. But how we order them is independent of how we model the information (classes, terms, and relationships among them).

> We also have to deal with invalid or illegitimate name usages that are
> never, or not yet, validated or replaced. I would like a term that I can use for these situations as well.

We can start with the terms "Validly Published"/"available" to distinguish them. Or we can settle on another Code-neutral term.  Does "illegitimate" have a specific meaning within the botanical Code?  Maybe that could be our code-neutral term.

> Is your issue that the protonym is not necessarily the first usage of
> a name, or that there might not necessarily be a legitimate usage.

The latter.  The Protonym is always the first chronological usage, it is usually also the first legitimate (Code-wise) usage, but as discussed, sometimes the Protonym usage does not make the name available/validly published under the respective Code(s).

> I think we can come up with a sufficiently broad definition, or
> sufficient qualifications, that we can use the same term in every
> scenario (as I had the feeling that was sort of the point of the
> term). So the first legitimate name usage if there is such a thing or the first or only usage if there is not.

I think we should adopt Protonym as the first chronological usage (regardless of whether it is the first legitimate usage), and continue to follow the already-established and -defined term dwc:originalNameUsageID to represent the TNU that first makes the name available/validly published under the relevant Code(s).  It is slightly confusing, but I fear it will be more confusing if we change the already-existing definition for dwc:originalNameUsageID, or create yet another new term.

Aloha,
Rich


**Email from @nielsklazenga, 2019-03-11:**

Hi Rich,
I am trying to understand why it is so important that the protonym is the first name usage, rather than the first legitimate usage. I think a real-life example might help, as it could be that we are talking about two different things (like we were with the homotypic and heterotypic synonyms). Will try to find one.

The word 'illegitimate' does have a specific meaning in the botanical code, but that might be the exact meaning you are looking for (I don't know). Illegitimate names are names that are validly published, but are illegitimate, because they either are homonyms (there are lots of those in fungi, I've discovered) or superfluous, because they include the type (or all the type material) of a prior name. For superfluous names the abbreviation 'nom. superfl.' is often used. There is no such abbreviation for homonyms, so they get the 'nom. illeg.' Abbreviation. Both are, however, illegitimate under the Code. The Code distinguishes between legitimate and illegitimate names; invalid names are considered not to be covered under the Code.

We don't use the term 'available' in the Code, but there is a use for 'unavailable'. This is used for names that have become de facto illegitimate, because a younger name has been sanctioned. Sanctioning is done for fungi names that have been treated in four works by two authors (Fries and Persoon, for different groups of fungi). For mosses, we have a similar work, but that covered all mosses, except Sphagnum, at the time, so for mosses, except Sphagnum, we use a later starting date, 1801; everything published before that is invalidly published.

Niels


**Email from @deepreef, 2019-03-12:**

Hi Niels,

> Hi Rich,
> I am trying to understand why it is so important that the protonym is
> the first name usage, rather than the first legitimate usage. I think
> a real-life example might help, as it could be that we are talking
> about two different things (like we were with the homotypic and heterotypic synonyms). Will try to find one.

Yeah, we debated this early on, as to whether the "Protonym" should be defined as the first Code-compliant usage of a name, or the first chronological usage of a name (independent of whether or not it is Code-compliant).  We spent an entire day on this topic at one of the NOMINA meetings, and somewhere I have a photograph of a whiteboard containing all the diagrams and points accumulated over the day that led to the decision to define it as the chronologically first usage.

I don't recall all of the reasons off-hand, but here are a few of the main ones:

1) The logic of Protonym in the TNU data model is that the Protonym is either self-referential, or links to a *previous* TNU to represent a re-use of a pre-existing name.  I know we in the Code business refer to names that are not validly published/available as though they "do not exist", the reality is that they DO exist (within publications and manuscripts and specimen identifications, etc.) -- and as such we need to track them (if for no other reason than to brand them as not validly published/available, so that future workers understand their status).  But the point is, the logic is that when a TNU proposes or uses a name for the very first time, it is "the first ... thing of a certain name; something from which another ... thing takes its name" (OED definition of Protonym).  The key here is "first". So, every TNU must either itself *be* a Protonym, or refer to an *existing* Protonym -- in order for it to exist, it must have been in the past.  A newly created TNU cannot refer to a Protonym that does not exist yet. There is much more to this point that would require paragraphs to describe, but logically the information flows chronologically.  Whether or not a particular Protonym represents a Code-compliant new name is a separate question, which needs a different layer of information to ascertain (see below).

2) Many TNUs contain nomenclatural acts -- not just the ones that represent Code-compliant establishment of new names.  Therefore, we already need the ability to layer a system of branding TNUs as a "Nomenclatural Act" on top of the TNUs instances.  The model designed what we call "Nomenclatural Event" -- which are the individual components that make up a Code-compliant act.  In any case, the point is, this structure made much more sense as a place to flag TNUs representing the first Code-compliant usage of a name, rather than defining Protonym in this way, because Protonym is fundamental to ALL Taxon Name Usages, regardless of whether they conform to ruels of a particular Code.

3) In some cases, it's not immediately obvious whether a new name is Code-compliant.  Sometimes a new name is proposed, then others follow this name, then a few years later someone takes a close look and realizes that the original usage wasn't Code compliant, so a reviser needs to do something to make it Code compliant.  By that time, we've already indexed the Protonym and subsequent TNUs, and it would create problems if the Protonym needed to change to the later reviser TNU.

There are other reasons (some more subtle), but for me the key is Protonym="first", regardless of whether it happens to conform to a particular Code of nomenclature.  Then we need another layer to capture the myriad nomenclatural acts that TNUs (Protonyms and otherwise) confer.

As for legitimate, available, etc., this is a very useful guide for mapping the different terms used in the three major Codes:
https://books.google.com/books?hl=en&lr=&id=Qky7_6-UcQQC

My copy happens to be boxed up right now, but this would be very useful to consult when we're trying to find neutral terminology for TCN.

Aloha,
Rich


**Email from @nielsklazenga, 2019-03-12:**

Thanks Rich,

I get it now. I'll find some examples. Would be good to get some examples that are not of Dicranoloma.

I see that the Hawksworth book has useful definitions for both 'protonym' and 'misapplied name'. Actually, the 'protonym' definition is quite different from what we are talking about here.

Niels


**Email from @deepreef, 2019-03-12:**

Yeah, the word "Protonym" was originally coined for a purpose in fungal names, but Paul Kirk strongly encouraged me to ignore that existing definition because the term never really caught on in that context.  Since then, Protonym has taken hold in the biodiversity informatics community in the way I've defined it, so I think we're OK keeping with that.
