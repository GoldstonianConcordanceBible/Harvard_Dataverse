# Field map (your form → Dataverse native JSON)

Dataverse uses metadataBlocks.citation.fields.

## Title
typeName: title (primitive)

## Author
typeName: author (compound)
- authorName (primitive, required)
- authorAffiliation (primitive, optional)

## Point of Contact
typeName: datasetContact (compound)
- datasetContactName (primitive, required)
- datasetContactEmail (primitive, required)
- datasetContactAffiliation (primitive, optional)

## Description
typeName: dsDescription (compound)
- dsDescriptionValue (primitive, required)
- dsDescriptionDate (primitive, optional)

## Subject
typeName: subject (controlledVocabulary, required)
Use Dataverse’s built-in subject terms.

## Keyword
typeName: keyword (compound, optional)
- keywordValue
- keywordTermURI
- keywordVocabulary
- keywordVocabularyURI

## Related Publication
typeName: publication (compound, optional)
- publicationRelationType
- publicationCitation
- publicationIDType
- publicationIDNumber
- publicationURL

## Notes
typeName: notesText (textbox/primitive)

## Producer
typeName: producer (compound, optional)
- producerName
- producerAffiliation
- producerAbbreviation
- producerURL
- producerLogoURL
