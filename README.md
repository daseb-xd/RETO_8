# RETO_8
Reto 8 de la clase de la clase de programacion orientada a objetos:

Implementar iteradores en el menu
Implementación:
``` python
class OrderIterable():
    def __init__(self, order: Order):
        self.order = order
        self.index = 0
    def __iter__(self):
        return self

    def __next__(self):
        if self.index < len(self.order.items):
            item = self.order.items[self.index]
            self.index += 1
            return item
        else:
            raise StopIteration
...
if __name__ == "__main__":
order = Order([...])
for item in OrderIterable(order):
        print(item)
```
## Resultado:








``` python
Appetizer: Empanadas, Price: 3.5
Appetizer: Cheese Sticks, Price: 4.0
Appetizer: Mini Burgers, Price: 5.0
Appetizer: Mini Waffles, Price: 2.5
Appetizer: Salchipapa, Price: 5.0
Main Course: Baby Beef, Price: 10.0, Protein: Beef, Grains: Rice, Vegetables: Salad
Main Course: Cordon Blue, Price: 12.0, Protein: Chicken, Grains: Potatoes, Vegetables: Salad
Main Course: Salmon, Price: 15.0, Protein: Fish, Grains: Quinoa, Vegetables: Lettuce
Main Course: Burger, Price: 8.0, Protein: Beef, Grains: Bread, Vegetables: Onion
Beverage: Coca Cola, Price: 2.0, Size: Medium, Type: Soda
Beverage: Orange Juice, Price: 3.0, Size: Large, Type: Juice
Beverage: Quatro, Price: 2.5, Size: Small, Type: Soda
Beverage: Chocolate Milkshake, Price: 4.0, Size: Large, Type: Milkshake
Dessert: Chocolate Cake, Price: 5.0
Dessert: Nutella Waffles, Price: 6.0
Dessert: Flan, Price: 4.0
Dessert: Lemon Cheesecake, Price: 5.0
```
