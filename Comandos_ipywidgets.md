# 🧰 Comandos ipywidgets

```python
from ipywidgets import Button, Dropdown, Output
from IPython.display import display

button = Button(description="Haz clic")
out = Output()

def evento(b):
    with out:
        print("¡Botón presionado!")

button.on_click(evento)
display(button, out)
```
