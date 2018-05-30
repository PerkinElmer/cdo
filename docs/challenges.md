# Challenges in *ChemDraw*-*Office* Integration

<!-- TOC depthFrom:2 -->

- [Challenges in *ChemDraw*-*Office* Integration](#challenges-in-chemdraw-office-integration)
  - [Copying & Pasting from *ChemDraw* to *Office 365*](#copying-pasting-from-chemdraw-to-office-365)
  - [Copying & Pasting from *ChemDraw* to *Office* on *Mac*](#copying-pasting-from-chemdraw-to-office-on-mac)
  - [Cross-Platform Support of *ChemDraw* Images in *Office* Documents](#cross-platform-support-of-chemdraw-images-in-office-documents)
  - [Poor SVG Support by *Office* Documents](#poor-svg-support-by-office-documents)

<!-- /TOC -->

## Copying & Pasting from *ChemDraw* to *Office 365*

Currently, one cannot copy and paste data from *ChemDraw* to *Office 365* or copy *ChemDraw* objects included in *Office* documents back to *ChemDraw* from *Office 365*.

One can save a *ChemDraw* structure to an image file and import that into *Office* documents, but the image cannot be used to recover the original *ChemDraw* structure data.

## Copying & Pasting from *ChemDraw* to *Office* on *Mac*

*ChemDraw* generates a PDF image containing structural data when *ChemDraw* structure is copied from *ChemDraw* to *Office* desktop application on Mac.  The *ChemDraw* structure data embedded in the pasted PDF image are used to restore the chemical structure in *ChemDraw* when the PDF image is copied from *Office* application to *ChemDraw*.

For some *Office* products and versions, the embedded structure data get stripped, and cannot be recovered when the image is copied from *Office* and pasted into *ChemDraw*.  Please refer to [this](mac-office-issues.md) on details of problematic cases.

## Cross-Platform Support of *ChemDraw* Images in *Office* Documents

The *ChemDraw* images included in *Office* documents are using platform-specific format. For instance, the *ChemDraw* image pasted in *Word* document authored on *Mac* is in PDF format.  On the other hand, the *ChemDraw* image pasted in *Word* document authored on *Windows* is in EMF/WMF format.

For this reason, when opening a *ChemDraw* structure containing *Office* documents on platforms other than the platform of origin, the *ChemDraw* structures may appear blurry.

Please refer to [this](cross-platform-image-issues.md) for more discussion on this topic.

## Poor SVG Support by *Office* Documents

*ChemDraw* generates SVG-format images. SVG is a vector image format that can be scaled without losing fidelity. It's an ideal format that can be used in cross-platform environment.  The reason that this format is not used in *Office* applications is that *Office* applications do not support SVG format very well.

In the recent version, *Microsoft* claims to [provide a better support for SVG](https://support.office.com/en-us/article/release-notes-for-office-2016-for-mac-ed2da564-6d53-4542-9954-7e3209681a41).

Issues related to rendering *ChemDraw* generated SVG images in *Office* applications are discussed in more detail in [this document](office-svg-support-issues.md).