
# 📚 Cheat Sheet – ipywidgets (uso en Jupyter)

## 📦 Importar widgets necesarios

```python
from ipywidgets import Button, FileUpload, Label, HBox, VBox, Tab, Output, Dropdown, IntSlider, Text
from IPython.display import display, clear_output
```

## 1. Botón (Button)
```python
btn = Button(description="Clic aquí", button_style='success')
display(btn)
```

## 2. Área de salida (Output)
```python
out = Output()
display(out)

with out:
    print("Esto se muestra en el output.")
```

## 3. Cargar archivos (FileUpload)
```python
uploader = FileUpload(accept='.csv, .xlsx', multiple=True)
display(uploader)
```

## 4. Etiqueta (Label)
```python
label = Label(value="Esto es una etiqueta.")
display(label)
```

## 5. Agrupar elementos (HBox y VBox)
```python
hbox = HBox([Button(description='Botón A'), Button(description='Botón B')])
vbox = VBox([Button(description='Botón C'), Button(description='Botón D')])
display(hbox, vbox)
```

## 6. Pestañas (Tab)
```python
tab1 = VBox([Label("Contenido 1")])
tab2 = VBox([Label("Contenido 2")])
tabs = Tab(children=[tab1, tab2])
tabs.set_title(0, 'Primera')
tabs.set_title(1, 'Segunda')
display(tabs)
```

## 7. Desplegable (Dropdown)
```python
dropdown = Dropdown(
    options=['Opción 1', 'Opción 2', 'Opción 3'],
    value='Opción 1',
    description='Elige:'
)
display(dropdown)
```

## 8. Barra deslizante (IntSlider)
```python
slider = IntSlider(value=5, min=0, max=10)
display(slider)
```

## 9. Cuadro de texto (Text)
```python
text = Text(value='Hola', description='Nombre:')
display(text)
```

## 🎯 Tip Final
Combinar widgets en `VBox`, `HBox` o `Tab` permite construir interfaces poderosas e interactivas.

---

## 🚀 Mini App Interactiva con Dropdown + Botón + Output

```python
from ipywidgets import Dropdown, Button, Output, VBox
from IPython.display import display, clear_output

dropdown = Dropdown(
    options=['Python', 'R', 'SQL', 'Java'],
    value='Python',
    description='Lenguaje:'
)
button = Button(description="Mostrar selección", button_style='success', tooltip='Haz clic para ver tu elección')
out = Output()

def mostrar_seleccion(b):
    with out:
        clear_output()
        print(f"Seleccionaste: {dropdown.value}")

button.on_click(mostrar_seleccion)
app = VBox([dropdown, button, out])
display(app)
```

---

## 🌍 Tabla de Estilos `button_style`

| Estilo (`button_style`) | Color Visual   | Uso Recomendado                         |
|-------------------------|----------------|------------------------------------------|
| `'primary'`             | Azul oscuro    | Acción principal, muy importante         |
| `'success'`             | Verde          | Confirmaciones, procesos exitosos        |
| `'info'`                | Azul claro     | Información, opciones neutrales          |
| `'warning'`             | Amarillo       | Advertencias, precauciones               |
| `'danger'`              | Rojo           | Acciones peligrosas (eliminar, cancelar) |
| `''` (vacío)            | Gris estándar  | Botón neutro sin estilo especial         |

## 📋 Ejemplo de creación rápida de botones con estilos
```python
from ipywidgets import Button, HBox
from IPython.display import display

btn_primary = Button(description="Principal", button_style='primary')
btn_success = Button(description="Éxito", button_style='success')
btn_info = Button(description="Info", button_style='info')
btn_warning = Button(description="Advertencia", button_style='warning')
btn_danger = Button(description="Peligro", button_style='danger')
btn_default = Button(description="Neutro", button_style='')

display(HBox([btn_primary, btn_success, btn_info, btn_warning, btn_danger, btn_default]))
```
