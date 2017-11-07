Tenemos el siguiente archivo que contiene una serie de funciones.

```python
#secretary.py
def print_students(students):
  for student in students:
    print(student)

def add_student(students, student):
  if not student in students:
    students.append(student)
    return student
  else:
    return None

def remove_student(students, index):
  if len(students) > index:
    students.append(student)
    return student
  else:
    return None
```

Para importarlo en el interpete de python ejecutamos lo siguiente:

```bash
python
import student
students = ["manolo", "manuel", "mike"]

student.print_students(students)
student.add_student(students, "sol")
student.add_student(students, "brenda")
student.remove_student(students, 0)
student.remove_student(students, 0)
student.remove_student(students, 0)

```

Modifica la librería students para que en vez de tener un arreglo de strings, 
contenga un arreglo de diccionarios con la siguiente estructura:

```python
{
  "name": "Jesus",
  "age": 23, # random integer from 20 to 35
  "id": 12 # random integer
}
```

Los métodos ya existentes deberán de seguir funcionando.

# Introducción a clases y objetos.

Una forma muy sencilla de empesar a definir el concepto de "clase" es como
un archivo que agrupa funciones en común:

```python
#secretary.py
class Secretary:
  def print_students(self,students):
    for student in students:
      print(student)

  def add_student(self, students, student):
    if not student in students:
      students.append(student)
      return student
    else:
      return None

  def remove_student(self, students, index):
    if len(students) > index:
      del students[index]
```

```bash
python
from student import Secretary
secretary = Secretary()
students = ["manolo", "manuel", "mike"]
secretary.print_students(students)
secretary.add_student(students, "jorge")
students
secretary.print_students(students)
```

Modifica la clase Secretary para que en vez de tener un arreglo de strings, 
contenga un arreglo de diccionarios con la siguiente estructura:

```python
{
  "name": "Jesus",
  "age": 23, # random integer from 20 to 35
  "id": 12 # random integer
}
```

Los métodos ya existentes deberán de seguir funcionando.

¿Cuál es la diferencia entonces entre tener una libreria de funciones a una clase?

Bueno, la clases clases pueden ser usadas mediante instancias (objetos) de ellos mismos.

Por ejemplo para utilizar las funciones de la clase Secretary se tuvo que crear una
instancia: 

```python
secretary = Secretary()
```

Una instancia contiene atributos de clase. Los atributos vistos de manera sencilla
son variables que le pertenecen a la clase. Por ejemplo una secretaria puede tener
los siguientes atributos: name, age, gender. Para representarlo seria de la siguiente manera:

```python
#secretary.py
class Secretary:
  def __init__(self, name, age, gender):
    self.name = name
    self.age = age
    self.gender = gender
  # el resto se deja como estaba
```

```bash
python
from student import Secretary
secretary = Secretary("Jesus", 27, "H")
secretary
secretary.name
secretary.age
secretary.gender

secretary.name = "Juan Alberto"
secretary.age = 18
secretary.gender = "M"

secretary.name
secretary.age
secretary.gender
```

## Crea una clase Student que contenga los atributos: name, age, id

Una secretaria se encarga de administrar alumnos. Por eso tiene la RESPONSABILIDAD
de administrarlos. Por lo que students puede ser un atributo de la secretaria.

```python 
#secretary.py

class Secretary:
  def __init__(self, name, age, gender, students):
      self.name = name
      self.age = age
      self.gender = gender
      self.students = students

  ...

```

```bash
python
from student import Secretary
students = ["manolo", "manuel", "mike"]
secretary = Secretary("maria", 29, "W", students)
secretary.print_students()
secretary.add_student("Jesus")
secretary.print_students()
secretary.remove_student(0)
secretary.print_students()
students
secretary.students
```

## Modifica los métodos para que respondan al atributo students de Secretary.

Si nos damos cuenta, estamos usando la variable students y esta es modificada cada
que modificamos el atributo students de Secretary. Para resolver este problema
debemos de inicializar el atributo students como un arreglo vacio y después llenarlo usando el método 
add_student


```python
class Secretary:
  def __init__(self, name, age, gender):
    self.name = name
    self.age = age
    self.gender = gender
    self.students = []

  ...
```

```bash
python
from student import Secretary
students = ["manolo", "manuel", "mike"]
secretary = Secretary("maria", 29, "W")
secretary.name
secretary.students
secretary.students.append("Manolo")
secretary.students
students
```

## Crea un método que se llame fill_students(students) que se encargue de llenar el
atributo students con el argumento recibido.


La clase Student y la clase Secretary tienen los mismos atributos: name, age y gender.
Ambos tienen la misma base de atributos. Para reutilizar código podemos utilizar Herencia.
La herencia es un termino muy completo que veremos en las siguientes clases. Por lo pronto
podemos verlo como una forma en la que podemos heredar atributos y comportamiento.

```python
class Human:
  def __init__(self, name, age, gender):
    self.name = name
    self.age = age
    self.gender = gender

class Secretary(Human):
...
```

```bash
python
from student import Secretary
secretary = Secretary("maria", 29, "W")
secretary.name
students
```

## Has que la clase Student herede de Human
## Has que el atributo students sea un arreglo de objetos tipo Student