# Java Recursive File Lister

A desktop GUI application built in Java that recursively traverses local file system directories and lists all contained files and subfolders in real time.

## 📌 Overview
This application demonstrates recursive algorithm design applied to file system navigation. Utilizing Java Swing and `JFileChooser`, users can select any target directory to initiate a depth-first recursive traversal that logs every folder and file path into a scrollable viewport.
---

## ✨ Key Features

* **Recursive Traversal:** Employs a recursive algorithm to systematically explore nested sub-directories down to terminal file leaves.
* **Directory-Only Selection:** Configures JFileChooser in DIRECTORIES_ONLY mode to restrict selection exclusively to valid folders.
* **Real-Time Path Logging:** Displays discovered paths clearly differentiated with DIR: and FILE: prefixes.
* **Scrollable Results Viewport:** Uses a JTextArea wrapped in a JScrollPane to cleanly display large file hierarchy listings.
* **Clean Desktop GUI:** Features a custom header title label, interactive action buttons, and responsive panel layout.

---

## 🛠️ Tech Stack & Architecture

* **Language:** Java 17+
* **GUI Framework:** Java Swing (JFrame, JLabel, JTextArea, JScrollPane, JButton, JFileChooser)
* **Algorithm Concept:** Depth-First Recursive Directory Search
* **IDE:** JetBrains IntelliJ IDEA

---

## 📁 Repository Structure

    src/
    └── RecursiveListerGUI.java    # Swing GUI frame housing user controls and recursive directory traversal logic
    README.md

---

## 🚀 How to Run

### Prerequisites
* Java Development Kit (JDK 17 or higher installed)
* An IDE such as IntelliJ IDEA, Eclipse, or VS Code

### Execution Steps
1. Clone the repository to your local system:

   git clone https://github.com/deshyah/java-recursive-file-lister.git

2. Open the project in your Java IDE.
3. Locate src/RecursiveListerGUI.java (or main execution entry point) and run the application.
4. Click Select Directory and List to pick a folder from your local file system.
5. View the recursive file tree rendered inside the text area.

---

## 💡 Key Engineering Takeaways

* **Terminal Conditions in File I/O:** The recursive algorithm processes directories by invoking itself on child folders while hitting its base terminal condition when encountering standard files.
* **UI Input Safeguards:** Enforcing directory-only selection at the JFileChooser level prevents file parsing errors before traversal begins.
* **Modular GUI Architecture:** Decoupling file system navigation methods from event handlers keeps the Swing user interface clean and maintainable.
