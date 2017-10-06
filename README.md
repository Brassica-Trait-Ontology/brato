# Brassica Trait Ontology (BraTO)
This Ontology hosts trait information from all Brassica Crop Species. Terms are collected from various trials for several international institutions.

BRATO will be based on the Crop Ontology Trait Dictionary Version 5.

Related links:

http://www.cropontology.org/

http://brassica.info/

## When adding Traits to BRATO:


### pre-defining BRATO IDs
Identifiers for Variables, Trait, Methods and Scales are made up of the Ontology code given by CropOntology.org (CO_348), followed by 7 digits, where digits and ontology code are separated by a colon like so:

CO_348:XXXXXXX

The **first digit** describes the type of **Section** the ID describes. For example:

| Variables       | Traits      |Methods  |  Scale |
| --------------- |:-----------:| -------:|-------:|
| CO_348:1XXXXXX  | CO_348:2XXXXXX |CO_348:3XXXXXX |CO_348:4XXXXXX|


The **second digit** describes the **Institution** that submits the ID. For example:

|---| Variables       | Traits      |Methods  |  Scale |
|---| ------------  |:------------:| -----:|-----:|
|**Inra => 0**|CO_348:10XXXXX  | CO_348:20XXXXX |CO_348:30XXXXX |CO_348:40XXXXX|
|**Earlham Institute => 1**| CO_348:11XXXXX   | CO_348:21XXXXX |CO_348:31XXXXX |CO_348:41XXXXX|
|**Southern Cross => 2**|CO_348:12XXXXX   | CO_348:22XXXXX |CO_348:32XXXXX |CO_348:42XXXXX|


The **individual entries** are then numbered **increasing right hand digits**. For example:

* Variable_entry_1 from Inra:
CO_348:1000001
* Variable_entry_2 from Inra:
CO_348:1000002
* Trait_entry_4 from Earlham Institute:
CO_348:2100004
* Method_entry_60 from Southern Cross University:
CO_348:3200060
* Scale_entry_6 from Southern Cross University:
CO_348:4200006

*Note* 'X' was only used for explanatory purposes above. Please replace all 'X' with 0 when submitting your IDs of each section to the Trait Dictionary.

### What if...?

#### Scale already exists
If the scale already exists in an international ontology, do reuse it, by refering to the international ID (cf. https://www.ebi.ac.uk/ols/ontologies/uo)
If the scale already exists in the spreadsheet, but is derived from a different institution, do reuse it, so as to avoid dublications. For example, if Inra has a Scale ID CO_348:4000005 for percent (%), Earlham Institute or Southern Cross University should reuse this Inra Scale ID, and not follow the above way of pre-defining BRATO IDs.

#### Method already exists
Whether a method is applied to multiple traits in your submission, make sure the ID is the same for all traits with that method.


### Mini Commit Ontology

For better navigation of the commit messages, we agreed to use a three-element-description in the commits related to the ontology document:

1) `[institute name ] -> [Earlham Institute] [Inra] [Southern Cross]` 

2) Followed by some small info on what is done; suggested elements for that are `[add traits] [update] [edit]` and whatever is reasonnable and reusable.

3) followed by any free text description of what you did . 

Here some example commits already existing:

git commit -m "`[Earlham Institute] [add traits]` next batch of RIPR traits"
git commit -m "`[Earlham Institute] [update]` method and Scale IDs"
git commit -m "`[Inra] [edit Trait IDs]` corrected IDs based on 1st BRATO version and agreed naming convention"
