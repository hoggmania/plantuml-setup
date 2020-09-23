# Plantuml Setup & Markup Rendering
Show how to setup Plantuml in VSCode and publish diagrams in Github

- Install VSCode
- [Install Plantuml plugin](https://marketplace.visualstudio.com/items?itemName=jebbs.plantuml)



# plantuml-stdlib
Contains official Standard Library for PlantUML
See http://plantuml.com/stdlib for more information.

This Standard Library is included in official release of PlantUML.
Following the C convention for "C standard library" (see https://en.wikipedia.org/wiki/C_standard_library )

## AWS library

The AWS library consists of Amazon AWS icons, it provides icons of two different sizes.

Use it by including the file that contains the sprite, eg: `!include <aws/Storage/AmazonS3/AmazonS3>`.
When imported, you can use the sprite as normally you would, using `<$sprite_name>`.

You may also include the `common.puml` file, eg: `!include <aws/common>`, which contains helper macros defined.
With the `common.puml` imported, you can use the `NAME_OF_SPRITE(parameters...)` macro.

Example of usage:
```
@startuml
!define PUML https://raw.githubusercontent.com/hoggmania/plantuml-stdlib/master
!include PUML/puml-themes.iuml
!include PUML/puml-methods.iuml



@enduml
```
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
