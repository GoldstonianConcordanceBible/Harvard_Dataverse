# Dataverse deposit pack — Goldstonian Concordance Bible (Series I)

This folder contains Dataverse "native JSON" metadata files for each Series I volume (6 datasets).

## What Dataverse requires (minimum)
Dataverse requires, at minimum:
- Title
- Author Name
- Point of Contact Email
- Description Text
- Subject
(These are in the "citation" metadata block.)  See Dataverse Native API docs. 

## How to use (API)
1) Get your Dataverse collection alias (e.g., "root" or your collection alias).
2) (Optional) download/validate against the collection schema:
   GET /api/dataverses/{alias}/datasetSchema
3) Create the dataset:
   POST /api/dataverses/{alias}/datasets
   with Content-type: application/json and --upload-file dataset.json

Example curl (edit SERVER_URL, API_TOKEN, and PARENT alias):
curl -H "X-Dataverse-key:$API_TOKEN" -X POST "$SERVER_URL/api/dataverses/$PARENT/datasets" \
  --upload-file series-I-vol-01/dataset.json -H 'Content-type:application/json'

## Notes
- License is set to CC0 1.0 by default; change if desired.
- Update placeholders in volumes 02–06 (title/description/date/keywords) as you finalize the book metadata.
