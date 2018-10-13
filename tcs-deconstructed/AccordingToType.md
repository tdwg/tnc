# AccordingToType

Label      | AccordingToType
-----------|-------------------------------------------------------
Definition | Describes the origin of the concept or assertion.

## Properties

### Simple

Label      | Simple
-----------|-------------------------------------------------------
Definition | Unstructured string as used in the data source describing the origin of the concept (e.g. AuthorTeam and year).
Type       | xs:string
Repeatable | No

### AuthorTeam

Label      | AuthorTeam
-----------|-------------------------------------------------------
Definition | This field should contain the authors of the concept. Note that the Simple sub element of this element is a signature field and should have the following content. For TCS signatures two situations are envisaged, one where concepts appear in printed publications and the other where concepts are published on-line. When representing a printed concept the field should contain the unabbreviated surnames of the authors in the order they appear in the publication separated by spaces. Initials and any punctuation marks should be omitted. If there are more than three authors only the first two author names should be included and they should be followed by the words “et al”. The full authorship of the concept will always be available via the PublishedIn element. Transliteration of names should be avoided unless they can't be represented in UTF-8 encoding. If the concept is being published on line, and does not exist in a paper form, then the DNS name of the institution publishing the concept should be used. A policy should be formulated for how many sub-domains should be cited and this should be stuck to. It is recommended that the www sub-domain should not be used (e.g. ipni.org not www.ipni.org). These DNS names are not expected to resolve to anything now or in future and so artificial sub-domains could be created to represent publishing authorities within larger organisation if required. If the concept is version sensitive then the DNS name should be followed by a space and then the versioning information.
Type       | NameCitation
Repeatable | No

### PublishedIn

Label      | PublishedIn
-----------|-------------------------------------------------------
Definition | Reference ID or GUID of the original publication in which the concept or relationship was introduced.
Type       | ReferenceType
Repeatable | No

### MicroReference

Label      | MicroReference
-----------|-------------------------------------------------------
Definition | This is an additional qualification to the reference given by 'PublishedIn'. It for holding things such as "page 34" or "tab. 67" etc.
Type       | xs:string
Repeatable | No
