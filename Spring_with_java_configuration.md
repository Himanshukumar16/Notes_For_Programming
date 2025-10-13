```Java-based configuration```

Java-based configuration uses @Configuration classes and @Bean methods instead of XML files to define Spring beans.

| Annotation                 | Description                                                         |
| -------------------------- | ------------------------------------------------------------------- |
| `@Configuration`           | Marks a class as a Spring configuration class (like XML `<beans>`)  |
| `@Bean`                    | Declares a bean to be managed by the Spring container               |
| `@ComponentScan`           | Enables component scanning (detects `@Component`, `@Service`, etc.) |
| `@PropertySource`          | Loads external `.properties` files                                  |
| `@Import`                  | Imports other configuration classes                                 |
| `@EnableAutoConfiguration` | Used in Spring Boot for automatic bean configuration                |

@Bean(name = "modern_desktop") for changing name of a bean we can also use array here and use any name from it to call this.
@Qualifier is used to give command to bean to use this object only... works as @primary

@Scope("prototype") used to make more than one object of a method.

for rest see code you will understand...
