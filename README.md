# IAG Flood Data

IAG are pleased to announce the release of a national dataset containing a view of flood risk across Australia. The released data is available at address and aggregated level. The address level data provides granular flood risk information and is based on the GNAF February 2016 release. IAG’s coordinates are used in areas where the IAG address database provides more appropriate information for defining primary dwelling flood risk.  The second level of released data is aggregated at admin boundaries level providing users with an overview of flood risk at a regional/national level. 

IAG, through our brand NRMA Insurance, are already leading the way in opening the Australian insurance view of risk. The Safer Homes portal (http://saferhomes.nrma.com.au) is an educational interactive web-based tool that helps customers and non-customers better understand the risk profile of the suburb they live in and the real value of their assets. Practical tips and tools are offered to users to better protect their homes. Safer Homes is the first new home insurance innovation developed with the customer in mind, and has resulted in driving cultural change within the IAG organisation.

IAG recognises that the data behind the tool has numerous potential benefits outside of the insurance industry and this provides the impetus for opening up our data to the public.

The data used for identifying the degree of flood risk is a combination of IAG modelling, industry sourced data, and local and state government data. The insurance industry is uniquely positioned in its ability to relate a physical risk into a financial risk through its exposure to claims data and the released dataset utilises these depth-damage functions to derive the risk categories supplied in the national dataset. It should be noted that the data represents a financial risk and consequently are not suitable to assess potential risk to life, public safety etc.

### Purpose
In releasing the data, IAG hope to assist in informing the general public on flood risk at their property and surrounding communities. The data release ties in with IAG’s core mission of making your world a safer place by:

1. Improving awareness of flood risk to property owners and communities.
2. Promoting self mitigation, especially in areas with significant flood risks.
3. Improving risk communication and coordination between general public, related government agencies and industries.
4. Promoting information sharing to benefit communities.
5. Attracting new innovations in communicating and visualisation of risks

![Map aerial view of suburb](https://github.com/iag-edge-labs/flood-data/blob/master/images/aus_201607_sample_json.jpg?raw=true)
Figure 1, Sample of Address data from API service

![Map view of council regions](https://github.com/iag-edge-labs/flood-data/blob/master/images/aus_201607_tweed_shire_council.jpg?raw=true)
Figure 2, Example of Aggregated data at LGA level

### Reference Date
July 2016

### Responsible party
IAG Flood Technical
Level 10, 388 George St, Sydney NSW 2000
iagfloodtechnical@iag.com.au

### Terms and definitions
<table>
    <tbody>
        <tr>
            <td width="20%">IAG Coordinates</td>
            <td>IAG’s coordinates are used in areas where the IAG address database provides more appropriate information for defining primary dwelling flood risk</td>
        </tr>
    </tbody>
</table>

### Abbreviations and acronyms 
<table>
    <tbody>
        <tr>
            <td width="20%">AAD</td>
            <td>The Average Annual Damage (AAD) measure the flood risk which combines the likely impacts and probabilities of all possible flood events at a given location, up to and including the Probable Maximum Flood</td>
        </tr>
        <tr>
            <td>FF</td>
            <td>The Flood Frequency (FF) measure the flood average recurrence interval. Combination between AAD and FF provides answers to how much it going to cost individual property owner, and how often it is going to cost them.</td>
        </tr>
        <tr>
            <td>G-NAF</td>
            <td>Address data provided by PSMA</td>
        </tr>
    </tbody>
</table>

## Data Product Delivery
IAG have a mature framework of data collection which includes direct communication with government.

### Delivery Medium Information

**Address level flood risk data**

This is available via an API with valid key.

* API URL: http://flood-risk-api.app.skyops.io
* API KEY: "iag-gov-hack-api"

**Aggregated Flood Risk Data**

This is available from

* https://github.com/iag-edge-labs/flood-data/data/

Please note that by using the IAG Flood Data you are agreeing to our [TERMS](terms-of-use.md).

## Appendix A – Data Dictionary
* [Address level flood risk](#address-level-flood-risk)
* [Residential flood risk – aggregated at locality boundaries](#residential-flood-risk--aggregated-at-locality-boundaries)
* [Residential flood risk – aggregated at local government area boundaries](#residential-flood-risk--aggregated-at-local-government-area-boundaries)
* [Residential flood risk – aggregated at commonwealth electoral boundaries](#residential-flood-risk--aggregated-at-commonwealth-electoral-boundaries)

## Address level flood risk

<table>
    <tbody>
        <tr>
            <th>Field name</th>
            <th>Data type</th>
            <th>Description</th>
            <th>Possible values</th>
        </tr>
        <tr>
            <td>GNAF_PID</td>
            <td>Varchar(15)</td>
            <td>GNAF’s permanent identifier</td>
            <td></td>
        </tr>
        <tr>
            <td>LONGITUDE</td>
            <td>Numeric(13,11)</td>
            <td>GNAF’s longitude</td>
            <td></td>
        </tr>
        <tr>
            <td>LATITUDE</td>
            <td>Numeric(13,11)</td>
            <td>GNAF’s latitude</td>
            <td></td>
        </tr>
        <tr>
            <td>FULL_ADDRESS</td>
            <td>Varchar(255)</td>
            <td>GNAF’s address</td>
            <td></td>
        </tr>
        <tr>
            <td>LOCALITY</td>
            <td>Varchar(100)</td>
            <td>GNAF’s locality</td>
            <td></td>
        </tr>
        <tr>
            <td>POSTCODE</td>
            <td>Varchar(4)</td>
            <td>GNAF’s postcode</td>
            <td></td>
        </tr>
        <tr>
            <td>STATE</td>
            <td>Varchar(3)</td>
            <td>GNAF’s state</td>
            <td></td>
        </tr>
        <tr>
            <td>RELIABILITY</td>
            <td>Integer</td>
            <td>GNAF’s geocode reliability</td>
            <td></td>
        </tr>
        <tr>
            <td>IAG_COORDINATE</td>
            <td>Integer</td>
            <td>Flag indicates which coordinates were used to assess the flood risk</td>
            <td>
                <ul>
                    <li>1 = IAG’s coordinate was used to assess flood risk at this address.</li>
                    <li>0 = GNAF’s coordinate was used to assess flood risk at this address.</li>
                </ul>
            </td>
        </tr>
        <tr>
            <td>SOURCE_TYPE</td>
            <td>Varchar(29)</td>
            <td>Type of flood hazard information</td>
            <td>
                <ul>
                    <li>Government Flood Mapping = State or local government flood mapping has been interpreted to risk assess flood risk at the site.</li>
                    <li>Other Government Flood Data = State or local government information including flood gauge data or flood levee data has been interpreted to assess flood risk at the site.</li>
                    <li>IAG Internal Flood Model = In areas where government data is not readily available, IAG’s internal flood modeling has been used to assess flood risk at the site.</li>
                    <li>Third Party Model = In areas where government data is not readily available, modeling by consultants has been used to assess flood risk at the site.</li>
                </ul>
            </td>
        </tr>
        <tr>
            <td>AVERAGE_ANNUAL_DAMAGE</td>
            <td>Varchar(1)</td>
            <td>Expected average annual damage</td>
            <td>
                <ul>
                    <li>L = Expected low average annual damage (≤ $100 for a typical Australian dwelling)</li>
                    <li>M = Expected medium average annual damage (> $100 AND ≤ $1,000 for a typical Australian dwelling)</li>
                    <li>H = Expected high average annual damage (> $1,000 for a typical Australian dwelling)</li>
                </ul>
            </td>
        </tr>
        <tr>
            <td>FLOOD_FREQUENCY</td>
            <td>Varchar(1)</td>
            <td>Flood frequency</td>
            <td>
                <ul>
                    <li>L = Low average recurrence interval (≥ 100 years)</li>
                    <li>M = Medium average recurrence interval (≥ 20 AND < 100 years)</li>
                    <li>H = High average recurrence interval (< 20 years)</li>
                </ul>
            </td>
        </tr>
    </tbody>
</table>



## Residential flood risk – aggregated at locality boundaries

<table>
    <tbody>
        <tr>
            <th>Field name</th>
            <th>Data type</th>
            <th>Description</th>
        </tr>
        <tr>
            <td>LOC_CODE</td>
            <td>Varchar(1)</td>
            <td>GNAF’s locality code</td>
        </tr>
        <tr>
            <td>LOC_DESC</td>
            <td>Varchar(50)</td>
            <td>GNAF’s locality description</td>
        </tr>
        <tr>
            <td>STATE_PID</td>
            <td>Varchar(15)</td>
            <td>GNAF’s state permanent identifier</td>
        </tr>
        <tr>
            <td>ST_ABBREV</td>
            <td>Varchar(3)</td>
            <td>GNAF’s state</td>
        </tr>
        <tr>
            <td>COUNT_BY_GOV_FM</td>
            <td>Integer</td>
            <td>Number of residential addresses assessed using Government Flood Mapping (GOV_FM)</td>
        </tr>
        <tr>
            <td>COUNT_BY_GOV_OD</td>
            <td>Integer</td>
            <td>Number of residential addresses assessed using Other Government Flood Data (GOV_OD)</td>
        </tr>
        <tr>
            <td>COUNT_BY_INTERNAL_MODEL</td>
            <td>Integer</td>
            <td>Number of residential addresses assessed using IAG’s internal flood model</td>
        </tr>
        <tr>
            <td>COUNT_BY_3RD_PARTY</td>
            <td>Integer</td>
            <td>Number of residential addresses assessed using third party models</td>
        </tr>
        <tr>
            <td>COUNT_LOW_AAD</td>
            <td>Integer</td>
            <td>Number of residential addresses with expected low average annual damage (≤ $100 for a typical Australian dwelling)</td>
        </tr>
        <tr>
            <td>COUNT_MEDIUM_AAD</td>
            <td>Integer</td>
            <td>Number of residential addresses with expected medium average annual damage (> $100 AND ≤ $1,000 for a typical Australian dwelling)</td>
        </tr>
        <tr>
            <td>COUNT_HIGH_AAD</td>
            <td>Integer</td>
            <td>Number of residential addresses with expected high average annual damage (> $1,000 for a typical Australian dwelling)</td>
        </tr>
        <tr>
            <td>COUNT_LOW_FREQUENCY</td>
            <td>Integer</td>
            <td>Number of residential addresses with low average recurrence interval (≥ 100 years)</td>
        </tr>
        <tr>
            <td>COUNT_MEDIUM_FREQUENCY</td>
            <td>Integer</td>
            <td>Number of residential addresses with medium average recurrence interval (≥ 20 AND < 100 years)</td>
        </tr>
        <tr>
            <td>COUNT_HIGH_FREQUENCY</td>
            <td>Integer</td>
            <td>Number of residential addresses with high average recurrence interval (< 20 years)</td>
        </tr>
        <tr>
            <td>TOTAL_AAD</td>
            <td>Big Integer</td>
            <td>Total expected average annual damage for the residential addresses in the locality. The figure is only for  buildings, and uses typical building values for the locality (rather than the typical Australian dwelling figures reported in the per-address dataset).</td>
        </tr>
        <tr>
            <td>RANK_AAD</td>
            <td>Integer</td>
            <td>Rank of the average annual damage for residential addresses in this locality compared to other localities in Australia.</td>
        </tr>
        <tr>
            <td>SHAPE</td>
            <td>Geography</td>
            <td></td>
        </tr>
    </tbody>
</table>



## Residential flood risk – aggregated at local government area boundaries

<table>
    <tbody>
        <tr>
            <th>Field name</th>
            <th>Data type</th>
            <th>Description</th>
        </tr>
        <tr>
            <td>LGA_PID</td>
            <td>Varchar(15)</td>
            <td>GNAF’s LGA permanent identifier</td>
        </tr>
        <tr>
            <td>LGA_NAME</td>
            <td>Varchar(100)</td>
            <td>GNAF’s LGA name</td>
        </tr>
        <tr>
            <td>STATE_PID</td>
            <td>Varchar(15)</td>
            <td>GNAF’s state permanent identifier</td>
        </tr>
        <tr>
            <td>ST_ABBREV</td>
            <td>Varchar(3)</td>
            <td>GNAF’s state</td>
        </tr>
        <tr>
            <td>COUNT_BY_GOV_FM</td>
            <td>Integer</td>
            <td>Number of residential addresses assessed using Government Flood Mapping (GOV_FM)</td>
        </tr>
        <tr>
            <td>COUNT_BY_GOV_OD</td>
            <td>Integer</td>
            <td>Number of residential addresses assessed using Other Government Flood Data (GOV_OD)</td>
        </tr>
        <tr>
            <td>COUNT_BY_INTERNAL_MODEL</td>
            <td>Integer</td>
            <td>Number of residential addresses assessed using IAG’s internal flood model</td>
        </tr>
        <tr>
            <td>COUNT_BY_3RD_PARTY</td>
            <td>Integer</td>
            <td>Number of residential addresses assessed using third party models</td>
        </tr>
        <tr>
            <td>COUNT_LOW_AAD</td>
            <td>Integer</td>
            <td>Number of residential addresses with expected low average annual damage (≤ $100 for a typical Australian dwelling)</td>
        </tr>
        <tr>
            <td>COUNT_MEDIUM_AAD</td>
            <td>Integer</td>
            <td>Number of residential addresses with expected medium average annual damage (> $100 AND ≤ $1,000 for a typical  Australian dwelling)</td>
        </tr>
        <tr>
            <td>COUNT_HIGH_AAD</td>
            <td>Integer</td>
            <td>Number of residential addresses with expected high average annual damage (> $1,000 for a typical Australian  dwelling)</td>
        </tr>
        <tr>
            <td>COUNT_LOW_FREQUENCY</td>
            <td>Integer</td>
            <td>Number of residential addresses with low average recurrence interval (≥ 100 years)</td>
        </tr>
        <tr>
            <td>COUNT_MEDIUM_FREQUENCY</td>
            <td>Integer</td>
            <td>Number of residential addresses with medium average recurrence interval (≥ 20 AND < 100 years)</td>
        </tr>
        <tr>
            <td>COUNT_HIGH_FREQUENCY</td>
            <td>Integer</td>
            <td>Number of residential addresses with high average recurrence interval (< 20 years)</td>
        </tr>
        <tr>
            <td>TOTAL_AAD</td>
            <td>Big Integer</td>
            <td>Total expected average annual damage for the residential addresses in the LGA. The figure is only for buildings, and  uses typical building values for the LGA (rather than the typical Australian dwelling figures reported in the per-address dataset).</td>
        </tr>
        <tr>
            <td>RANK_AAD</td>
            <td>Integer</td>
            <td>Rank of the average annual damage for residential addresses in this LGA compared to other LGAs in Australia.</td>
        </tr>
        <tr>
            <td>SHAPE</td>
            <td>Geography</td>
            <td></td>
        </tr>
    </tbody>
</table>



## Residential flood risk – aggregated at commonwealth electoral boundaries

<table>
    <tbody>
        <tr>
            <th>Field name</th>
            <th>Data type</th>
            <th>Description</th>
        </tr>
        <tr>
            <td>CE_PID</td>
            <td>Varchar(15)</td>
            <td>GNAF’s Commonwealth Electoral (CEL) permanent identifier</td>
        </tr>
        <tr>
            <td>NAME</td>
            <td>Varchar(100)</td>
            <td>GNAF’s CEL name</td>
        </tr>
        <tr>
            <td>STATE_PID</td>
            <td>Varchar(15)</td>
            <td>GNAF’s State permanent identifier</td>
        </tr>
        <tr>
            <td>ST_ABBREV</td>
            <td>Varchar(3)</td>
            <td>GNAF’s State</td>
        </tr>
        <tr>
            <td>COUNT_BY_GOV_FM</td>
            <td>Integer</td>
            <td>Number of residential addresses assessed using Government Flood Mapping (GOV_FM)</td>
        </tr>
        <tr>
            <td>COUNT_BY_GOV_OD</td>
            <td>Integer</td>
            <td>Number of residential addresses assessed using Other Government Flood Data (GOV_OD)</td>
        </tr>
        <tr>
            <td>COUNT_BY_INTERNAL_MODEL</td>
            <td>Integer</td>
            <td>Number of residential addresses assessed using IAG’s internal flood model</td>
        </tr>
        <tr>
            <td>COUNT_BY_3RD_PARTY</td>
            <td>Integer</td>
            <td>Number of residential addresses assessed using third party models</td>
        </tr>
        <tr>
            <td>COUNT_LOW_AAD</td>
            <td>Integer</td>
            <td>Number of residential addresses with expected low average annual damage (≤ $100 for a typical Australian dwelling)</td>
        </tr>
        <tr>
            <td>COUNT_MEDIUM_AAD</td>
            <td>Integer</td>
            <td>Number of residential addresses with expected medium average annual damage (> $100 AND ≤ $1,000 for a typical  Australian dwelling)</td>
        </tr>
        <tr>
            <td>COUNT_HIGH_AAD</td>
            <td>Integer</td>
            <td>Number of residential addresses with expected high average annual damage (> $1,000 for a typical Australian  dwelling)</td>
        </tr>
        <tr>
            <td>COUNT_LOW_FREQUENCY</td>
            <td>Integer</td>
            <td>Number of residential addresses with low average recurrence interval (≥ 100 years)</td>
        </tr>
        <tr>
            <td>COUNT_MEDIUM_FREQUENCY</td>
            <td>Integer</td>
            <td>Number of residential addresses with medium average recurrence interval (≥ 20 AND < 100 years)</td>
        </tr>
        <tr>
            <td>COUNT_HIGH_FREQUENCY</td>
            <td>Integer</td>
            <td>Number of residential addresses with high average recurrence interval (< 20 years)</td>
        </tr>
        <tr>
            <td>TOTAL_AAD</td>
            <td>Big Integer</td>
            <td>Total expected average annual damage for the residential addresses in the commonwealth electorate. The figure is  only for buildings, and uses typical building values for the electorate (rather than the typical Australian dwelling figures reported in the per-address dataset).</td>
        </tr>
        <tr>
            <td>RANK_AAD</td>
            <td>Integer</td>
            <td>Rank of the average annual damage for residential addresses in this commonwealth electoral compared to other  commonwealth electoral in Australia.</td>
        </tr>
        <tr>
            <td>SHAPE</td>
            <td>Geography</td>
            <td></td>
        </tr>
    </tbody>
</table>
