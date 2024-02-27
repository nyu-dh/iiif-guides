# IIIF Quick-Start Guide

IIIF (pronounced triple-i-f), simply put, is a **method of displaying content on the web with standards, rules and guidelines that allow that content to seamlessly transition into different views, formats, and applications.**

This understanding helps to break down the four letters:

**International:** Content can be used across institutions, communities, and internationally. Additionally, the community that develops and uses IIIF exists across the globe.

**Image:** IIIF allows hosting of high-quality (full-scale) images in one source to be used elsewhere. While initially developed just for its image capabilities, IIIF has expanded to audio and video capabilities as well.

**Interoperability:** The capability to take one hosted image and use it across multiple APIs[link to this section], allowing for many users to research different aspects of the same hosted content. This interoperability also refers to collections that may be geographically or institutionally separated. In this framework, these works can be “reunited” in new ways.

**Framework:** The standards, guidelines, and metadata that allow for the former 3 functionalities.

## How does IIIF change image files?

IIIF compatibility relies on the ability to “cut” larger images (and larger files) into smaller tiles that allow for deeper zoom, faster processing, and higher quality.

This tiling effect also aligns coordinates to sections of the image, which is useful for annotations, cropping, and image manipulation

<div style="display:flex;">
  <img src="images/VG Self Portrait - Original.jpeg" alt="VG Self Portrait - Original" style="width:calc(50% - 5px); margin-right:10px;">
  <img src="images/VG Self Portrait - Grid.png" alt="VG Self Portrait - Grid" style="width:calc(50% - 5px); margin-left:10px;">
</div>

_Self-portrait Dedicated To Paul Gauguin (1888) by Vincent Van Gogh_

By doing this tiling, IIIF viewers only download the tile(s) being zoomed into from the image server, instead of the entire image.

**IIIF in Action:**

Using the same source content (the painting), we can see some of the benefits of using IIIF-compliant images and IIIF viewers. This is the painting viewed with an IIIF viewer, [Mirador](https://mirador-dev.netlify.app/__tests__/integration/mirador/), while the other is a hosted .jpg on [Artchive's server](https://www.artchive.com/wp-content/uploads/2023/04/Self-portrait-Dedicated-To-Paul-Gauguin-1888-by-Vincent-Van-Gogh.jpg) seen through the browser. 

<img src="images/Mirador Viewer - VG.gif" alt="VG Self Portrait - Original" style="width:calc(50% - 5px); margin-right:10px;">
</p>

Compare this to a .jpg of the painting hosted on [Artchive's server](https://www.artchive.com/wp-content/uploads/2023/04/Self-portrait-Dedicated-To-Paul-Gauguin-1888-by-Vincent-Van-Gogh.jpg), seen through the browser viewer: 

<img src="images/browser view - VG.gif" alt="VG Self Portrait - Original" style="width:calc(50% - 5px); margin-right:10px;">
</p>

You _could_ host a full-scale image on a server, but they are generally very large and take more time to download. This hosting also only solves the quality issue, but does not allow for the interoperability with other APIs that IIIF does. For example, if you wanted to add an annotation or additional context to the photo on the right, you may have to download and load it into another program (or several). Using the IIIF link for this painting, you can bring it into any other IIIF API.

## What are APIs?
API stands for Application Programming Interface. In the context of IIIF, APIs define how users can interact with content once it’s compliant with IIIF standards. There are many, but the two people interface with most often are the Image API and Presentation API.
- Image API
- Presentation API 

## What can you do with IIIF?
