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
