### Summary of Last Lecture: Conceptual Model

In the last lecture, we covered the basics of the **Conceptual Model** in data modeling. This model focuses on representing the high-level structure of the data without going into the technical details. Key points included:
- Identifying entities and their relationships.
- Understanding the overall architecture of the data without diving into specifics like attributes or keys.
- Entities identified: Employee, Department, Role, Role Assignment, Project, Project Assignment.

### Logical Data Model

The **Logical Data Model** refines the conceptual model by adding attributes to the entities and defining primary and foreign keys. Here are the steps followed in logical modeling:

#### Steps in Logical Modeling

1. **Create Attributes for Entities**:
    - **Employee**: Employee number, Employee name, Job, Salary, Hire date, Department number.
    - **Department**: Department number, Department name, Location name, City type.
    - **Role**: Role ID, Role name.
    - **Role Assignment**: Assignment ID, Employee number, Role ID.
    - **Project**: Project ID, Project name.
    - **Project Assignment**: Assignment ID, Employee number, Project ID.

2. **Identify Primary Keys**:
    - **Employee**: Employee number (unique identifier).
    - **Department**: Department number (unique identifier).
    - **Role**: Role ID (unique identifier).
    - **Role Assignment**: Assignment ID (unique identifier).
    - **Project**: Project ID (unique identifier).
    - **Project Assignment**: Assignment ID (unique identifier).

3. **Normalize the Database**:
    - **Normalization**: Ensuring that the data model is free of redundancy and dependency issues.
    - **First Normal Form (1NF)**: Ensuring that the table contains only atomic (indivisible) values.
    - **Second Normal Form (2NF)**: Ensuring that the table is in 1NF and all non-key attributes are fully functional dependent on the primary key.
    - **Third Normal Form (3NF)**: Ensuring that the table is in 2NF and all attributes are not only fully functional dependent on the primary key but also non-transitively dependent.
    - **Example**: Department table normalization
        - Original attributes: Department number, Department name, Location name, City type.
        - Identified dependencies: Department number -> Location name, Location name -> City type.
        - Transitive dependency: Department number -> City type.
        - Solution: Split into two tables:
            - **Department Table**: Department number, Department name, Location ID (foreign key).
            - **Location Table**: Location ID (primary key), Location name, City type.

4. **Validation and Refinement**:
    - **Validate the Data Model**: Ensure the model is correct and consistent using data modeling tools.
    - **Iterate and Refine**: Continuously improve and refine the data model through iterations.

#### Example Diagrams

- **Conceptual Model**: High-level entities and relationships without attributes.
- **Logical Model**: Entities with attributes, primary keys, foreign keys, and normalized structure.

### Moving Forward

In the next lecture, we will discuss the final stage of data modeling: the **Physical Data Model**. This stage involves translating the logical model into a schema that can be implemented in a specific database management system (DBMS).

### Conclusion

The logical data model is a crucial step in data modeling as it bridges the gap between high-level concepts and detailed implementation. By defining attributes, primary keys, and normalizing the data, we ensure a robust and efficient database design.
