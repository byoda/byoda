## BYODA, the _privacy-first_ social media platform

Bring Your Own Data and Algorithms is a new open source social media platform that refactors the technology behind social media services:
- People operate their own _data pods_ that store their data for services that they have joined. They can revoke access to, or remove data from their pod at any time.
- A _service contract_ documents the information stored on behalf of the service in your data pod and who has access to that data.

Byoda is a social media platform, not a service. it delivers the building blocks to deliver and consume services but does not offer services itself.

The [first release of Byoda](https://github.com/StevenHessing/byoda-python) is now available. It is an alpha release, meaning the a subset of the final product has been implemented and it requires some linux-in-the-cloud skills to deploy. This release includes:
- The data pod that people can run on a VM in Amazon Web Services, Microsoft Azure, Google Cloud or a server in their home.
- The 'Address Book' proof-of-concept service that people can use to find other people that joined the Address Book service
- A reference implementation of a service running on a BYODA network
- The byoda.net network

Byoda introduces the [_data contract_]({% post_url datacontract %}), a technical specification that describes the data that a service collects from its members. When someone joins a service, they have to accept the data contract for that service. Their pod implements a _data firewall_ that enforces the accepted data contract when it receives a request to store or retrieve data for the service. The data firewall implements a separate namespace for each service to silo off the data from other services.

I came up with the idea of BYODA after watching the documentary ['The Social Dilemma'](https://www.thesocialdilemma.com/) on the dangerous impact of social media companies on our own mental health and on our society as a whole. In addition, the online advertising industry breaches our right to privacy by [extracting our data and monetizing it](https://en.wikipedia.org/wiki/Surveillance_capitalism) in any form they can. Byoda addresses both these issues by delivering the _privacy-first_ social media platform.
