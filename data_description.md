# Data required to reproduce the analysis

This repository uses a combination of openly available and restricted datasets.
The following documentation describes all datasets required to reproduce the analysis, including temporal coverage, data providers, access conditions, and preprocessing requirements. 

## Basic data


### Residential densification dataset (2013–2023)

* **Description:** Parcels of 2013 with information on occurence and extent of residential densification from 2013-2023.
* **Years used:** Parcels 2013; densification 2013–2023
* **Provider:** Referat für Stadtplanung und Bauordnung der Stadt München and Authors
* **Access:** Restricted / internal use only


### Parcel and building data (ALKIS)

* **Description:** Official cadastral parcel and building geometries used as the base spatial dataset. 
* **Years used:** 2013, 2023 (2011, 2021)
* **Provider:** Bavarian cadastral authority
* **Access:** Partly open; older datasets must be requested
* **Links:**

  * Current parcel data: https://geodaten.bayern.de/opengeodata/OpenDataDetail.html?pn=parzellarkarte
  * ALKIS information: https://www.ldbv.bayern.de/produkte/liegenschaftsinformationen/alkis.html
* **Required preprocessing:**

  * Add ALKIS *Tatsächliche Nutzung* if land use information is missing:
    https://geodaten.bayern.de/opengeodata/OpenDataDetail.html?pn=tatsaechlichenutzung
  * Add 3D building model (LoD2) if building use or building height is missing:
    https://geodaten.bayern.de/opengeodata/OpenDataDetail.html?pn=lod2
  * If a building footprint covers more than one parcel, the parcels are merged to allow for unambiguous assignment of building to parcels.
  * If a parcel is vacent in 2013, but built-up in 2011, the building of 2011 was included in the dataset, to correctly account for reconstruction processes. The same is done for 2023/2021.


### Built-up area

* **Description:** The Tree Protection Ordinance (Baumschutzverordnung) is used as approximation of built-up area.
* **Years used:** 2013
* **Provider:** Geodaten-Service München
* **Access:** Restricted
* **Link:** https://stadt.muenchen.de/rathaus/stadtrecht/vorschrift/901.pdf


### Planned projects with more than 50 housing units (PLAN-FIS)

* **Description:** Internal planning dataset for large housing projects.
* **Years used:** 2013, 2023
* **Provider:** Referat für Stadtplanung und Bauordnung der Stadt München
* **Access:** Restricted / internal use only


### Building type

* **Description:** Classification of buildings in building types (SFH/MFH detached, semi-detached, multi-detached, non-residential buildings)
* **Years used:** 2013, 2023
* **Provider:** Geodaten-Service München and Authors
* **Access:** Restricted


## Additional data for preparing predictors

### Year of construction of buildings

* **Description:** Building age information linked to building geometries.
* **Years used:** 2013, 2023 (2011, 2021)
* **Provider:** Geodaten-Service München
* **Access:** Restricted


### Structure type

* **Description:** Urban structure type classification (detached low-density areas, perimeter blocks, housing estates, industrial, other)
* **Years used:** 2016
* **Provider:** Geodaten-Service München
* **Access:** Restricted


### Number and age of residents per parcel

* **Description:** Number of residents per parcel. Age of residents per parcel provided in age groups. 
* **Years used:** 2013, 2023 (2011, 2021)
* **Provider:** Referat für Stadtplanung und Bauordnung der Stadt München
* **Access:** Restricted


### Public transport quality

* **Description:** Public transport service quality classified by stop category based on departure frequency and mode, with upgrades for combined high-frequency services, and translated into graded accessibility zones (A–E) using distance-based multi-ring buffers.
* **Years used:** 2020,2040
* **Provider:** Referat für Stadtplanung und Bauordnung der Stadt München
* **Access:** Restricted


### Center quality

* **Description:** Classification of urban center quality based on Munich’s center concept categories, where centers are assigned graded catchment areas (A–E) using distance-based multi-ring buffers.
* **Years used:** 2020
* **Provider:** Referat für Stadtplanung und Bauordnung der Stadt München
* **Access:** Restricted


### Zoning plans

* **Description:** Planning geometries without attribute information.
* **Years used:** 2013, 2023
* **Provider:** Geodaten-Service München
* **Access:** Restricted; recent versions partly open
* **Link:** https://geoportal.muenchen.de/portal/master/


### Listed buildings and ensembles

* **Description:** Heritage protection information.
* **Years used:** 2013, 2023
* **Provider:** Geodaten-Service München
* **Access:** Partly open / restricted
* **Link:** https://atlas.bayern.de/


### Parcels owned by municipality

* **Description:** Parcels which are owned by the municipality.
* **Years used:** 2013, 2023
* **Provider:** Geodaten-Service München
* **Access:** Restricted


### House prices and rents for flats

* **Description:** Real estate prices and rents aggregated in a 1 km² grid. Median of all years 2009-2013 and 2019-2023.
* **Years used:** 2009-2013; 2019-2023
* **Provider:** RWI Scientific Use File
* **Access:** License required
* **Links:**

  * Dataset access: https://www.rwi-essen.de/forschung-beratung/weitere/forschungsdatenzentrum-ruhr/datenangebot/rwi-geo-red-real-estate-data
  * Documentation: https://www.rwi-essen.de/fileadmin/user_upload/RWI/FDZ/FDZ_Datensatzbeschreibung_RED_v14.pdf


### Land reference values

* **Description:** Official land valuation data.
* **Years used:** 2013, 2023
* **Provider:** Geodaten-Service München
* **Access:** Partly open / restricted
* **Link:** https://atlas.bayern.de/

