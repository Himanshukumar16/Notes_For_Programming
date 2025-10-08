```           SPRING                ```

```Introduction to Spring Framework```

Spring Framework is an open-source, lightweight framework developed by Rod Johnson in 2003.

It provides comprehensive infrastructure support for developing Java applications.

Spring aims to simplify enterprise application development by handling common concerns (like dependency management, transactions, security, etc.).

```Key Features```

Lightweight – Minimal memory footprint; doesn’t force you to use heavyweight containers like EJB.

Inversion of Control (IoC) – Objects are created and managed by the Spring container.

Dependency Injection (DI) – Dependencies between objects are injected rather than created manually.

Aspect-Oriented Programming (AOP) – Handles cross-cutting concerns like logging, security, and transactions.

Modular – Spring modules can be used independently (Core, AOP, MVC, JDBC, ORM, etc.).

Integration – Easily integrates with frameworks like Hibernate, JPA, Struts, etc.

```Spring Architecture Overview```

Spring framework is divided into several modules organized into layers:

| Layer                     | Module                                                                                  | Description                                        |
| ------------------------- | --------------------------------------------------------------------------------------- | -------------------------------------------------- |
| Core Container            | **spring-core**, **spring-beans**, **spring-context**, **spring-expression**            | Provides IoC, DI, BeanFactory, ApplicationContext  |
| Data Access / Integration | **spring-jdbc**, **spring-orm**, **spring-oxm**, **spring-jms**, **spring-transaction** | Manages database operations, ORM, and transactions |
| Web                       | **spring-web**, **spring-webmvc**, **spring-websocket**, **spring-webflux**             | Provides support for web and REST applications     |
| AOP & Instrumentation     | **spring-aop**, **spring-aspects**, **spring-instrument**                               | Used for Aspect-Oriented Programming               |
| Test                      | **spring-test**                                                                         | Provides integration testing with JUnit/TestNG     |
