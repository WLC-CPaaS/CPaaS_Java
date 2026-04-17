

# TypesGeoLocation


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**continentCode** | **String** | The two-letter code for the continent.  Amazon Route 53 supports the following continent codes:    - AF: Africa    - AN: Antarctica    - AS: Asia    - EU: Europe    - OC: Oceania    - NA: North America    - SA: South America  Constraint: Specifying ContinentCode with either CountryCode or SubdivisionCode returns an InvalidInput error. |  [optional] |
|**countryCode** | **String** | For geolocation resource record sets, the two-letter code for a country.  Amazon Route 53 uses the two-letter country codes that are specified in [ISO standard 3166-1 alpha-2].  Route 53 also supports the country code UA for Ukraine.  [ISO standard 3166-1 alpha-2]: https://en.wikipedia.org/wiki/ISO_3166-1_alpha-2 |  [optional] |
|**subdivisionCode** | **String** | For geolocation resource record sets, the two-letter code for a state of the United States. Route 53 doesn&#39;t support any other values for SubdivisionCode . For a list of state abbreviations, see [Appendix B: Two–Letter State and Possession Abbreviations]on the United States Postal Service website.  If you specify subdivisioncode , you must also specify US for CountryCode .  [Appendix B: Two–Letter State and Possession Abbreviations]: https://pe.usps.com/text/pub28/28apb.htm |  [optional] |



