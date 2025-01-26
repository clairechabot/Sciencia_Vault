---
aliases: 
tags:
  - protocol
title: Protocol Title
date_created: 2024-06-28-Friday
date_modified: 2024-06-28-Friday
created: 2024-06-28
summary: Protocol summary
Recommended_by:
  - "[[Albert Einstein]]"
source: Source
projects:
  - "[[Example Project MOC]]"
protocol_type: Histology
---

[[Protocol MOC]]/ [[Ph.D. Dashboard]] 

---


```ad-abstract
title: Purpose

My initial purpose is to use this microscope to take slides from my [[RNA in situ Protocol Dev MOC]] experiments. 


```

---

# Experiments  
%%The query will pull any projects that have used this protocol. Sorted by the last modified time of that experiment file.%% 

<br> 

```dataview
	LIST 
	FROM "100 Lab Notes/Projects" 
	WHERE contains(file.outlinks, [[]])
	GROUP BY file.link
	SORT file.mtime ASC
```

<br> 

---

# Lab Inventory Items
%%This query will pull any lab inventory items that are associated with this protocol. Sorted by the last modified time of that experiment file. %%
<br> 

```dataview
	LIST 
	FROM "100 Lab Notes/Lab Inventory" 
	WHERE contains(file.outlinks, [[]])
	GROUP BY file.link
	SORT file.mtime ASC
```

<br> 

---

# Relevant Papers 

<br> 

- [[2024_09_17 Olympus SOP Training]] --> the raw meeting notes when I got trained by Pamela 


<br> 

---

# Protocol
%%Documentation of the actual protocol.%%

_I have attached here an overview of the notes I took from my original training session._


**Microscope Training Notes**

**1. General Setup & Usage**  
- **Password for Olympus**: cellSens4  
- **Transmitted Light**: Click to turn on/off the light (useful when stepping away).  
- **BFg RGB**: Brightfield with color and glass; also provides shading correction.  
- **Yellow Indicators**: Active settings are highlighted in yellow.  
- **Live Mode**: Click “Live” to start live imaging.  
- **SFL**: Provides clearer images; follow protocol for when to turn it off.  
- **Exposure Compensation**: Used for fluorescence imaging.  
- **Region**: Full image.  
- **Resolution**: Use the highest available resolution for both live and camera modes.  
- **Aspect Ratio**: Set to the highest option (usually 16:10).  
- **DP74**: Adjust contrast here.  
- **Process Manager**: View the entire process section.  

**2. Slide Preparation & Focus**  
- **Objective Setup**: 
  - 60x requires oil, 4x for overview.
  - Use #4 objective to avoid scratching the lens.  
- **Clean Slides**: Use ethanol on a Kimwipe to clean slides.  
- **Mounting Media**: If you have excessive mounting media, only xylene will remove it.  
- **Fine Adjustors**: Use the fine adjustors on the objectives; if not adjusted properly, slides can appear cloudy, which cannot be fixed any other way.  

**3. Navigation & Layout**  
- **Stage Navigator**:  
  - Use the white block to move to the top left corner of the image.  
  - Acquire overview from top left to bottom right, then click "OK".  
  - Acquire overview: Red next to white box.  
  - Define area overview (from top left to bottom right) using the 2x objective.  

- **Image Navigation**:  
  - Located in the bottom left (instead of camera control).  
  - Pull up to the top monitor to navigate the stage.  

- **Layout**:  
  - Before logging off, reset the layout to default (especially if others have changed it).  
  - Use the “Layout Button” to reset the current layout.  
  - Exposure compensation and gain settings do not reset automatically and must be done manually.

**4. Image Acquisition & Stitching (MIA)**  
- **MIA (Multiple Image Acquisition)**: Used to stitch together multiple images.  
- **Process Manager**: Access via the green button at the bottom right.  
- **Stage Navigator**: Use the rectangular scan area button (grid icon) to drag a shape over the area of interest.  
  - **Small Area**: Use a 3-point focus map for small areas.  
  - **Medium Density Focus Map**: Adds more focus points to ensure all areas are in focus.  
  - **Large Area**: Use Z-stack acquisition.  

- **Z-Stack**:  
  - Use for larger areas. Takes longer and generates larger files.  
  - Manually focus on each section to set a baseline for the computer.  
  - **Focus Areas**:  
    - Green = done  
    - Blue = current  
    - Clear = not done yet  
  - Adjust the exposure time as needed (note: exposure times may vary across tiles).  

**5. Z-Stack Setup**  
- **Focus**:  
  - Set the position and start to 0 in the Z-stack section (lowest plane of focus).  
  - Use fine focus to find the highest plane of focus and set the "End" point.  
  - Repeat for all areas in the grid to ensure uniform focus across the image.  

- **Step Size**:  
  - Adjust based on the quality of the image. Smaller steps improve focus, but too many steps can make the image fuzzy.  
  - **Recommended Settings**:  
    - Z-slices: No more than 10  
    - Step size: ~1.0 µm  
  - Lock settings once checked and verified.  

- **Extended Focal Imaging**:  
  - Always enable to avoid massive file sizes.  
  - Located at the bottom of the grey square in the settings.  

**6. Saving & File Management**  
- **File Saving**:  
  - Always save files under **C:**  
  - Use only underscores ("_") in file names, no special characters.  
  - Save the original file as a `.vis` (can only be opened on Olivia).  
  - For processed images, save as `.tiff`.  
  - To save with the scale bar, don’t forget to select “Burn in Info” at the top of the screen.  
  - **Raw .vsi File**: Save in case you need to return to the unprocessed image.  

- **Scale Bar**:  
  - Options for the scale bar are at the top of the screen.  
  - The scale bar does not reset automatically, so note your settings for consistency.  
  - Sometimes the scale bar can get distorted, so it’s important to keep a raw file.  

- **File Transfer**:  
  - NEVER insert a USB into the microscope computer (it is not virus-protected).  
  - Save files to **D:**, then move to **S:** for long-term storage.  
  - Use **O:** for further editing (Olivia program).  




