# IAG Flood Risk Data

IAG are pleased to announce the release of a national dataset containing a view of flood risk across Australia. The released data is available at address and aggregated level. The address level data provides granular flood risk information and is based on the G-NAF February 2016. IAG’s coordinates are used in areas where the IAG address database provides more appropriate information for defining primary dwelling flood risk. The second level of data is aggregated at admin boundaries level providing users with an overview of flood risk at a regional/national level.

IAG, through our brand NRMA Insurance, are already leading the way in opening the Australian insurance view of risk. The Safer Homes portal (http://saferhomes.nrma.com.au) is an educational interactive web-based tool that helps customers and non-customers better understand the risk profile of the suburb they live in and the real value of their assets. Practical tips and tools are offered to users to better protect their homes. Safer Homes is the first new home insurance innovation developed with the customer in mind, and has resulted in driving cultural change within the IAG organisation.

IAG recognises that the data behind the tool has numerous potential benefits outside of the insurance industry and this provides the impetus for opening up our data to the public.

The data used for identifying the degree of flood risk is a combination of IAG modelling, industry sourced data, and local and state government data. The insurance industry is uniquely positioned in its ability to relate a physical risk into a financial risk through its exposure to claims data and this dataset utilises these depth-damage functions to derive the risk categories supplied in the national dataset. It should be noted that the data represents a financial risk and consequently are not suitable to assess potential risk to life, public safety etc.

### Purpose
In releasing the data, IAG hope to assist in informing the general public on flood risk at their property and surrounding communities. The data release ties in with IAG’s core mission of making your world a safer place by:

1. Improving awareness of flood risk to property owners and communities.
2. Promoting self mitigation, especially in areas with significant flood risks.
3. Improving risk communication and coordination between general public, related government agencies and industries.
4. Promoting information sharing to benefit communities.
5. Attracting new innovations in communicating and visualisation of risks

### Summary of Dataset Coverage
The released dataset assesses flood risk for 88% of all addresses nationally. The remaining 12% contains third party modelling which cannot be released due to licensing constraints and the table below provides a breakdown of the source type for IAG’s flood risk data.

<table>
    <tbody>
        <tr>
            <td>Source of Data (Source_type)</td>
            <td>Count</td>
            <td>Percentage</td>
            <td>Count of flood risk assessment included</td>
            <td>Percentage of flood risk assessment included</td>
        </tr>
        <tr>
            <td>GOVERNMENT FLOOD MAPPING</td>
            <td>2,291,441</td>
            <td>16%</td>
            <td>2,291,441</td>
            <td>16%</td>
        </tr>
        <tr>
            <td>OTHER GOVERNMENT FLOOD DATA</td>
            <td>1,054,220</td>
            <td>8%</td>
            <td>1,054,220</td>
            <td>8%</td>
        </tr>
        <tr>
            <td>IAG INTERNAL FLOOD MODEL</td>
            <td>8,870,278</td>
            <td>64%</td>
            <td>8,870,278</td>
            <td>64%</td>
        </tr>
        <tr>
            <td>THIRD PARTY MODEL</td>
            <td>1,674,696</td>
            <td>12%</td>
            <td>0</td>
            <td>0%</td>
        </tr>
        <tr>
            <td>TOTAL</td>
            <td>13,890,635</td>
            <td>100%</td>
            <td>12,215,939</td>
            <td>88%</td>
        </tr>
    </tbody>
</table>

*Source_type categories are describe in data dictionary*

### Data Category Description

The High, Medium and Low risk bands describe the financial risk. The risk is based on two factors, how severe the flooding is and how often the property is likely to be flooded. You may have heard in the media that a flood is a 1 in 100 year event. This doesn’t mean that the flood will happen exactly once every 100 year but that on average it will. A more appropriate way to think about it is that the event has a 1% chance of happening in any given year. A 1% event can be thought of as quite a rare event and there will be events that for example have a 10% chance of happening every year or even a 99% chance of happening every year. The consequences of a rare event are expected to be more severe and it is that relationship between how often an event is likely to occur and how severe (damage to property) an event is that informs the financial risk.

The insurance industry uses Average Annual Damage (AAD) which is the cost of potential flood events integrated across how likely these events are to occur in a given year (flood frequency). This can be thought of as a house that floods very often but with only minor damage versus a house that floods rarely but when it does significant damage is incurred. Both mechanisms may incur Low, Medium or High flood ratings but it is the relationship between the frequency of the event and the cost of the event that determines which risk band the house falls into.

<table>
    <tbody>
        <tr>
            <td>Flood Risk AAD (average_annual_damage)</td>
            <td>Count</td>
            <td>Percentage</td>
        </tr>
        <tr>
            <td>High (H)</td>
            <td>388,993</td>
            <td>2.8%</td>
        </tr>
        <tr>
            <td>Medium (M)</td>
            <td>609,402</td>
            <td>4.4%</td>
        </tr>
        <tr>
            <td>Low (L)</td>
            <td>11,217,544</td>
            <td>80.8%</td>
        </tr>
        <tr>
            <td>NULL</td>
            <td>1,674,696</td>
            <td>12.0%</td>
        </tr>
        <tr>
            <td>TOTAL</td>
            <td>13,890,635</td>
            <td>100.0%</td>
        </tr>
    </tbody>
</table>

*Flood Risk AAD (average_annual_damage) categories are described in Data Dictionary
All null Values are from Third Party Models*

The likelihood of a property being flooded (Flood Frequency) is also provided in banded form to assist the user.

<table>
    <tbody>
        <tr>
            <td>Frequency of over ground flooding (FLOOD_FREQUENCY)</td>
            <td>Count</td>
            <td>Percentage</td>
        </tr>
        <tr>
            <td>High (H)</td>
            <td>220,045</td>
            <td>1.6%</td>
        </tr>
        <tr>
            <td>Medium (M)</td>
            <td>437,478</td>
            <td>3.1%</td>
        </tr>
        <tr>
            <td>Low (L)</td>
            <td>11,558,416</td>
            <td>83.2%</td>
        </tr>
        <tr>
            <td>NULL</td>
            <td>1,674,696</td>
            <td>12.1%</td>
        </tr>
        <tr>
            <td>TOTAL</td>
            <td>13,890,635</td>
            <td>100.0%</td>
        </tr>
    </tbody>
</table>

*Frequency of over ground flooding (FLOOD_FREQUENCY) categories are described in Data Dictionary
All null Values are from Third Party Models*

The three aggregated dataset includes values for “total AAD”. This value is calculated using the estimated building flood risk AAD of residential addresses. This doesn’t include home content AAD or the AAD of other assets that might be flood prone like commercial and industry assets. Therefore this value will not accurately estimate the whole community flood risk. The total AAD is best used to identify regions where residential communities are exposed to flooding.

### Example of the IAG Flood Risk Data in Maps

![Map aerial view of suburb](https://github.com/iag-edge-labs/flood-data/blob/master/images/aus_201607_sample_json.jpg?raw=true)
Figure 1, Sample of Address data from API service

![Map view of council regions](https://github.com/iag-edge-labs/flood-data/blob/master/images/aus_201607_tweed_shire_council.jpg?raw=true)
Figure 2, Example of Aggregated data at LGA level

### IAG versus GNAF coordinates

GNAF coordinates are typically located at the centroid of the cadastral lot. The centroid is not always representative of the flood risk to a property especially when the asset sits on a large cadastral lot as illustrated on Figure 3. While the provided dataset is supplied in GNAF coordinates, it is important to note that the flood risk bands provided apply to where the major asset is located and not the GNAF point location. This shift affects approximately 2,000,000 points in total.

![Map view of GNAF coordinate](https://github.com/iag-edge-labs/flood-data/blob/master/images/IAG_vs_GNAF.png?raw=true)
Figure 3, Example of adjustment of GNAF coordinate to better represent flood risk

### Third Party Models

IAG uses several third party models from consultants to assess flood risk in areas where Government or IAG internal data is not readily available. This represents about 12% of all addresses nationally. *Due to licensing restriction covering third party models no derived data from these models is provided.* This means flood risk assessments are likely to be underestimated when it relies on a third party model. This will particular affect the accuracy of the total AAD and Rank in the aggregated data.

### Reference Date
July 2016

### Responsible party and primary contact
IAG Flood Technical
Insurance Australia Limited
Level 10, 388 George St, Sydney NSW 2000
hydrology@iag.com.au

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
            <td>The Average Annual Damage (AAD) measure the flood risk which combines the likely impacts and probabilities of all possible flood events at a given location, up to and including the Probable Maximum Flood (PMF)</td>
        </tr>
        <tr>
            <td>FF</td>
            <td>The Flood Frequency (FF) measure the flood average recurrence interval. Combination between AAD and FF provides answers to how much it going to cost individual property owner, and how often it is going to cost them.</td>
        </tr>
        <tr>
            <td>G-NAF</td>
            <td>Address data provided by PSMA. G-NAF License is available here http://data.gov.au/dataset/19432f89-dc3a-4ef3-b943-5326ef1dbecc/resource/09f74802-08b1-4214-a6ea-3591b2753d30/download/20160226---EULA---Open-G-NAF.pdf</td>
        </tr>
    </tbody>
</table>

## Data Product Delivery

### Delivery Medium Information

Your access to and use of the information constitutes your agreement to the [Terms of Use](TERMS.md).

**Address level flood risk data**

This is available via an API with valid key.

* API URL: http://flood-risk-api.app.skyops.io
* API KEY: "iag-gov-hack-api"

**Aggregated Flood Risk Data**

CSV and JSON format flood risk data is available from:

* [Aggregated Flood Risk Data](data/)

CSV format contains flood risk data and no administrative boundary GIS data. Use the G-NAF permanent identifier to join CSV format data to GIS G-NAF administrative boundaries

JSON format contains flood risk data and GIS administrative boundaries.

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
            <td>Numeric(11,8)</td>
            <td>GNAF’s longitude</td>
            <td></td>
        </tr>
        <tr>
            <td>LATITUDE</td>
            <td>Numeric(10,8)</td>
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

Note: this will not assess flood risk impact to whole community as it only aggregates residential flood risk

<table>
    <tbody>
        <tr>
            <th>Field name</th>
            <th>Data type</th>
            <th>Description</th>
        </tr>
        <tr>
            <td>LOC_PID</td>
            <td>Varchar(15)</td>
            <td>GNAF’s locality permanent identifier</td>
        </tr>
        <tr>
            <td>NAME</td>
            <td>Varchar(100)</td>
            <td>GNAF’s locality name</td>
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
            <td>ONLY available in the JSON format data</td>
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
            <td>ONLY available in the JSON format data</td>
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
            <td>ONLY available in the JSON format data</td>
        </tr>
    </tbody>
</table>

## Appendix B – Terms of Use

### Terms of Use – IAG Flood Risk Data

Your access to and use of this data is governed by these Terms of Use. Your access to and use of the data constitutes your agreement to these Terms of Use.

"This data" means all data provided to you by Insurance Australia Limited (ABN 11 000 016 722) (**IAL**).

If you use or reproduce this data, you must, amongst other things, identify the creator of this data in any reasonable manner as requested by Insurance Australia Limited.

Please note: **This data may not be used for insurance, reinsurance or comparative pricing purposes.**

### Other Important Information

To the maximum extent permitted by law, IAL provides the data on an ‘as is’ basis and makes no warranties or representations, whether express or implied, as to the accuracy or reliability of the data or that the data is fit for a particular purpose. Further, you acknowledge that the data provided is an assessment of financial risk only and is not necessarily suitable for use in assessing any other kinds of risk, including risks regarding safety.

To the maximum extent permitted by law, IAL excludes liability of any kind (including for negligence) to any person arising directly or indirectly from accessing, using or being unable to access or use, the data.

If you contravene these Terms of Use, IAL reserves the right to terminate, modify or suspend your access to the data, in its sole discretion, without notice and without prejudice to any other rights that it may have.

Any failure by IAL to exercise any right, power or remedy under these Terms of Use shall not operate as a waiver of IAL’s rights.
The law of New South Wales governs these Terms of Use.
