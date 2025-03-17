# Graph QL for NLGov

## Introduction

GraphQL is a query language and runtime for APIs, offering a flexible and efficient alternative to traditional REST API standards. It was developed by Facebook in 2012 and open-sourced in 2015. While REST has been the de facto standard for APIs, GraphQL addresses some of REST’s limitations, particularly around data fetching, flexibility, and over-fetching or under-fetching of data.

The most relevant quotes obtained from the Nordic API Summit in 2024 are:

> Rob Allen: APIs can be realised in any style but, which makes the most sense? 
>
> Arnaud Lauret: If you suck at providing REST APIs, you will suck at providing a GraphQL API !

The hype around GraphQL has passed and REST is still more popular. However, GraphQL surpasses OpenAPI and gRPC as the most trending topic. Where REST lacks functionality and efficiency, GraphQL gains traction and fills in the gaps.

## Links

- Official website: https://graphql.org/
- Repository: https://github.com/graphql/graphql-spec
- Wikipedia: https://en.wikipedia.org/wiki/GraphQL
- The GraphQL Specification - oktober 2021 -: https://spec.graphql.org/October2021/
- The GraphQL Specification - working draft -: https://spec.graphql.org/draft/
- The GraphQL foundation: https://graphql.org/community/foundation/
- Blog on mocking and testing GraphQL: https://microcks.io/blog/graphql-features-what-to-expect/
- Running an open source GraphQL backend: https://tailcall.run/


## Books

- [The GraphQL Guide](https://graphql.guide) by John Resig and Loren Sands-Ramshaw
- [Learning GraphQL](https://www.amazon.com/Learning-GraphQL-Declarative-Fetching-Modern/dp/1492030716/) by Eve Porcello and Alex Banks
- [Fullstack GraphQL](https://www.graphql.college/fullstack-graphql) by Julian Mayorga
- [Craft GraphQL APIs in Elixir with Absinthe](https://pragprog.com/book/wwgraphql/craft-graphql-apis-in-elixir-with-absinthe) by Bruce Williams and Ben Wilson
- [Learning GraphQL and Relay](https://www.packtpub.com/web-development/learning-graphql-and-relay) by Samer Buna
- [Hands-on Full-Stack Web Development with GraphQL and React](https://www.packtpub.com/web-development/hands-full-stack-web-development-graphql-and-react) by Sebastian Grebe
- [The Road to GraphQL](https://www.robinwieruch.de/the-road-to-graphql-book/) by Robin Wieruch
- [Production Ready GraphQL](https://book.productionreadygraphql.com/) by Marc-Andre Giroux
- [GraphQL Best Practices: Hands-on experience with schema design, security, and error handling for developers](https://www.amazon.com/dp/B0D9H7MJQV) by Artur Czemiel, Nov 2024

## Key Concepts of GraphQL in Relation to REST:

The folowing table lists ten concepts and relates the GraphQL aspects to the same aspects in a REST API

| **Concepts**             | REST API                                                     | GraphQL API                                                  |
| ------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
| **Endpoint Structure**   | Multiple endpoints for different resources (e.g., /users, /posts). | Single endpoint (e.g., /graphql) handles all queries, mutations, and subscriptions. |
| **Data Fetching**        | Server defines response structure, often causing over-fetching or under-fetching. | Clients define the exact data needed, reducing over-fetching and under-fetching. |
| **Schema**               | Relies on documentation and conventions for understanding data structure. | Uses a strongly typed schema that explicitly defines data types and relationships. |
| **Nested Queries**       | Requires multiple requests for related data, increasing latency. | Supports nested queries, enabling retrieval of related data in a single request. |
| **Versioning**           | New versions are handled via new endpoints (e.g., /v1/users, /v2/users). | Avoids versioning by evolving the schema, adding fields without breaking existing queries. |
| **Real-Time Data**       | Requires additional infrastructure like WebSockets or polling for real-time updates. | Native support for real-time updates via subscriptions.      |
| **Flexibility**          | Less flexible; data structure determined by the server.      | Highly flexible; clients control what data they receive.     |
| **Performance**          | Multiple requests may result in higher network overhead.     | Fewer API calls reduce network overhead and latency.         |
| **Learning Curve**       | Easier to learn and implement, with well-established conventions and tools. | Steeper learning curve, requiring understanding of schema design and query optimization. |
| **Potential Challenges** | Simple to scale but may require many endpoints for complex APIs. | Performance bottlenecks can arise from poorly optimized or overly complex queries. |



## Why GraphQL?

Back in 2012, we began an effort to rebuild Facebook’s native mobile applications.

At the time, our iOS and Android apps were thin wrappers around views of our mobile website. While this brought us close to a platonic ideal  of the “write once, run anywhere” mobile application, in practice it  pushed our mobile-webview apps beyond their limits. As Facebook’s mobile apps became more complex, **they suffered poor performance** and frequently crashed.

As we transitioned to natively implemented models and views, we found ourselves for the first time needing an API data version of News Feed — which up until that point had only been delivered as HTML. We evaluated our options for delivering News Feed data to our mobile apps, including RESTful server resources and FQL tables (Facebook’s SQL-like API). We  were frustrated with **the differences between the data we wanted to use  in our apps and the server queries they required**. We don’t think of data in terms of resource URLs, secondary keys, or join tables; we think  about it in terms of a graph of objects and the models we ultimately use in our apps like NSObjects or JSON.

There was also **a considerable amount of code to write on both the  server to prepare the data and on the client to parse it**. This  frustration inspired a few of us to start the project that ultimately  became GraphQL. GraphQL was our opportunity to **rethink mobile app  data-fetching** from the perspective of product designers and developers.  It moved the focus of development to the client apps, where designers  and developers spend their time and attention.

> Bron: https://engineering.fb.com/2015/09/14/core-infra/graphql-a-data-query-language/

## Bennefits, challenges, advantages & limitations

GraphQL became a hype after it was published as open source back in 2015. In the post-hype era the interest in GraphQL has been stable for the past years. 

### Benefits of GraphQL Over REST:

- Greater flexibility and control for clients.
- Reduced network overhead due to fewer API calls.
- Self-documenting APIs through the schema and introspection capabilities.

### Advantages of GraphQL:

- Efficient Data Loading by reducing over-fetching and under-fetching.
- Strongly Typed services define a set of types which completely describe the set of possible data.
- Rapid Development based on the declarative nature and strong type system


### Challenges of GraphQL:

- Steeper learning curve compared to REST.
- Potential for complex queries leading to performance bottlenecks.
- Requires careful server-side implementation to prevent over-fetching or inefficient database queries.

### Limitations of GraphQL

- Complexity in Client for constructing complex queries and managing the resulting data structures
- Caching in GraphQL can't leverage HTTP caching mechanisms because each query can be unique. This requires more sophisticated caching strategies.
- Authorization other than the entire endpoint

## Positioning GraphQL in relation to the NL API Strategy & Digikoppeling

First of all you should comply with the [NL API Strategy](https://apigov.nl) and the [API Design Rules](https://gitdocumentatie.logius.nl/publicatie/api/adr/2.0.2/) and develop relevant REST API's for your situation.

When implementing API's for G2G and M2M the [Digikoppeling REST profile](https://gitdocumentatie.logius.nl/publicatie/dk/restapi/) must be implemented.

Finally, when addressed with poor performance and data overhead in client and server you must consider adding GraphQL aside of REST for specific groups of users.



## Conclusions

Both GraphQL and REST facilitate data exchange between client and server in a client-server model, using HTTP as the underlying communication protocol.

GraphQL complements REST rather than replacing it entirely. In scenarios requiring fine-grained data fetching or complex relationships, GraphQL excels, while REST remains a robust choice for simpler APIs or when compliance with existing standards and tooling is a priority.

GraphQL is a good choice as long as you have straightforward business logic, transparent data structures, or a rapidly evolving schema. GraphQL’s focus ensures you get *exactly* and *only* what you need.

If you’re building an app or system where caching or fine-grained authorization is important, then REST would be more suitable, thanks to its built-in HTTP caching and authorization capabilities.

Either way, both formats have strong points that make them worth considering. Start simple with REST and add GraphQL when the advantages are clear and the limitations can be overcome.