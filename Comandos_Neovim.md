
# 🧠 Comandos Neovim (nvim)

## 📂 Abrir archivos y explorar
```bash
nvim archivo.txt         # Abrir archivo específico
nvim .                   # Explorador de archivos (netrw)
```

## 💾 Guardado y salida
```vim
:w      # Guardar
:q      # Salir
:wq     # Guardar y salir
:q!     # Salir sin guardar
:qa     # Cerrar todos los buffers
```

## 🧭 Navegación de texto
```vim
h / l       # Izquierda / Derecha
j / k       # Abajo / Arriba
gg          # Ir al inicio del archivo
G           # Ir al final del archivo
:n          # Ir a la línea n
```

## 🔍 Búsqueda
```vim
/palabra     # Buscar palabra hacia adelante
?palabra     # Buscar hacia atrás
n            # Siguiente coincidencia
N            # Coincidencia anterior
```

## ✂️ Copiar, cortar y pegar
```vim
yy       # Copiar línea
dd       # Cortar línea
p        # Pegar debajo del cursor
P        # Pegar encima del cursor
```

## 🖱️ Modo visual (selección)
```vim
v        # Visual mode (carácter por carácter)
V        # Visual line mode (línea completa)
Ctrl + v # Visual block (modo columna)
d        # Borrar selección
y        # Copiar selección
```

## 🧭 Plugins: netrw (explorador de archivos)
```vim
:Ex        # Volver a netrw desde un archivo
:D         # Borrar archivo
:R         # Renombrar archivo
:%         # Crear nuevo archivo
:d         # Crear carpeta
<C-l>      # Refrescar vista
```
