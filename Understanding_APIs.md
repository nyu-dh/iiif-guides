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

The scheme, server, prefix, and identifier are set for a specific image. However, every parameter after that (region, size, etc) can be determined by the user to manipulate how the image is displayed. And this the basis on how the rest of IIIF viewers work!

## Presentation API
