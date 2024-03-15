Got it! Let's adjust the README to focus on how to add a new pedal firmware to the `firmwares.json` file, intended for developers or advanced users who are managing or contributing to the firmware library.

---

# Chase Bliss Firmware Sources

This guide is intended for developers or contributors who wish to add a new pedal firmware entry to the `firmwares.json` file in the Chase Bliss firmware library.

## Introduction

The `firmwares.json` file serves as a directory for all available firmware updates for Chase Bliss devices. Each entry in this JSON file contains essential information about a specific firmware, including its name, target device model, file path, and other attributes.

## Adding a New Firmware Entry

To add a new pedal firmware to the `firmwares.json`, follow the steps outlined below:

### Step 1: Prepare the Firmware File

Ensure your firmware binary file (`.bin`) is ready and has been thoroughly tested. Place the file in the appropriate directory within your project. Typically, this would be in a directory path similar to `./dist/models/`.

### Step 2: Construct the JSON Block

Create a JSON block for the new firmware entry. This block should include the following information:

- `id`: A unique identifier for the firmware entry. This should be an integer, incrementing from the last entry in the file.
- `name`: The name of the pedal or firmware.
- `platform`: The device model this firmware is designed for. Use a consistent identifier for each model.
- `filepath`: The relative path to the firmware binary file within the project.
- `description`: A brief description of the firmware or the features it introduces.
- `bgColor`: A hex color code representing the firmware in UIs (optional).
- `active`: A boolean indicating whether this firmware should be considered active or visible to users. Set to `true` for new active firmware.

Example:

```json
{
  "id": 3,
  "name": "Reverse Mode C",
  "platform": "models",
  "filepath": "./dist/models/CB_REVERSE_MODE_C.bin",
  "description": "Chase Bliss Reverse Mode C Firmware",
  "bgColor": "#b1c0ca",
  "active": true
}
```

### Step 3: Add the JSON Block to `firmwares.json`

Open the `firmwares.json` file in your text editor or IDE. Append the JSON block you constructed in Step 2 to the array of firmware entries, ensuring it is correctly formatted as valid JSON.

### Step 4: Validate JSON Integrity

After adding the new entry, validate the JSON file to ensure there are no syntax errors. You can use online JSON validation tools or IDEs with JSON support to check the file.

### Step 5: Commit Your Changes

Once validated, commit your changes to the repository, following your project's contribution guidelines. If you're working within a team, consider creating a pull request for review.

## Conclusion

By following these steps, you can successfully add a new pedal firmware to the `firmwares.json` file, contributing to the Chase Bliss firmware ecosystem. This process ensures that the firmware library remains organized and easily accessible for updates and management.

---

**Note**: Replace placeholders like `CB_REVERSE_MODE_C.bin` and hex color codes with actual values corresponding to the new firmware you're adding. Ensure all information is accurate and reflective of the firmware's purpose and compatibility.
