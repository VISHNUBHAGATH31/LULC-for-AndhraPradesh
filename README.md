
# Land Cover Classification for Andhra Pradesh

This project leverages Google Earth Engine (GEE), geemap, and Streamlit to analyze and visualize land cover changes in Andhra Pradesh, India. The tool allows users to classify land cover into categories such as Water, Buildup, Vegetation, and Barren land for specific districts and years.

## Features

- **Interactive Map:** Visualize land cover classifications for selected years and districts.
- **Classification:** Uses Sentinel-2 Harmonized imagery to classify land cover using a trained classifier.
- **Area Analysis:** Provides detailed statistics of the area covered by each land cover class.
- **Comparison:** Compare land cover changes between two selected years.
- **Streamlit Interface:** User-friendly interface for exploring and interacting with the data.

## Getting Started

### Prerequisites

Ensure you have the following installed:

- Python 3.8+
- Required Python libraries:
  - `earthengine-api`
  - `geemap`
  - `streamlit`
  - `pandas`
  - `matplotlib`
  - `seaborn`
  - `numpy`

### Installation

1. Clone this repository:
   ```bash
   git clone https://github.com/your-repo-name/land-cover-classification.git
   cd land-cover-classification

2. Install the required dependencies:

    pip install -r requirements.txt

3. Authenticate with Google Earth Engine:

      earthengine authenticate

4. Update the  ee.Initialize() method with your GEE project ID in the script

### Code Overview

### Key Components

- **Training Data:** Utilizes GEE FeatureCollection for training the classifier.

- **Classifier:** Employs smileCart classifier from GEE.

- **Visualization:** Generates land cover classification maps with color-coded categories.

- **Area Calculation:** Computes the area covered by each class in square kilometers.

### Core Functions

- get_median_image(year, roi): Fetches the median image for the specified year and region of interest.

- classify_image(image, roi): Classifies the input image based on the trained classifier.

- extract_class_areas_optimized(classified_image, roi, year): Computes and displays the area of each class.

- classify_district(year1, year2, district_name): Processes and visualizes land cover classification for the selected district and years.

### Example Usage

1. Select Krishna as the district.

2. Choose 2020 and 2022 as the comparison years.

3. View the classification map and area statistics in the Streamlit interface.

### Visualization

- **Maps:** Display land cover classifications with district borders.

- **Bar Charts:** Compare areas covered by each class for the selected years.

### Future Enhancements

- Include more land cover classes for detailed analysis.

- Add support for additional imagery datasets.

- Enhance the GUI for better interactivity.

### License

This project is licensed under the MIT License.

### Acknowledgements

- **Google Earth Engine** for providing powerful geospatial analysis capabilities.

- **Geemap** for interactive mapping tools.

- **Streamlit** for creating an intuitive user interface.

### Contact

For questions or suggestions, feel free to reach out at [vishnubhagath898@gmail.com].

### Visualization and Comparison

#### Land Cover Classification for Krishna District, 2022
![Land Cover Classification for Krishna District, 2022](https://github.com/user-attachments/assets/1f3a1786-73d0-4347-bc59-9ef3a37366d3)

#### Land Cover Classification for Krishna District, 2023
![Land Cover Classification for Krishna District, 2023](https://github.com/user-attachments/assets/3fde18f1-1f0b-45d3-a3de-cc65f56031b1)

#### Land Cover Area Comparison for Krishna District (2022 vs 2023)
![Land Cover Area Comparison](https://github.com/user-attachments/assets/10f37e55-73d9-4a6f-8f0f-bf9dbada2f5d)

#### District Border Overlay with Land Cover Classes
![District Border Overlay](https://github.com/user-attachments/assets/e8174b5c-1caf-49ca-bf6a-4264f556b728)

