# Recap de variables y funciones.

## Las variables mueren

![alt text](https://pa1.narvii.com/6313/d3bc98e331f0509e48142822efe9b224f6e8eba9_hq.gif "Logo Title Text 1")

Escribe en tu terminal lo siguiente
```bash
python3
name = "jeusus lerma"
name
print(name)
type(name) is str
exit()

python3
name
```
¿Qué pasa? La variable ya no existe. Debido a que el programa terminó de ejecutarse.
Las variables existene dentro de un bloque y viven solamente durante el bloque se
está ejecutando
```python
def f():
  x = 0
  print(x)

print(x)

```

Cuando ejecutamos un script se crea un bloque de ejecución automáticamente. Las
variables que se definen en ese bloque solo pueden ser accedidas durante
la ejecución de ese bloque. Tambien las variables pueden ser utilizadas en sub 
bloques

```python
name = "jesus lerma"

def showName():
  print(name)

def type_of_name():
  print(type(name))

showName()
type_of_name()
```

Las variables pueden ser modificadas de valor en cualquier parte de la ejecución
de un programa. Incluso pueden ser cambiadas de tipo de dato.

```python
name = "jesus lerma"
name 
name = "mariana"
name = 89

def name():
  return 90
name
name()
name = 190
name()
```

Tampoco se pueden compartir variables entre funciones

```python
def f():
  x = 90

def fn():
  x + 1

f()
fn()
```

¿Por qué?

![alt text](https://media.giphy.com/media/fNFEGm0TgpTs4/source.gif "Logo Title Text 1")

Por lo tanto tampoco podemos compartir variables entre archivos. Por que cada
que se ejecuta un archivo es un bloque de ejecución diferente.



Tenemos el siguiente programa que se encarga de agregar y buscar productos
en una tienda.

```
products = [ ]

def add_product(name, price, sku, category):  
  product = { "name": name, "price": price, "sku": sku, "category": category }
  products.append(product)
  
  return product

def find_product(product_name):
  p = {}
  for product in products:
    if product['name'] === product_name
      p = product
  if not p == {}:
    return p
  else:
    return None

def main():
    for product in products:
      print(product['name'])

    print('Agregamos dos productos')
    add_product("Carro", 100, 'CS988', "juguete")
    add_product("Peluche", 99, 'CS989', "juguete")

    for product in products:
      print(product['name'])

    print('Buscando el producto Carro')
    product = find_product('Carro')
    print('Lo hemos encontrado!')
    print(product)


main()
```

### Ejercicio 1: 
guardar las funciones en un archivo separado que se llame
product.py. Importar esta libreria en el archivo oxxo.py y procurar que al ejecutar
el comando ```python3 main.py``` el programa regrese el siguiente resultado:

```
Agregamos dos productos
Carro
Peluche
Buscando el producto Carro
Lo hemos encontrado!
{'sku': 'CS988', 'name': 'Carro', 'category': 'juguete', 'price': 100}
```

### Ejercicio Grupal: 
¿qué otras funciones agregarian en el archivo producto?

# Clases
Hasta el momento hemos utilizado clases. En TODOS los programas que hemos usado

¿Por qué?

![alt text](https://ibme.info/wp-content/uploads/2017/05/monkey-mind.gif "Logo Title Text 1")

```python
name = "jesus"
age = 18
names_list = ["manolo", "benito", "pedro", "juan pablo"]
person = {
  "name": name,
  "age": age
}
def print_person_name(person):
  print(person["name"])

type(name)
type(age)
type(person)
type(names_list)
```

¡De tal forma que hemos estado usando Clases y Objetos sin Darnos cuenta!

Para utilizar una Clase hemos creado una instancia de ella de la siguiente forma:

```python
name = "string"
list_of_names = ["jesus", "lerma", "sanchez"]
```

Sin embargo tambien pueden instanciarse de diferentes formas. Por ejemplo:

```python
list_of_names = list()
list_of_names.append("jesus")
list_of_names.append('lerma')
list_of_names.append('sanchez')

list_of_names
```

Las clases y sus instancias tienen metodos:

```python
list_of_names.append("andy")
list_of_names.sort()
list_of_names
list_of_names.sort(reverse=True)
list_of_names.reverse()
```

### Ejercicio Grupal.
Investiga 5 funciones de clases que ya hemos utilizado y compartelas con tus compañeros

