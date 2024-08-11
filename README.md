
### Discord Nitro Code Generator and Checker

This project is a Discord Nitro Checker tool that automates the process of generating and validating Discord Nitro gift codes. It uses multithreading to efficiently check multiple codes simultaneously and provides a progress bar to track the checking process.

#### Features:
- **Code Generation**: Generates random Discord Nitro gift codes.
- **Code Validation**: Checks the validity of the generated codes by making HTTP requests to Discord's API.
- **Progress Bar**: Displays a progress bar to show the status of the code-checking process.
- **Logging**: Logs valid and invalid codes into separate files.
- **Terminal Title Update**: Updates the terminal title with the number of checked codes and elapsed time.

#### Project Structure:
- **`main.py`**: The main script that runs the application.
- **`generate.py`**: (Not shown in the provided code) Presumably used for generating codes or other related tasks.
- **`run.bat`**: A batch file to run the script on Windows systems.
- **`assets/`**: Directory containing resources used by the project.
  - **`images/`**: Subdirectory for image files.
- **`data/`**: Directory containing data files used by the project.
  - **`codes.txt`**: File containing generated codes.
  - **`invalid.txt`**: File containing invalid codes.
  - **`valid.txt`**: File containing valid codes.

#### How to Use:
1. **Install Dependencies**: Ensure you have the required libraries installed. You can install `tqdm` using pip:
   ```sh
   pip install tqdm
   ```
2. **Add Your Cookie**: Populate the `cookie` variable in the `main.py` file with a valid session cookie.
3. **Run the Script**: Execute the `main.py` script to start the application.
   ```sh
   python main.py
   ```
4. **Enter Number of Codes**: When prompted, enter the number of codes you want to generate and check.

#### Code Overview:
- **Imports**: The script imports necessary libraries, including `random`, `string`, `requests`, `os`, `platform`, `concurrent.futures`, `threading`, `time`, `datetime`, and `tqdm`.
- **DiscordGiftChecker Class**: Handles the HTTP requests to check the validity of the codes.
- **TerminalTitleSetter Class**: Updates the terminal title with the number of checked codes and elapsed time.
- **FileHandler Class**: Manages reading from and writing to files.
- **CodeGenerator Class**: Generates random Discord Nitro gift codes.
- **GiftCheckerApp Class**: The main application class that sets up the environment, generates codes, checks their validity, and displays the results.

#### Example Usage:
```python
if __name__ == "__main__":
    cookie = ""  # Add your cookie here
    CA = int(input("Enter the number of codes to generate: "))  # Ask user for the number of codes to generate

    app = GiftCheckerApp(cookie)
    app.setup()
    app.check_codes(CA)
```

This script will generate the specified number of codes, check their validity, and display the results along with a progress bar.

#### Note:
- The tool may no longer work due to updates or changes made by Discord. Please refer to the repository for any updates or alternatives.

---

Feel free to customize this description further to fit your specific needs or to add more details as necessary.
