# Take back your data!

Bring Your Own Data and Algorithms (BYODA) is a radical, new, and, open social media platform:
- All your data is stored in your own personal data server (your 'pod'), running in the cloud. You have full access to your data and full control to give and withdraw access to that data to others.
- Anyone can develop apps and services on the platform, lowering the effort required to develop new social media services.
- The platform is open source; every one can contribute or review the code.

With this platform, we can build new services where you can:
- chose a recommender algorithm to generate your feed.
- define your own monetization strategy for content you create.
- select who you want to moderate content for you.
- have your identity confirmed by a trusted third party and use your identity across multiple services.

We came up with the idea of BYODA after watching the documentary 'The Social Dilemma' on the dangerous impact of social networking services on our mental health and on our societies. We believe a fundamental redesign of social media services is needed, where we decouple the core functionalities of a social media service and enable people to chose who they want to provide these various functionalities for them.

The alpha release of reference implementation of the BYODA pod is available on [Github](https://github.com/byoda/byoda-python), including [instructions](https://github.com/byoda/byoda-python/blob/master/docs/infrastructure/clouds.md) on how to get your pod up and running on either Azure, Amazon Web Services, or Google Cloud. With the alpha release of the pod now available, we are now focussing on implementing a demo service to show to power of the concept.

Storing data in your own pod is not a new concept but BYODA introduces a data contract between you and a service you sign up for. The data contract is a technical specification of all data that the service can store and fetch from your data pod. In [some blog articles I wrote](https://stevenhessing.medium.com/), you can read more about how this data contract can fundamentally change how social media services work.
