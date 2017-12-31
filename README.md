## Spring Boot eureka server
  * as of 2017-12-31, SpringBoot version 2.0.0.M7

  * EurekaServerApplication.java
```java
@SpringBootApplication
@EnableEurekaServer
public class EurekaServerApplication {
  public static void main(String[] args) {
    SpringApplication.run(EurekaServerApplication.class, args);
  }
}
```

  * application.yml
```yml
server:
  port: 8761
eureka:
  instance:
    hostname: localhost
  client:
    registerWithEureka: false
    fetchRegistry: false
    serviceUrl:
      defaultZone: http://${eureka.instance.hostname}:${server.port}/eureka/
```

  * to see registered service
```
http://localhost:8761
```

