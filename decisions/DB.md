## Database Choice and Rationale

After careful consideration, we have chosen a **relational database** to handle our application's storage requirements. Specifically, we are using **PostgreSQL**.

### Why Choose a Relational Database Over NoSQL (Key-Value or Document-Based)?

At first glance, a NoSQL solution—such as a key-value store or document database like **Amazon DocumentDB**—seemed sufficient for storing simple short and long URL pairs. However, as we scoped out future features and scalability plans, a relational database became the preferred option for several key reasons:

1. **User-Specific Link Management**  
   Our application supports user-specific link customization and sharing. Relational databases are ideal for modeling and maintaining relationships between users and their links, ensuring data consistency and integrity.

2. **Subscription-Based URL Creation**  
   Managing subscription tiers involves handling access levels, quotas, and billing logic. These are best modeled using a structured relational schema with constraints, joins, and transactional support.

3. **Scalability and Evolving Feature Set**  
   As we build more features, the need for structured queries, data validations, and foreign key relationships grows. Relational databases are more adaptable for these evolving needs and ensure long-term maintainability.

Given these requirements, a relational database provides significantly more flexibility and value than a NoSQL approach in our use case.

### Why PostgreSQL Over Other Relational Databases?

There are many excellent relational databases to choose from. We selected **PostgreSQL** for the following reasons:

1. **Open Source with Strong Community Support**  
   PostgreSQL is a mature, open-source database with a vibrant and active community. Compared to alternatives like MySQL, it offers greater flexibility, fewer licensing concerns, and broader ecosystem support.

2. **Advanced Feature Set**  
   PostgreSQL provides a range of advanced features out of the box that align well with our requirements, including:
   - Support for returning full rows on `INSERT` operations (not just IDs), streamlining application logic.
   - Robust indexing and query planning capabilities.
   - Native support for JSON and other semi-structured data formats.
   - Rich extension ecosystem (e.g., PostGIS for geospatial data, pg_cron for scheduling).

3. **Scalability and Performance**  
   With its well-architected concurrency model and support for large-scale data, PostgreSQL is well-suited for applications expected to grow in both complexity and traffic.

---

While no database is a one-size-fits-all solution, **PostgreSQL** offers the right balance of power, flexibility, and reliability for our current and future application needs.
