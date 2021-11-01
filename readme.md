# DRF - Django Rest Framework

### O que é o Django Rest Framework?
É um conjunto de ferramentas que auxiliam na criação de API's.


**app Todo List**
aplicação web rest api que mostra uma lista de tarefa que anota o nome da tarefa, se a tarefa foi feita, a data de criação da tarefa e o id da tarefa.






**metodos rest api:**

- **Get:**
- **Post:**
- **Put:**
- **Delete:**

 **-> Criando um elemento no banco de dados**
___
```shell
from app.models import Todo

todo = Todo()

todo.name = 'Acordar cedo'

todo.save()

todo.__dict__



```

___

**Serializando  os dados**

- Transformando os dados  em objetos JSON
- ``{"name": "Criar API", "done":"false"}``

```shell
from  app.models import Todo

from app.serializers import TodoSerializer

todo = Todo.objects.first()

serializer = TodoSerializer(todo)

serializer.data

## {'id': 1, 'name': 'Acordar cedo', 'done': False, 'created_at': '2021-11-01T11:42:37.411304-03:00'}

```