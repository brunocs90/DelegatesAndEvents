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
  <img alt="layout" src="./images/layout.gif" width="100%">
</p>

<br>

## 💻 Projeto

Neste projeto foram estudados os principais conceitos de delegates e como são criados. Através da plataforma pluralsight pelo seguinte curso:
https://app.pluralsight.com/library/courses/csharp-events-delegates/table-of-contents.

## 🚀 Conceitos

Esse projeto foi desenvolvido com as seguintes tecnologias:

- Creating a Delegate
- Defining an Event
- Raising Events
- Creating an EventArgs Class

Custom delegates are defined using the delegate keyword

```c#
public delegate void WorkPerformedHandler(int hours,
WorkType workType);
```

## :memo: Licença

Esse projeto está sob a licença MIT. Veja o arquivo [LICENSE](LICENSE.md) para mais detalhes.

---
**Desenvolvido por [Bruno César](https://github.com/brunocs90).**
