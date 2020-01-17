FLY Best Practices
===

Before you get started with FLY, we recommend you consider the following information:

- It is important to understand that breaking up migrations into separate jobs can help increase performance, especially when the jobs are set to run either in sequence via a schedule or jobs are set to run on multiple agents.

- Including multiple agents in your FLY installation architecture can assist in overcoming obstacles to performance, especially in regard to latency and throttling. The size and structure of data for each job that runs can also affect performance.

- When installing FLY, scheduling jobs sequentially or having multiple agents can significantly increase performance when:

Data sets exceed 200 GBs

o  There are large numbers of site collections, mailboxes or other container objects (over 100)

o  Large numbers of items or documents (over 100,000)

o  Many items or documents with large amounts of metadata

o  Multiple agents can improve performance when the physical distance from server to server exceeds 500 (800 km) miles or has significant latency