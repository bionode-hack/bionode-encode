# bionode-encode

Encyclopedia of DNA Elements (ENCODE)
-------------------------------------

Homepage: https://genome.ucsc.edu/ENCODE/

Steps to metadata
-----------------

1: How do I find the set of (human) datasets that are available?

The query:
https://www.encodeproject.org/search/?type=Dataset&replicates.library.biosample.donor.organism.scientific_name=Homo+sapiens&limit=all

results in a page including a table of results. This response had a limit of 50 results: https://github.com/bionode-hack/bionode-encode/blob/master/example_responses/ENCODE_Homo_sapiens.html

2: How do I request information on an individual dataset (or maybe a batch of datasets)?

Extract from each entry just the 'accession' value, e.g. "accession":"ENCSR385UPQ".
Retrieve the URL constructed from this accession number as follows:
https://www.encodeproject.org/experiments/_accession_/
e.g.:
https://www.encodeproject.org/experiments/ENCSR385UPQ/

Result: https://github.com/bionode-hack/bionode-encode/blob/master/example_responses/ENCSR385UPQ.html


3: Where do I find the dataset attributes?

Accession number: Use _accession_

URL: Use the URL constructed above.

Title: From per-dataset result use _Biosample summary_

Description: From per-dataset result use _Description_

Technology: From per-dataset result use _Platform_

Assay type: From per-dataset result use _Assay_