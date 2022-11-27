---
# You don't need to edit this file, it's empty on purpose.
# Edit theme's home layout instead if you wanna make some changes
# See: https://jekyllrb.com/docs/themes/#overriding-theme-defaults

last_modified_at: 22/11/2022


layout: splash
author_profile: false

header:
  overlay_image: assets/images/stripes_banner_1.png
  overlay_filter: linear-gradient(rgba(255, 255,255, 0), 20%, rgba(255, 255, 255, 1))
  text_color: rgb(80, 80, 80)
  actions:
  - label: "Carbon footprint calculator"
    url: http://calculator.green-algorithms.org

permalink: /
title: "Green Algorithms"
excerpt: "Towards environmentally sustainable computational science"

feature_row_1:
- image_path: /assets/images/GAapp_16x9.jpg
  alt: "Screenshot of the green algorithms calculator."
  title: "The online calculator"
  excerpt: "A tool to easily estimate the carbon footprint of a project."
  url: "/app-user-guide/"
  btn_label: "Learn more"
  btn_class: "btn--primary"
- image_path: /assets/images/GA4HPC_16x9.jpg
  alt: "Screenshot of the green algorithms HPC tool."
  title: "Green Algorithms 4 HPC"
  excerpt: "A tool that calculates the carbon footprint of all computations run on an HPC platform."
  url: /GA4HPC/
  btn_label: "Learn more"
  btn_class: "btn--primary"
- image_path: /assets/images/idea_16x9.jpg
  alt: ""
  title: "Tips for green computing"
  excerpt: "Resources to move towards more sustainable computing."
  url: /training/
  btn_label: "Learn more"
  btn_class: "btn--primary"

feature_training:
- image_path: /assets/images/placeholder_16x9.jpg
  alt: "Placeholder."
  title: "Including sustainability in computational training."
  excerpt: "How can we include sustainability in training, from undergraduates to post-docs."
  url: /training/
  btn_label: "Learn more"
  btn_class: "btn--primary"

gallery_logos:
  - url: "https://www.phpc.cam.ac.uk"
    image_path: /assets/images/DPHPC_gallery.png
  - url: "https://www.hdruk.ac.uk"
    image_path: /assets/images/HDRuk_gallery.png
  - url: "https://baker.edu.au"
    image_path: /assets/images/Baker_gallery.png
---

__Are you looking for the online calculator?__ It's been moved to [calculator.green-algorithms.org](http://calculator.green-algorithms.org)
{: .notice--success}

__:hourglass: This website is a work in progress, and we will keep adding content in the coming weeks!__
{: .notice--warning}

The Green Algorithms project aims at promoting more environmentally sustainable computational science. It regroups calculators that researchers can use to estimate the carbon footprint of their projects, tips on how to be more environmentally friendly, training material, past talks etc.



<!-- ## Estimating the carbon footprint of algorithms -->

<!-- {% include feature_row id="feature_row_1" type="left"  %} -->
{% include feature_row id="feature_row_1" %}

<!-- ## From measuring to reducing the environmental impacts of our work

{% include feature_row id="feature_training" %} -->

## Get in touch

You can reach out by email at green.algorithms(at)gmail.com.

For any technical issues with one of the tools, either email or open an issue on the corresponding [GitHub](https://github.com/GreenAlgorithms).

## Supported by:

{% include gallery id="gallery_logos" type="left"%}

[![CC BY 4.0][cc-by-image]][cc-by]&nbsp;&nbsp; All the work on this website is licensed under a [Creative Commons Attribution 4.0 International License][cc-by].

[cc-by]: http://creativecommons.org/licenses/by/4.0/
[cc-by-image]: https://i.creativecommons.org/l/by/4.0/88x31.png
