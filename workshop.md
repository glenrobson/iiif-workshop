This page: **http://bit.ly/iiif-va-workshop**

## Prerequisites:

For all parts:

 * Chrome JSON view plugin: https://chrome.google.com/webstore/detail/jsonview/chklaanhfefbnpoihckbnefhakgolnmc

For the IIIF Image API:
 * Java 8 from https://iiif.github.io/training/intro-to-iiif/PREREQUISITES.html
 * Note the above link also provides useful information on command line usage.

For working on the Presentation API:
 * Chrome Web Server: http://ronallo.com/iiif-workshop/preparation/web-server.html (For working with Manifests).
 * If you are comfortable with Apache or nginx you could use that but you will need to add the CORS headers see:
  * For apache http://iiif.io/api/annex/notes/apache/ and
  * For nginx: https://github.com/IIIF/api/issues/737
 * And http://ronallo.com/iiif-workshop/preparation/directory.html to check the webserver is working.
 * Text editor, preferably one that does syntax highlighting and brace matching (e.g. Atom)


## Introduction to iiif

 Interoperable - viewers
 * http://projectmirador.org/demo/
 * http://hdl.handle.net/10107/4574752

Interoperable - Images
 * Edge MS No. 1 Manuscript - http://projectmirador.org/demo/

Interoperable - Collections
 * Ben Albritton’s blog: http://stanford.io/1PW789d

Europeana
 * http://www.europeana.eu/portal/en/record/07932/diglit_stahd_h106.html?q=jost+pirckhammer

musiclibs
 * http://musiclibs.net

Museum Use cases
 * https://youtu.be/AefD7wbfTFU

Image API:
 * IIIF Image API specification: http://iiif.io/api/image/2.1/

Image API Example:
 * https://tomcrane.github.io/the-long-iiif/image-api.html
 * Original Painting from the Welcome Trust:  http://wellcomelibrary.org/item/b14658197
 * Demo part of the Introduction to IIIF: http://resources.digirati.com/iiif/an-introduction-to-iiif/

Image API - info.json
 * https://dlcs.io/iiif-img/3/2/04fbbb28-d5a7-4408-b7da-800c4e65eda3/info.json

Zoom
 * http://tomcrane.github.io/presentations/tile-exploder.html
 * Open sea dragon zoom: https://tomcrane.github.io/the-long-iiif/dee-osd.html

Tiles:
 * Mike Appleby's puzzle: http://puzzle.mikeapps.me/

Viewers & Image Servers:
 * https://github.com/IIIF/awesome-iiif   

Image Server options:

 * Hosted
    * Klokan: https://www.iiifhosting.com/
    * Digirati: https://dlcs.info/
 * Static tiles
    * https://github.com/zimeon/iiif/tree/master/demo-static
    * Example: https://glenrobson.github.io/iiif/2018/01/12/iiif-from-scrtach.html
 * IIIF Image server
    * https://github.com/IIIF/awesome-iiif#image-servers
 * Provided by DAMS/Repository
    * ContentDM: https://www.oclc.org/developer/news/2017/image-open-access.en.html
    * Rosetta: https://knowledge.exlibrisgroup.com/Rosetta/Training/What%27s_New_Videos/Rosetta_5-3/IIIF_Image_Viewing
    * Axiell Collections" http://alm.axiell.com/collections-management-solutions/axiell-collections/


Image API Cantaloupe install
 * https://iiif.github.io/training/intro-to-iiif/INSTALLING_CANTALOUPE.html
 * If you don't have access to the command line you can download the following bat file to start Cantaloupe: [startCantaloupe.bat](files/startCantaloupe.bat). Store this in the Cantaloupe directory.

Exercises
 * Show image in Leaflet
    * http://mejackreed.github.io/Leaflet-IIIF/examples/?url=http://127.0.0.1:8182/iiif/2/eddie.jpg/info.json
 - Show image in Openseadragon
    * Todo
 * Image cropping
    * https://jbhoward-dublin.github.io/IIIF-imageManipulation/index.html?imageID=https://iiif.ucd.ie/loris/ivrla:10408
 * HTML page:
    * Create simple HTML page with img link
    * e.g. [showImage.html](files/showImage.html)
 * Image comparison:
    * http://ronallo.com/iiif-workshop/image/comparison.html

## Presentation API

Presentation API:
 * http://iiif.io/api/presentation/

Example Manifest:
 * http://dams.llgc.org.uk/iiif/2.0/4642022/manifest.json

Metadata:
 * Simple: https://iiif.harvardartmuseums.org/manifests/object/299843
 * Multilingual: http://dams.llgc.org.uk/iiif/2.0/4642022/manifest.json

Table of Contents:
 * http://dams.llgc.org.uk/iiif/2.0/4642022/manifest.json

Image Choice
 * http://resources.digirati.com/iiif/an-introduction-to-iiif/dee-sbs.html

BNF Manuscript Illustration Example
 * http://demos.biblissima-condorcet.fr/chateauroux/osd-demo/

Example manifest with OCR annotations:
 * https://damsssl.llgc.org.uk/iiif/2.0/1097087/manifest.json

Creating your own manifest:
 * http://ronallo.com/iiif-workshop/presentation/creating-manifest.html

IIIF Audio and Visual
 * Fire example: https://tomcrane.github.io/fire/

IIIF Search API
 * API: http://iiif.io/api/search/1.0/
 * UV viewer search: https://d.lib.ncsu.edu/collections/catalog/nubian-message-1995-04-01/

Authentication API:
 * http://iiif.io/api/auth/1.0/

Exercises
 * Validate Manifest with
    * http://iiif.io/api/presentation/validator/service
 * Open in Mirador
    * http://projectmirador.org/
 * Open in UV
    * http://universalviewer.io/
 * Annotate with
    * http://swib.gdmrdigital.com/

Community:
 * Email group: iiif-discuss@google.com   
 * Join Slack discussions: http://bit.ly/iiif-slack

## IIIF Audio Visual
https://tomcrane.github.io/fire/

## IIIF Search API:
Spec:
   * http://iiif.io/api/search/1.0/
Annotation:
  * https://www.w3.org/TR/annotation-model/
NCSU Manifest with search API:
  * https://d.lib.ncsu.edu/collections/catalog/nubian-message-1995-04-01/manifest
Example search result:
  * https://ocr.lib.ncsu.edu/search/nubian-message-1995-04-01?q=warrior
Example auto suggest:
  * https://ocr.lib.ncsu.edu/suggest/nubian-message-1995-04-01?q=war
Search in UV:
  * https://d.lib.ncsu.edu/collections/catalog/nubian-message-1995-04-01/  

Exercise:
 * Simple Annotation Server:
    * https://github.com/glenrobson/SimpleAnnotationServer/blob/mirador-2.1.4/doc/IIIFSearch.md
 * Index Manifest: http://swib.gdmrdigital.com/sas/uploadManifest.html
    * Note search link
 * Annotate manifest using mirador: http://swib.gdmrdigital.com/
 * Add search service replacing `@id` with id from the index manifest above.
```
"service": [
    {
        "@context": "http://iiif.io/api/search/0/context.json",
        "@id": "https://ocr.lib.ncsu.edu/search/nubian-message-1995-04-01",
        "profile": "http://iiif.io/api/search/0/search",
        "label": "Search within this thing"
    }
]
```
  * Load manifest into: http://universalviewer.io/

## IIIF Authentication api
Spec:
 * http://iiif.io/api/auth/1.0/  

## Further reading:
 * IIIF Guide: http://resources.digirati.com/iiif/an-introduction-to-iiif/ from Tom Crane
 * A two day workshop from Jason Ronallo: http://ronallo.com/iiif-workshop/
 * Hands on workshop from Jack Reed and Drew Widget: https://iiif.github.io/training/intro-to-iiif/
 * List of IIIF compatible software and projects: https://github.com/IIIF/awesome-iiif

## Extras
Crowdsourcing:
 * https://www.youtube.com/playlist?list=PLMd2mmRYjSJlKs829X0z_kYueQemSfwDd

Cooper Hewitt Example metadata:
 * https://github.com/cooperhewitt/collection/blob/master/objects/169/619/579/169619579.json


## Feedback form

 https://goo.gl/forms/fZmCbOxzlfTwZBjF2  

## Contact

Glen Robson - IIIF Technical Coordinator

glen.robson [at] iiif.io

twitter: @glenrobson
