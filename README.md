# SMILES Structure Viewer

A simple single-page website for drawing molecular structures from SMILES strings and looking up English IUPAC names.

## Features

- Enter a SMILES string and render a 2D molecular structure.
- Look up the English IUPAC/systematic name through PubChem.
- Includes an aspirin example button.
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
