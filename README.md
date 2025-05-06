
# Probando el code viewer
# Probando el OnlyFor

## 5. Usando el Code component
```javascript
var divElem = document.getElementById("myFirstDiv"); //Selecciona un elemento padre
```

Contenido general visible para todos los usuarios.

<onlyfor saas="true">
	
# Contenido restringido
	
Este contenido solo es visible para usuarios con habilitación SaaS.
	
</onlyfor>

## Contenido general visible para todos los usuarios.

```Hola soy un bloque de codigo simple```

# Título Principal del Documento

Este es un párrafo introductorio normal. Se procesará directamente por el `MarkDownParser` principal.

Aquí hay una lista:
- Item 1
- Item 2

<how-to-start>
	
## Sección Especial "Cómo Empezar"

Este contenido está **dentro** de las etiquetas `how-to-start`. Será extraído y procesado por el `HowToStartComponent`, que a su vez usará `ReactMarkdown`.

Puedes incluir cualquier Markdown válido aquí:
*   Paso 1: Haz esto.
*   Paso 2: Haz aquello.

Incluso bloques de código:
```javascript
console.log("Hola desde how-to-start!");
```

[Y enlaces](https://example.com)
	
</how-to-start>

Este es otro párrafo normal, que aparece *después* del bloque `how-to-start`.

## Otra sección normal

Más contenido estándar de Markdown.

## Codeviewer solo con css
```css runable="true"
h1 {
			color: red;
	}
```

## Codeviewer con html y css

```html runable="true"
	<div>
			<h1>hello friend!</h1>
			<button id="button" onclick="clickButton">click me</button>
	</div>
```
```css runable="true"
		h1 {
			color: red;
	}
```
```js runable="true"
	const button = document.getElementById('button');
button.addEventListener('click', () => {
	button.innerText = button.innerText + "1";
});
```

## 1. Que pasa si el codeviewer no recibe nada?

```js runable="true"

```

## 2. Que pasa si recibe todas las tecnologias posibles?

```jsx runable="true"    
    console.log('x');
```
```python runable="true"
    print('x');
```
```js runable="true"
	console.log('a');
```
```node runable="true"
	console.log('a');
```
```node.js runable="true"
	console.log('a');
```
```py runable="true"
    print('py');
```
```html runable="true"
	<div>Hello</div>
```

## 3. Que pasa si el codigo es casi infinito?

```js runable="true"
  for(let i = 0; i < 1000000000; i++){
    console.log(i);
  }
```

## 4. Que pasa si pasas dos code runable con uno sin ser runable en el medio

```js runable=true
console.log("js");
```
```py runable=true
print("hea")
```

## 4. Usando el CodeDiff component
```py compare=true color=#420b00
def check_ticket(ticket):
    if ticket is not None:
        if not ticket.is_expired():
            if ticket.is_valid():
                return "Welcome to the movie!"
            else:
                return "Invalid ticket!"
        else:
            return "Ticket expired!"
    else:
        return "No ticket!"
```
```py compare=true color=#420b00
def check_ticket(ticket):
    if ticket is None:
        return "No ticket!"
    if ticket.is_expired():
        return "Ticket expired!"
    if not ticket.is_valid():
        return "Invalid ticket!"
    return "Welcome to the movie!"
```
