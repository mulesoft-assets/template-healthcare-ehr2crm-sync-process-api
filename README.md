# Template EHR to CRM Sync Process API

With the systems like Salesforce Health Cloud there is a need to bridge patient data from EHRs like Epic to a more light-weight patient management systems. This template provides an API implementation best practice to synchronize patient and its related data from EHR into system like Salesforce Health Cloud. This Process API encapsulates the underlying business processes that interact with source and target systems via a set of FHIR System APIs.

![](https://www.lucidchart.com/publicSegments/view/6c0eab9d-b684-43bd-96c5-61b323fd6399/image.png)

## Implementation Flow in Anypoint Studio

![021c12f7-8f84-4d43-a725-b2ac1b6a0c82-image.png](https://exchange2-file-upload-service-kprod.s3.us-east-1.amazonaws.com:443/021c12f7-8f84-4d43-a725-b2ac1b6a0c82-image.png)

## Accelerator for Healthcare

This API implementation is one of many components included in [Accelerator for Healthcare](/exchange/68ef9520-24e9-4cf2-b2f5-620025690913/catalyst-accelerator-for-healthcare/). This API provides organizations with connectivity assets that accelerate project delivery in healthcare, including pre-built API designs and implementations that support core healthcare business processes. Contact [info@mulesoft.com](mailto:info@mulesoft.com) for more information.

# License Agreement 
This template is subject to the conditions of the [MuleSoft License Agreement](https://s3.amazonaws.com/templates-examples/AnypointTemplateLicense.pdf). Review the terms of the license before downloading and using this template. You can use this template for free with the Mule Enterprise Edition, CloudHub, or as a trial in Anypoint Studio. 

# Use Case

As a user of Healthcare API Led Connectivity Web Portal I want a microservice to act as a process API to perform synchronization of data between EHR medical system and Salesforce Health Cloud instance.

EHR to CRM Sync Process API is part of the Healthcare Templates Solution and uses the standardized FHIR structures [version 3.0.1 STU3](https://www.hl7.org/FHIR/index.html).

The API is defined using [RAML 1.0](http://raml.org/) to provide type information for validation of requests and to help with the data transformation during development by providing useful metadata.
Both EHR and CRM system share the same API definition.

Synchronization of the following FHIR objects are supported by this API:

 - AllergyIntolerance
 - Appointment
 - Condition
 - Patient

# Considerations

To run this template, there are certain preconditions that must be considered. Failing to do so could lead to unexpected behavior of the template.

### Run the Application


# Run it!
Simple steps to get Healthcare EHR to CRM Sync Process API running.
See below.

## Run On Premises
In this section we detail the way you should run your template on your computer.

### Where to Download Anypoint Studio and the Mule Runtime

If you are new to Mule, download this software:

- [Download Anypoint Studio](https://www.mulesoft.com/platform/studio)
- [Download Mule runtime](https://www.mulesoft.com/lp/dl/mule-esb-enterprise)

### Import a Template into Studio
Anypoint Studio offers several ways to import a project into the workspace, for instance: 

- Anypoint Studio Project from File System
- Packaged mule application (.jar)

You can find a detailed description on how to do so in this [About Anypoint Studio](https://docs.mulesoft.com/studio/7.3/).

### Run in Studio

After opening your template in Anypoint Studio, follow these steps to run it:

1. Locate the properties file `mule.dev.properties`, in src/main/resources.
2. Complete all the properties in the "Properties to Configure" section.
3. Right click the template project folder.
4. Hover your mouse over `Run as`.
5. Click `Mule Application (configure)`.
6. Inside the dialog, select Environment and set the variable `mule.env` to the value `dev`.
7. Click `Run`.

### Run on Mule Stand Alone
Add properties to a property file, for example in mule.prod.properties, and run your application with an environment variable for each property. In this example, use `mule.env=prod`.

## Run on Runtime Manager
When creating your application in Runtime Manager, click an application and click **Manage Application** > **Properties** to set the environment variables described in the Properties to Configure section.

## Deploy in CloudHub
In Studio, right click your project name in Package Explorer and select **Anypoint Platform** > **Deploy on CloudHub**.

## Properties to Configure
To use this template, configure properties in a properties file or in Runtime Manager as environment variables.

### Application Properties

- http.port `8081`

- ehr.system.api.host `ehr-system-api.cloudhub.io`
- ehr.system.api.port `80`
- ehr.system.api.basePath `/api`
- ehr.system.api.protocol `HTTP`

- sfdc.system.api.host `sfhc-system-api.cloudhub.io`
- sfdc.system.api.port `80`
- sfdc.system.api.basePath `/api`
- sfdc.system.api.protocol `HTTP`
