# Design Principles - The First 5 Principles of Object-Oriented Design

## Single Resposinility Principle

* A class or method should have only one reason to change.
* Example: Define a class named ProductService. It holds both product data and product registration as per following code snippet.
```
namespace SingleResposibilityApplication
{
  public class ProductService
  {
      public string ProductName { get; set; }
      public string ProductDescription { get; set; }
      
      public void ProductRegistration(ProductService product)
      {
          StaticData.Products.Add(product);
      }
  }
}
```
* Here we have 2 requirements. Both requirements are toally different. 
  * One is changing the data; whereas
  * Another one is impacting the functionality.
* Hence, we have 2 different types of reason to change a single class. So it violates the SRP.
