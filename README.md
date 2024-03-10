# StockPrediction

<pre>
  
  /$$$$$$  /$$                      /$$             /$$$$$$$                        /$$/$$           /$$    /$$                  
 /$$__  $$| $$                     | $$            | $$__  $$                      | $|__/          | $$   |__/                  
| $$  \__/$$$$$$   /$$$$$$  /$$$$$$| $$   /$$      | $$  \ $$/$$$$$$  /$$$$$$  /$$$$$$$/$$ /$$$$$$$/$$$$$$  /$$ /$$$$$$ /$$$$$$$ 
|  $$$$$|_  $$_/  /$$__  $$/$$_____| $$  /$$/      | $$$$$$$/$$__  $$/$$__  $$/$$__  $| $$/$$_____|_  $$_/ | $$/$$__  $| $$__  $$
 \____  $$| $$   | $$  \ $| $$     | $$$$$$/       | $$____| $$  \__| $$$$$$$| $$  | $| $| $$       | $$   | $| $$  \ $| $$  \ $$
 /$$  \ $$| $$ /$| $$  | $| $$     | $$_  $$       | $$    | $$     | $$_____| $$  | $| $| $$       | $$ /$| $| $$  | $| $$  | $$
|  $$$$$$/|  $$$$|  $$$$$$|  $$$$$$| $$ \  $$      | $$    | $$     |  $$$$$$|  $$$$$$| $|  $$$$$$$ |  $$$$| $|  $$$$$$| $$  | $$
 \______/  \___/  \______/ \_______|__/  \__/      |__/    |__/      \_______/\_______|__/\_______/  \___/ |__/\______/|__/  |__/                                                               
                                                                                                                                   </pre>

## Descripción del proyecto
Análisis y predicción a corto palzo de series de temporales de stock basadas en noticias para la asignatura de Descubrimineto de Conocimiento en Datos Complejos usando el dataset de [French news - Stocks prediction](https://www.kaggle.com/datasets/arcticgiant/french-financial-news).

## Estrucutra del repositorio

```tree
📦StockPrediction
 ┣ 📂code --- carpeta con el archivo de código de la práctica
 ┃ ┗ 📜DCDC_PrácticaFinal_Predicción de Stock.ipynb
 ┣ 📂data --- carpeta con los archivos de datos de la práctica
 ┃ ┣ 📂img --- carpeta de imágenes
 ┃ ┃ ┗ 📜euro_open.png
 ┃ ┣ 📜FrenchNews.csv --- dataset de noticias en francés
 ┃ ┣ 📜FrenchNewsDayConcat.csv --- dataset de noticias en francés concatenadas por día
 ┃ ┗ 📜euro.csv --- dataset de acciones de la bolsa europea
 ┣ 📜.gitattributes --- 
 ┣ 📜LICENSE --- Apache-2.0 license
 ┗ 📜README.md --- Este archivo
```

## Prerquisitos
Antes de inciar a ejecutar los archivos se debe tener instalado:
- Python 3.x.
- El resto de paquetes vienen con el código necesario en el .ipynb para su fácil uso y reproductibilidad.

## Uso
Tan solo sigue las instrucciones del .ipynb que se encuentra en la carpeta de code del repositorio

## Extra
### 1. Git LFS para subir archivos grandes al repositorio
   Git Large File Storage (LFS) reemplaza archivos grandes como muestras de audio, videos, conjuntos de datos y gráficos con punteros de texto dentro de Git, mientras almacena el contenido del archivo en un servidor remoto como GitHub.com o GitHub Enterprise. Esta herramienta se utiliza para poder subir el dataset a utilizar en la práctica.

Para más información, visita: [repositorio de Git LFS](https://github.com/git-lfs/git-lfs/tree/main).

 > **ADVERTENCIA:** Cada cuenta que usa Git Large File Storage recibe 1 GiB de almacenamiento gratuito y 1 GiB al mes de ancho de banda gratuito, por lo que para evitar problemas al subir archivos pesados, se recomienda subir solo los archivos pesados uno a la vez y no realizar otros cambios adicionalmente.

<p align="center">
  <img src="https://git-lfs.com/images/graphic.gif" width="350">
</p>

  **1.1.** Descargar e instalar la extensión de línea de comandos de Git:

<table>
<thead>
  <tr>
    <th><a href="https://git-lfs.com/">Windows</a></th>
    <th><a href="https://github.com/git-lfs/git-lfs/blob/main/INSTALLING.md">Linux</span></a></th>
    <th><a href="https://formulae.brew.sh/formula/git-lfs">MacOS</span></a></th>
  </tr>
</thead>
<tbody>
  <tr>
    <td>Descargar e instalar el instalador de git-lfs</td>
    <td><ul><li><code>sudo apt-get install software-properties-common</code></li><li><code>sudo curl -s https://packagecloud.io/install/repositories/github/git-lfs/script.deb.sh | sudo bash</code></li><li><code>sudo apt-get install git lfs</code></li></ul>
    <td><code>$brew install git-lfs</code></td>
  </tr>
</tbody>
</table>

  Una vez descargado e instalado, configura Git LFS para tu cuenta de usuario ejecutando:

  ```bash
    git lfs install
```

> **NOTA:** Solo necesitas ejecutar esto una vez por cuenta de usuario.

**1.2.** Navega a tu repositorio local:

```bash
  cd /ruta/a/tu/repo
```
**1.3** En cada repositorio de Git donde quieras usar Git LFS, selecciona los tipos de archivos que te gustaría que Git LFS administre (o edita directamente tu .gitattributes). Esto se hace usando el comando `git lfs track`:

```bash
  git lfs track "*.ext"
```

Puedes configurar extensiones de archivo adicionales en cualquier momento. Por ejemplo, si quieres rastrear archivos con una extensión .csv y .h5 usando Git LFS, ejecutarías: git lfs track "*.csv" "*.h5". Después de ejecutar ese comando, se creará un archivo .gitattributes donde puedes agregar más archivos para ser rastreados editándolo usando el comando ``git lfs track`` nuevamente o editando .gitattributes directamente.

Ahora asegúrate de que .gitattributes esté rastreado:

```bash
  git add .gitattributes
```

> **NOTA:** Solo tienes que ejecutar los comandos 1.3 la primera vez que uses Git LFS y cuando quieras añadir más extensiones para rastrear.

**1.4** No hay un paso cuatro. Simplemente haz commit y push a GitHub como lo harías normalmente; por ejemplo, si tu rama actual se llama main:

```bash
  git add file.ext
  git commit -m "subir archivo pesado"
  git push origin main
```
 
## Autores 
Este proyecto ha sido desarollado por estudiantes de la Universidad Poltécina de Madrid (UPM) para el trabajo final de la asignatura de Descubirmiento de Conocimiento de Datos Complejos (DCDC). Los autores son [Che Cui](che.cui@alumnos.upm.es) y [Alejandro Pequeño Lizcano](alejandro.pequeno@alumnos.upm.es).
