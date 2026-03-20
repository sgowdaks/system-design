## The Adapter Pattern: The "Translator"

### The Core Problem: The "Interface Mismatch"
Imagine you have an old **Legacy Billing System** that only accepts data in **XML**. You just bought a modern **Analytics Tool** that only sends data in **JSON**. They speak different languages and cannot talk to each other.

### Why We Need It: The Three Red Flags
1.  **Incompatible APIs:** You want to use a 3rd-party library, but its method names don't match your existing code.
2.  **The "Square Peg, Round Hole":** You have a `PowerSocket` (3-prong) and a `LaptopCharger` (2-prong). You can't change the wall, and you can't change the charger.
3.  **Legacy Code Wrappers:** You are stuck with old code that you aren't allowed to touch, but you need it to work with a new system.

--- 

I completely understand. Structural patterns are all about the "plumbing" of your code—how different pieces connect. If the connections aren't clear, the pattern doesn't make sense.

Following the **Core Problem/Red Flags/Code** format from your Singleton reference, here are the examples for all four.

---

### How to Address It:
Create a **Wrapper class** (The Adapter). It "talks" to the old sensor, gets the XML, converts it to JSON, and hands it to the display.

```python
# Old Class (XML)
class LegacyWeatherSensor:
    def get_xml_data(self):
        return "<temp>25</temp>"

# New Interface (Expects JSON)
class WeatherDisplay:
    def show_temp(self, json_data):
        print(f"Displaying: {json_data['temp']}°C")

# --- THE ADAPTER ---
class WeatherAdapter:
    def __init__(self, sensor):
        self.sensor = sensor

    def get_json_data(self):
        xml = self.sensor.get_xml_data()
        # Fake conversion logic: XML -> JSON
        return {"temp": 25}

# Execution
sensor = LegacyWeatherSensor()
adapter = WeatherAdapter(sensor)
display = WeatherDisplay()

display.show_temp(adapter.get_json_data())
```


