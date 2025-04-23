# 🐍 Comandos Conda y Jupyter

```bash
conda create --name mi_entorno python=3.10 -y
conda activate mi_entorno
conda install notebook
jupyter notebook
jupyter server list
python -m ipykernel install --user --name=mi_entorno --display-name "Entorno ML"
```

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

## 💡 Recomendación de estructura para proyectos

```
📁 mi_proyecto/
├── main.ipynb
├── README.md
├── environment.yml      # si usas conda
└── requirements.txt     # si usas pip
```