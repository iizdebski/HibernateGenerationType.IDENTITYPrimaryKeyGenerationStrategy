# HibernateGenerationType.IDENTITYPrimaryKeyGenerationStrategy

GeneratinTyoe.IDENTITY

The GeneratinType.IDENTITY is the easiest to use. It relies on an auto-incremented database column and lets the database generate a new value with each insert operation. From a database point of view, this is very efficient because the auto-increment columns are highly optimized, and it doesn’t require any additional statements.

@Id

@Column(name=”employee_id”)

@GeneratedValue(strategy=GeneratedType.IDENTITY)

Private Integer employeeId;

This approach has a significant drawback if you use Hibernate. Hibernate requires a primary key value for each managed entity and therefore has to perform the insert statement immediate. This prevents it from using different optimization techniques like JDBC batching. 
