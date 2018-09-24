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