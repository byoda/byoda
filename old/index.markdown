---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: home
---
## BYODA, open-source social media platform where you own your data

Bring Your Own Data and Algorithms is a new open source social media platform that refactors the technology behind social media services:
  - People operate their own _data pods_ that store their data for services that they have joined. They can revoke access to, or remove data from their pod at any time.
  - A _data contract_ documents the information stored on behalf of the service in your data pod and who has access to that data.

Byoda is a social media platform, not a service. it delivers the building blocks to deliver and consume services but does not offer services itself.

The [first release of Byoda](https://github.com/StevenHessing/byoda-python) is now available. This release includes:
  - The data pod that people can run on a VM in Amazon Web Services, Microsoft Azure, Google Cloud or a server in their home.
  - The ‘Address Book’ proof-of-concept service that people can use to find other people that joined the Address Book service
  - A reference implementation of a service running on a BYODA network
  - The byoda.net network

Byoda introduces the _data contract_, a technical specification that describes the data that a service collects from its members. When someone joins a service, they have to accept the data contract for that serqvice. Their pod implements a _data firewall_ that enforces the accepted data contract when it receives a request to store or retrieve data for the service. The data firewall implements a separate namespace for each service to silo off the data from other services.
