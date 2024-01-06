# Crystallographic Twins Identification Tool using OVITO
## Overview
This tool is designed to automate the identification, time-tracking and validation of crystallographic twins within crystal structures using OVITO. The tool is divided into two parts. 
`Identification_and_tracking.py` finds, connects and tracks suspected twin boundaries. `Validate_Findings.py` validates the findings from the previous part. 
The Python script provided here streamlines the process, making it efficient and easy to use.

## Features
- Automatic identification of crystallographic twins in crystal structures.
- Time-tracking functionality to monitor twin evolution over time frames.
- Validation of single detected structures, yielding of atomistic data files that allow for comprehensive analysis of results

## Requirements
Python environment with OVITO package installed.

## Installation and Usage
Download files: Download the contained files to your local machine.

Run the Script: Execute either Python file within a Python environment.

### Part 1: Identification and tracking
Example: `python Identification_and_tracking.py --numfram 6 shear.dump.*` would apply the algorithm to 6 frames of the dump file range.

Run `python Identification_and_tracking.py -h` to see all available flags.

Input Data: Provide crystal structure data as required by the script. Ensure the data format is compatible with OVITO.

Review Results: The tool will automatically identify crystallographic twins and provide time-tracking data if applicable.

### Part 2: Validation

Example: `python Validate_findings.py twins.*` would apply the algorithm to all timesteps, analyzed and exported in part 1.

Input Data: Part 1 creates a new directory "twinfiles" and exports lammps.dump files to the same. These files are the required input for part 2.

## Sample Data
For testing and demonstration purposes, sample lammps.dump files are included in the 'Testfiles' directory.

## Contributing
Contributions and improvements to this tool are welcome! Feel free to fork this repository or make changes.

## License
This tool is licensed under GNU GPLv3. See the LICENSE file for more details.

## Contact
For inquiries or suggestions, contact hendrik.ehrich@tuwien.ac.at.

