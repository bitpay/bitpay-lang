# Client

## Data Requirements

### A client should return a PEM file with its keys on request
### A single client has a single token
### Export/Import
* A client should export to a a JSON of the form
    ```json
    {  
       api_uri: <api_uri string>
       pem: <pem string>
       token: { 
                pairing_code: <string>
                facade: <string>
                token: <string>
              } 
    }
* Given a json string of the prior form, we should generate a workable client

## Validation Requirements
* Clients check the semantic correctness of pairing codes
* Clients validate the format of currency when creating invoices
* Clients validate the format of amounts when creating invoices
