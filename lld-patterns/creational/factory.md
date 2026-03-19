
# The Factory Method Pattern: The "On-Demand" Creator

## 1. The Core Problem: The "Hard-Coded" Bottleneck
Imagine you are building a **Payment Gateway** like Stripe. Initially, you only support **Credit Cards**.
* **Without Factory:** Everywhere in your code where a payment happens, you write `processor = CreditCardProcessor()`. 
* **The Issue:** Your boss says, "We need to support **PayPal** and **Apple Pay** tomorrow." 
* **The Result:** You now have to find and change 50 different files to replace `CreditCardProcessor()` with `PayPalProcessor()`. If you miss one, the app crashes. You are "tightly coupled" to one specific class.

## 2. Why We Need It: The Three Red Flags
### A. The "If-Else" Nightmare (Scalability)
If your code looks like `if type == "card": ... elif type == "paypal": ...`, you are in trouble. Every time you add a new payment method, this list grows. The Factory Method moves this logic into one specialized "Creator" class so the rest of your app stays clean.
### B. The "Black Box" Requirement (Abstraction)
Sometimes your code needs an object, but it shouldn't care *how* it's made or *which* specific version it gets. It just needs something that can `.process_payment()`.
### C. Subclass Empowerment (Flexibility)
You want to give other developers a "template" but let them decide the final product. A `Logistics` class provides the "delivery" logic, but a `SeaLogistics` subclass decides the "product" is a `Ship`.

## 3. The Python Implementation
```python
class PaymentProcessor(ABC):
    @abstractmethod
    def pay(self, amount): pass

class CardProcessor(PaymentProcessor):
    def pay(self, amount): print(f"Paid ${amount} via Card")

class PayPalProcessor(PaymentProcessor):
    def pay(self, amount): print(f"Paid ${amount} via PayPal")

# THE FACTORY METHOD
class PaymentFactory:
    def get_processor(self, method):
        if method == "card": return CardProcessor()
        if method == "paypal": return PayPalProcessor()

# Client uses the Factory, not the classes directly
factory = PaymentFactory()
processor = factory.get_processor("paypal")
processor.pay(100)
```
