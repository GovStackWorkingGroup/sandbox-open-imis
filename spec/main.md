# [openIMIS](https://github.com/openimis) 

Minimum set of components:

* Database
* Backend
* Gateway

## [Database](https://github.com/openimis/database_postgresql) 

Backend expects database with predefine schema and data.

To get DB with particular state needs to use
[Helm chart](https://github.com/GovStackWorkingGroup/sandbox-open-imis/blob/9d5f4f907d5acbbfe4ecd4bf6194de711e2f1a09/sandbox-open-imis/charts/db/templates/db.yaml) based on specific snapshot. 

Predefined DB [backup](https://github.com/GovStackWorkingGroup/sandbox-open-imis/tree/main/backup) can be helpful. 

## [Backend](https://github.com/openimis/openimis-be_py.git)

Backend expects communication via Gateway component.

### API

OpenIMIS uses [FHIR](https://en.wikipedia.org/wiki/Fast_Healthcare_Interoperability_Resources) standard.

Consider using an [adapter](https://github.com/GovStackWorkingGroup/specifications/blob/b86b16b85d2e1260d6c7005c49fb76787dc7a7a6/architecture-and-nonfunctional-requirements/6-onboarding.md#61-adapters) for compatibility.

## [Gateway](https://github.com/openimis/openimis-gateway_dkr.git) 

## Docker images

Docker images are organized based on [infra repository](https://github.com/GovStackWorkingGroup/sandbox-infra).