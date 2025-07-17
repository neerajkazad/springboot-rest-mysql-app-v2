# springboot-rest-mysql-app-v2

In this repository, the code is almost the same as the previous version: **`springboot-rest-mysql-app`**.  
Here, I have added an extra feature: **Swagger Implementation**.

---

## ✅ Steps to Add Swagger in Any Spring Boot Application

### 🔹 Step 1: Add the below dependency inside `pom.xml`

```xml
<dependency>
    <groupId>org.springdoc</groupId>
    <artifactId>springdoc-openapi-starter-webmvc-ui</artifactId>
    <version>2.4.0</version>
</dependency>
```

---

### 🔹 Step 2: Create a `config` package (`com.nk.config`) and add the following Java class

```java
package com.nk.config;

import io.swagger.v3.oas.models.OpenAPI;
import io.swagger.v3.oas.models.info.Info;
import org.springframework.context.annotation.Bean;
import org.springframework.context.annotation.Configuration;

@Configuration
public class SwaggerConfig {

    @Bean
    public OpenAPI ecommerceOpenAPI() {
        return new OpenAPI()
                .info(new Info()
                        .title("E-Commerce API")
                        .description("Spring Boot REST API for E-Commerce application")
                );
    }
}
```

---

## 📌 Swagger UI URL

Once your application is running, open the below URL in your browser to view the Swagger UI:

```
http://localhost:8080/swagger-ui.html
```

