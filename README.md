# Plantuml Setup & Markup Rendering
Show how to setup Plantuml in VSCode and publish diagrams in Github

- Install VSCode
- [Install Plantuml plugin](https://marketplace.visualstudio.com/items?itemName=jebbs.plantuml)


## Markup Rendering

Rendering requires a call to the online plant server, there are a few methods available: -
- Render inline encode plantuml stream (png/svg) to endpoint ```http://www.plantuml.com/plantuml/png/{stream}```
- Render remote file ```http://www.plantuml.com/plantuml/proxy?idx=0&src={UrlEncoded(file location)}```


So if the puml file is located 
```

![Example](http://www.plantuml.com/plantuml/proxy?idx=0&src=<UrlEncoded(file.puml)> "Example")
```

This example renders the following image:

![Example](http://www.plantuml.com/plantuml/proxy?idx=0&src=https%3A%2F%2Fraw.githubusercontent.com%2Fhoggmania%2Fplantuml-setup%2Fmaster%2Ftest.puml "Example")

This example renders the following image:

![Example](http://www.plantuml.com/plantuml/png/SoWkIImgAStDuLBCp4lEAKr9LR19B2_MJyxFpStFiqCJ3Ix9BqfCJzLtp4sioiyBDeOp22fCAatEJYs1KdPSN8w-Zb7-Vi766iN6yPbv9Qb5UOavcYYY1K1tvQKMwIY5fUQbv1Uf5oi46ojfSY6fLx3HLK0ev780gWDw1000 "Example")


This example renders the following image:

![Example](http://www.plantuml.com/plantuml/proxy?idx=0&src=https%3A%2F%2Fraw.githubusercontent.com%2FRicardoNiepel%2FAzure-PlantUML%2Fmaster%2Fsamples%2FBasic%2520usage%2520-%2520Stream%2520processing%2520with%2520Azure%2520Stream%2520Analytics.puml "Example")



## Using include files to change styles

Example of usage:
```
@startuml
!define PUML https://raw.githubusercontent.com/hoggmania/plantuml-stdlib/master
!include PUML/puml-themes.iuml
!include PUML/puml-methods.iuml



@enduml
```
