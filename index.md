---
title: "Stat 999: Principles and Techniques of Data Science"
subtitle: "UC Berkeley, Spring 2024"
authors:
  - name: Fernando Perez
    affiliations: ["Instructor"]
    email: fernando.perez@berkeley.edu
  - name: Facu Sapienza
    affiliations: ["GSI"]
    email: fsapienza@berkeley.edu
---

<!--div class="staffer">
  <img class="staffer-image" src="{{ staff_photo }}" height=50 width=50 alt="{{ staff_name }}">
  <div>
    <h3 class="staffer-name">
      <a href="{{ staff_website }}" target="_blank">{{ staff_name }}</a>
      <p class="staffer-pronouns"><b>{{ staff_pronouns }}</b></p>
    </h3>
    <p><a href="mailto:{{ staff_email }}">{{ staff_email }}</a></p>
    <p><b>Office Hours:</b> {{ staff_oh }}</p>
  </div>
</div-->

::::{grid} 1 2 3 3

:::{card}
:header: Fernando Perez
Instructor
<div class="staffer">
  <img class="staffer-image" src="images/fernando.jpg" alt="Fernando Perez">
  <div>
      <p class="staffer-pronouns"><b>He/Him/His</b></p>
      <p><a href="mailto:fernando.perez@berkeley.edu">fernando.perez@berkeley.edu</a></p>
      <p><b>Office Hours:</b> Tue 11-12pm (Evans 419)</p>
  </div>
</div>
:::

:::{card}
:header: Facundo Sapienza
Teaching Assistant
<div class="staffer">
  <img class="staffer-image" src="images/facu2.jpg" alt="Facundo Sapienza">
  <div>
      <p class="staffer-pronouns"><b>He/Him/His</b></p>
      <p><a href="mailto:fsapienza@berkeley.edu">fsapienza@berkeley.edu</a></p>
      <p><b>Office Hours:</b> MW 2-3pm (Evans 337)</p>
  </div>
</div>
:::

:::{card}
:header: Isaac Sloan
Reader
<div class="staffer">
  <div>
      <p class="staffer-pronouns"><b>He/Him/His</b></p>
      <p><b>Office Hours:</b> MW 2-3pm (Evans 337)</p>
  </div>
</div>
:::

::::


:::{attention} Welcome to [Week 2](#week2) of Data 100!
:class: dropdown
:icon: false
👋
:::


# Schedule

MyST doesn't give you the ability to have freestyle HTML with colors and styles.

<div><p style="color: blue;">For example, this text should be blue, but it isn't.</p></div>

Instead we leverage the callout widgets to approximate highlighted links. We'd like to be able to define custom html classes for the callouts below (presumably in CSS style file). Currently only `simple` is permitted.

(week1)=
```{card}
:header: Week 1

```{list-table}
:header-rows: 0
:name: table-week1

* - Aug 24
  - :::{note} {sc}`Lecture`
    :class: simple
    :icon: false
    [Introduction](lecture/lec01)
    :::
  - :::{note} {sc}`Lecture Participation`
    :class: simple
    :icon: false
    [Lecture Participation 1](https://app.sli.do/event/w7jeDVDxMNKRaS86U4g3rQ/embed/polls/00ef9633-394c-4b61-9061-4bc4a301ed06)
    :::
  - :::{tip} {sc}`Notes`
    :class: simple
    :icon: false
    [Note 1](course-notes/intro_lec/introduction)
    :::
* - Aug 25
  - :::{attention} {sc}`Lab 1`
    :class: simple
    :icon: false
    [Prereq coding](https://data100.datahub.berkeley.edu/hub/user-redirect/git-pull?repo=https%3A%2F%2Fgithub.com%2FDS-100%2Ffa23-student&urlpath=lab%2Ftree%2Ffa23-student%2F%2Flab%2Flab01%2Flab01.ipynb&branch=main) (due Aug 29)
    :::
  - :::{danger} {sc}`Homework 1A`
    :class: simple
    :icon: false
    [Plotting and Permutation Test](https://data100.datahub.berkeley.edu/hub/user-redirect/git-pull?repo=https%3A%2F%2Fgithub.com%2FDS-100%2Ffa23-student&urlpath=lab%2Ftree%2Ffa23-student%2F%2Fhw%2Fhw01%2Fhw01.ipynb&branch=main) (due Aug 31)
    :::
  - :::{danger} {sc}`Homework 1B`
    :class: simple
    :icon: false
    [Prerequisite Math](https://drive.google.com/file/d/1PS69ERS6TNJ5lRq0gJF5Bd_VTz7xYgp-/view?usp=sharing) (due Aug 31)
    :::
```


(week2)=
```{card}
:header: Week 2

```{list-table}
:header-rows: 0
:name: table-week2

* - Aug 29
  - :::{note} {sc}`Lecture 2`
    :class: simple
    :icon: false
    [Pandas I](lecture/lec02)
    :::
  - :::{note} {sc}`Lecture Participation 2`
    :class: simple
    :icon: false
    [Lecture Participation 2](https://app.sli.do/event/w7jeDVDxMNKRaS86U4g3rQ/embed/polls/00ef9633-394c-4b61-9061-4bc4a301ed06)
    :::
  - :::{tip} {sc}`Discussion 1`
    :class: simple
    :icon: false
    [Prerequisites](course-notes/intro_lec/introduction)
    :::
* - Aug 31
  - :::{note} {sc}`Lecture 3`
    :class: simple
    :icon: false
    [Pandas III](lecture/lec03)
    :::
  - :::{note} {sc}`Lecture Participation 3`
    :class: simple
    :icon: false
    [Lecture Participation 3](https://app.sli.do/event/w7jeDVDxMNKRaS86U4g3rQ/embed/polls/00ef9633-394c-4b61-9061-4bc4a301ed06)
    :::
* - Sep 1
  - :::{attention} {sc}`Lab 2A`
    :class: simple
    :icon: false
    [Pandas](https://data100.datahub.berkeley.edu/hub/user-redirect/git-pull?repo=https%3A%2F%2Fgithub.com%2FDS-100%2Ffa23-student&urlpath=lab%2Ftree%2Ffa23-student%2F%2Flab%2Flab01%2Flab01.ipynb&branch=main) (due Sep 5)
    :::
  - :::{danger} {sc}`Homework 2A`
    :class: simple
    :icon: false
    [Food Safety Math](https://drive.google.com/file/d/1PS69ERS6TNJ5lRq0gJF5Bd_VTz7xYgp-/view?usp=sharing) (due Sep 7)
    :::
```
