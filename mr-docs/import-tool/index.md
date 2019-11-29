---
author: JBrentJ
description: Overview of converting and optimizing 3D models to use with Dynamics 365 Import Tool (Preview).  
ms.author: v-jerja
ms.date: 10/29/2019
ms.service: crm-online
ms.topic: overview
title: Overview of Dynamics 365 Import Tool (Preview)
ms.reviewer: v-brycho
---

# Overview of Dynamics 365 Import Tool (Preview)

If you’re using [!include[cc-microsoft](../includes/cc-microsoft.md)] [!include[pn-dyn-365](../includes/pn-dyn-365.md)] mixed-reality applications, you might want to import your own 3D models ([CAD](https://en.wikipedia.org/wiki/Computer-aided_design) models) into the applications. This guide shows you how to prepare your 3D models for use with [!include[pn-dyn-365](../includes/pn-dyn-365.md)] mixed-reality applications using a combination of third-party tools and [!include[pn-dyn-365-import-tool](../includes/pn-dyn-365-import-tool.md)].

## glTF and GLB file formats
All geometry in [!include[pn-dyn-365](../includes/pn-dyn-365.md)] mixed-reality applications uses the Khronos Group glTF™ file format. This royalty-free specification minimizes both the size of 3D models and the run-time processing needed to unpack and use those models. The GLB format is the binary version of .glTF version 2.0, which can include textures.

> [!TIP] 
> The Khronos Group provides a robust overview of best practices: [Art Pipeline for glTF](https://aka.ms/glTFbestpractices).

## Parametric geometry vs. polygonal geometry

Modeling tools in most CAD applications use sets of adjustable mathematical parameters to define parametric solids. Parametric solids and surfaces provide highly accurate detail that can be used to carry out engineering simulations and manufacturing processes. glTF and real-time rendering applications require models to be represented as a triangulated polygon surface.

> [!div class="mx-imgBorder"]
> ![Parametric vs. polygonal geometry](media/compare-geometry.PNG "Parametric vs. polygonal geometry")  

*Model visualized in Autodesk Inventor and [!include[cc-microsoft](../includes/cc-microsoft.md)] 3D Viewer*

A.	Parametric 3D model ready for simulation and manufacturing<br>
B.	Polygonal surface 3D model ready for real-time rendering

## Overall process for preparing 3D models

Preparing CAD content for [!include[pn-dyn-365](../includes/pn-dyn-365.md)] mixed-reality applications involves three main steps: 

1.	**Convert 3D models** from their original geometric definition into one that supports real-time rasterization. This converts the models from parametric geometry into polygonal geometry. 

2.	**Optimize the converted 3D models** to ensure the best possible performance in real-time applications.

3.	**Use [!include[pn-dyn-365-import-tool](../includes/pn-dyn-365-import-tool.md)]** to prepare the models for [!include[pn-dyn-365](../includes/pn-dyn-365.md)] mixed-reality applications. 

The following illustration shows a more detailed view of this process.

> [!div class="mx-imgBorder"]
> ![Overall flow](media/overall-flow.png "Overall flow") 

**A.**	Create 3D models using the CAD software of your choice.<br>
**B.**	Convert CAD files to one of these file formats: GLB, glTF, FBX, OBJ, STL, PLY, JT, SKP, or STP.<br>
**C.**	If you save your model as one of the file formats with a red asterisk next to it, you can optimize the 3D model yourself and use the [!include[pn-dyn-365-import-tool](../includes/pn-dyn-365-import-tool.md)] to convert the 3D model to a GLB file locally. If you use any of the listed formats, including those with the red asterisks, you can use the [!include[pn-dyn-365-import-tool](../includes/pn-dyn-365-import-tool.md)] to send your model to [!include[cc-microsoft](../includes/cc-microsoft.md)] for manual optimization and conversion to a supported format.<br>
**D.**	3D models are optimized and converted into the GLB format.<br>
**E.**	3D models ready to be imported into [!include[pn-dyn-365](../includes/pn-dyn-365.md)] mixed-reality applications.

### See also
[Convert 3D models](convert-models.md)<br>
[Optimize 3D models](optimize-models.md)<br>
[Best practices for converting and optimizing 3D models](best-practices.md)<br>
[Tutorials for converting and optimizing 3D models](tutorials-overview.md)<br>
[Use Dynamics 365 Import Tool (Preview)](import-tool.md)

 

