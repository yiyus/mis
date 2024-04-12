Calculate misorientations
========================

Dyalog APL script to calculate the distribution of misorientation angles
assuming cubic symmetry.

Installation
------------

Download and extract the `mis.apls` script into the directory
where you want to run it. You will need to have
[Dyalog APL v18.2](https://www.dyalog.com/download-zone.htm) installed.

Usage
-----

Run the script inside an empty directory to generate the misorientations
distribution for a random texture of the defined number of orientations
(5000 by default). Run it in a directory with an ang file to calculate
the (non-correlated) misorientations distribution. Run it in a directory
with two ang files and the distribution of misorientations between them
will be calculated.

Configuration
--------------

Some parameters can be configured at the beginning of the mis.apls file:

- `degrees`: read angles in degrees
- `angle_resolution`: angles resolution for input files (in degrees)
- `disorientation_resolution`: disorientations resolution (in degrees)
- `number_of_orientations`: for random texture
- `output_file_0`: output file when no ang file is found
- `output_file_1`: output file when 1 ang file is found
- `output_file_2`: output file when 2 ang files are found

Input ang files
---------------

Any file with `ang` extension is considered a valid ang file. Euler
angles are read from the first three columns, for every row, and rounded
according to `angle_resolution`. No filtering is performed neither by
phase or by other parameters.

Output files
------------

Each line corresponds to the fraction for consecutive misorientation
levels according to the `disorientation_resolution` parameter.



jesus.galanlopez@ugent.be 2024
