
# 🧰 Comandos ipywidgets – Ejemplo de botón interactivo

Este ejemplo muestra cómo crear un botón interactivo con salida dinámica usando `ipywidgets` en Jupyter Notebook.

## 🧪 Código mejorado

```python
# 📦 Importación de widgets y display
from ipywidgets import Button, Output
from IPython.display import display

# 🎯 Crear un botón
button = Button(description="Haz clic", button_style='info')  # estilos: 'primary', 'success', 'info', 'warning', 'danger'

# 🖥️ Crear un área de salida
out = Output()

# 🧠 Definir función que se ejecuta al hacer clic
def al_hacer_clic(b):
    with out:
        out.clear_output()  # Limpia la salida anterior
        print("¡Botón presionado!")

# 🔗 Asociar evento al botón
button.on_click(al_hacer_clic)

# 📋 Mostrar el botón y la salida
display(button, out)
```

✅ Usa este bloque en cualquier celda de Jupyter Notebook para ver cómo funciona la interactividad básica.
