# superoffice-connector

Example account_id: `Cust41399`

Note that the system, token_url and login_url currently points to the `sod` (development) environment, if you want to use the connector against the `online` (production) environment these urls need to be updated.

## Template Breakdown
- Supports Webhooks, Continuation, PATCH operations, and Writing
  - Master template: **contact.json**
  - Datatypes:
    - Contact
    - Person
    - Project
    - Sale
    - Ticket
- Supports Continuation, and Writing
  - Master template: **product.json**
  - Datatypes:
    - Product
- Supports Continuation, PATCH operations, and Writing
  - Master template: **pricelist.json**
  - Datatypes:
    - Pricelist
- Supports Writing and Uses Default Lookup
  - Master template: **listbusinessitems.json**
  - Datatypes:
    - listbusinessitems
    - listcategoryitems
    - listproductcategoryitems
    - listproductfamilyitems
    - listproducttypeitems
    - listprojectstatusitems
    - listprojecttypeitems
    - listsaletypeitems
    - listticketcategoryitems
- Supports Writing
  - Master template: **listcurrencyitems.json**
  - Datatypes:
    - listcurrencyitems
- Read Only, Need to Add _id
  - Master template: **listcountryitems.json**
  - Datatypes:
    - listcountryitems
- Read Only, Supports Continuation
  - Master template: **role.json**
  - Datatypes:
    - role
- Read Only
  - Master template: **user.json**
  - Datatypes:
    - user
- Quote infrastructure, each datatype has its own template in order to implement the right parent/child relationships and particular share template
  - quote.json
  - quoteversion.json
  - quotealternative.json
  - quoteline.json
- System infrastructure, system operations and webhook setup
  - system.json
  - webhook.json