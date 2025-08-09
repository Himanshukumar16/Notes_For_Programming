Why Use Hibernate?
```
Simplifies database CRUD operations.
Reduces boilerplate JDBC code.
Prevents SQL injection via parameterized queries.
Works well with enterprise Java frameworks (Spring, JPA).
```

Key Features of Hibernate :

| Feature                             | Description                                                               |
| ----------------------------------- | ------------------------------------------------------------------------- |
| **ORM (Object-Relational Mapping)** | Maps Java classes to database tables automatically.                       |
| **Automatic SQL Generation**        | Reduces the need to write SQL manually — Hibernate generates it for you.  |
| **Database Independence**           | Code is largely DBMS-independent — switch databases with minimal changes. |
| **Caching**                         | Built-in caching improves performance by reducing database calls.         |
| **Lazy Loading**                    | Loads data only when it's needed, improving performance.                  |
| **Transaction Management**          | Supports atomic transactions with automatic rollback on failure.          |
| **Annotations/XML Configuration**   | Flexible configuration using annotations or XML files.                    |

Creates a new Configuration object which will be used to configure Hibernate by reading settings :
```
Configuration con = new Configuration();
```
Tells Hibernate to use the Students class as an entity that is linked to a database table (using annotations on Students):
```
con.addAnnotatedClass(Students.class);
```
Loads Hibernate configuration from the default config file (hibernate.cfg.xml) located in the classpath:
```
con.configure();
```
Builds a SessionFactory from the configuration. This factory creates sessions to interact with the database. It's expensive to create, so usually created once per application:
```
SessionFactory sf = con.buildSessionFactory();
```
Opens a new database session from the SessionFactory. A Session is like a single connection and cache for database operations:
```
Session s = sf.openSession();
```
Starts a database transaction which groups SQL statements as a single unit so they either all succeed or fail together:
```
        Transaction tr = s.beginTransaction();
```
Saves the Students object s1 to the database. Hibernate translates this into an SQL INSERT command:
```
        s.save(s1);
        use: s.persist(s1) as save is depriciated from hibernate 6.0
```
Commits the transaction, which means all changes (inserts, updates, deletes) within the transaction are finalized and saved in the database:
```
        tr.commit();
```

we have to make the xml file for giving instructions to the hibernate: (namely:-> ```hibernate.cfg.xml```)
```
<hibernate-configuration xmlns="http://www.hibernate.org/xsd/orm/cfg">
    <session-factory>
        <property name="hibernate.connection.driver_class">com.mysql.cj.jdbc.Driver</property> // name of jdbc conector
        <property name="hibernate.connection.url">jdbc:mysql://localhost:3306/spring</property> // url
        <property name="hibernate.connection.username">root</property> // username
        <property name="hibernate.connection.password">1234</property> // password
        <property name="hibernate.hbm2ddl.auto">update</property> // it will make table if not exist and update if exist.
    </session-factory>
</hibernate-configuration>
```
we have to add anotation to a class which we are goingto make table in database : 
for this we use : ```@Entity```

and in every data it is compulsery to have a primary key :
for this we se : ```@Id```

to see what comand or queries hibernate is giving to the database we can add this in xml file made above:
```
<property name="hibernate.show_sql">true</property>
```
it will give output as : ```Hibernate: insert into Students (sgpa,sname,sid) values (?,?,?)```

in order to reduse the linesof code we can use :
```
import org.hibernate.Session;
import org.hibernate.SessionFactory;
import org.hibernate.Transaction;
import org.hibernate.cfg.Configuration;

public class Main {
    public static void main(String[] args) {
        Students s1 = new Students();
        s1.setSid(6);
        s1.setSname("Sibu");
        s1.setSgpa(7.90);

        SessionFactory sf = new Configuration()
                .addAnnotatedClass(Students.class)
                .configure()
                .buildSessionFactory();

        Session s = sf.openSession();
        Transaction tr = s.beginTransaction();

        s.persist(s1);
        tr.commit();

        s.close();
        sf.close();
    }
}
```
here we have used configuration as annonmous object...

for fetching data from database:
we use ```session.get();```

```
public class Main {
    public static void main(String[] args) {

        SessionFactory sf = new Configuration()
                .addAnnotatedClass(Students.class)
                .configure()
                .buildSessionFactory();

        Session s = sf.openSession();

        Students detail = s.get(Students.class,1);
        s.close();
        sf.close();

        System.out.println(detail);
    }
}
```
for updating and deleting a data : 
```
session.merge(s1); // updates the table. but it is not updated in database.if data is not present it insert in the table.
```
for saving this or updating in database we have to commit by: ```transaction.commit();```

for deleting :
```
session.remove(s1);
```
To change the name of the columns of the table use ```@Column(name = "NameOfColumn")```

if we want to not to store the data in the database we can use ```@Transient```
```
@Entity
public class Students {
    @Id
    @Column(name = "Student_id")
    private int sid;
    @Column(name = "Student_Name")
    private String sname;
    @Column(name = "Student_CGPA")
    private double sgpa;
    private Subjects subject;
```
if we have to add a class or complex as a fields then add ```@Embeddable```at the top of the subject class..
if we have to create self sql query or add qury which cannot be directly added using hibernate then use this :
```
TypedQuery<Students> query = s.createQuery("FROM Students ORDER BY sgpa DESC", Students.class);
List<Students> list = query.getResultList();
for(Students std : list){
    System.out.println(std.toString());
}
```
Mapping : 4 types :->
        1. One-to-One ```@OneToOne``` is used !
        2. One-to-Many```@OneToMany```is used !
        3. Many-to-One```@ManyToOne```is used !
        4. Many-to-Many```@ManyToMany```is used !
one to many & many to one -> creates new table for common parts.
