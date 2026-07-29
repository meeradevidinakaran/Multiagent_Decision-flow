# Tradeoffs

**Costing( Token Utilization / Infra ) Vs Quality of the Decisions** - This is always a crucial tradeoff. Business scenarios/Use case is always the ruling factor to help assess what is the priority of the workflow. How automated do you want the flow to be? A Human in the loop is essential but how are you easing the load on the human? Quality gates are non negotiable when you are building high stake production ready workflows.

**Complexity Vs Maintainability**- While the Complex Architecture tackels the real life PM scenario. Each additional agent and database integration is a new "point of failure." We must balance the "trustworthiness" of the output against efforts required to maintain and debug a complex orchestration.

**RAG Maintenance** - While RAG helps with token limits by only retrieving relevant features, it also introduces risk of stale data. tradeoff between the cost of Real-time Syncing (constantly updating the Vector DB with new Jira/Productboard requests) vs. the risk of the agent making decisions based on week-old data is worth considering before implementation as per the use case.
