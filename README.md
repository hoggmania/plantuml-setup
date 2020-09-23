# Plantuml Setup & Markup Rendering
Show how to setup Plantuml in VSCode and publish diagrams in Github

- Install VSCode
- [Install Plantuml plugin](https://marketplace.visualstudio.com/items?itemName=jebbs.plantuml)


## Markup Rendering

Rendering requires a call to the online plant server, there are a few methods available: -
- Render inline encode plantuml stream (png/svg) to endpoint ```http://www.plantuml.com/plantuml/png/{stream}```
- Render remote file ```http://www.plantuml.com/plantuml/proxy?idx=0&src={UrlEncoded(raw github location)}```


So if the raw github location of the puml file is https://raw.githubusercontent.com/hoggmania/plantuml-setup/master/test.puml the encode markup is: -
```
![Example](http://www.plantuml.com/plantuml/proxy?idx=0&src=https%3A%2F%2Fraw.githubusercontent.com%2Fhoggmania%2Fplantuml-setup%2Fmaster%2Ftest.puml "Example")
```

This example renders the following image:

![Example](http://www.plantuml.com/plantuml/proxy?idx=0&src=https%3A%2F%2Fraw.githubusercontent.com%2Fhoggmania%2Fplantuml-setup%2Fmaster%2Ftest.puml "Example")


## Using include files to change styles

Example of usage:
```
@startuml
!define PUML https://raw.githubusercontent.com/hoggmania/plantuml-stdlib/master
!include PUML/puml-themes.iuml
!include PUML/puml-methods.iuml



@enduml
```
