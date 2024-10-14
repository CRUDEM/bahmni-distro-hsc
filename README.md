![alt tag](readme/crudem-hsc-logo.png)

# Hôpital Sacré Coeur distribution

>Hôpital Sacré Coeur (HSC) is the largest private hospital in the North of Haiti. Located in the town of Milot, Haiti the 200 bed hospital has provided uninterrupted service for almost 30 years.
><br>This premier Haitian healthcare facility has been a beacon of hope for the people of Northern Haiti as it creates a healthier Haiti, one dignified life at a time.
><br>
><br>http://crudem.org

-----

This repository maintains the 'distro POM' for the _HSC distribution_.

It downloads and brings in one place all artifacts needed by the distribution, simply run:
```
mvn clean package
```
### Target inventory:

* `bahmni_emr/`
<br/>The target version of the front-end apps that makes 'Bahmni EMR'.
* `bahmni_config/`
<br/>The bespoke Bahmni configuration (more [here](https://github.com/CRUDEM/bahmni-config-hsc)) to be consumed by Bahmni Apps.
* `openmrs_modules/`
<br/>The required set of OpenMRS modules.
* `openmrs_config/`
<br/>The OpenMRS bespoke configuration (more [here](https://github.com/CRUDEM/openmrs-config-hsc)) to be processed by the [Initializer module](https://github.com/mekomsolutions/openmrs-module-initializer).
* `openmrs_core/`
The target version of OpenMRS Core.

## Release Notes

### Version 1.8.2
* Fixed BOM lines in Odoo that caused products not to load
* Reverted Examen physique form to original UUID and ID

### Version 1.8.1
* Updated drugs in the EMR 

### Version 1.8.0
* Added a new section Groupe Antecedants Gynecologiques to Examen Gynecologique form
* Added a new question "Position" to the section "Details du fœtus" of the Consultation Prénatale form
* Changed the date field to a numeric field in "Groupe de contraception > Date" section of the Examen gynécologique form
* Allowed selection of multiple choices for "Groupe de plaintes gynécologiques" question and added three new options to it in the Examen Gynecologique form
* Added new Lab test D-Dimer Exclusion in Bahmni and Odoo
* Updated HSC logo
* Added a slot to pin  patient lists of visit type Médecine Interne
* Added new services to Odoo and Bahmni EMR
* Created a new visit type Post-Natale 
* Updated products in Odoo and drugs in the EMR 
* Added "Examen obstétrical" form for the Pre-Natal clinic
* Made ‘General set’ block mandatory in the Examen des Systemes form
* Added 'None' as an option to the Personal History Set,Family History Set and modified Allergies question to have answers 'Yes' with a text box and 'No' in the Historique de santé form
* Made some fields in the Historique de santé form mandatory
* Made Motif de Consultation form fields mandatory
* Removed Examination field from the Physical Examination form
* Fixed sync issue of Nystatin & Metronidazole 1,000,000units/500mg (Ovule(s)) to Odoo
* Fixed sync issue of Clotrimazole ovule vaginale 500mg (Ovule(s)) to Odoo
* Added SENAITE to Bahmni Docker Compose

### Version 1.7.0
#### Updates
* Added Odoo Sale Delivery Status add-on.
* Added Odoo Sale Payment Status add-on.
#### Fixes
* Fixed  lab test datatypes, from Free Text to Numeric.
* Synced DOB and Patient ID of patients created prior 1.6.0 to Odoo
* Correctly mapped sickle cell and cardiology visit patients to respective patient lists in French locale
* Fixed drug name presentation for multi-ingredient medications

### Version 1.6.1
* Fixed lab tests with changed uuids

### Version 1.6.0
* Fixed error on the HSC Dev clinical app occurred when logged in with FR locale.
* Added missing Metronidazole to EMR.
* Added Widal’s and Zeihl to the Blood sample.
* Added Filariasis to blood sample type
* Added procedures for new maxillofacial surgical procedures.
* Changed Spironolactone 50mg Units to Comprime(s).
* Added consultation 'Odontology' in Odoo.
* Added Direct and Indirect Bilirubin Lab Tests.
* Added Decapuchonnage (Odontology) Service.
* Added Additional Instructions to the quotation line.
* Updated Distro Haiti to use the Most Recent Bahmni Apps.
* Added new chief complaints: Douleur ostéo-articulaire, Suivis diabétique, Suivis HTA, Rendez-vous clinique.
* Added ability to cancel quotations in bulk to Odoo.
* Added ability to display patient weight and DOB on Odoo quotation.
* Disabled Odoo's Quotation default filter.
* Added ability to cancel a quotation when no order line is present anymore.
* Enhanced 'New' vs 'subsequent' MSPP visits to be based on the year of visit.
* Changed materials from consumables to stockable products.
* Added ability to display Patient ID on the quotation, order and invoice.
* Stopped recreation of Manufacturing operation types  (for Pharmacy and Warehouse) at server restart.
* Added Weight on Patient banner.
* Reworked patient registration card printout.
