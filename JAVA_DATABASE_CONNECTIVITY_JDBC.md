            --------------------------------------
            | JDBC -> Java Database Connectivity |
            --------------------------------------
JDBC (Java Database Connectivity) is a Java API that lets your Java code talk to a database.
```
It gives you classes & interfaces to:
            📡 Connect to a database.
            📄 Send SQL commands (SELECT, INSERT, UPDATE, DELETE).
            📥 Get results (like ResultSet for SELECT queries).
            ⚙️ Handle database tasks from Java code.
```

/*
    steps to connect :
```
    import package by java.sql.*;
    load and register
    create connection
    create statement
    execute statement
    process the result
    close by connector_object.close();
*/
```
//  load and register :->
```
        /* this became optional after java 6.
        try {
            Class.forName("org.postgresql.Driver");
            System.out.println("Successful executed !");
        } catch (ClassNotFoundException e) {
            System.out.println("There was an error !");
        }*/
```
//      for writing url :- javaConnectigToWhat:JDBC_WillConnectWith://portNumberOf_DBMS_Using/DatabaseName
```        
        String url = "jdbc:postgresql://localhost:5432/college";// for postgresql portnumber is 5432 for mysql portnumber is 3306.
        String user = "postgres";
        String pass = "1234";

        try {
            Connection con = DriverManager.getConnection(url, user, pass);
        } catch (SQLException e) {
            throw new RuntimeException(e);
        }
        System.out.println("Connection established");
```
// creating object of the statement:
```
Statement st = con.createStatement();
```
// for executing a statement:
```
ResultSet res = st.executeQuery("select name from emp where id < 106;");
```
res.next() returns true if next rowis present else false.
fetch record:
```
res.getString("name") // one record fetch 1st record.

while(res.next()){
            System.out.println(res.getString("name")); // prints all record.
        }
```

To add data :
```
Statement st = con.createStatement();
st.execute("insert into emp values (107,'Sibu')");
```

to update data :
```
st.execute("update emp set name = 'Anubhav' where name = 'jaddu'");
```

to delete data : 
```
st.execute("delete from emp where name = 'Sibu';");
```

Problem with statements :
```
1) we cannot use directly the variables that we taken input in statements without concatenation and to do concetination here is a hard task..
2) sql injections can be there and data may be leaked from database..
```
Prepared Statement :
```
int  id = 50;
String name = "Ram";
String sql = "insert into emp values(?,?);";
PreparedStatement pst = con.prepareStatement(sql);
pst.setInt(1,id);
pst.setString(2,name);
pst.execute();
```
This will change the data in the table by adding this..

Use Statement only for executing fixed SQL or DDL commands where no user input is inserted and the statement is executed once.

Use PreparedStatement for most SQL commands, especially when queries are executed many times, require parameters, 
or when you want better security and performance..

## 🔍 Feature Comparison: `Statement` vs `PreparedStatement`

| Feature               | `Statement`                                             | `PreparedStatement`                                               |
|-----------------------|---------------------------------------------------------|-------------------------------------------------------------------|
| **Use Case**          | Single, static executions (e.g., DDL, simple queries)   | Repeated, parameterized, dynamic SQL executions                   |
| **Parameterization**  | ❌ Not supported                                        | ✅ Supported via setters                                           |
| **Security**          | ❌ Prone to SQL injection                               | ✅ Prevents SQL injection                                          |
| **Query Compilation** | Compiled on every execution                            | Precompiled once, reused                                          |
| **Performance**       | ⬇️ Lower for repeated/dynamic queries                   | ⬆️ Higher for repeated/dynamic queries                            |
| **Handling Binary Data** | ❌ Not supported                                     | ✅ Supported                                                       |
| **Batch Processing**  | ❌ Less efficient                                       | ✅ More efficient                                                  |
| **DDL Statements**    | ✅ Preferred                                            | ⚠️ Possible, but not commonly used                                |

> ✅ = Supported / Preferred  
> ❌ = Not supported / Less preferred  
> ⚠️ = Possible but not recommended  
> ⬆️⬇️ = Indicates relative performance

```
            THE END
```
