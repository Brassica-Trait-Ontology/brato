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

The **first digit** describes the type of **Section** the ID describes. For example:

| Variables       | Traits      |Methods  |  Scale |
| ------------  |:------------:| -----:|-----:|
| BRATO:1XXXXXX   | BRATO:2XXXXXX |BRATO:3XXXXXX |BRATO:4XXXXXX|




The **second digit** describes the **Institution** that submits the ID. For example:


|---| Variables       | Traits      |Methods  |  Scale |
|---| ------------  |:------------:| -----:|-----:|
|**Inra**|BRATO:10XXXXX   | BRATO:20XXXXX |BRATO:30XXXXX |BRATO:40XXXXX|
|**Earlham Institute**| BRATO:11XXXXX   | BRATO:21XXXXX |BRATO:31XXXXX |BRATO:41XXXXX|
|**Southern Cross**|BRATO:12XXXXX   | BRATO:22XXXXX |BRATO:32XXXXX |BRATO:42XXXXX|




The **individual entries** are then numbered **increasing right hand digits**. For example:

* Variable_entry_1 from Inra:
BRATO:10XXXX1
* Variable_entry_2 from Inra:
BRATO:10XXXX2
* Trait_entry_4 from Earlham Institute:
BRATO:11XXXX4
* Method_entry_60 from Southern Cross University:
BRATO:32XXX60
* Scale_entry_6 from Southern Cross University:
BRATO:42XXXX6

*Note* 'X' was only used for explanatory purposes above. Please replace all 'X' with 0 when submitting your IDs of each section to the Trait Dictionary.

### What if...?

#### Scale already exists
If the scale already exists in the spreadsheet, but is derived from a different institution, do reuse it, so as to avoid dublications. For exmaple, if Inra has a Scale ID BRATO:4000005 for percent (%), Earlham Institute or Southern Cross University should reuse this Inra Scale ID, and not follow the above way of pre-defining BRATO IDs.

#### Method already exists
Whether a method is applied to multiple traits in your submission, make sure the ID is the same for all traits with that method.


### Mini Commit Ontology

For better navigation of the commit messages, we agreed to use a three-element-description in the commits related to the ontology document:

1) `[institute name ] -> [Earlham Institute] [Inra] [Southern Cross]` 

2) Followed by some small info on what is done suggested elements for that are `[add traits] [update]  [edit]` and whatever is reasonnable and reusable.

3) followed by any free text description of what you did . 

Here some example commits already existing:

git commit -m "`[Earlham Institute] [add traits]` next batch of RIPR traits"
git commit -m "`[Earlham Institute] [update]` method and Scale IDs"
git commit -m "`[Inra] [edit Trait IDs]` corrected IDs based on 1st BRATO version and agreed naming convention"
