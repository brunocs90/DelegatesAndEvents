<h1 align="center">
  <span>Creating Delegates, Events and EventArgs</span>
</h1>

<p align="center">
  <a href="#-projeto">Projeto</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="#-conceitos">Conceitos</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="#memo-licença">Licença</a>
</p>

<br>

<p align="center">
  <img alt="layout" src="./images/layout.PNG" width="50%">
</p>

<br>

## 💻 Projeto

Neste projeto foram estudados os principais conceitos de delegates e como são criados. Através da plataforma pluralsight pelo seguinte curso:
https://app.pluralsight.com/library/courses/csharp-events-delegates/table-of-contents.

## 🚀 Conceitos

## O que é Delegate?
É um tipo que representa referências aos métodos com lista de parâmetros e tipo de retorno específicos. Ao instanciar um delegado, você pode associar sua instância a qualquer método com assinatura e tipo de retorno compatíveis. Você pode invocar (ou chamar) o método através da instância de delegado.

Delegados são usados para passar métodos como argumentos a outros métodos. Os manipuladores de eventos nada mais são do que métodos chamados por meio de delegados. Ao criar um método personalizado, uma classe como um controle do Windows poderá chamá-lo quando um determinado evento ocorrer


### 1. Creating a Delegate
Custom delegates are defined using the delegate keyword
```c#
public delegate void WorkPerformedHandler(int hours, WorkType workType);
```

Invoke a delegate
```c#
WorkPerformedHandler del1 = new WorkPerformedHandler(WorkPerformed1);

del(5, WorkType.Golf);

static void WorkPerformed1(int hours, WorkType workType)
{
	Console.WriteLine($"WorkPerformed1 called {hours}");
}
```

### 2. Defining an Event
Events can be defined in a class using the event keyword
```c#
public event WorkPerformedHandler WorkPerformed;
```

### 4. Raising Events
Events are raised by calling the event like a method:
```c#
if (WorkPerformed != null) {
    WorkPerformed(8, WorkType.GenerateReports);
}
```

Another option is to access the event’s delegate and invoke it directly:
```c#
WorkPerformedHandler del = WorkPerformed as WorkPerformedHandler;
if (del != null) {
    del(8, WorkType.GenerateReports);
}
```

### 4. Creating an EventArgs Class
The EventArgs class is used in the signature of many delegates and event handlers:
```c#
public void button_Click(object sender, EventArgs e)
{
// Handle button click
}
```

When custom data needs to be passed the EventArgs class can be extended.

- Using EventHandler<T>

NET includes a generic EventHandler<T> class that can be used instead of a custom delegate:

```c#
public delegate void WorkPerformedHandler(object sender,WorkPerformedEventArgs e); 
or
public event EventHandler<WorkPerformedEventArgs> WorkPerformed;
```


## :memo: Licença

Esse projeto está sob a licença MIT. Veja o arquivo [LICENSE](LICENSE.md) para mais detalhes.

---
**Desenvolvido por [Bruno César](https://github.com/brunocs90).**
