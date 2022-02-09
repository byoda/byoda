## The data contract

The data contract is a technical specification written by a service that specifies for the pod of a member of the service:
  - What data will be stored
  - Who has access to the data: the member (aka. the owner of the pod), the service, or people in the network of the member
  - What type of access is granted: Create, Read, Update, Delete, Append and/or Search (let's abbreviate that to 'CRUDAS')

You can think of the data contract as a technical translation of the privacy policy of the service, but then documented with each and every detail of the data to be collected and stored for a member of the service. The pod implements a _data firewall_ that reviews each incoming request for pieces of data in the pod against the access rules specified in the service contract and processes the request accordingly.

After creating the data contract, a service digitally signs the data contract and then submits the contract to the network to review and sign. When a person wants to become a member of a service, they have to accept the data contract for that service. If the service latest updates its data contract, it must again submit the contract to the network for review and signature. The members of the service must then explicitly accept the new version of the data contract before the pod will start using the new contract.

The data stored for a service in the pod is for exclusive use by you, the service the data is stored for and the people in your network for that service. The pod implements a namespace for each service and services can not access data stored per the data contract of other services.

The data contract is specified in a [JSON Schema](https://json-schema.org/) document. The data pod parses the specification and generates a [GraphQL](https://graphql.org/) API for queries for the data in the contract. All GraphQL queries are evaluated against the access rules in the data contract.
