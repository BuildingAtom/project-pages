---
# Front matter. This is where you specify a lot of page variables.
title:  "Example Page"
date:   2023-06-16 03:03:01 -0400
description: >- # Supports markdown
  This is the main project page and the page used to demonstrate how this works with all of the options for the Front Matter present
show-description: true

# Preview image for social media cards
image:
  path: /assets/img/twitter.png
  height: 100
  width: 100
  alt: Twitter Logo

# Only the first author is supported by twitter metadata
authors:
  - name: Someone
    footnotes: 1
  - name: Adam Li
    url: https://buildingatom.io
    email: person [at] example.edu
    mailto: person@example.edu
    footnotes: 2
  - name: Person 3
    email: someemail@example.com
    footnotes: 3
  - name: Guy 4
    mailto: combined@example.com
    footnotes: 3
  - name: Another Person

# If you just want a general footnote, you can do that too.
# See the sel_map and armour-dev examples.
author-footnotes:
  1: >- # Supports markdown
    You can add random extra footnotes
  2: And include websites or emails which are detached from their mailto
  3: You can also just specify the email and not have a mailto, or if there's a mailto you want to use, you can specify only that

links:
  - icon: arxiv
    icon-library: simpleicons
    text: Arxiv HP
    url: https://arxiv.org/
  - icon: github
    icon-library: simpleicons
    text: Code
    url: https://github.com/BuildingAtom/project-pages

# End Front Matter
---

{% include sections/authors %}
{% include sections/links %}

# Section Break
---

# As you can see, the authors and link are just includes

In other words, I can actually move them wherever I want, or place them here again.
The data is provided by the front matter.
Let's try flipping the order.

{% include sections/links %}
{% include sections/authors %}

---

There is quite a bit of flexibility to how you structure the text too.
Here, I'm going to make a justified grey content block with the heading outside.

# Content
<div markdown="1" class="content-block grey justify no-pre">
some text
</div>

I made this look right by adding the `no-pre` class.
If you don't include `markdown="1"` it will fail to render any markdown inside.

You can also make fullwidth embeds
<div class="fullwidth">
<video controls="" width="100%" style="background-color:black;"></video>
</div>

<div markdown="1" class="content-block grey justify">
# Topic inside of the content block

Lorem ipsum dolor sit amet Consectetur adipiscing elit Integer molestie lorem at massa.

![Alt Text](https://cdn.pixabay.com/photo/2019/09/05/01/11/mountainous-landscape-4452844_1280.jpg "Random Image")
</div>

# Topic outside of content block

![Alt Text](https://cdn.pixabay.com/photo/2019/09/05/01/11/mountainous-landscape-4452844_1280.jpg "Random Image")

Lorem ipsum dolor sit amet Consectetur adipiscing elit Integer molestie lorem at massa.

## This is how we can get the image at 100%

<div markdown="1" class="fullwidth">
![Alt Text](https://cdn.pixabay.com/photo/2019/09/05/01/11/mountainous-landscape-4452844_1280.jpg "Random Image")
</div>

## And this is how we can get the image closer

<div markdown="1" class="no-pre">
![Alt Text](https://cdn.pixabay.com/photo/2019/09/05/01/11/mountainous-landscape-4452844_1280.jpg "Random Image")
</div>

Lorem ipsum dolor sit amet Consectetur adipiscing elit Integer molestie lorem at massa.


<div markdown="1" class="content-block grey justify">
# Citation

*Insert whatever message*

```bibtex
@article{nash51,
  author  = "Nash, John",
  title   = "Non-cooperative Games",
  journal = "Annals of Mathematics",
  year    = 1951,
  volume  = "54",
  number  = "2",
  pages   = "286--295"
}
```
</div>