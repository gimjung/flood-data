# IAG Flood Data

For years, IAG has actively collects flood hazard information from government agencies, and external providers. It also actively develops internal models in areas where flood hazard information is not exists. The collected data covers the majority of populated places in Australia. IAG has significant works to standardize the information and transform the hazard information (i.e. flood depths and extent) to flood risk information (i.e. Average Annual Damage and Flood Frequency).

The Average Annual Damage (AAD) measure the flood risk which combines the likely impacts and probabilities of all possible flood events at a given location, up to and including the Probable Maximum Flood. The Flood Frequency (FF) measure the flood average recurrence interval. Combination between AAD and FF provides answers to how much it going to cost individual property owner, and how often it is going to cost them.

IAG has release flood risk information through Safer Home website (http://saferhomes.nrma.com.au), and would like to release the underlying data in a format that accessible for other purposes. The released data is available at address and aggregated level. The address level data provides granular flood risk information at individual address. The address information is based on GNAF February 2016 version. IAG’s coordinates are used in areas where IAG address database provide better information compare to GNAF. Thus improves the accuracy of flood risk assessment.  The second level is aggregated at admin boundaries lever. This will provides users with overview of flood in areas. 

### Purpose
The purpose of releasing this data is to inform general public on flood risk at their property and surrounding communities. IAG hope by releasing the data could provide a safer world by:

1. Improving awareness of flood risk to property owners and communities.
2. Promoting self mitigation, especially in areas with significant flood risks.
3. Improving risk communication and coordination between general public, related government agencies and industries.
4. Promoting information sharing to benefit communities.
5. Attracting new innovations in communicating and visualisation of risks



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
            <td>Flag  indicates which coordinates were used to assess the flood risk</td>
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
                    <li>IAG Internal Flood Model = In areas where government data is not readily available, IAG’s internal flood modelling has been used to assess flood risk at the site.</li>
                    <li>Third Party Model = In areas where government data is not readily available, modelling by consultants has been used to assess flood risk at the site.</li>
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



## Residential flood risk – agrregated at locality boundaries

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



## Residential flood risk – agrregated at local goverment area boundaries

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



## Residential flood risk – agrregated at commonwealth electoral boundaries

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
