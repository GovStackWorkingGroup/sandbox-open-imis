# [openIMIS](https://github.com/openimis) 

Minimum set of components:

* Database
* Backend
* Gateway

## [Database](https://github.com/openimis/database_postgresql) 

Backend expect database with predefine schema and data.

To get DB with particular state need to use
[Helm chart](https://github.com/GovStackWorkingGroup/sandbox-open-imis/blob/9d5f4f907d5acbbfe4ecd4bf6194de711e2f1a09/sandbox-open-imis/charts/db/templates/db.yaml) base on specific snapshot. 

Predefined DB [backup](https://github.com/GovStackWorkingGroup/sandbox-open-imis/tree/main/backup) can be helpful. 

## [Backend](https://github.com/openimis/openimis-be_py.git)

Backend expect communication via Gateway component.

## [Gateway](https://github.com/openimis/openimis-gateway_dkr.git) 

## Docker images

Docker images organized base on [infra repository](https://github.com/GovStackWorkingGroup/sandbox-infra).