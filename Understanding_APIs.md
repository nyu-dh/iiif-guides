# 🔎 Understanding APIs

## What are APIs?
API stands for Application Programming Interface. In the context of IIIF, APIs define how users can interact with content once it’s compliant with IIIF standards. There are many, but the two people interface with most often are the Image API and Presentation API.

## Image API
The Image API in IIIF focuses on delivering images **efficiently** and **consistently** across different systems and viewers. The Image API uses a standardized URI syntax to request images. This means that images can be requested, accessed, and manipulated through the Image API and displayed through a browser, without having to download or manipulate the original image. 

- The URI can look like this in a browser: 
**{scheme}://{server}{/prefix}/{identifier}/{region}/{size}/{rotation}/{quality}.{format}** 
- In practice, this link may look like: https://example.org/image-service/abcd1234/full/max/0/default.jpg

Here's a quick rundown explaining the pieces of the URI syntax: 
| Syntax element | What it does                                                                                                                                                                                                                                                      |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Scheme         | This specifies the protocol or method used to access the resource. Usually, this is _http_, or _https_, like other links on the web                                                                                                                                  |
| Server         | This represents the host of the IIIF images. It identifies the location where the images are held                                                                                                                                                                |
| Prefix         | This part is optional, and refers to any path that may be used to locate a specific image (if, for example, it is held in a specific collection                                                                                                                  |
| Identifier     | This is the specific image or resource being requested from the server                                                                                                                                                                                           |
| Region         | This parameter can change what portion of the image is requested (essentially, crop an image). For example, it can define a rectangular region using pixels as coordinates, or use predefined values like "full" (the entire image) or "square" (a square region) |
| Size           | This parameter specifies the size or dimension of the image in terms of width and height. This can be through pixel values or percentages of the original image size.                                                                                             |
| Rotation       | This parameter allows users to retrieve images rotated at different angles (90°, 180°, etc)                                                                                                                                                                       |
| Quality        | This parameter allows users to change some quality of the image, like returning in color ("color"), grayscale ("gray") or two-tone ("bitonal")                                                                                                                   |
| Format         | This parameter specifies the format of the image. Common types include .jpeg and .png                                                                                                                                                                            |

The scheme, server, prefix, and identifier are set for a specific image. However, every parameter after that (region, size, etc) can be determined by the user to manipulate how the image is displayed. 

For example: 

_A Creek in St. Thomas_, by Camille Pissarro (1856) - Full display:
![_A Creek in St. Thomas, Camille Pissarro_](https://media.nga.gov/iiif/b1461d28-88d4-4aee-88dd-a78d368308ff/full/full/0/default.jpg)

The same painting, square + black and white display:
![_A Creek in St. Thomas, Camille Pissarro_](https://media.nga.gov/iiif/b1461d28-88d4-4aee-88dd-a78d368308ff/square/full/0/gray.jpg)

The same painting, with a portion selected and rotated: 
![_A Creek in St. Thomas, Camille Pissarro_](https://media.nga.gov/iiif/b1461d28-88d4-4aee-88dd-a78d368308ff/800,600,900,800/full/90/default.jpg)

Try to play around with the different uses! The link for this image is [https://media.nga.gov/iiif/b1461d28-88d4-4aee-88dd-a78d368308ff/full/full/0/default.jpg](https://media.nga.gov/iiif/b1461d28-88d4-4aee-88dd-a78d368308ff/full/full/0/default.jpg), and you can edit it directly in your browser to see the variety of displays you can get.

## Presentation API
The Presentation API is the second most-used IIIF API. It complements the Image API by providing metadata about how to structure, describe, and display digital content. It is what allows users to bring objects into different viewers and systems consistently.

What makes the Presentation API work is a _Manifest_. A Manifest is a JSON file that contains the "metadata wrapper" for images and collections of images. This metadata includes the title, description, author, date, and licensing information for an object. 