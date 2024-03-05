# _Markdown_

_Markdown_ es un lenguaja de marcado que sirve para definir contenido. Es muy usado para documentar proyectos de _software_, es el estandar

En markdown un parrafo sigue hazta que le des a la tecla **enter**

Las **negritas** se ponen así: \**Negritas**

Las __cursiva__ se pone así: \__Cursivas__

# Encabezado nivel 1
## Encabezado nivel 2
### Encabezado nivel 3
#### Encabezado nivel 4
##### Encabezado nivel 5
###### Encabezado nivel 6
![Dino Gamer](https://www.tabascohoy.com/wp-content/uploads/2023/02/gamer-300x288.jpg)

[Youtube](https://youtube.com/)

[Encabezado 1](#encabezado-nivel-1)

[Ir a archivo de comandos. text](./comandos.txt)

[![Dino Gamer](https://www.tabascohoy.com/wp-content/uploads/2023/02/gamer-300x288.jpg)](./comandos.txt)
---

Esta otra sección, la linea de arriba se llama **división**

- Primavera
- Verano
- Otoño
- Invierno

1. Primavera
1. Verano
1. Otoño
1. Invierno

- Primavera
  - listas secundarias
     - listas
- Verano
- Otoño
- Invierno

1. Primavera
   1. Enero 
      1. primer día
1. Verano
1. Otoño
1. Invierno


## Citas
### Citas en línea

> Yo solo se que no se náda

### Cita en bloque 
> Todo lo que escuchamos es una opinión, no un hecho.
>
>Todo lo que vemos es una perspectiva, no la verdad
>
> Marco Aurelio


## Tablas

| País    | Ciudad | Continente |
| --- |  ---  | --- |
| México | Ciudad de Mexico | America |
| Japón | Tokio |  Asia |
| Francia | Paris | Europa|



## Codigo

```` js
async function enviarScript(scriptText){
	const lines = scriptText.split(/[\n\t]+/).map(line => line.trim()).filter(line => line);
	main = document.querySelector("#main"),
	textarea = main.querySelector(`div[contenteditable="true"]`)
	
	if(!textarea) throw new Error("Não há uma conversa aberta")
	
	for(const line of lines){
		console.log(line)
	
		textarea.focus();
		document.execCommand('insertText', false, line);
		textarea.dispatchEvent(new Event('change', {bubbles: true}));
	
		setTimeout(() => {
			(main.querySelector(`[data-testid="send"]`) || main.querySelector(`[data-icon="send"]`)).click();
		}, 100);
		
		if(lines.indexOf(line) !== lines.length - 1) await new Promise(resolve => setTimeout(resolve, 250));
	}
	
	return lines.length;
}
````

### Codigo _HTML_

<from>
  <label for="q">Buscar:</label>
    <input>


## Comentario

<!-- Esto es un comentario -->

### Escape de caracteres 

Texto \_Cursiva_