# Amino Acid Pairwise Potential Table Generator (Onck Force Field)

This Python project generates pairwise nonbonded potential energy and force tables for amino acid pairs using the Onck coarse-grained force field model.  
It parses amino acid properties from a text input file, calculates electrostatic and Lennard-Jones type interactions, and outputs formatted tables compatible with molecular simulations.

---

## 📚 Project Description

Accurate modeling of amino acid interactions is crucial for coarse-grained molecular simulations of proteins.  
This script automates:

- Parsing amino acid charges and hydrophobic parameters from a text file.
- Generating all possible amino acid pair combinations (i <= j).
- Computing distance-dependent electrostatic interactions using screened Coulomb (Debye-Hückel) potentials.
- Calculating Lennard-Jones type hydrophobic and repulsive terms.
- Producing nonbonded interaction tables formatted for use in molecular simulations (e.g., LAMMPS).

The force field is based on parameterizations from the Onck coarse-grained model.

---

## 📂 Repository Structure

```
pairwise_potential_generator/
├── aa_code_x3.txt        # Input file containing amino acid properties (charges, epsilon, names)
├── ff_FGx3/              # Output directory containing generated pairwise potential tables
├── generate_potentials.py # Main Python script to run the calculations
└── README.md             # Project overview and usage instructions
```

---

## 🚀 How to Run

1. Make sure the following files/folders are present:
   - `aa_code_x3.txt` (input file with amino acid data)
   - Create an empty folder named `ff_FGx3/` (output files will be written here).

2. Run the Python script:
   ```bash
   python generate_potentials.py
   ```

3. Output:
   - Pair-specific table files (`nbint_XX_YY_x3.table`) will be generated inside `ff_FGx3/`.
   - Each table corresponds to a specific amino acid pair (XX = amino acid 1, YY = amino acid 2).

---

## ⚡ Skills and Tools Demonstrated

- Python scripting for scientific data generation
- SymPy symbolic algebra for force and energy derivative calculations
- Handling combinatorial pairings of input datasets
- File I/O and formatted data output for simulation use
- Application of coarse-grained biophysical force fields (Onck FF)

---

## 📄 License

This project is licensed under the MIT License.

---

## 👨‍💻 Developed By

Sanjeev Kumar Gautam
