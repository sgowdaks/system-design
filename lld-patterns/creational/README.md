* If you are looking at an interface (a "Factory") and trying to decide which one it is, look at the number of different products it is responsible for:
``` python
# ABSTRACT FACTORY
class UIFactory(ABC):
    @abstractmethod
    def create_button(self): pass
    @abstractmethod
    def create_checkbox(self): pass
```

