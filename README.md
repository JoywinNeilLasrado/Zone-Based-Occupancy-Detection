#  Zone based occupancy Detection 

##  Project Description

This project is a computer vision-based  Slot Detection System developed using OpenCV and Python. It allows users to manually mark, save, and manage  slot areas on a static image (e.g., a warehouse shelf image captured by a surveillance camera). The system provides  users to draw and delete slot rectangles using mouse inputs.

It is particularly useful in scenarios like:

- Setting up an initial map of a objects in the shelf.
- Marking ocupied or available  spaces.
- Preprocessing for automated  space occupancy detection models.

##  Key Features

### ✅ Draw and Save Parking Slots
Users can draw rectangles on the image to define the boundaries of object space. These positions are saved using Python’s `pickle` module, allowing persistence between sessions.

### ✅ Delete Existing Slots
Users can switch to a delete mode, allowing them to remove previously marked spaces by simply clicking on them.

### ✅ Mouse Interaction
The entire slot marking system is built using OpenCV's mouse callback features, offering real-time, intuitive interaction.

### ✅ Position Storage
All slot coordinates are saved in a file (`Pos`) using serialization. This allows loading and editing previously marked parking layouts.

### ✅ Lightweight and Easy to Use
No deep learning or heavy models required – it’s a clean, fast, and easy-to-use utility for  mapping objects  or similar use cases.

## 🖼️ How It Works

1. **Load Image**  
   The image file (e.g., `frame.jpg`) of a ware house area where objects aregoing to be kept is loaded using OpenCV.

2. **Draw Mode (Default)**  
   Click and drag on the image to draw a rectangle (object space).

3. **Delete Mode (Toggle Option)**  
   Switch to delete mode and click on an existing rectangle to remove it.

4. **Save Positions**  
   Slot coordinates are saved automatically and persist in a file for future use.

5. **Display**  
   Updated images with slot overlays are shown live using OpenCV GUI windows.

## 🛠️ Installation & Setup

### Prerequisites

Ensure you have Python 3.x installed, then install the required libraries:

```bash
pip install opencv-python matplotlib pillow cvzone numpy.



