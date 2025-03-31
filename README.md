# Pokemon Colour Sorter

## Overview
This project processes Pokémon images to extract their dominant colors using K-means clustering. It then matches these colors to human-readable color names and updates a CSV file containing Pokémon data.

## Features
- Extracts dominant colors from Pokémon images (.png format).
- Uses K-means clustering to determine the most prevalent colors.
- Matches extracted colors to human-readable names.
- Updates a CSV file with the extracted color information.
- Displays sample color extractions with visualizations.

## Installation
To run this project, install the required dependencies:
```bash
pip install scikit-learn pillow webcolors pandas numpy matplotlib
```

## Usage
1. Ensure you have a CSV file (e.g., `PokemonData.csv`) with `Num` and `Name` columns.
2. Place Pokémon images in a folder (e.g., `Pokemon/`), ensuring they are in `.png` format.
3. Run the script:
```python
csv_file = "path/to/PokemonData.csv"
image_folder = "path/to/Pokemon"
result_df = process_pokemon_images(csv_filename=csv_file, image_folder=image_folder, num_colors=3, show_samples=1)
```

## Output
- A new CSV file (`PokemonData_Colours.csv`) with an additional `Colour` column containing the extracted color names.
- Sample Pokémon images and their dominant colors are displayed.

## Known Issues
- The extracted hex values are accurate, but the color name conversion may be inaccurate due to limitations in the `webcolors` library.
- Some Pokémon images may not be found if their filenames do not match the expected format (`Num.png`).
- Dataset is limited upto Generation VI Pokémon.

## Contributing
If you find issues or have improvements, feel free to open a pull request or issue in the repository.

## License
This project is open-source and available under the MIT License.

