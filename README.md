# SMILES Structure Viewer

A simple single-page website for drawing molecular structures from SMILES strings and looking up English IUPAC names.

## Features

- Enter a SMILES string and render a 2D molecular structure.
- Look up the English IUPAC/systematic name through PubChem.
- Open the matching PubChem compound page when PubChem finds a result.
- Click an atom in the structure, choose from a broad element list, and redraw the edited molecule.
- Download the current structure as PNG, JPG, or XYZ.
- Recognize SMILES from pasted or uploaded 2D/3D MOL, SDF, MOL2, PDB, or XYZ structure files.
- Handles invalid SMILES input with a clear message.

## How to Use

Open `index.html` in a browser, enter a SMILES string, and click **Draw structure**.

Example SMILES:

```text
CCO
```

This draws ethanol and displays the IUPAC name `ethanol`.

## Notes

- Structure rendering uses the local `smiles-drawer.min.js` file.
- IUPAC name lookup requires an internet connection because it queries PubChem.
- XYZ export uses PubChem 3D coordinates when available, with a flat initial-coordinate fallback.
- Reverse recognition converts MOL2, PDB, and XYZ into temporary SDF before querying PubChem. XYZ and PDB files without bond records use distance-based initial bond inference.
- Transition-metal complexes in XYZ/PDB may require explicit bonds, charges, and coordination details before PubChem can return a reliable SMILES.
