---
title: Accessing Data
summary: Guide covering two main tools for dataset interaction
thumbnail_url: https://raw.githubusercontent.com/janelia-cosem/openorganelle-blog/main/assets/accessdatabanner.png
carousel_url: https://raw.githubusercontent.com/janelia-cosem/openorganelle-blog/main/assets/accessdatabanner.png
tags: ["FIB-SEM","data visualization","data access","open organelle","open data"]
authors: ["Alyson Petruncio"]
date: "2024-12-02T01:14"
published: true
---

# A Quick Guide to Accessing Data

**So much data, so little time!** OpenOrganelle offers an incredible resource of large-scale, cloud-based datasets, including raw data and labels, for researchers worldwide. Whether you're visualizing these datasets in Neuroglancer or importing them into Fiji for advanced analysis, this guide will help you get started. Let’s dive into the tools and techniques for accessing, visualizing, and manipulating data on OpenOrganelle.

---

## **Visualizing Data in Neuroglancer**

![OpenOrganelle to Neuroglancer instance](https://raw.githubusercontent.com/janelia-cosem/openorganelle-blog/main/assets/accessdata4.gif)

Neuroglancer is a powerful browser-based tool that enables visualization of large datasets at a range of resolutions. Here’s how to explore OpenOrganelle datasets step-by-step:

### **Getting Started**

1. **Select a View:**
   - Choose a pre-made view or the default location provided for your dataset.

2. **Pick Your Layers:**
   - Options may include:
     - FIB-SEM data
     - Organelle predictions
     - Refined organelle segmentations
     - Analysis of organelle segmentations (e.g., contact sites, skeletons, curvature)
     - Correlative light microscopy data

3. **Launch the Viewer:**
   - Click the **“VIEW”** button or the dataset thumbnail to open a Neuroglancer instance in a new tab.

### **Navigating Neuroglancer**

Once in Neuroglancer, you can interact with the data using the following key bindings and tools:

- **Layer Visibility:** Left-click a layer name to toggle visibility or right-click to access its settings in the side panel.
- **Navigation:**
  - **Pan:** Left-click and drag.
  - **Recenter:** Right-click.
  - **Zoom:** Use `Ctrl + Mouse Wheel`.
  - **Slice Navigation:** Scroll with the mouse wheel, or hold `Shift` to move faster.
  - **Rotation:** Use `Shift + Left Click` to rotate in-plane.
  - **Return to Orthogonal View:** Press `Z`.

- **View Customization:**
  - Toggle 3D rendering of a segmentation with a double left-click.
  - Adjust axis lines with `A` and the scale bar with `B`.
  - Modify settings like resolution, blending, opacity, and contrast in the **Side Panel**.

- **Advanced Navigation:**
  - Copy and share coordinates using the top toolbar. You can also save regions of interest (ROIs) within Neuroglancer links for easy collaboration.

For a full list of key bindings, visit the [OpenOrganelle FAQ](https://www.openorganelle.com/faq).

---

## **Visualizing and Downloading Data with Fiji**

![OpenOrganelle URI to Fiji](https://raw.githubusercontent.com/janelia-cosem/openorganelle-blog/main/assets/accessdata5.gif)

For users who prefer local visualization or need to edit and download datasets, importing data into [Fiji](https://imagej.net/software/fiji/) is a practical solution.

### **Steps to Import Data into Fiji**

1. **Copy the Dataset URL:**
   - Click the blue Fiji icon on OpenOrganelle to copy the dataset’s URL.

2. **Open the Dataset in Fiji:**
   - In Fiji, go to **File > Import > HDF5/N5/Zarr/OME-NGFF...** and paste the dataset URL.
   - Select **Detect Datasets** to view available datasets for import.

3. **Prepare and Customize Your Data:**
   - Ensure that all selected datasets match in resolution for overlaying labels onto raw data.
   - Convert datasets to 16-bit via **Image > Type > 16-bit**.
   - Adjust colors using **Image > Lookup Tables**.
   - Merge channels for overlay visualization using **Image > Color > Merge Channels**.

4. **Save or Export Data:**
   - Save the overlayed processed data as a combined TIFF file using **File > Save As > Tiff...** or as hierarchical and chunked data formats using **File > Save As > HDF5/N5/Zarr/OME-NGFF...**. Split channels using **Image > Color > Split Channels** to download individual image stacks.

### **Limitations:**
   - Be cautious of Fiji’s memory usage; loading large datasets in full may cause failures.
   - Interactive 3D visualization is currently unsupported.

---

## **Programmatic Access to OpenOrganelle Data**

If you prefer to access OpenOrganelle data programmatically, instructions for using Python packages or the AWS Command Line Interface (CLI) are available on the [OpenOrganelle FAQ](https://www.openorganelle.com/faq).

---

OpenOrganelle is a treasure trove of high-resolution datasets, and with tools like Neuroglancer and Fiji, you can explore, analyze, and share these resources seamlessly. Whether you're a seasoned data scientist or a new user, these tools make the journey into cellular data accessible.
