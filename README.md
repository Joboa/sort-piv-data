# PIV Data Sorter

## Description
This Python script organizes Particle Image Velocimetry (PIV) data by sorting files within a specified folder into subfolders based on file types.

## Installation
- Clone the repository: \`git clone https://github.com/yourusername/PIV-Data-Sorter.git\`
- Ensure Python 3.x is installed.

## Usage
1. Run the script \`PIVDataSorter.py\`.
2. The script will prompt for a folder name that contains the PIV data.
3. Ensure the folder structure matches the expected format: 
    ```
    Main_Folder/
    │
    ├── RawData/
    │   ├── Files to be sorted
    │   └── ...
    ├── Main_Folder.run
    └── Analysis/
        └── (Will be removed and recreated by the script)
    ```
4. The script will sort files within the `RawData` folder into `Calibration`, `Right`, or `Left` subfolders based on file types.

## Functionality
- `get_input_folder`: Prompts the user to input the folder name containing the PIV data.
- `process_folder(main_folder)`: Processes the specified folder by sorting PIV data into respective subfolders.

## Example
```python
from PIVDataSorter import PIVDataSorter

def main():
    sorter = PIVDataSorter()
    main_folder = sorter.get_input_folder()
    sorter.process_folder(main_folder)

if __name__ == "__main__":
    main()
```

## Notes
- Ensure the PIV data folder follows the expected structure.
- This script removes the `Analysis` folder and `Main_Folder.run` file within the specified folder if they exist.
- Be cautious as the script performs file operations and may overwrite existing files with the same name.