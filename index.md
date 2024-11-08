---
# You don't need to edit this file, it's empty on purpose.
# Edit theme's home layout instead if you wanna make some changes
# See: https://jekyllrb.com/docs/themes/#overriding-theme-defaults

last_modified_at: 07/07/2023


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
  excerpt: "A tool to easily estimate the carbon footprint of a computation."
  url: "/GAapp-overview/"
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
  url: /resources/
  btn_label: "Learn more"
  btn_class: "btn--primary"

feature_training:
- image_path: /assets/images/placeholder_16x9.jpg
  alt: "Placeholder."
  title: "Including sustainability in computational training."
  excerpt: "How can we include sustainability in training sessions, from undergraduates to post-docs."
  url: /resources/
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

<!-- __Are you looking for the online calculator?__ It's been moved to [calculator.green-algorithms.org](http://calculator.green-algorithms.org)
{: .notice--success} -->

<!-- __:hourglass: This website is a work in progress, and we will keep adding content in the coming weeks/months!__ Comments/suggestions can be made [here](https://github.com/GreenAlgorithms/GreenAlgorithms.github.io/issues).
{: .notice--warning} -->

__:bust_in_silhouette: We are recruiting!__ Interested in joining the Green Algorithms Initiative? We have a range of roles (research, software engineering, Community management and project coordination), more details [here](/join-us) (:warning: closing date coming up: 25/11/2024).
{: .notice--info}

__:tada: The Green Algorithms project has won the [2024 Susannah Boddie Impact of the Year Award](https://www.hdruk.ac.uk/news/winners-announced-2024-hdr-uk-annual-prizes/){:target="_blank"} at the Health Data Research UK annual conference!__ “The panel applauded the work’s clear impact on policy in a short time frame. The panel were impressed by the direct and tangible environmental impacts of these efforts, and recognised the pioneering role of this collaborative effort in raising awareness and providing tools for carbon footprint estimation in computational research.”
{: .notice--success}

__:mega: We are starting a Community of Practice around Environmentally Sustainable Computational Science!__ Interested in joining it or just seeing how this goes? __Just fill in [this form](https://forms.gle/pftpt2YEFsQqayut6).__
{: .notice--info}

__:mega: New publication! _"GREENER principles for environmentally sustainable computational science".___ We have just released a Perspective in _Nature Computational Science_ which sets out fundamental principles for environmentally sustainable computational science (acronym GREENER), as well as guidance for best practices moving forward. The work was a collaboration with major stakeholders such as HDR-UK, EMBL-EBI, Wellcome and UKRI. [\[link\]](https://rdcu.be/dfpLM)
<!-- {% include figure image_path="assets/images/roadmap figures 8b.jpg" %} -->
{: .notice--info}

The Green Algorithms project aims at promoting more environmentally sustainable computational science. It regroups calculators that researchers can use to estimate the carbon footprint of their projects, tips on how to be more environmentally friendly, training material, past talks etc.

<!-- TODO add news -->

<!-- TODO do the google SEO -->

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
