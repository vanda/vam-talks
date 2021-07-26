# TaNC Registration Webinar - Links

This is to accompany the introduction given by Luca at the Towards a National Collection Image Registration Webinar organised by the National Gallery - https://tanc-ahrc.github.io/IIIF-TNC/seminar01.html

## V&A Use Cases

These are different varieties of the problem of image alignment/registration we have uncovered so far.

  - **Multispectral imaging / scans**
    - Balenciaga
      - [vam.ac.uk/articles/x-raying-balenciaga](https://www.vam.ac.uk/articles/x-raying-balenciaga)
    - Raphael
      - [vam.ac.uk/articles/explore-the-raphael-cartoons](https://www.vam.ac.uk/articles/explore-the-raphael-cartoons)
      - [vam.ac.uk/articles/the-raphael-cartoons-the-miraculous-draught-of-fishes](https://www.vam.ac.uk/articles/the-raphael-cartoons-the-miraculous-draught-of-fishes)
  - **Preparatory sketches  / final work**
    - Constable
      - [vam.ac.uk/articles/john-constables-sketches](https://www.vam.ac.uk/articles/john-constables-sketches)
  - **Sequence, Series**
     - Midsummer Night
       - [vanda.github.io/layerstack/?manifest=./public/manifest_midsummer_night.json](https://vanda.github.io/layerstack/?manifest=./public/manifest_midsummer_night.json)
  - **Temporal before/after**
      - Creswell 
        - [vam.ac.uk/articles/creswells-egypt-syria-and-palestine-photographs](https://www.vam.ac.uk/articles/creswells-egypt-syria-and-palestine-photographs)
  - **Restoration before/after**
      - Constable Haywain
        - [vanda.github.io/layerstack/?manifest=./public/manifest_constable_restoration.json](https://vanda.github.io/layerstack/?manifest=./public/manifest_constable_restoration.json)
  - **Cross-Institutional Research**
      - Raphael Cartoons/tapestries 
        - [vanda.github.io/layerstack/?manifest=./public/manifest_raphael_cartoon_tapestry.json](https://vanda.github.io/layerstack/?manifest=./public/manifest_raphael_cartoon_tapestry.json)
      - Raphael Cartoon/prints  
        - [vanda.github.io/layerstack/?manifest=./public/manifest_raphael_miraculous_prints.json](https://vanda.github.io/layerstack/?manifest=./public/manifest_raphael_miraculous_prints.json)
      - Rembrandt Etchings 
        - [vanda.github.io/layerstack/?manifest=./public/manifest_rembrandt_etching.json](https://vanda.github.io/layerstack/?manifest=./public/manifest_rembrandt_etching.json)

## Discussion intro
I'm Luca from the V&A museum, where curators, conservators, researchers and casual browsers have been comparing objects and their images since the museum's conception. And close comparison has always demanded some alignment of some sort, if only in the eye of the observer. 

Here's a list of roughly categorised use cases we've uncovered so far for image registration & alignment, with links to live examples that you're welcome to try. 

Working with images of objects, any misalignment as a result of the imaging or scanning processs is locked into the image for posteristy, and when comapring images those misalignments have to be compensated for by the observer.

Since adopting IIIF we've been using its Image API to realign images on the fly, for close comparison in some of our image viewers. This alleviates the need for potentially endless image derivatives, depending on the comparisons being made around any number of specific regions of interest within an image.

From my perspective as a developer of the V&A website, some cases for image registration are simpler than others: in the case of our most recent digitisation project, the job of registering the various scan types of the Raphael Cartoons fell to the team delivering us the scans as pre-registered images. However, since then we've also encoutered our most complicated example for alignment in a viewer - that of the Cartoons with the tapestries that once mirrored them precisely, but have distorted in the centuries since they were made. We can now pull in the tapestry images directly from the Vatican Museum collections, but it's obvious we can only go so far at realigning them using the on-the-fly crop/scale/rotate Image API parameters. As such we've started wondering about the feasibility of extending the API's power to include warping/skewing, but realise this would pose some big technical challenges, not least around processing power and caching impilcations. Maybe a more practical approach would be to use the Presentation API to record and replay more complex image operations within IIIF viewers able to process extra image manipultion instructions recorded within image manifests. These are some of the subjects we'd like to discuss as part of this webinar. 
