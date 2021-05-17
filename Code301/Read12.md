# SQL vs NoSQL: High-Level Differences

* **SQL** databases are primarily called as Relational Databases (RDBMS); whereas **NoSQL** database are primarily called as non-relational or distributed database.

* **SQL** databases are table based databases whereas **NoSQL** databases are document based, key-value pairs, graph databases or wide-column stores. This means that **SQL** databases represent data in form of tables which consists of n number of rows of data whereas **NoSQL** databases are the collection of key-value pair, documents, graph databases or wide-column stores which do not have standard schema definitions which it needs to adhered to.

* **SQL** databases have predefined schema whereas **NoSQL** databases have dynamic schema for unstructured data.

* **SQL** databases are vertically scalable whereas the **NoSQL** databases are horizontally scalable. **SQL** databases are scaled by increasing the horse-power of the hardware. **NoSQL** databases are scaled by increasing the databases servers in the pool of resources to reduce the load.

* **SQL** databases uses **SQL** ( structured query language ) for defining and manipulating the data, which is very powerful. In **NoSQL** database, queries are focused on collection of documents. Sometimes it is also called as UnQL (Unstructured Query Language). The syntax of using UnQL varies from database to database.

* For complex queries: **SQL** databases are good fit for the complex query intensive environment whereas **NoSQL** databases are not good fit for complex queries. On a high-level, NoSQL don’t have standard interfaces to perform complex queries, and the queries themselves in **NoSQL** are not as powerful as **SQL** query language.

* For the type of data to be stored: **SQL** databases are not best fit for hierarchical data storage. But, **NoSQL** database fits better for the hierarchical data storage as it follows the key-value pair way of storing data similar to JSON data. **NoSQL** database are highly preferred for large data set (i.e for big data). Hbase is an example for this purpose.

* For scalability: In most typical situations, **SQL** databases are vertically scalable. You can manage increasing load by increasing the CPU, RAM, SSD, etc, on a single server. On the other hand, **NoSQL** databases are horizontally scalable. You can just add few more servers easily in your NoSQL database infrastructure to handle the large traffic.

* For high transactional based application: **SQL** databases are best fit for heavy duty transactional type applications, as it is more stable and promises the atomicity as well as integrity of the data. While you can use **NoSQL** for transactions purpose, it is still not comparable and sable enough in high load and for complex transactional applications.

* For DB types: On a high-level, we can classify **SQL** databases as either open-source or close-sourced from commercial vendors. **NoSQL** databases can be classified on the basis of way of storing data as graph databases, key-value store databases, document store databases, column store database and XML databases.
