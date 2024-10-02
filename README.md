 Project Title:
Image to PDF Converter

Description:
This Python-based GUI application allows users to select multiple image files (PNG, JPEG, JPG) and convert them into a single PDF document. It provides a simple interface for selecting images, specifying the output PDF name, and saving the PDF. The application resizes and centers the images within the PDF, ensuring proper formatting.

Features:
- Select multiple images from your local file system.
- Displays selected images in a list for review.
- Converts the selected images into a single PDF file.
- Customizable output PDF file name.
- Error and success messages are displayed for user feedback.
- Automatic scaling of images to fit within the PDF dimensions (612x792).

---

Installation:

1. Prerequisites:
Before running the program, ensure that Python is installed on your system. Additionally, the following Python packages are required:
   - `tkinter`: Built-in Python library for creating graphical user interfaces.
   - `reportlab`: For PDF generation.
   - `PIL` (Pillow): For handling image file formats.
   - `os`: For file path manipulations.
   - `messagebox`: A part of `tkinter` for showing dialog boxes.

2. Install Required Packages:
Use `pip` to install the necessary packages:
```bash
pip install reportlab Pillow
```

3. Clone or Download the Repository:
Clone the repository using the command:
```bash
git clone https://github.com/your-repo-url.git
```

Alternatively, download the ZIP and extract it.

---

How to Run:
1. Run the Script:
   Navigate to the directory where the script is located and run:
   ```bash
   python app.py
   ```

2. Usage:
   - After the GUI window appears, click on "Select Images" to choose multiple images.
   - The selected images will be displayed in the list box.
   - Enter the desired name for the output PDF in the text box.
   - Click "Convert to PDF" to generate the PDF file.
   - A success or error message will be displayed upon completion.

---

Code Overview:

  1.  Modules Used :
   -  tkinter : Provides the GUI components such as buttons, labels, and entry fields.
   -  filedialog : From `tkinter`, used to open file dialog windows for image selection.
   -  os : Used for handling file paths and splitting file names.
   -  reportlab : Handles PDF generation, including drawing images and managing pages.
   -  PIL (Pillow) : Used for opening image files and getting their dimensions.
   -  messagebox : From `tkinter`, used to display pop-up windows to the user (e.g., success or error messages).
   -  colors : From `reportlab.lib`, allows setting the background color of PDF pages.

  2.  Class: `ImageToPDFConvertor` :
   -  `__init__(self, root)` : Initializes the GUI components, setting up buttons and entry fields.
   -  `initialize_ui(self)` : Creates the user interface (buttons, labels, entry fields, and listbox).
   -  `select_images(self)` : Opens a file dialog to allow users to select images.
   -  `update_selected_images_listbox(self)` : Updates the listbox with the names of the selected images.
   -  `convert_images_to_pdf(self)` : Converts the selected images into a PDF, handling scaling, centering, and PDF generation.
   -  Error Handling : Displays a warning if no images are selected, or an error message if the conversion fails.

  3.  Main Function :
   - The `main()` function creates the root window, sets its title and size, and starts the `tkinter` event loop.

---

  Example:
```bash
$ python app.py
# Opens the GUI where you can select images and convert them to PDF.
```

  Future Improvements:
- Add a drag-and-drop feature for selecting images.
- Include image preview functionality within the UI.
- Provide more options for PDF page layouts (e.g., multiple images per page).
- Add the ability to reorder the selected images.

---

  License:
This project is licensed under the MIT License.

---

