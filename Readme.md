# School Management System (PyQt5 GUI)

This project implements a School Management System with a graphical user interface (GUI) built using PyQt5. It allows for the management of professors, modules, and departments, providing functionalities to add, delete, display, and update records. The application utilizes a SQLite database for efficient and persistent data storage.




## Installation

To run this project, you will need Python 3 and PyQt5 installed on your system. The project uses SQLite for database management, which is typically included with Python.

1.  **Clone the repository:**

    ```bash
    git clone https://github.com/yassin-elkhamlichi/School-management-with-GUI-use-tkinter.git
    ```

2.  **Navigate to the project directory:**

    ```bash
    cd School-management-with-GUI-use-tkinter/
    ```

3.  **Install dependencies:**

    ```bash
    pip install PyQt5
    ```

    *Note: If you encounter issues with the PyQt5 GUI not displaying, especially in environments without a graphical display, you might need to install additional XCB plugins or run the application with `xvfb-run`.*

    ```bash
    sudo apt-get update
    sudo apt-get install -y libxcb-xinerama0 libxcb-icccm4 libxcb-image0 libxcb-keysyms1 libxcb-render-util0 libxcb-util1 libxcb-xfixes0 libxcb-xkb1 libxkbcommon-x11-0 libqt5gui5 libqt5core5a libqt5dbus5 qtbase5-dev qtchooser qt5-qmake qtbase5-dev-tools xvfb
    ```




## Usage

To start the application, navigate to the project directory and run the `main.py` file:

```bash
python3 main.py
```

If you are running in a headless environment (e.g., a server without a graphical display), you might need to use `xvfb-run`:

```bash
xvfb-run python3 main.py
```

Upon launching, the application will display a main window with various options to manage school data. The GUI provides an intuitive way to interact with the system.

### Key Features:

-   **Professor Management:** Add, edit, delete, and view professor details.
-   **Module Management:** Manage academic modules, including assigning professors.
-   **Department Management:** Organize departments and their associated data.

Interact with the application using the provided buttons, input fields, and tables within the GUI.




## Project Structure

The project is structured to separate concerns, making it modular and easier to maintain:

-   `main.py`: The entry point of the application, responsible for initializing the database and launching the main PyQt5 window.
-   `createTables.py`: Contains functions to establish a SQLite database connection and create the necessary tables (`Prof`, `Module`, `Department`).
-   `models/`: Defines the data models and their interactions with the database.
    -   `database.py`: Handles the SQLite database connection and basic CRUD operations.
    -   `prof.py`: Model for Professor data.
    -   `module.py`: Model for Module data.
    -   `department.py`: Model for Department data.
-   `controllers/`: Contains the logic that connects the views (GUI) with the models (data).
    -   `prof_controller.py`: Manages operations related to professors.
    -   `module_controller.py`: Manages operations related to modules.
    -   `department_controller.py`: Manages operations related to departments.
-   `view/`: Contains the PyQt5 UI definitions.
    -   `main_window.py`: The main application window.
    -   `prof_view.py`: UI for professor management.
    -   `module_view.py`: UI for module management.
    -   `department_view.py`: UI for department management.
-   `images/`: Stores image assets used in the GUI.
-   `scolarite.db`: The SQLite database file (automatically created if it doesn't exist).
-   `README.md`: The original README file for the project.
-   `README_pyqt5_gui.md`: This README file.


