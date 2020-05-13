# Project 3: Product Availability 

## Level 1 : 

    [ ] Build a product microservice which maintains information of productid, name, dept Id, dept name eg 11234, Long Sleeves,100, Shirts  

    [ ] Build a location microservice which maintains information of a location- locationId, locname, zipcode eg. 500, Irving, 75063 

    [ ] Build a balance service, which has the available items in a given location.  productid, location Id, balance e.g 11234, 500,10 implying there are 10 long sleeve shirts in zip 75063 

**Usecase – Find the availability of a given item and/or department in all locations where the item/department is available.**

**UI**:  

    React / Angular  

    TDD with jasmine/karma/enzyme 

    State management – Redux 

**Build**: gradle 

**Database**: MySql, DynamoDb, Mongo 

**Services**: 

    Java, .Net, Scala, Spring , 

    TDD with junit, Mockito 

    Integration tests 

    Contract Tests (spring contracts) 

**Cloud**: Azure, AWS, K8 OpenShift 

**Pipeline**: AWS Cloudformation, AWS CodePipeline, Jenkins, Azure pipelines 

## Level 2 :  
**Usecase - Given an item and a zipcode, find the nearest x(given) locations within x(given) miles radius.** *(Use an external [api](http://www.geonames.org/export/web-services.html#findNearbyPostalCodes))*

**Cache**: Redis , Memcached 

**Fault Tolerence** – hystrix , spring retry 

## Level 3 :

**UseCase – Be able to view availability in realtime for the items in a given location so the items that are running low on availability can be ordered sooner.**

    [ ] Build a batch job, which will call the balance service and update the availability for an item at a location.

    [ ] Stream the update events and display the data in real time graph. 

**Batch**: AWS Batch 

**Streaming**: Kinesis, apache beam, Kafka streams 

## Level 4 : 

**Add security** – Only the batch job has to be authorized to update the balance table. Users will be authenticated and only authorized users will be allowed to see the real time graph. Use config server to store application config properties. 

**Security**: OAuth, JWT, Cognito 

## Level 5 :

**Add Monitoring and alerting. Monitor if the service takes more than ‘x’ ms to generate the next board state, if it does generate an alert, which will send an email notification to you.**

**Profiling**: Micrometer, cloudwatch, Prometheus
