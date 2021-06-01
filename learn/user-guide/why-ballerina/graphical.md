---
layout: ballerina-left-nav-pages-swanlake
title: Graphical
description: See why the support for a graphical model lays the foundation for designing the syntax and semantics of the Ballerina programming language.
keywords: ballerina, programming lanaguage, sequence diagram, graphical, diagram editor, why ballerina
permalink: /learn/user-guide/why-ballerina/graphical/
active: graphical
intro: See why the support for a graphical model lays the foundation for designing the syntax and semantics of the Ballerina programming language.
redirect_from:
  - /why/sequence-diagrams-for-programming/
  - /why/sequence-diagrams-for-programming
  - /learn/user-guide/why-ballerina/sequence-diagrams-for-programming
  - /learn/user-guide/why-ballerina/sequence-diagrams-for-programming/
  - /learn/user-guide/why-ballerina/graphical
---

In today’s cloud era, technologies that can model distributed systems in a more developer-friendly way are required. This means that for a single use case, you need to model a flow that shows how multiple actors interact with each other, how concurrent execution flows, and what remote endpoints are involved. Sequence diagrams are known to be the best way to visually describe this.

That’s why sequence diagrams are the foundation for designing the syntax and semantics of the Ballerina language. Ballerina provides the flexibility of a general-purpose language while having features to model solutions based on higher-level abstractions.

> ***"[With Ballerina] you can get sequence diagrams automatically. When things start to get complicated and you need to understand and socialize with the rest of your team what it is that you're building, these diagrams become very helpful." -- Christian Posta, field CTO, solo.io***

## Sequence Diagrams in Ballerina

 In Ballerina, there is a bidirectional mapping between the textual representation of code in the Ballerina syntax and the visual representation as a sequence diagram. It allows you to visualize any function or a service resource written in Ballerina as a sequence diagram. The diagram will display all the logic and network interaction of that function. You can view these diagrams using the Ballerina VSCode plugin.

<img src="/img/why-pages/sequence-diagrams-for-programming-1.png" alt="Ballerina sequence diagram" width="700">

One of the key benefits of the diagram is that it acts as documentation to the code. It makes it far easier to comprehend the program than reading the source code. Even if you are not familiar with Ballerina code syntax it is easier to understand the diagram. 


### Get Started

The Ballerina IDE plugin ( the [VSCode plugin](https://ballerina.io/learn/tooling-guide/vs-code-extension/installing-the-vs-code-extension/)) can generate a sequence diagram dynamically from the source code. To start generating a sequence diagram from your Ballerina code, [download the VSCode plugin and launch the graphical ](https://ballerina.io/learn/tooling-guide/vs-code-extension/installing-the-vs-code-extension/)viewer.


## Graphical Syntax


### Functions 

Functions in Ballerina are visualized as a sequence diagram. The diagram will have a lifeline with start and end which represent the default worker of the function. The worker lifeline will be displayed as a flow diagram to represent function logic. 



<img src="/img/why-pages/sequence-diagrams-for-programming-2.png" alt="Ballerina sequence diagram of HTTP resource definition" width="700">


### Client Objects and Remote Methods

Ballerina has special network client objects, like HTTP clients and database connections, that have their own lifeline to represent its functionality and the messages that it can receive. The messages sent to or the invocations done on these network clients are called _remote methods_ — a special method inside a client object that represents a call through the network. Remote calls are distinguished from normal method calls by using the arrow “`->`” notation.

The following code shows an HTTP client that is used to do GET and POST requests to a remote endpoint:


```
function execute() returns error?{
   http:Client lookupService = check new(lookupUrl);
   http:Client reportService = check new(reportUrl);

   json result = check lookupService->get("/query");
   http:Response response = check reportService->post("/report", result);
}
```


The HTTP clients represented by `lookupService` and `reportService` variables are of type `http:Client`, which represents remote HTTP endpoints. The following diagram shows the generated sequence diagram for the above remote method calls



<img src="/img/why-pages/sequence-diagrams-for-programming-3.png" alt="Ballerina sequence diagram of HTTP resource definition" width="700">


We can see here how the HTTP clients have become participants of the sequence diagram with its own lifeline, where we visualize the messages sent and received to represent the network calls we do.
