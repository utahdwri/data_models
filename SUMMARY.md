# Table of contents

* [Utah Division of Water Rights Data Models](README.md)
* [Distribution Accounting Data](distribution_accounting/README.md)
* [Measurement Data](measurement_data/README.md)
  * [Modernization Plan](measurement_data/modernization-plan.md)
  * [Sharing Data with DWRi](measurement_data/sharing-data-with-dwri.md)
  * [DWRi DIVRT Data Model](measurement_data/divrt/README.md)
  * [HydroServer Data Model](measurement_data/hydroserver/README.md)
    * [HydroServer Data Model Data Dictionary](measurement_data/hydroserver/hydroserver_data_model_data_dictionary.md)
    * [Standard Data Format Specifications for DWRi's Data Scraping System](measurement_data/hydroserver/standard_data_formats.md)
    * [HydroServer API](measurement_data/hydroserver/hydroserver-api/README.md)
      * ```yaml
        type: builtin:openapi
        props:
          models: true
          downloadLink: true
        dependencies:
          spec:
            ref:
              kind: openapi
              spec: test
        ```
* [Water Use Program Data](water_use_program_data/README.md)
