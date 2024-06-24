# Singleton Pattern

## Definition

The Singleton Pattern ensures that a class has only one instance and provides a global point of access to it.

## Structure

![Singleton Structure](https://user-images.githubusercontent.com/xxxxxx/singleton_structure.png)

## Implementation

Here’s an example implementation in Python:

```python
class Singleton:
    _instance = None

    def __new__(cls):
        if cls._instance is None:
            cls._instance = super(Singleton, cls).__new__(cls)
        return cls._instance
