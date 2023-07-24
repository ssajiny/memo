## @Bean vs. @Component
### Use case for @Bean
+ Make an existing third-party class available to Spring framework
+ You may not have access to the source code of third-party class
+ However, you would like to use the third-party class as a Spring bean
### Real-World Project Example
+ The AWS S3 Client code is part of AWS SDK
+ The AWS S3 Client class was not originally annotated with @Component
  + We can't modify the AWS SDK source code, can't just add @Component
+ However, we can configure it as a Spring bean using @Bean
  + It is now a Spring Bean and we can inject it into other services of our application
