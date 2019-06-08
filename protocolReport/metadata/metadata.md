# Metadata 
## Metadata Application Profile

The creation of the VaxStats’ metadata schema was guided by the needs of users, with regard to both consumption and submission of data. As the primary focus of the VaxStats’ repository is government created documents and reports, the metadata schema was modeled after Project Open Metadata’s, whose primary purpose is to describe datasets and other publications produced by government agencies. VaxStats’ schema differs from Project Open metadata’s primarily by way of which fields are required.

VaxStats’ metadata schema is modeled according to the Data Catalog Vocabulary (DCAT), an RDF vocabulary which uses terminology from the Dublin Core Terms vocabulary. It is intended for use in government repositories, and was especially suited to the needs of VaxStats user community.


## Controlled Vocabulary

An additional controlled vocabulary was needed to exert control over the keywords that were used to describe submissions. As the terminology used to describe submissions was largely medical in nature, VaxStats’ leveraged the MeSH vocabulary provided by the National Library of Medicine to control potential keywords. By utilizing MeSH authorized terms, VaxStats is able to better facilitate discovery of content, as well as lay the foundation for integration into the semantic web.

MeSH does not control for every term that users have used to describe their datasets, and so an extension to the MeSH vocabulary was needed. These terms describe additional vaccines, such as IPV (Inactiviated Polio Vaccine), as well as entities who may be involved with data collection, such as the Department of Health, WHO, and the CDC. 

## JSON Schemas

The metadata application profiles have been provided in JSON, a machine readable format. The schemas are conformant with the most recent release of JSON schema specifications, draft 07.
