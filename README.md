# ShareVolume

## Project Description
ShareVolume is a web application designed to fetch and display outstanding share data for publicly traded companies from the SEC's XBRL API. This project pulls the most recent data for Clorox (CIK: 0000021076) and allows users to view the maximum and minimum outstanding shares post-2020. Users can also query other companies by setting the CIK parameter in the URL.

## Features
- Fetches and displays outstanding share data for the specified company.
- Identifies and displays maximum and minimum outstanding shares since 2020.
- Allows live retrieval of data for any other company using their CIK.
- Presents the information in a clean and visually appealing HTML format.
- Supports user-defined CIK queries through the URL.

## Setup Instructions
To get started with the ShareVolume project, follow these steps:

1. **Clone the Repository:**
   ```bash
   git clone https://github.com/yourusername/sharevolume.git
   cd sharevolume
   ```

2. **Install Dependencies:**
   Ensure you have Node.js and npm installed. Then install any required dependencies:
   ```bash
   npm install
   ```

3. **Run the Application:**
   Open your browser and navigate to `index.html` to view the application. 

## Usage
- The application will load with Clorox's outstanding share data displayed.
- You can view the maximum and minimum shares by looking at the respective fields in the interface.
- To query data for other CIK values, modify the URL by appending `?CIK=0001018724` (replace `0001018724` with the desired CIK).

## Code Explanation
- The application sends a GET request to the SEC's API, specifying a user-agent for compliance.
- It parses the JSON response to extract the entity name and filters shares with fiscal years greater than 2020, ensuring that only numeric values are considered.
- The resulting data is saved in a `data.json` file with the required structure including max and min share values with corresponding fiscal years.
- The HTML interface updates dynamically based on the CIK provided in the URL without requiring a page reload.

## License
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for more details.

---

**Note:** Please ensure to maintain good practices when fetching data from external API endpoints, particularly respecting their usage policies (e.g., setting an appropriate user-agent string). For deploying this application or further development, additional error handling and UI improvements may be considered.