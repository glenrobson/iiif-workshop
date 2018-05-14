This is a short guide to edit an example manifest to use your own local images. This guide assumes you have already followed the [Cantaloupe Tutorial](https://iiif.github.io/training/intro-to-iiif/INSTALLING_CANTALOUPE.html) and also installed Chrome Web Server: http://ronallo.com/iiif-workshop/preparation/web-server.html.

Step 1:

 * Save the following manifest to your directory that is shared through the Chrome Web Server:
  * [manifest.json](files/manifest.json)

Step 2:
 * Edit the "@id" to point to the resolvable location of the manifest:

```
4: "@id": "**CHANGE_ME** - e.g. http://localhost:3000/manifest.json",
```  

This needs to be the URL you put in your browser to access the manifest. If you saved the manifest in the root of your Chrome Web Server you can use `http://localhost:3000/manifest.json`.

Step 3:
 * Edit the label, description and attribution. The attribution and description are text fields that can include a limited set of HTML: http://iiif.io/api/presentation/2.1/#html-markup-in-property-values. Put some basic metadata in that would allow a user to identify the item e.g:

```
5: "label": "Sheep pictures",
6: "description": "These are the most wonderful pictures of <b>sheep</b> gather together in one place. ",
7: "attribution": "Copyright Glen Robson",
```

Step 4:
 * Change canvas ID.
 * Change the canvas ID to something that is unique. It should be a http URL but doesn't have to resolve.
 * A canvas ID is important as its the target for any annotations or transcriptions. It is important that once published the canvas id is preserved so that any external annotations still work.

```
14:           "@id": "http://localhost:3000/manifest/canvas/1.json",
```

'''Note:''' in real live localhost:3000 is not a good id to use as it is not unique.

 * Now change the `on` value to match the canvas id you've created:
```
22: "on": "http://localhost:3000/manifest/canvas/1.json"
```

Step 5:
 * Add a link to the image API.
 * You need to look at your info.json for the image you are going to add. You should see something like:

```
{

    "@context": "http://iiif.io/api/image/2/context.json",
    "@id": "http://iiif.gdmrdigital.com/image/iiif/2/lc%2Fblock_books%2FBB-AoM_595_00%2FBB-AoM_595_00_PSC.jp2",
    "protocol": "http://iiif.io/api/image",
    "width": 6132,
    "height": 8176,
    "sizes": [
        {
            "width": 96,
            "height": 128
        },
        {
            "width": 192,
            "height": 256
        },
        {
            "width": 383,
            "height": 511
        },
        {
            "width": 767,
            "height": 1022
        },
        {
            "width": 1533,
            "height": 2044
        },
        {
            "width": 3066,
            "height": 4088
        },
        {
            "width": 6132,
            "height": 8176
        }
    ],
    "tiles": [
        {
            "width": 1024,
            "height": 1024,
            "scaleFactors": [
                1,
                2,
                4,
                8,
                16,
                32,
                64
            ]
        }
    ],
    "profile": [
        "http://iiif.io/api/image/2/level2.json",
        {
            "formats": [
                "jpg",
                "tif",
                "gif",
                "png"
            ],
            "maxArea": 400000000,
            "qualities": [
                "bitonal",
                "default",
                "gray",
                "color"
            ],
            "supports": [
                "regionByPx",
                "sizeByW",
                "sizeByWhListed",
                "cors",
                "regionSquare",
                "sizeByDistortedWh",
                "sizeAboveFull",
                "canonicalLinkHeader",
                "sizeByConfinedWh",
                "sizeByPct",
                "jsonldMediaType",
                "regionByPct",
                "rotationArbitrary",
                "sizeByH",
                "baseUriRedirect",
                "rotationBy90s",
                "profileLinkHeader",
                "sizeByForcedWh",
                "sizeByWh",
                "mirroring"
            ]
        }
    ]

}
```

 * The things we need to copy to the manifest is the `@id` of the image, the height and width. In the example above the `@id` is:

```
"@id": "http://iiif.gdmrdigital.com/image/iiif/2/lc%2Fblock_books%2FBB-AoM_595_00%2FBB-AoM_595_00_PSC.jp2",
```

and the width is 6132 and the height is 8176. Now add these to your manifest:

```
16: "width": 6132,
17: "height": 8176,
```

'''Note:''' you don't need speech marks around numbers.

Now add the id:
```
29:  "@id": "http://iiif.gdmrdigital.com/image/iiif/2/lc%2Fblock_books%2FBB-AoM_595_00%2FBB-AoM_595_00_PSC.jp2",
```

Lastly add a link to a image for the resource @id to ensure the manifest works in Mirador. This is a good chance to test your image API knowledge.
```
25: "@id": "http://iiif.gdmrdigital.com/image/iiif/2/lc%2Fblock_books%2FBB-AoM_595_00%2FBB-AoM_595_00_PSC.jp2/full/500,/0/default.jpg",
```

Step 6:
 * Test to see if it works:
  * http://projectmirador.org/demo/
  * Click the four boxes in a square at the top right.
  * Select 'Replace Object'
  * Add you manifest url to `Add new object from URL:`
  * Click load.
  * All being well your manifest should appear. 

Exercises
 * Validate Manifest with
    * http://iiif.io/api/presentation/validator/service
 * Open in Mirador
     * http://projectmirador.org/
 * Open in UV
     * http://universalviewer.io/
