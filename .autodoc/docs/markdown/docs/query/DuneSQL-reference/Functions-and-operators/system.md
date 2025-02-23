[View code on GitHub](https://dune.com/docs/query/DuneSQL-reference/Functions-and-operators/system.md)

# System Information

This section of the app technical guide for the Dune Docs project covers functions that provide information about the Trino cluster system environment. The Trino cluster is a distributed SQL query engine designed to query large datasets. The functions described in this section can be used to obtain information about the version of Trino being used on the cluster.

The `/connector/system` exposes various schemas and tables that can be queried to obtain more information about the Trino cluster system environment. The `version()` function is one such function that can be used to obtain the Trino version used on the cluster. This function returns a varchar value that is equivalent to the value of the `node_version` column in the `system.runtime.nodes` table.

Here is an example of how to use the `version()` function:

```
SELECT version();
```

This query will return the Trino version used on the cluster.

Overall, this section of the app technical guide provides developers with the necessary information to obtain system information about the Trino cluster. This information can be useful for debugging and optimizing queries.
## Questions: 
 1. What is the purpose of the Trino cluster system environment in the context of blockchain SQL analysis?
- This app technical guide provides functions that offer information about the Trino cluster system environment. A blockchain SQL analyst might want to know how this environment can be utilized for their analysis.

2. How does querying the `/connector/system` schema and tables relate to blockchain data analysis?
- The app technical guide mentions that querying the various schemas and tables exposed by the `/connector/system` can provide more information about the Trino cluster system environment. A blockchain SQL analyst might want to know how this information can be used in their analysis.

3. Is the `system.runtime.nodes` table relevant to blockchain data analysis?
- The `version()` function returns the value of the `node_version` column in the `system.runtime.nodes` table. A blockchain SQL analyst might want to know if this table contains any relevant information for their analysis.