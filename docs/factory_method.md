# Factory Method Pattern

## Definition

The Factory Method Pattern defines an interface for creating an object but lets subclasses alter the type of objects that will be created.

## Structure

![Factory Method Structure](https://user-images.githubusercontent.com/xxxxxx/factory_method_structure.png)

## Implementation

Here’s an example implementation in Python:

```python
class Creator:
    def factory_method(self):
        raise NotImplementedError

    def some_operation(self):
        product = self.factory_method()
        return f"Creator: The same creator's code has just worked with {product.operation()}"

class ConcreteCreator(Creator):
    def factory_method(self):
        return ConcreteProduct()

class Product:
    def operation(self):
        pass

class ConcreteProduct(Product):
    def operation(self):
        return "{Result of the ConcreteProduct}"
```
