# Spring Cloud AWS

#### Running the Integration Tests

To run the Live Tests, we need to have an AWS account and have API keys generated for programmatic access. Edit 
the `application.properties` file to add the following properties:

```
cloud.aws.credentials.accessKey=YourAccessKey
cloud.aws.credentials.secretKey=YourSecretKey
cloud.aws.region.static=us-east-1
```

To test automatic DataSource creation from RDS instance, we also need to create an RDS instance in the AWS account.
Let's say that the RDS instance is called `spring-cloud-test-db` having the master password `se3retpass`, then we need 
to write the following in `application.properties`:

```
cloud.aws.rds.spring-cloud-test-db.password=se3retpass
```
Multiple application classes are available under this project. To launch InstanceProfileAwsApplication application, replace `start-class` under `pom.xml`:

```
<start-class>com.baeldung.spring.cloud.aws.InstanceProfileAwsApplication</start-class>
```
