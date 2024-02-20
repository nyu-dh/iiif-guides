# IIIF Dictionary

This page is made to be kept open while doing a training ([IIIF Self-Guided Training](https://training.iiif.io/iiif-online-workshop/)) and as a quick reference for terms that are frequently encountered used while learning about IIIF.

**IIIF:** International Image Interoperability Framework

**IIIF Link:** A special URL that connects an image URL with the additional JSON context that makes an image IIIF compliant. These links often end with /*info.json* or /*manifest.json*. When opened in a web browser, it should appear as JSON code, _not_ the image itself

**IIIF Image:** an Image that is can be made available through an IIIF Image API Server. Can usually be identified with the /info.json file name

**IIIF Manifest:** a collection of 1+ IIIF images with additional metadata in the JSON file. Can usually be identified with the /manifest.json file name

**Level 0 Image:** Usually a converted smaller file, like a standard .jpg, that is enough for a zoomable viewer, but has a limited number of sizes and regions defined due to the size of the file.

 ***Canvas**: A single image/page as part of a larger IIIF Manifest (From IIIF: the frame of reference for the display of your content, both spatial and temporal (just like a painting canvas for two-dimensional materials, or with an added time dimension for a/v content).) **... huh**

**Tiling:** The breaking of an image into different tiles that define regions and allow for zooming in an Image API

**Server**: Software that runs on a machine at all times and is accessible over the Web. For this workshop I will mostly be referring to Image API Servers but there are other types of servers including Web servers or Email servers. Sometimes they are also know as Services e.g. Image API service, Web Service or Mail Service.

**Metadata**: Data that contextualizes content. This could include the institution it is held at, when it was created, the rights associated with it, alternate text for an image, etc

***Image Server:** Software that specializes in providing access to images

**API:** Application Programming Interface. In this case an agreed standard between the Image API Server and the Image API Client.

**Image API:** the agreed standard and specification which forms the contract between Client and Server

**Presentation API:**

**Annotations:** a standard way to associate different types of content to whatever is on your canvas (such as a translation of a line or the name of a person in a photograph. In the IIIF model, images and other presentation content are also technically annotations onto a canvas) (IIIF)

**JSON:** JavaScript Object Notation, a human-readable format that holds the metadata and extra information about how to order or display content
