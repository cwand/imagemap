# REDCap module: Image Map (DK alt)



This REDCap module replaces an input, radio, or checkbox field with an image that users can interact with to select one or more options. Specific applications include a body map (with over 70 body regions), a smile scale from 1-7 with facial expressions, three representations of teeth and teeth surfaces, among others. See below for a complete list of current imagemaps. The module is tied to questions via the `@IMAGEMAPDK` action tag and the name of one of the pre-defined image maps.  e.g. `@IMAGEMAPDK=PAINMAP_MALE_DK_ALT`. The original ImageMaps (with English or no alt-text) are also available through the original names (e.g. `@IMAGEMAPDK=PAINMAP_MALE`)

This project is a derived version of the original Image Map project, with the only change being the addition of Danish ALT-text when hovering with the mouse over the images.


## Prerequisites
- REDCap >= 8.0.3 (for versions < 8.0.3, [REDCap Modules](https://github.com/vanderbilt/redcap-external-modules) is required).


## Manual Installation
- Clone this repo into `<redcap-root>/modules/imagemapdk_vX.Y.Z`.
- Go to **Control Center > External Modules** and enable Image Map (DK alt).
- To activate this module for a particular project, go to the project home page, click on the **External Modules** link, and then enable Image Map (DK alt) for that project.


## Features included
This module defines a new action tag: `@IMAGEMAPDK`. The possible values which differ from the original ImageMap module are:


**`PAINMAP_MALE_DK_ALT`**

Representation of a generic male body with alt text in Danish.  
![PAINMAP_MALE](./img/painmap_male.png)



## Usage
To display one of the images above in a survey or data entry form, add a new field of type **Text Box** and include one of the following options in the **Action Tags / Field Annotation (optional)** field:

```
@IMAGEMAPDK=PAINMAP_MALE
@IMAGEMAPDK=PAINMAP_MALE_DK_ALT
@IMAGEMAPDK=PAINMAP_FEMALE
@IMAGEMAPDK=SMILE_SCALE
@IMAGEMAPDK=5_FACE_PAINMAP
@IMAGEMAPDK=SINGLE_TOOTH
@IMAGEMAPDK=TEETH_SURFACE
@IMAGEMAPDK=TEETH
@IMAGEMAPDK=PIRADS
@IMAGEMAPDK=PI-RADS_V2-1
@IMAGEMAPDK=RHEUMATOID_MAN
@IMAGEMAPDK=VA_CHART
@IMAGEMAPDK=MBODY
@IMAGEMAPDK=BEES
@IMAGEMAPDK=DO_TOUCH_NET_BODY_COLOUR
@IMAGEMAPDK=DO_TOUCH_NET_BODY_GREY
@IMAGEMAPDK=66SWOLLEN_68TENDER_JOINT_COUNT
```

Each region of an image is associated with a key, for example, the "Ankle (front-left)" of the female body diagram is linked to the key "f34". To find a particular key for a body part, please refer to the HTML files (map files) located in the folder `maps`. After selecting multiple body parts, the field containing the action tag `@IMAGEMAPDK` will have as a value a string of comma-separated keys, e.g. "f36,f17,f18,f21". Similarly, if using the faces diagram, the field containing the action tag (e.g. `@IMAGEMAPDK=SMILE_SCALE`) will have the value corresponding to the face clicked.


## Acknowledgements & Copyright
 * The original body was devised by Dr. Ming-Chih J Kao and Professor Sean Mackey at Stanford University as part of [CHOIR](choir.stanford.edu). Use of the 'bodymap' images requires that the CHOIR attribution remains intact.
 * The imagemap plugin/hook was written at Stanford by Andrew Martin and converted to an external module in collaboration with CTS-IT - University of Florida.
 * The 5-face pain image and map was included by Lewisa2.
 * The odontogram maps were contributed by Bas de Veer and collaborators at the ITHS and Christy McKinney at the University of Washington and Seattle Children’s Research Institute.
 * The PIRADS images were contributed by Dr. Richard Fan from Stanford University. Geoffroey-Allen Franklin gfranklin@atsu.edu provided the new image and mapping for Pirads v2.1.
 * Rheumatoid Man was contributed by Dr. Blaine Vlantis of the University of Cape Town.
 * VA Chart image appears in the paper ["Deep Affect Prediction in-the-Wild: Aff-Wild Database and Challenge, Deep Architectures, and Beyond"](https://link.springer.com/article/10.1007/s11263-019-01158-4) by Kollias, D., Tzirakis, P., Nicolaou, M.A. et al. For image usage, refer to [Springer's copyright information](https://link.springer.com/article/10.1007/s11263-019-01158-4#copyrightInformation).
 * The Michigan Body Map (MBODY) image was created by the Division of Pain Research Anesthesiology of the University of Michigan. Please refer to their [website](https://medicine.umich.edu/dept/pain-research/clinical-research/michigan-body-map-mbm) for copyright information.
 * The DO-Touch.NET body map was created by Jamie Carroll using the international standard for osteopathic manipulative medicine (OMM) research established by DO-Touch.NET. Use of this image map requires the attributions to remain in place. [website](https://www.do-touch.net). Jane Coe Johnson jjohnson@atsu.edu assisted Geoffroey-Allen Franklin gfranklin@atsu.edu updating information about the DO-Touch.NET image maps.
 * The 66 Swollen / 68 Tender Joint Map was contributed by Dr Tom Lynch from the Institute of Bone and Joint Research, University of Sydney. The image was adopted with permission from Dr Alexis Ogdie-Beatty and first published in this article from the OMERACT group: [website](http://www.jrheum.org/content/early/2019/05/24/jrheum.181089).
 * The addition of Danish alt text was implemented by Chris Andersen (Open Patient data Explorative Network, Odense).
