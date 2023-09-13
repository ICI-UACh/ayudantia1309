# ayudantia1309  
Sin ayuda del intérprete, **rutee** (utilizando tablas de ejecución, a mano) los siguientes programas y determine la salida que producen.

Recuerde hacer **tablas de ejecución para cada namespace por separado**, para evitar confundir las variables del mismo nombre y reconocer el ámbito de cada una.

## Observación:
Los nombres de variables y funciones en esta guía no cumplen con las recomendaciones de buenos nombres. Estos nombres fueron escogidos precisamente para dificultar la solución de los ejercicios obligándole a concentrarse y demostrarle el esfuerzo que requiere leer un código con nombres mal escogidos. Como aprendizaje, esperamos que el código que usted genere en el futuro no haga sufrir a otros programadores como usted sufrirá con el código en esta guía.

### Ejercicio 1:
```bash
# Ejercicio 1
def f(x, y = 3):
   x += 6
   print(x + y)
   return(2*(x+y))
x = 4
y = 5
f(x, f(x))
print(x + y)
```

### Ejercicio 2:
```bash
# Ejercicio 2
def f(b, a):
   b[0] = 'b'
   a[1] = b[1]
   print('  ' + str(a))
   print('  ' + str(b))
a = ['a', 'b']
f(a, a.copy())
print(a)
```

### Ejercicio 3:
```bash
# Ejercicio 3
x = 1
def f():
   def g():
       nonlocal x
       def h():
           global x
           print(x)
           x = 5
           print(x)
       print(x)
       h()
       print(x)
   x = 2
   print(x)
   g()
print(x)
f()           
print(x)
```

### Ejercicio 4:
```bash
# Ejercicio 4
x = [1, 2]
def f():
   def g():
       nonlocal x
       def h(y):
           global x
           print(x)
           x[0] = 5
           y[1] = 7
           print(x)
           print(y)
       print(x)
       h(x)
       print(x)
   x = [3, 4]
   print(x)
   g()
print(x)
f()           
print(x)
```
