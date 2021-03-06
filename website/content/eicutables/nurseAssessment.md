+++
date = "2015-09-01T19:34:46-04:00"
title = "nurseAssessment"
linktitle = "nurseAssessment"
weight = 10
toc = "true"

[menu]
  [menu.main]
    parent = "Tables in eICU-CRD"
+++

# nurseAssessment

**Purpose:**

The Nursing Assessment Flowsheet provides the capability to assess and document patient items such as pain, psychosocial status, patient/family education, neurologic, cardiovascular, respiratory, oral/GI/GU, skin, and other nursing assessment data.

**Links to:**

* PATIENT on `patientUnitStayID`

<!-- # Important considerations

* To follow. -->

# Table columns

Name | Datatype | Null Option | Comment | Is Key | Stored Transformed Created
---- | ---- | ---- | ---- | ---- | ----
`nurseAssessID` | int | IDENTITY | surrogate key for the nurse assessment | PK | C
`patientUnitStayID` | int | NOT NULL | foreign key link to the patient table | FK | C
`nurseAssessYear` | smallint | NOT NULL | year of the nurse assessment column date |  | T
`nurseAssessTime24` | time(0) | NOT NULL | time in 24 hour format of the assessment column e.g.: "12:45", "15:30", "3:45" |  | T
`nurseAssessTime` | varchar(20) | NOT NULL | time frame of the nurse assessment column date: 'midnight', 'morning', 'midday', 'noon', 'evening', or 'night' |  | T
`nurseAssessOffset` | int | NOT NULL | number of minutes from unit admit time that nurse assessment column |  | C
`nurseAssessEntryYear` | smallint | NOT NULL | year when the nurse assessment column date was entered |  | T
`nurseAssessEntryTime24` | time(0) | NOT NULL | time in 24 hour format of when the assessment column was entered e.g.: "12:45", "15:30", "3:45" |  | T
`nurseAssessEntryTime` | varchar(20) | NOT NULL | time frame of when the nurse assessment item was entered: 'midnight', 'morning', 'midday', 'noon', 'evening', or 'night' |  | T
`nurseAssessEntryOffset` | int | NOT NULL | number of minutes from unit admit time that nurse assessment column was entered |  | C
`cellAttributePath` | varchar(255) | NOT NULL | the full path string of the nurse assessment entry selected in eCareManager, the sections of the assessment will be separated by a | symbol e.g.: flowsheet|Flowsheet Cell Labels|Nursing Assessment|Scores|Braden Scale|Activity |  | S
`cellLabel` | varchar(255) | NOT NULL | label of the selected nurse assessment entry |  | S
`cellAttribute` | varchar(255) | NOT NULL | attribute for the nurse assessment entry selected in eCareManager |  | S
`cellAttributeValue` | varchar(7500) | NULL | value for the nurse assessment attribute selected for the nurse assessment entry in eCareManager |  | S

<!--
# Detailed description

* To follow. -->
