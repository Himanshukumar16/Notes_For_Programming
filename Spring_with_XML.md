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


```Inversion of Control (IoC)```

```Definition:```IoC is a design principle where object creation and dependency management are controlled by the container (Spring) instead of manually coding it.

```IoC Container Types:```

```BeanFactory``` – Basic container, lazy initialization (creates bean only when requested).

```ApplicationContext``` – Advanced container, eager initialization, supports AOP, event handling, internationalization, etc.

```Dependency Injection (DI)```

```Definition:```DI is the process of providing external dependencies to a class rather than the class creating them itself.

```Types of DI in Spring:```

Constructor Injection

Setter Injection

Field Injection (via annotations)

```Setter Injection``` here name refer to the variable and value is value set by injection..
```
<bean id = "alien" class = "Code.Alien">
    <property name="Rollno" value="18"> </property>
</bean>
```

```Constructor Injection```we have to pass in same order as it was declared except for ```index``` argument 
if we want it to work in any sequence : use ```@ConstructorProperties({"field_1","field_2"})..
```
| Attribute | Description                                                                                           | Usage                                       |
| --------- | ----------------------------------------------------------------------------------------------------- | ------------------------------------------- |
| `value`   | Used to pass **literal (primitive) values** like int, String, double, etc.                            | `<constructor-arg value="101"/>`            |
| `ref`     | Used to pass **reference of another bean** (object dependency).                                       | `<constructor-arg ref="addressBean"/>`      |
| `type`    | Used to specify the **data type** of constructor argument (helpful when multiple constructors exist). | `<constructor-arg type="int" value="101"/>` |
| `index`   | Used to specify the **position (order)** of the constructor parameter (starting from 0).              | `<constructor-arg index="0" value="101"/>`  |

```

```Bean Scopes```
Defines how many instances of a bean will be created.

| Scope           | Description                              |
| --------------- | ---------------------------------------- |
| **singleton**   | One bean per Spring container (default). |
| **prototype**   | New bean every time it’s requested.      |
| **request**     | One bean per HTTP request (web context). |
| **session**     | One bean per HTTP session.               |
| **application** | One bean per ServletContext.             |

```Spring Configuration Types```

```XML-based Configuration```Beans defined in applicationContext.xml.

```Annotation-based Configuration```Using annotations like @Component, @Autowired, @Configuration, @Bean.

```Java-based Configuration```Using @Configuration and @Bean in a Java class instead of XML.

```Autowiring```
Autowiring means automatically injecting one bean into another by matching certain criteria (like name, type, or constructor).


```Primary Bean```
When you have multiple beans of the same type, and you try to autowire by type, Spring gets confused and throws an exception.
if we use primary, it Marks a bean as the default choice when multiple beans of the same type exist.

```Lazy-Initialization of Beans```
Marks a bean as the default choice when multiple beans of the same type exist..
```<bean id="heavyBean" class="com.example.HeavyBean" lazy-init="true"/>```

