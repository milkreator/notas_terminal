
# 🐍 Comandos Conda y Jupyter

## 📦 Crear y gestionar entornos
```bash
conda create --name mi_entorno python=3.10 -y
conda activate mi_entorno
conda deactivate
conda env list
conda remove --name mi_entorno --all
```

## 🧪 Instalar paquetes
```bash
conda install numpy
conda install -c conda-forge matplotlib
conda install pip
```

## 🔄 Actualizar y eliminar paquetes
```bash
conda update numpy
conda update --all
conda remove pandas
```

## 🔍 Verificación de instalación
```bash
conda list
which python
python -m pip list
```

## 📤 Exportar y reproducir entornos
```bash
conda env export --from-history > environment.yml
conda env export > full_environment.yml
conda env create -f environment.yml
```

## 📚 Jupyter + entorno
```bash
conda install notebook
jupyter notebook
jupyter server list
python -m ipykernel install --user --name=mi_entorno --display-name "Entorno ML"
```
