#**PROYECTO: "Filogenia gen COX1 familia Salticidae, Araneae"**
Mi proyecto consistió en conocer la relación filogenética con base en el gen COX1 de la familia Salticidae del orden Aranea.
En total utilicé una secuencia de proteína de nueve distintas especies de la familia Salticidae y como grupo externo a una especie de la familia Thomisidae, disponicles en NCBI.

##**Empezando**
Primero descargué las secuencias proteícas del NCBI, en el buscador coloqué en genes yrealicé la busqueda de COX1 Salticidae y COX1 Thomisidae (grupo externo).
Tuvé que descargar las secuencias de una en una ya que el programa no me permitio descargar en paquete. 

###**Prerequisitos**
**PROGRAMAS**
Tener abierta la terminal (Git Bash).
Tener acceso al Software Muscle.
Tener el programa IQ-TREE
Tener el programa FigTree
Tener un editor de texto (Sublime)

**DATOS**
Tener todas las secuencias descargadas en formato fasta.
 

###**Instalando**
Para obtener el programa IQ-TREE para windows utilicé este link: 
https://github.com/iqtree/iqtree2/releases/download/v2.2.0/iqtree-2.2.0-Windows.zip

##**Comandos**
1. Git Bash (terminal)
Crear una carpeta en el escritorio y tres subarpetas (data, results, scripts)
mkdir ProyectoFinalBio24
mkdir data results scripts

2. Secuencias
Las secuencias que utilicé las descargue de NCBI como explique anteriormente. Estas fueron guardadas en la carpeta data (SecuenciasArañas en data) .

3. Programa Sublime
A cada una de mis secuencias las redacte de mejor manera al editarlas y dejar solo el nombre científico de la especie y la secuencia.
Como tenía por separado a cada una de mis secuencias, las uní en un solo documento. Este fue guardado en formato fasta (Alineamiento_SecuenciasArañas.fasta). 

4. Software Muscle
En el buscador de Google coloque "Muscle Software" allí subí mi documento en formato fasta (Alineamiento_SecuenciasArañas.fasta), coloque en archico Pearson (fasta).
Una vez obtenido el documento alineado lo descargué y lo guardé en la carpeta results (alineamineto_muscle.aln-fasta).

5. Git Bash
Al descargar el programa iqtree lo guarde en el escritorio entonces en la terminal para llegar al programa emplee los siquientes comandos:
cd Desktop/ 
cd iqtree-2.2.0-Windows/
ls
cd bin/
"#"export PROJ_DIR=
*Tomar en cuenta que al colocar el numeral va sin comillas*

Luego use el siguiente comando
pwd

Y obtuvé lo siguiente:
/c/Users/home/Desktop/iqtree-2.2.0-Windows/bin/

Copié ese comando, coloqué lo siguiente y pegue la línea: 
export PROJ_DIR=/c/Users/home/Desktop/iqtree-2.2.0-Windows/bin/iqtree2.exe 

Finalmente para obtener mis árboles coloque el siguiente comando:
$PROJ_DIR -s alineamiento_muscle.aln-fasta -B 1000

6. Figtree
Emplee el archivo alineamineto_muscle.aln-fasta.treefile guardado en la carpeta results.
Enraíce a mi especie como grupo externo: *Oxytate striatipes* (Thomisidae, Araneae).
Modifique el árbol para que las especies queden alineadas y cambie el color de los taxones.
En color rojo se encuentra la especie seleccionada como grupo externo.

##Autora
**Diana Guallasamin**



