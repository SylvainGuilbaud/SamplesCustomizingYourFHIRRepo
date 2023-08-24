# Customizing Your InterSystems FHIR Repo Sample
This respository provides sample code that shows how you can customize the InterSystems IRIS for Health FHIR Repository.
It was created along with a presentation delivered at InterSystems Global Summit 2023.

The use cases addressed with the code in this repo are:

1. Input – pre-processing
- Resource IDs must be globally unique
- Identifiers for a resource must be unique
2. Output – post-processing
- References must be enriched with a display value
- Resource.text must be populated
- Ordering (json) resource properties as defined in the specification (resourceType, id, meta, text, extension)
3. Debugging using $$$FSLog()
4. References
- Referential Integrity must be ensured for  create, update and delete
- Logical references and conditional references must be transformed into a literal reference


These use cases are further explained in the accompanying presentation (to be added to this repo).

## Set Up
No docker has been provided as part of this repo. It is recommended that you connect to a local InterSystems IRIS instance and import / compile.

Create a new FHIR Server in this namespace with the following settings:
	-Core FHIR package: hl7.fhir.r4.core@4.0.1
	-Additional packages: MyFhirServer-searchparameters@0.0.1
	-Interactions strategy class: HS.Local.FHIRServer.Storage.Json.InteractionsStrategy

## Run the Sample
A [Postman collection](https://github.com/intersystems/SamplesCustomizingYourFHIRRepo/blob/2718e8db7973206cacbb4ffdd2c05e91e5d033b3/My%20Customized%20FHIR%20Server.postman_collection.json) is available to test the customizations

## Documentation
The following InterSystems IRIS for Health Documentation is helpful as background information:

[FHIR Server: An Introduction](https://docs.intersystems.com/irisforhealth20231/csp/docbook/Doc.View.cls?KEY=HXFHIR_server_intro)

[Customizing a FHIR Server](https://docs.intersystems.com/irisforhealth20231/csp/docbook/DocBook.UI.Page.cls?KEY=HXFHIR_server_customize_arch)

The FHIR specification

[RESTful API](https://hl7.org/fhir/R4/http.html)

[Search](https://hl7.org/fhir/R4/search.html)

[References](https://hl7.org/fhir/R4/references.html)

## Bugslist
There are no known bugs at this point in time

## Finally
Use or operation of this code is subject to acceptance of the license available in the code repository for this code.

