---
layout: page
title: Data Policies
permalink: /data-policies/
nav: true
weight: 5
---

The previous sections outline the key management roles and responsibilities to support and maintain cross-agency data sharing. The following sections describe key data policies that promote data quality, data accuracy, and acceptable use standards.  

## Data Quality
The quality of the data in the P20 WIN ultimately determines the system’s overall value to state officials and external researchers. The National Center for Education Statistics (NCES) notes that key attributes of data quality are accuracy, completeness, timeliness, validity, and consistency[^2]. Data inaccuracy refers to errors in records that are often the result of poor data entry practices and poor regulation of data accessibility[^3]. Data completeness refers to the degree to which all data is available, which is often measured by the number of missing records[^4]. Data validity refers to whether the data fields actually measure and reflect the systems or outcomes of interest. Data consistency refers to the degree the data is stable across both time and sources.

Integrated data systems must account for data inconsistencies across agencies. For example, an individual’s race as tracked in DSS Medicaid tables may not match the CCEH HMIS race identifier. Nonetheless, strong data governance policies can increase the value of such systems for key stakeholders. The Minnesota’s SLDS Governance Manual notes that “The key to maintaining high quality data is a proactive approach to data governance that requires establishing and regularly updating strategies for preventing, detecting, and correcting errors and misuses of data.” 

P20 WIN Participating Agencies providing data do not ensure 100% accuracy of all fields and each Data Recipient accepts the quality of the data as received.[^5]

The Executive Board can establish a data quality committee to introduce strategies to improve data standards. Other states have suggested participating agencies conduct regular data quality audits. For example, Virginia’s State Longitudinal Data System research sub-committee encourages participating agencies to develop some basic data quality reports that show range of values and frequency of missing values to accompany the master Data Dictionary. Other strategies include automatic edit checks that crosscheck the same field from year to year, reports on matching rates, and clean metadata for all possible extracts in the SLDS.

## Input File Format

To facilitate identity resolution in an interagency data request, each Participating Agency must  structure the input file so that there is one unique record per Individual represented. Data that may have been pulled from a dimensional data source will be flattened to produce an input file in this format. Additionally, the Participating Agency should structure the file with a unique generic ID to each unique record in the file that identifies the Participating Agency which is providing the information. 

Participating Agencies Data Stewards should follow the standardized formatting requirements when preparing a data file for matching. The Data Integration Hub has the right to reject any data that does not meet these standards. 

For matching files – Files should be in a tab delimited text file. There should not be quotations around text fields.

For analytic files – Files should be in the format requested and approved for the given data request.

## Standard naming convention for files and data elements:

The file naming standard for data files transferred via SFTP is as follows:  
a. Agency acronym
b. Data Request Number listed in DSA
c. Date file was created (MM_DD_YYYY)
d. Contents of file (matching, analytical, key)
example: "DOL.000.01_01_2000.matching"

The table below identifies the most commonly requested data variables.

| Field/Data Element | Format | Possible Values | Definition | Comment | 
| ----- | ----- | ----- | ----- | ----- |
| SSN | Text or Varchar(9) | | Social security # | With leading zero |
| DOB | YYYYMMDD | YYYYMMDD | Date of Birth | As a text field |
| Gender |  Text or varchar(1) | M = male, F = female, U = unknown | Gender | |
| Race/Ethnicity | | | | |
| LastName | Text | | | |
| MiddleName | Text | | | |
| FirstName | Text | | | |
| SASID | Text or varchar(10) | | State Assigned Student Identification Number | |
| HighSchoolCode | Text or varchar(6) | | CollegeBoard HS assigned code | Include leading zero |
| Fake ID | | | A unique fake identifier to be used | |

## Metadata and Data Dictionaries 

Metadata is structured data about data. High quality metadata provides helpful context about the data’s creation, quality, and uses and is key to improving data discovery. Metadata helps to answer the question “what is the data about?” by providing more detail about various characteristics of the data, including information about the data source, update frequency, and level of detail. Dataset metadata elements should include:

- Human-readable name of the dataset
- A description of what the dataset entails 
- The number of rows 
- Temporal coverage 
- The update frequency  
- Any unique identifier

Related guidance for metadata on the open data portal can be found here. Participating Agencies should provide key metadata to accompany the interagency Data Dictionary fields. The Data Governing Board is responsible for developing, documenting and monitoring Data Definitions and Metadata for shared Data Elements within the cross-agency Data Dictionary. The Operating Group works with the Data Governing Board to ensure that the Data Dictionary for each Participating Agency is complete and up-to-date. 

## Acceptable use

Cross-agency data sharing is for legitimate governmental purposes, which can include evidence-based policy-making, academic research to support the wellbeing of state residents, and mandated, periodic state reporting. Each Participating Agency and the Data Integration Hub can only use Data for the authorized Data Sharing Request purpose and no other purpose in accordance with applicable federal and state law, the P20Win E-MOU and the Data Sharing Agreement. No participating agency, person or entity can maintain, use, disclose or share Data in a manner inconsistent with the terms of the P20Win E-MOU or its Appendices and applicable federal and state laws and regulations. 
Upon completion of the approved project in a Data Request, all Data must be destroyed as determined by the Participating Agencies in the Data Sharing Agreement. In accordance with applicable law and the P20Win E-MOU, the Data Governing Board establishes the parameters for Data Transmission and Data destruction.

[^2]: https://nces.ed.gov/programs/slds/pdf/data_quality_striking_a_balance_may2014.pdf 
[^3]: https://dataladder.com/what-is-data-accuracy/ 
[^4]: https://dataladder.com/missing-data-and-data-completeness/ 
[^5]: http://www.hunt-institute.org/wp-content/uploads/2019/06/Hunt-Institute-Connecting-the-Continuum.pdf
[^6]: https://vlds.virginia.gov/media/1087/vlds_book_of_dg.pdf 
