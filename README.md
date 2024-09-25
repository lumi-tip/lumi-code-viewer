
# Probando el code viewer

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
	console.log('node');
```
```node.js runable="true"
	console.log('node.js');
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

```
console.log(fd);
```

```py runable=true
print("hea")
```
