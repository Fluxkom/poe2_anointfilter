# Path of Exile 2 - Anoint Finder

This project is a web-based tool designed to help players of Path of Exile 2 easily find and filter "Anoints". Anoints are special enhancements in the game that can be obtained through specific combinations of items called "Emotions".

The Anoint Finder allows users to:
* Filter anoints based on the required Emotion combinations.
* Specify the count of each Emotion needed for a particular anoint.
* Search for anoints by their name or descriptive effect text.

## Project Structure

The project consists of the following key files:

*   `index.html`: This is the main HTML file that you open in your web browser. It contains the user interface for the Anoint Finder, including the filter options and the results display. It also houses the JavaScript logic for fetching data, filtering anoints, and updating the view.
*   `anoints_data.json`: This JSON file acts as a database for the tool. It stores all the anoint information, including their names, the effects they provide, and the specific combinations of "Emotions" (e.g., Ire, Guilt, Greed) required to obtain them.
*   `README.md`: This file, providing an overview and instructions for the project.

## How to Use

To use the Anoint Finder:

1.  **Open the Tool**: Simply open the `index.html` file in any modern web browser (e.g., Chrome, Firefox, Edge, Safari).
2.  **Filter by Emotions**:
    *   On the left side, you will find a list of "Emotions" (e.g., Ire, Guilt, Greed).
    *   Each emotion has a checkbox. By default, all emotions are selected (checked).
    *   Uncheck any emotion to exclude anoints that require that emotion from the results.
    *   Next to each emotion checkbox is a dropdown menu (defaulting to "3+"). This allows you to specify the maximum number of times that particular emotion can appear in an anoint's combination. For example, if you select "1" for "Ire", only anoints requiring exactly one Ire (and meeting other filter criteria) will be shown.
3.  **Search by Name or Effect**:
    *   Use the search bar (labeled "Search by Name or Effect...") to type keywords.
    *   The tool will filter the anoints in real-time, showing only those whose name or effect text contains your search query.
4.  **View Results**:
    *   The main table will display the filtered anoints with the following columns:
        *   **Name**: The name of the anoint.
        *   **Anoint Effect**: A description of what the anoint does.
        *   **Combination**: The specific Emotions and their sequence required for the anoint. The emotions in the combination are color-coded for easier identification.
    *   The number of currently displayed results is shown above the table.
    *   If no anoints match your filter criteria, a "No matching anoints found" message will appear.

## Data Source

All the anoint data, including names, effects, and their emotion combinations, is stored locally within the `anoints_data.json` file. The `index.html` page fetches and processes this data directly in the browser.

## Updating Data (Optional)

The anoint data is contained within `anoints_data.json`. If new anoints are discovered or existing ones change in Path of Exile 2, this file will need to be updated.

To update the data:

1.  Open `anoints_data.json` in a text editor.
2.  The file contains a JSON array of anoint objects. Each object has the following structure:
    ```json
    {
        "Name": "Name of the Anoint",
        "Anoint Effect": "Description of its effect",
        "Combinations": ["Emotion1", "Emotion2", "Emotion3"]
    }
    ```
3.  You can modify existing entries or add new anoint objects to the array, following the established format.
4.  Ensure the JSON syntax remains valid after making changes.
