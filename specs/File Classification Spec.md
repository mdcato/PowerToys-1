# **PowerToys File Classification Spec**

![MS PowerToys](https://hothardware.com/ContentImages/NewsItem/48038/content/Microsoft_PowerToys.jpg "PowerToys")
## Users can quickly rename and group files.
### Authors: Benjamin Leverette and Prudence Phillips
### Spec Status: Draft
## Overview

### Elevator Pitch / Narrative 

David has recently uploaded thousands of pictures from his camera to his Surface Laptop.  Unfortunately, the images all have generic names such as 'IMG_141' instead of labels that he can identify.  David downloads the File Classification PowerToy that allows him to create new folders with files that share a label, rename a group of files with a label, or change the name or portion of a name in a group of files to another name.

### Customers

Like all utilities from PowerToys, the File Classification feature is for power users and developers who are looking to tune and streamline their Windows experience for greater productivity.
  
### Problem Statement and Supporting Customer Insights

Power users need a better way to organize files, from renaming files to creating new folders for similar files.  Our PowerToys Consumer Survey received feedback validating the usefulness of a feature that provides such functionality.

### Existing Solutions or Expectations

Users currently have to highlight a group of files and right click to rename them.  Users must manually create a folder, move files to that folder, and rename them.  There are third-party resources that allow users to rename files similarly.

We expect users to install and enable PowerToys for Windows in order to access the File Classification utility.

### Goals/Non-Goals

Design and develop a feature that can rename and group files within an 8 week period.

## Definition of Success

### Expected Impact: Customer, and Technology Outcomes, Experiments + Measures

Our PowerToys Consumer Survey received an abundant amount of participation and feedback from a community of passionate power users.  This feature will give them the ability to rename, group and organize files in a way that makes their virtual library of files more organized and efficient.  As interns, we would have 8 weeks to complete the project.

## Requirements

### Functional Requirements

**1. Initial UX/UI**
   
   Users must open File Explorer and select a group of files by checking each file or using Shift + directional keys.  They must then use a shortcut to open the File Classification utility, which opens in the center of the screen and provides options that require input from the user.

   **For a visual example of the UX see Figure 1*

   **For limitations in user input see 2.4*

**2. Rename File Options**   

   2.1. Simple File Rename
   - Renames all user-selected files after receiving a label, which is typed by the user to be the files' new name.
     - Example: If the user types that the label is "C" then selected files named "A" and "B" would be renamed to "C(1)" and "C(2)"

   2.2. Folder and File Rename
   - Automates folder creation and movement of user-selected files into the new folder.
   - The user must type in a label, which will serve as the name of the folder and renames the files.
     - Example: If the user types that the label is "Hello" then a folder will be created and named "Hello". The selected files will be moved to the folder and renamed "Hello(1)"...

   2.3. Replace by Characters
   - Identifies a group of characters, which are typed by the user, in the names of user-selected files and replaces that group of characters with characters input by the user.
   - Every instance of the characters found in each selected file's name will be replaced.
     - Example: If the user types that "e" should be replaced with "o" then a selected file named "bleed" would be changed to "blood"

   2.4. Shared Functionality
   
   - **Labels**
     - Used as the name for the new folders created.  
     - Used to rename files by completely overwriting the files' current names with the custom 'Label' typed by the user and each file receives a counting number.
   - **Confirmation**  
     - After the user selects an option and fills in the required text boxes, they must click 'Apply' for the utility to make the changes, or they can click 'Cancel' which closes the utility without making changes.
   - **Input Limitations**
     - Only a single option can be applied at a time, so if the user begins to type text for one option, the others options should block input (*text area turns grey?*) unless input is removed from the original option.
     - If a space alone is inputted into any of the options, no changes are made when apply is clicked.
- **Shortcut Accessibility**
  - Perhaps Ctrl + Tab, which does not have a function within File Explorer.
  - Alternatives include : Alt + C , Ctrl + Alt + F

Figure 1: Initial UX/UI Visual
![Figure 1-1](https://raw.github.com/indierawk2k2/PowerToys-1/images/PT%20Images/File%20Classification%20Design%20Blurred.png "FC")

### Measure Requirements

- A score of an average of 4 stars on a new Consumer Design Satisfaction Survey
- 100 Github comments
- 20 pull requests
- Installed by 40% of Power Users
- Uninstalled by less than 10% of installs
- Launched by over 90% of installs

## Dependencies

- Explore Internship Program limits us to an 8-week window to complete the task.

- Availability of public API's