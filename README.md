# brato
This Ontology hosts trait information from all Brassica Crop Species. Terms are collected from various trials for several international institutions.

Brato will be based on the Crop Ontology Trait Dictionary Version 5.

Related links:
http://www.cropontology.org/
http://brassica.info/

## When adding Traits to BRATO:


### pre-defining BRATO IDs
Identifiers for Variables, Trait, Methods and Scales are made up of the Ontology name, followed by 7 digits, where digits and ontology name are separated by a colon like so:

BRATO:XXXXXXX

The first digit describes the type of Section the ID describes. For example:

- Variables:
BRATO:1XXXXXX
Traits:
BRATO:2XXXXXX
Methods:
BRATO:3XXXXXX
Scale:
BRATO:4XXXXXX

The second digit describes the Institution that submits the ID. For example:

Variables from Inra:
BRATO:10XXXXX
Traits from Inra:
BRATO:20XXXXX
Methods from Earlham Institute:
BRATO:31XXXXX
Scale from Southern Cross University:
BRATO:42XXXXX

The individual Field contents are then numbered increasing right hand digits. For example:

Variable_entry_1 from Inra:
BRATO:10XXXX1
Variable_entry_2 from Inra:
BRATO:10XXXX2
Trait_entry_4 from Earlham Institute:
BRATO:11XXXX4
Method_entry_60 from Southern Cross University:
BRATO:32XXX60
Scale_entry_6 from Southern Cross University:
BRATO:42XXXX6

'X' was only used for explanatory purposes above. Please replace all 'X' with 0 when submitting your IDs of each section to the Trait Dictionary.

#### Scale already exists
If the scale already exists in the spreadsheet, but is derived from a different institution, do reuse it, so as to avoid dublications. For exmaple, if Inra has a Scale ID BRATO:4000005 for percent (%), Earlham Institute or Southern Cross University should reuse this Inra Scale ID, and not follow the above way of pre-defining BRATO IDs.

#### Method already exists
Whether a method is applied to multiple traits in your submission, make sure the ID is the same for all traits with that method.
