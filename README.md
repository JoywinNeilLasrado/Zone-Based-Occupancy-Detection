


<h1> Zone-Based-Occupancy-Detection using OpenCV</h1>
<h2>Problem Statement</h2>
<p>In warehouse and inventory management, tracking the presence or absence of objects on storage shelves is crucial for operational efficiency. Traditional automated object detection systems often require heavy computational resources and training data. There is a need for a lightweight, user-friendly tool that enables manual region labeling and simple presence detection based on visual cues.</p>

<h2>Project Description</h2>
<p>This project is a computer vision-based <strong>Zone-Based-Occupancy-Detection System</strong> developed using <strong>OpenCV and Python</strong>. It allows users to manually mark, save, and manage slots of the objects areas on a static image (e.g., a warehouse shelf image captured by a surveillance camera).The system provides  users to draw and delete slot rectangles using mouse inputs.</p>
<p>It is particularly useful in scenarios like:

- Setting up an initial map of a objects in the shelf.
- Marking ocupied or available  spaces.
- Preprocessing for automated  space occupancy detection models.
</p>

<h2> Key Features</h2>
<ul>
    <li><strong>Draw and Save object area:</strong> Users can draw rectangles on the image to define the boundaries of object space. These positions are saved using Python’s pickle module, allowing persistence between sessions.</li>
    <li><strong>Delete Existing Slots:</strong> Users can switch to a delete mode, allowing them to remove previously marked spaces by simply clicking on them.</li>
    <li><strong>Mouse Interaction:</strong> The entire slot marking system is built using OpenCV's mouse callback features, offering real-time, intuitive interaction.</li>
    <li><strong>Position Storage:</strong> All slot coordinates are saved in a file (Pos) using serialization. This allows loading and editing previously marked  layouts of the object.</li>
    <li><strong>Lightweight:</strong> No deep learning or heavy models required – it’s a clean, fast, and easy-to-use utility for  mapping objects  or similar use cases.</li>
</ul>

<h2> How It Works</h2>
<ol>
    <li><strong>Load Image: </strong>  The image file (e.g., frame.jpg) of a ware house area where objects aregoing to be kept is loaded using OpenCV.</li>
    <li><strong>Draw Mode (Default): </strong>  Click and drag on the image to draw a rectangle (object space).</li>
    <li><strong>Delete Mode (Toggle Option): </strong>Switch to delete mode and click on an existing rectangle to remove it.</li>
    <li> <strong>Save Positions: </strong>Slot coordinates are saved automatically and persist in a file for future use.</li>
    <li> <strong>Display: </strong>Updated images with slot overlays are shown live using OpenCV GUI windows.</li>
</ol> 

<h2>Steps of Our Zone-Based Occupancy Detection Project</h2>
<ol>
    <li>
        <strong>Image Acquisition</strong><br>
        We capture or upload an image (e.g., image of the warehouse where the object is kept).
    </li>
    <li>
        <strong>Object Position Definition</strong><br>
        We manually define coordinates for each object we want to monitor.
    </li>
    <li>
        <strong>Region Cropping</strong><br>
        The image is divided into individual regions based on the defined coordinates.
    </li>
    <li>
        <strong>Occupancy Detection</strong><br>
        Each position is analyzed based on:
        <ul>
            <li>Pixel intensity</li>
            <li>Edge presence</li>
        </ul>
        to determine whether the object is present or missing.
    </li>
    <li>
        <strong>Visualization</strong><br>
        Colored positions are drawn to indicate status:
        <ul>
            <li><span style="color:red;">🟥 Red</span> – Object is <strong>present</strong></li>
            <li><span style="color:green;">🟩 Green</span> – Object is <strong>missing</strong></li>
        </ul>
    </li>
</ol>

<h2> Installation & Setup</h2>

<h3> Technology Used</h3>
<ul>
    <li><strong>Python:</strong> Core programming language used for implementing logic and UI interactions.</li>
    <li><strong>OpenCV:</strong> Computer vision library for image handling, mouse interaction, and GUI display.</li>
    <li><strong>Matplotlib:</strong> Used for optional image visualization and debugging.</li>
    <li><strong>Pillow:</strong> Python Imaging Library used for image manipulation tasks if needed.</li>
    <li><strong>cvzone:</strong> Utility wrapper built on OpenCV to simplify common vision tasks (optional but helpful).</li>
    <li><strong>NumPy:</strong> For efficient numerical operations and coordinate management.</li>
    <li><strong>Pickle:</strong> Python’s built-in module used to serialize and store slot coordinates.</li>
    <li><strong>Jupyter Notebook:</strong> Interactive development and testing environment for running the application.</li>
</ul>

<h3>Prerequisites</h3>
<pre><code>pip install opencv-python matplotlib pillow cvzone numpy</code></pre>

<h3>Project Structure</h3>
<pre><code>project-folder/
├── final_dip.ipynb               # Main notebook
├── frame.jpg                #  image of video frame
├── Pos                      # Saved positions
</code></pre>

<h3>Running the Notebook</h3>
<pre><code>jupyter notebook final_dip.ipynb</code></pre>
Run each cell in order and follow on-screen instructions for marking slots.

<h2>💡 Use Cases</h2>
<ul>
    <li>Preprocessing for automated object detection systems.</li>
    <li>Manual tagging of regions in CCTV survileence images to focus on one object.</li>
    <li>Interactive labeling tool for computer vision tasks.</li>
</ul>

<h2>📂 File Descriptions</h2>
<ul>
    <li><code>final_dip.ipynb</code> - Main interactive notebook.
       In the notebook, each Python cell is accompanied by a corresponding Markdown cell that provides clear instructions and operational details. These Markdown cells ensure that users understand how to utilize 
       each code cell effectively, facilitating structured execution and comprehension.</li> 
    <li><code>frame.jpg</code> - Input image file.</li>
    <li><code>Pos</code> - Stores drawn slot positions.</li>
</ul>

<h2>👨‍💻 Contributing</h2>
<p>Contributions are welcome! Please fork the repo, create a new branch, and submit a pull request with your changes.</p>

<h2>📄 License</h2>
<p>This project is licensed under the MIT License.</p>

</body>
</html>
