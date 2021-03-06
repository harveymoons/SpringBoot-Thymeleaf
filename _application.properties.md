###### application.properties
```sh
## mariaDB
spring.datasource.driverClassName=org.mariadb.jdbc.Driver
spring.datasource.url=jdbc:mariadb://[ip-address]/siem?useSSL=false&zeroDateTimeBehavior=convertToNull
spring.datasource.username=[database-name]
spring.datasource.password=[password]

## thymeleaf
spring.thymeleaf.cache=false
spring.thymeleaf.check-template=true
spring.thymeleaf.check-template-location=true
spring.thymeleaf.enable-spring-el-compiler=false
spring.thymeleaf.servlet.content-type=text/html
spring.thymeleaf.prefix=classpath:templates/
spring.thymeleaf.suffix=.html
spring.thymeleaf.mode=HTML
spring.thymeleaf.enabled=true
spring.thymeleaf.encoding=UTF-8

## set static path
spring.mvc.static-path-pattern=/static/**
spring.resources.static-locations=classpath:/static/
spring.resources.add-mappings=true 

## devtools
spring.devtools.livereload.enabled=true

## log-history
logging.level.com.log.insight=trace

## port
server.port=80

## session
server.servlet.session.timeout=30m
```
---
###### 외부 파일로 분리
- jar 파일 `외부` 우선순위와 `경로` 확인 후 설정
- jar 파일 `내부` 우선순위와 `경로` 확인 후 설정  
[Ref.] https://engkimbs.tistory.com/765
