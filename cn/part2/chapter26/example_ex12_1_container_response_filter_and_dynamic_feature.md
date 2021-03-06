# Example ex12_1 : ContainerResponseFilter and DynamicFeature


*ex12_1* implements the **@MaxAge** and **CacheControlFilter** example in the section DynamicFeature.


### The Server Code


The **@MaxAge**, **CacheControlFilter**, and **MaxAgeFeature** classes were explained pretty well in DynamicFeature, so I’m not going to go into them again here. We applied the **@MaxAge** annotation to the **CustomerResource.getCustomer()** method:


```Java:src/main/java/com/restfully/shop/services/CustomerResource
   @GET
   @Path("{id}")
   @Produces("application/xml")
   @MaxAge(500)
   public Customer getCustomer(@PathParam("id") int id)
   {
      Customer customer = customerDB.get(id);
      if (customer == null)
      {
         throw new WebApplicationException(Response.Status.NOT_FOUND);
      }
      return customer;
   }
```


Applying this annotation to this method will cause the **CacheControlFilter** to be bound to this method when it is executed. The filter will cause a **Cache-Control** header to be added to the HTTP response with a max age of 500 seconds. Let’s also take a look at how these classes are registered:


```Java:src/main/java/com/restfully/shop/services/ShoppingApplication.java
@ApplicationPath("/services")
public class ShoppingApplication extends Application
{
   private Set<Object> singletons = new HashSet<Object>();
   private Set<Class<?>> classes = new HashSet<Class<?>>();

   public ShoppingApplication()
   {
      singletons.add(new CustomerResource());
      classes.add(MaxAgeFeature.class);
   }

   @Override
   public Set<Class<?>> getClasses()
   {
      return classes;
   }

   @Override
   public Set<Object> getSingletons()
   {
      return singletons;
   }
}
```


Notice that we only register the **MaxAgeFeature** class. This class handles the registration of the **CacheControlFilter** if the JAX-RS method is annotated with **@MaxAge**.



### The Client Code


The client code hasn’t changed much from other examples. We first start off by creating a **Customer** on the server. We then do a GET request to get the customer, checking for the **Cache-Control** header generated by the **CacheControlFilter** on the server side:


```Java:src/test/java/com/restfully/shop/test/CustomerResourceTest.java
...

      System.out.println("*** GET Created Customer **");
      response = client.target(location).request().get();
      CacheControl cc = CacheControl.valueOf(
                           response.getHeaderString(HttpHeaders.CACHE_CONTROL));
      System.out.println("Max age: " + cc.getMaxAge());
```


There is nothing really special about this code other than it shows you how to create a **CacheControl** object from a header string.


### Build and Run the Example Program


Perform the following steps:

1. Open a command prompt or shell terminal and change to the *ex12_1* directory of the workbook example code.
2. Make sure your PATH is set up to include both the JDK and Maven, as described in [Chapter 17](../chapter17/workbook_introduction.md).
3. Perform the build and run the example by typing **maven install**. 