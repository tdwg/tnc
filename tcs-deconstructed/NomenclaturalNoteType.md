# NomenclaturalNoteType

Label      | NomenclaturalNoteType
-----------|-------------------------------------------------------
Definition | A base object that defines a common structure for a number of elements within TaxonName.


## Properties

### RuleConsidered

Label      | RuleConsidered
-----------|-------------------------------------------------------
Definition | The article/note/recommendation in the code in question that is commented on below
Type       | xs:string
Repeatable | No

### Note

Label      | Note
-----------|-------------------------------------------------------
Definition | Comment concerning this name.
Type       | xs:string
Repeatable | No

### RelatedName

Label      | RelatedName
-----------|-------------------------------------------------------
Definition | If status is conservation, the rejected name and vice versa, if illegitimate because homonym the earlier homonym, etc.
Type       | ReferenceType
Repeatable | No

### PublishedIn

Label      | PublishedIn
-----------|-------------------------------------------------------
Definition | The publication/reference source used to determine the nomenclatural status.
Type       | ReferenceType
Repeatable | No

### MicroReference

Label      | MicroReference
-----------|-------------------------------------------------------
Definition | Specifies any minor reference parts connected to the According to publication e.g. page number.
Type       | xs:string
Repeatable | No
