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
    close
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
    }
}


