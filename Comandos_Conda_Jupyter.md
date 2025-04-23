# 🐍 Comandos Conda y Jupyter



## 📤 Exportar entornos Conda

### 🔹 Exportar solo los paquetes instalados manualmente
```bash
conda env export --from-history > environment.yml
```
✅ Útil para compartir proyectos. Solo incluye los paquetes esenciales que tú instalaste, no todas las dependencias internas.

### 🔹 Exportar todo el entorno (incluye dependencias internas)
```bash
conda env export > full_environment.yml
```
📦 Incluye versiones específicas de todas las dependencias.

### 🔹 Para recrear un entorno a partir del archivo
```bash
conda env create -f environment.yml
```

---

## 💡 Recomendación de estructura para proyectos

```
📁 mi_proyecto/
├── main.ipynb
├── README.md
├── environment.yml      # si usas conda
└── requirements.txt     # si usas pip
```
