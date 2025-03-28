# Census Dataset Viewer

## Demo the Solution
Hosted here on GitHub: [Census Dataset Viewer](https://josephbooth.github.io/list-datasets-census-api/source/filter-datasets-api-census-gov.html)

Census API provided: [api.census.gov/data.html](https://api.census.gov/data.html)

## Overview

The **Census Dataset Viewer** is a simple web-based tool that provides users with a way to easily filter and navigate the vast datasets available on the U.S. Census Bureau's API (`api.census.gov`). It addresses the challenge of browsing through thousands of datasets on the **[Census Data API page](https://api.census.gov/data.html)**, which can be overwhelming, especially when users are trying to find specific datasets. Instead of scrolling through long lists or relying on search (Ctrl+F), this tool enables efficient filtering and easy access to dataset details through `.html` and `.json` links.

## Problem

The official Census data page presents a massive amount of data in a long list. Manually searching through it, either by scrolling or using the browser’s "find" function (Ctrl+F), is time-consuming and inefficient. The tool described in this project provides a solution by enabling users to filter datasets based on different criteria, making it easier to find datasets that meet their needs.

## Solution

The Census Dataset Viewer offers a user-friendly interface to filter datasets by:

- **Dataset Name**
- **Year of Data (Vintage)**
- **Dataset Title**

Once the user applies filters, they can easily access:

- **Dataset details in HTML format** by following the `.html` link.
- **Downloadable JSON data** through the `.json` link.

This approach drastically improves the usability and efficiency of working with the thousands of datasets offered by the Census API.

## Features

### Filtering Options:
- **Filter by Dataset Name**: Allows users to filter datasets based on the name (e.g., `acs1`, `acs5`).
- **Filter by Year**: Enables filtering of datasets based on the year (e.g., `2019`, `2022`).
- **Filter by Dataset Title**: Allows users to filter datasets based on keywords found in the dataset title (e.g., `Population`, `Housing`).

### Dataset Details:
- Clicking on the **Read Details** link opens the detailed information about a dataset in HTML format. This is pulled directly from the Census API.
- Clicking on the **Open .json** link lets users access the raw JSON data for the selected dataset.

### Performance Enhancements:
- **Caching**: To reduce repeated calls to the API, the tool caches the dataset information in the browser’s `localStorage` for 24 hours. This ensures that the data is quickly loaded without making a new API request every time the page is refreshed.

## How It Works

1. **Data Fetching**: On page load, the tool makes an API request to the Census API endpoint (`https://api.census.gov/data.json`), fetching the dataset information.
2. **Local Storage**: The fetched data is stored in the browser’s `localStorage` for up to 24 hours. This allows for faster page loading and reduces unnecessary API calls.
3. **Data Display**: The fetched dataset is displayed in a table, with the ability to filter by Dataset Name, Year, and Title.
4. **Filtering**: As users type in the filter fields, the dataset table is dynamically updated to show only the rows that match the filters.
5. **Dataset Details Links**: Users can click on the dataset’s **Read Details** link to view information in HTML format, or the **Open .json** link to download the raw data.

## Benefits

- **Improved User Experience**: The filtering system simplifies the process of finding datasets, especially for users who need to filter through thousands of entries.
- **Time-Saving**: The tool allows users to quickly find datasets without the need to manually scroll or search through the entire API page.
- **Instant Access to Details**: With direct links to both `.html` and `.json` files for each dataset, users can easily access and examine the details of any dataset.
- **Performance Optimized**: By caching the API data in the browser’s `localStorage`, the tool offers faster performance and reduces the need for repeated API requests.

## Installation

To use the Census Dataset Viewer, follow these steps:

1. **Clone or Download the Repository**: 
   - Clone the repository using `git clone https://github.com/josephbooth/list-datasets-census-api.git` or download the ZIP file from GitHub.
   
2. **Open the HTML File**:
   - Open the `filter-datasets-api-census-gov.html` file in any modern web browser (e.g., Chrome, Firefox, Edge, Safari).
   
   The tool should now be up and running in your browser, and you can begin filtering the Census datasets.

## Dependencies

The Census Dataset Viewer does not have any external dependencies. It is built using:
- **HTML**
- **CSS**
- **JavaScript** (vanilla JS)

All the functionality is implemented in a single HTML file, making it lightweight and easy to integrate into any project.

## Limitations

- **Data Size**: The tool currently fetches data from the Census API without any compression. If the dataset grows larger, this could impact performance. The tool does cache the data for 24 hours to mitigate frequent API calls, but further optimizations may be necessary as the data grows.
- **Census API Changes**: If the structure of the Census API changes, the tool may need to be updated to reflect these changes. However, as long as the API response structure remains consistent, the tool should continue to work.

## Usage

1. **Filter Datasets**: Use the input fields to filter the datasets by name, year, and title. The table will dynamically update to show matching datasets.
   
2. **Access Dataset Details**: For each dataset, you’ll see two links:
   - **Read Details**: Opens the dataset information in `.html` format.
   - **Open .json**: Opens the raw `.json` data for the dataset.

3. **Refreshing Data**: If the data in the tool is more than 24 hours old, the page will automatically fetch fresh data from the API.

## Contribution

If you want to contribute to the Census Dataset Viewer project, feel free to fork the repository and submit a pull request with your improvements. Any suggestions, bug fixes, or enhancements are welcome!

## License

This project is open source and available under the [MIT License](LICENSE).

## Contact

For any questions or feedback, feel free to open an issue on the repository.

---

Thank you for using the **Census Dataset Viewer**!
