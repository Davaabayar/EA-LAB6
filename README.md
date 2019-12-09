#Lab 6 - Java Persistence Query Language (JPQL) Exercise JPQL.1</br>
*The Exercise*
a)	All flights leaving the USA with a capacity > 500
```java
List<Flight> flights = em.createQuery("from Flight f where f.origin.country='USA' and f.airplane.capacity>500", Flight.class).getResultList();
        
````
b)	All airlines that use A380 (model) airplanes

```java
 List<Airline> airlines = em.createQuery("Select distinct al from Airline al join al.flights f join f.airplane ap where ap.model='A380'", Airline.class).getResultList();      
````
c)	All fights using 747 planes that don’t belong to ‘Star Alliance’

```java
flights = em.createQuery("from Flight f where f.airplane.model='747' and f.airline.name not like 'Star Alliance'", Flight.class).getResultList();      
````
d)	All flights leaving before 12pm on 08/07/2009

```java
TypedQuery<Flight> query = em.createQuery("from Flight f where f.departureDate < '2009-08-07 12:00:00 PM'", Flight.class);        
````

