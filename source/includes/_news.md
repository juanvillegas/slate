# News and Updates

## Updates Week 3 - May 2018

### Breaking changes on Incident Update response

Until today, the api responded with the string 'updated' in the data property of the returned JSON.
This has been removed to standardize the responses of the api in general.

### Diagnosis Codes removed from Patient, added to Incident

As of now, Diagnosis Codes are a property of the Incident model, not the Patient anymore.

Also, the database now supports having Incidents with many Diagnosis Codes. At the moment, the 
limit is capped to 2 codes per Incident.

To set the Diagnosis Codes for an Incident, use the new "diagnosis_codes" property of the Incident model
to provide the ids of the desired Diagnosis Codes. More information in the corresponding endpoint description.