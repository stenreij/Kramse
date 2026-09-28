# Kramse

Kramse is een ETL-project (Extract, Transform, Load) gebouwd met SQL Server Integration Services (SSIS). Het project verplaatst en transformeert data tussen verschillende bronsystemen en doelsystemen, waaronder ERP-, PSA-, ODS- en RAW-omgevingen. Daarnaast is het doel om dashboards te ontwerpen op basis van de verzamelde en getransformeerde data.

## Doel

Het doel van Kramse is om data uit diverse bronnen (Excel, Access, MSSQL) te extraheren, te transformeren en te laden in de juiste doelsystemen. Op deze manier wordt data centraal beschikbaar gesteld voor analyse, rapportage en dashboarding.

## Functionaliteiten

Het project bestaat uit meerdere SSIS-packages die elk een specifieke datastroom verzorgen:

- **FILES to RAW** – Ruwe bestanden inladen naar de RAW-laag
- **RAW to ERP** – Data vanuit de RAW-laag naar het ERP-systeem brengen
- **ERP to PSA** – Data vanuit ERP naar het PSA-systeem brengen
- **PSA to ODS** – Data vanuit PSA naar de ODS-laag brengen
- **Run Packages** – Coördinatie en uitvoering van de verschillende packages

Daarnaast zijn er diverse connection managers aanwezig voor:

- Excel-bestanden
- Access-databases
- MSSQL-databases (ERP, ODS, PSA, RAW)

## Architectuur

Het project volgt een gelaagde ETL-aanpak:

Bronnen --> RAW --> ERP --> PSA --> ODS

Elke laag heeft een eigen doel en verantwoordelijkheid binnen de dataflow. De uiteindelijke data wordt gebruikt voor het ontwerpen van dashboards.

## Technologieën

- SQL Server Integration Services (SSIS)
- SQL Server (MSSQL)
- Microsoft Excel
- Microsoft Access
- Visual Studio (SSDT)
