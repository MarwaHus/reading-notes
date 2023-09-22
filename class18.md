# Class 18

### Many to many relationships
1. Name a few examples of real world ManyToMany relationships.<br>
* A student taking multiple courses and a course having multiple students enrolled.
* A bookstore selling multiple books and a book being sold by multiple bookstores.
* A patient having multiple doctors and a doctor treating multiple patients.

2. Explain the significance of a join table for ManyToMany relationships.<br>
    A join table is used for ManyToMany relationships to create an association between the primary keys of two tables without introducing a circular reference, which would cause problems in database management. The join table serves as an intermediary table that maps the relationship between the two tables.


3. What are the values held within a join table?<br>
   The join table typically holds the foreign keys of the primary tables involved in the relationship. For example, in the employee-project ManyToMany relationship described in the tutorial, the join table `employee_project` holds the `employee_id` and `project_id` columns that link the `Employee` and `Project` tables, respectively. Additional values may be stored in the join table if the ManyToMany relationship requires additional information, such as a join table storing the date a student enrolled in a course.

### Security: a humorous overview
1. According to the author of the article, will you ever be truly secure from ALL possible security threats?<br>
   According to the author, it's unlikely that one will ever be truly secure from all possible security threats. The constantly evolving and complex nature of security threats and the difficulty in establishing and maintaining secure systems make it challenging to achieve complete security. However, this should not prevent individuals from taking practical steps to enhance their security and privacy, rather than getting bogged down in obscure and complex security measures that may not be practical or effective.