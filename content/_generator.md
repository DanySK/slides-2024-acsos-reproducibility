
+++

title = "Reproducible experiments or didn't happen"
description = "The replicability crisis and recipes for self-organizing systems"
outputs = ["Reveal"]
aliases = [
    "/guide/"
]

+++

# PhD forum talk @ ACSOS 2024

#### {{% today %}}
## [Danilo Pianini](mailto:danilo.pianini@unibo.it)
### Alma Mater Studiorum -- Università di Bologna

---

{{< slide background-image="hippo2.jpg" state="blur-animation-light" transition="fade-in fade-out" >}}
<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>

<!-- white background -->
<span style="background-color: white; border-radius: 0.2em;">
source: https://www.earth.com/news/hippopotamus-population-hit-hard-by-habitat-destruction

</span>

---

# Hippos (Hippopotamus amphibius) facts

* {{% frag c="Big (second largest land animal after elephants)" %}}
* {{% frag c="(Relatively) Fast (30km/h on land, 8km/h in water)" %}}
* {{% frag c="Strong bite (13.8MPa, twice the strength of a lion bite)" %}}
* {{% frag c="Aggressive and highly unpredictable" %}}
* {{% frag c="Among the deadliest animals worldwide by human deaths" %}}

---

I'm now making a claim, and I want to see if you believe me

{{% fragment %}}
# An adult hippo's bite can crush in half an adult crocodile

Please *raise your hand if you believe this claim*
{{% /fragment %}}

{{% fragment %}}
![crocodile](crocodile80.jpg)

Please raise your hand if you believe this claim *now*
{{% /fragment %}}

---

![pic](pic.webp)

---

Let's do the same game

{{% fragment %}}
# It is possible to tame and ride a hippo

Please *raise your hand if you believe this claim*
{{% /fragment %}}

{{% fragment %}}
![riding](riding60.jpg)

Please raise your hand if you believe this claim *now*
{{% /fragment %}}

{{% fragment %}}
Would it be more convincing if I precisely explained how the hippo was tamed and ridden?
{{% /fragment %}}

{{% fragment %}}
Would it be more convincing if multiple independent people applied the same procedure and obtained the same result?
{{% /fragment %}}

---

# ~~Picture~~ Reproducible experiments, or didn't happen

![experiment](experiment.webp)

---

![image](https://user-images.githubusercontent.com/1991673/236500955-b65de211-3b51-4adf-b0e5-6f248771e479.png)

---

## Replication crisis
### aka replicability crisis or reproducibility crisis

* ongoing *methodological crisis*
* the results of many scientific studies are hard or impossible to *reproduce*.

* empirical reproductions are essential for the the scientific method

#### no reproducibility $\Rightarrow$ scientific credibility is undermined

---

## People working in computer science are lucky!
#### (on average)

* It's the only engineering discipline producing *mass-less* artifacts
    * Much easier to *share*
* Even if we work in highly unpredictable contexts, we can *control randomness* in many experiments
    * Much easier to *reproduce*
* We have support tools to *track changes*, *automate*, and *manage* complexity
    * Much easier to *maintain*

---

## Three pillars

### Availability

Let others *access* your work

### Reproducibility / Maintenance

If it is an **experiment**, make sure others can *obtain the same results* of yours

If it is a **tool** make sure your work is *sustainable* over time

### Reusability

Let others *build upon* your work

---

## Availability



---


### Specifically for data science and computer science

* Make your artifacts *available*
  * Share code as open source (**licensing**)
  * Share code and data where people will find it (**GitHub**)
  * Share code and data where it will be archived for the foreseeable future (**Zenodo**)
* Make your artifacts *reproducible*
  * It works on your PC? Ship your PC! (**containerization**)
* Make your artifacts *maintainable*
  * Be ready to accept contributions and work in team (**version control**)
  * Always check that the software is working (**continuous integration**)
* Make your artifacts *reusable*
  * document them appropriately (**GitHub Pages**)

---

* Also please don't mess around with hippos

# Short guide to Markdown slides

---

# Headers

# H1
## H2
### H3
#### H4

---

# Text

normal text

`inline code`

*italic*

**bold**

**_emphasized_**

*__emphasized alternative__*

~~strikethrough~~

[link](http://www.google.com)

---

# Lists and enums

1. First ordered list item
1. Another item
    * Unordered sub-list.
    * with two items
        * another sublist
            1. With a sub-enum
            1. yay!
1. Actual numbers don't matter, just that it's a number
  1. Ordered sub-list
1. And another item.

---

# Inline images

![Alternative text](https://upload.wikimedia.org/wikipedia/commons/6/6c/Scavolino_innevata.jpg)

---

## Fallback to shortcodes for resizing

Autoresize specifying

* `max-w` (percent of parent element width) and/or `max-h` (percent of viewport height) as max sizes , and
* `width` and/or `height` as *exact* sizes (as percent of viewport size)

{{< figure src="https://upload.wikimedia.org/wikipedia/commons/6/6c/Scavolino_innevata.jpg" height="20">}}

---

## Multi-column slide

{{% multicol %}}{{% col %}}
Column 1
{{% /col %}}{{% col %}}
Column 2
{{% /col %}}{{% /multicol %}}

---

## Tick and Cross

{{% tick %}} This is something good {{% /tick %}}
{{% cross %}} This is something good {{% /cross %}}

---

## Chart.js

{{< chart >}}
{
    type: 'bar',
    data: {
        labels: ['Red', 'Blue', 'Yellow', 'Green', 'Purple', 'Orange'],
        datasets: [{
            label: 'Bar Chart',
            data: [12, 19, 18, 16, 13, 14],
            backgroundColor: [
                'rgba(255, 99, 132, 0.2)',
                'rgba(54, 162, 235, 0.2)',
                'rgba(255, 206, 86, 0.2)',
                'rgba(75, 192, 192, 0.2)',
                'rgba(153, 102, 255, 0.2)',
                'rgba(255, 159, 64, 0.2)'
            ],
            borderColor: [
                'rgba(255, 99, 132, 1)',
                'rgba(54, 162, 235, 1)',
                'rgba(255, 206, 86, 1)',
                'rgba(75, 192, 192, 1)',
                'rgba(153, 102, 255, 1)',
                'rgba(255, 159, 64, 1)'
            ],
            borderWidth: 1
        }]
    },
    options: {
        maintainAspectRatio: false,
        scales: {
            yAxes: [{
                ticks: {
                    beginAtZero: true
                }
            }]
        }
    }
}
{{< /chart >}}

---

## FontAwesome

<i class="fa-solid fa-mug-hot"></i>
<i class="fa-solid fa-lemon"></i>
<i class="fa-solid fa-flask"></i>
<i class="fa-solid fa-apple-whole"></i>
<i class="fa-solid fa-bacon"></i>
<i class="fa-solid fa-beer-mug-empty"></i>
<i class="fa-solid fa-pepper-hot"></i>

---

## Bootstrap 1

<div class="card w-100" >
  <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/e/e9/View_of_Cesena_from_the_Abbey.jpg/1920px-View_of_Cesena_from_the_Abbey.jpg" class="card-img-top" alt="...">
  <div class="card-body">
    <h5 class="card-title">Card title</h5>
    <p class="card-text">Some quick example text to build on the card title and make up the bulk of the card's content.</p>
    <a href="#" class="btn btn-primary">Go somewhere</a>
  </div>
</div>

---

## Bootstrap 2

<button type="button" class="btn btn-primary">Primary</button>
<button type="button" class="btn btn-secondary">Secondary</button>
<button type="button" class="btn btn-success">Success</button>
<button type="button" class="btn btn-danger">Danger</button>
<button type="button" class="btn btn-warning">Warning</button>
<button type="button" class="btn btn-info">Info</button>
<button type="button" class="btn btn-light">Light</button>
<button type="button" class="btn btn-dark">Dark</button>

<button type="button" class="btn btn-link">Link</button>

---

## Low res, plain markdown

![](https://upload.wikimedia.org/wikipedia/commons/thumb/6/6c/Scavolino_innevata.jpg/260px-Scavolino_innevata.jpg)

---

## Hi res, plain markdown

![](https://upload.wikimedia.org/wikipedia/commons/6/6c/Scavolino_innevata.jpg)

---

## Low res, default

{{< figure src="https://upload.wikimedia.org/wikipedia/commons/thumb/6/6c/Scavolino_innevata.jpg/260px-Scavolino_innevata.jpg" >}}

---

## Hi res, default

{{< figure src="https://upload.wikimedia.org/wikipedia/commons/6/6c/Scavolino_innevata.jpg" >}}

---

## Low res, enlarged horizontally

{{< figure src="https://upload.wikimedia.org/wikipedia/commons/thumb/6/6c/Scavolino_innevata.jpg/260px-Scavolino_innevata.jpg" width="100">}}

---

## Low res, enlarged vertically

{{< figure src="https://upload.wikimedia.org/wikipedia/commons/thumb/6/6c/Scavolino_innevata.jpg/260px-Scavolino_innevata.jpg" height="100">}}

---

## Hi res, reduced horizontally

{{< figure src="https://upload.wikimedia.org/wikipedia/commons/6/6c/Scavolino_innevata.jpg" width="50">}}

---

## Hi res, reduced vertically

{{< figure src="https://upload.wikimedia.org/wikipedia/commons/6/6c/Scavolino_innevata.jpg" height="50">}}

---

## Hi res, reducing maximum expansion horizontally

{{< figure src="https://upload.wikimedia.org/wikipedia/commons/6/6c/Scavolino_innevata.jpg" width="50">}}

---

## Hi res, reducing maximum expansion vertically

{{< figure src="https://upload.wikimedia.org/wikipedia/commons/6/6c/Scavolino_innevata.jpg" height="50">}}

---

{{< slide background-image="https://upload.wikimedia.org/wikipedia/commons/6/6c/Scavolino_innevata.jpg" >}}

# Large images as background
## (May affect printing)

---

{{< slide background-image="https://upload.wikimedia.org/wikipedia/commons/6/6c/Scavolino_innevata.jpg" state="blur-animation-light"  transition="fade-in fade-out" >}}

# Also available with blur and custom transitions
## (May affect printing)

---

# $$\LaTeX{}$$


Inline equations like $E=mc^2$

$$\frac{n!}{k!(n-k)!} = \binom{n}{k}$$

---

# Code snippets


```kotlin
val x = pippo
```

```go
package main

import "fmt"

func main() {
    fmt.Println("Hello world!")
}
```

---

# Tables

Colons can be used to align columns.

| Tables        | Are           | Cool  |
| ------------- |:-------------:| -----:|
| col 3 is      | right-aligned | $1600 |
| col 2 is      | centered      |   $12 |
| zebra stripes | are neat      |    $1 |

There must be at least 3 dashes separating each header cell.
The outer pipes (|) are optional, and you don't need to make the
raw Markdown line up prettily. You can also use inline Markdown.

---

# Quotes

> Multiple
> lines
> of
> a
> single
> quote
> get
> joined

> Very long one liners of Markdown text automatically get broken into a multiline quotation, which is then rendered in the slides.

---

# Fragments

* {{< frag c="pluto" >}}
* {{< frag c="pluto" >}}
* {{< frag c="pluto" >}}

---

# Graphs via Gravizo

{{< gravizo "Example Gravizo graph" >}}
  digraph G {
    aize ="4,4";
    main [shape=box];
    main -> parse [weight=8];
    parse -> execute;
    main -> init [style=dotted];
    main -> cleanup;
    execute -> { make_string; printf}
    init -> make_string;
    edge [color=red];
    main -> printf [style=bold,label="100 times"];
    make_string [label="make a string"];
    node [shape=box,style=filled,color=".7 .3 1.0"];
    execute -> compare;
  }
{{< /gravizo >}}

---

# Graphs via mermaid.js

```mermaid
classDiagram
  Class01 <|-- AveryLongClass : Coosssl
  Class03 *-- Class04
  Class05 o-- Class06
  Class07 .. Class08
  Class09 --> C2 : Where am i?
  Class09 --* C3
  Class09 --|> Class07
  Class07 : equals()
  Class07 : Object[] elementData
  Class01 : size()
  Class01 : int chimp
  Class01 : int gorillasaaaaaaaaaaaaaaaaaaaaaa
  Class08 <--> C2: Cool label
```

---


# Graphs via mermaid.js with options

```mermaid
%%{init: {'theme':'default', 'themeVariables': { 'fontSize': '.34em', 'fontFamily': 'verdana' }}}%%
classDiagram
  Class01 <|-- AveryLongClass : Coosssl
  Class03 *-- Class04
  Class05 o-- Class06
  Class07 .. Class08
  Class09 --> C2 : Where am i?
  Class09 --* C3
  Class09 --|> Class07
  Class07 : equals()
  Class07 : Object[] elementData
  Class01 : size()
  Class01 : int chimp
  Class01 : int gorillasaaaaaaaaaaaaaaaaaaaaaa
  Class08 <--> C2: Cool label
```


---
# Graphs via mermaid.js 2

```mermaid
graph TD
  SL([fa:fa-user second level]) --> L[solution]
  L -- solution email --> db[(mysql)]
  db --> X[automatic]
  X --> CM([fa:fa-users first level])
  db -- Email --> c([customer support]);
```

---

# Graphs via mermaid.js 3

```mermaid
gitGraph
  commit id: "Initialize project"
  commit id: "Make some changes"
  branch develop
  checkout develop
  commit
  commit
  checkout main
  merge develop
  commit
  commit
```

---

# Keystrokes

<kbd>Ctrl</kbd> + <kbd>Alt</kbd> + <kbd>Del</kbd>

---

# Import shared slides

<!-- write-here "shared-slides/devops/devops-intro.md" -->
<!-- end-write -->
