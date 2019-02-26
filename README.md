# Tesis
Estructura de Tesis segun los criterios de la Universidad Rafael Landivar.

## Compilacion
* PDFLatex

## Para compilar
* Compilador de latex
* ActivePerl

### Compilacion de indices
1. Debes generar el indice principal
```
\tableofcontents
``````

2. Generar los demas indices
```
\tableofcontents.
\listoffigures.
\listoftables.
\listofcharts.
\listofformulas.
```

3. Eliminar los puntos
```
\tableofcontents
\listoffigures
\listoftables
\listofcharts
\listofformulas
```

### Compilacion de glosario y abreviaturas
1. Agregar el script (Orden personalizados), Make glossaries
```
makeglossaries %
```

2. Ejecutar compilacion PDFLatex

3. Ejecutar script, Make Glossaries

4. Ejecutar compilacion PDFLates

**Observacion**: Cada glosario y abreviatura, debe referenciarse en el documento (La primera vez), en caso contrario no se genera.

## Codigo
### Insertar una tabla
```
\begin{table}[]
	\label{tabl:nombre}
	\caption{descripcion}
	\begin{tabular}{|c|c|}
	% tabla
	\end{tabular} \\
	Fuente:
\end{table}
```

### Insertar una grafica
```
\begin{chart}[h]
	\label{chr:nommbre}
	\centering
	\caption{descripcion}
	\includegraphics[]{path} \\
	Fuente:
\end{chart}
```

### Insertar una imagen
```
\begin{figure}[h]
	\label{fig:nombre}
	\caption{descripcion}
	\centering
	\includegraphics[]{path} \\
	Fuente:
\end{figure}
```

### Insertar una ecuacion
```
\begin{formula}[h]
	\label{frm:demo}
	\centering
	\caption{ejemplo de formula}
	\begin{equation}
	% Ecuacion
	\end{equation}
\end{formula}
```

### Glosario
#### Insertar un glosario
```
 \newglossaryentry{nombre} 
 {
 name={nombre},
 description={desc}
 }
```

#### Utilizacion de glosario
```
\gls{nombre}
```

### Acronimos

#### Insertar un acronimo
```
\newacronym{NAME}{NAME}{DESCRIPCION}
```

#### Referenciar un acronimo
```
\acrfull{NOMBRE}
```

#### Descripcion del acronimo
```
\acrshort{NOMBRE}
```

