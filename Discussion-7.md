# What are the problems with a “one size fits all” approach to relational databases?

The NoSQL movement, where “NoSQL” stands for “Not Only SQL” is based on the concept that relational databases are not the right database solution for all problems.  Relational databases are so ubiquitous in most organizations these days that many people may not even be aware that there are other types of databases, let alone when using another database might be preferable. Relational databases perform transaction update functions very well, particularly handling the difficult issues of consistency during update. Production strength relational databases can handle the complexity of two phase commit capability, where one business transaction affects multiple databases and tables, and all updates have to be effected at the same moment.
However, relational databases apply much of the same overhead required for complex update operations to every activity, and that can handicap them for other functions. Relational databases struggle with the efficiency of certain operations key to Big Data management. Firstly, they don’t scale well to very large sizes, and although grid solutions can help with this problem, the creation of new clusters on the grid is not dynamic and large data solutions become very expensive using relational databases. Secondly, they don’t do unstructured data search very well (i.e. google type searching) nor do they handle data in unexpected formats well. Thirdly, but not lastly, it is difficult to implement certain kinds of basic queries using SQL and relational databases, such as the shortest path between two points.

Social networking and Big Data organizations such as Facebook, Yahoo, Google, and Amazon were among the first to decide that relational databases were not good solutions for the volumes and types of data that they were dealing with, hence the development of the Hadoop file system, the MapReduce programming language, and associated databases such as Cassandra and HBase. One of the key capabilities of a Hadoop type environment is the ability to dynamically, or at least easily, expand the number of servers being used for data storage. The cost of storing large amounts of data in a relational database gets very expensive, where cost grows geometrically with the amount of data to be stored, reaching a limit in the petabyte range. The cost of storing data in a Hadoop solution grows linearly with the volume of data and there is no ultimate limit.

# How could a service like Google BigQuery change the way you deal with Data?




# What problem does a “serverless” database like Athena solve?
# Post a screenshot of a lab where you had difficulty with a concept or learned something.
