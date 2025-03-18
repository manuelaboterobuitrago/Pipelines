# Preprocesamiento Chocolate Bar Rating
Por: Manuela Botero Buitrago

Este repositorio contiene un pipeline de preprocesamiento de datos aplicado a un conjunto de datos de chocolates. Se utiliza `scikit-learn` para transformar las variables y preparar los datos para su análisis.

## 📌 Descripción del Dataset
El conjunto de datos incluye información sobre diferentes fabricantes de chocolate, su ubicación, el porcentaje de cacao en las barras, la calificación de los productos y el origen de los granos de cacao.

### **Columnas Principales:**
- `Company_(Maker-if known)`: Nombre del fabricante.
- `Specific Bean Origin or Bar Name`: Nombre específico del chocolate.
- `REF`: Identificador de referencia.
- `Review_Date`: Año de revisión.
- `Cocoa_Percent`: Porcentaje de cacao.
- `Company_Location`: Ubicación de la empresa.
- `Rating`: Calificación del chocolate.
- `Bean_Type`: Tipo de grano.
- `Broad_Bean_Origin`: Origen general del grano.

## 🚀 **Pasos del Preprocesamiento**

### 1️⃣ **Carga y Exploración de Datos**
- Se leen los datos y se analizan los valores nulos.
- Se identifican variables categóricas y numéricas.

### 2️⃣ **Limpieza de Datos**
- Se convierte `Cocoa_Percent` de object  a valor float.
- Se imputan valores nulos con estrategias adecuadas:
  - Media para variables numéricas.
  - Más frecuente para variables categóricas.

### 3️⃣ **Transformaciones Aplicadas**
- **Escalado:** Se usa `StandardScaler` para normalizar las variables numéricas.
- **Codificación de Variables Categóricas:**
  - `OneHotEncoder` para variables nominales.
  
### 4️⃣ **Construcción del Pipeline**
Se implementa un `ColumnTransformer` que aplica las transformaciones a cada tipo de variable

### 5️⃣ **Aplicación del Pipeline y Validación**
- Se transforma el dataset con `fit_transform()`.
- Se convierten los datos procesados en un DataFrame con nombres de columnas adecuados.
- Se validan los resultados con `describe()` y `head()`.

### 6️⃣ **Exportación de Datos Limpios**
Los datos preprocesados se guardan en un archivo CSV para su posterior análisis:


## 📊 **Futuras Mejoras**
- Añadir técnicas avanzadas de imputación.
- Implementar selección de características para optimizar el modelo.



