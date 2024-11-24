
# NFL Point Kicker Data Scraper

A Python-based tool that retrieves NFL game data within a specified time period and extracts detailed point-kicking statistics. The data is formatted into clean, ready-to-use CSV files, ideal for analysis and visualization.

## Purpose

This project simplifies the process of analyzing NFL kicking data by automating data extraction and formatting. The generated datasets are perfect for creating graphs, identifying trends, or conducting in-depth statistical analysis. It utilizes data sourced from [Pro-Football-Reference](https://www.pro-football-reference.com/), ensuring accurate and comprehensive information.

## Features

- **Customizable Time Frame**: Fetch games from any specified time period by year.
- **Detailed Kick Data**: Extract key data points for each kick, such as distance, success rate, and wind conditions.
- **CSV Export**: Automatically formats the data into CSV files for seamless integration with data analysis tools.

## Use Cases

- **Sports Analytics**: Analyze trends in field goal success rates or identify patterns across different teams and players.
- **Data Visualization**: Create compelling graphs and visualizations for presentations or personal projects.
- **Machine Learning**: Use the formatted datasets as input for predictive modeling or other AI applications.

## Getting Started

### Prerequisites
- Python 3.x

### Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/Code-JL/NFL-Point-Kicker-Data-Scraper.git
   ```

### Usage
1. Execute the following files in order:
   - `FootballInfoScraper.py`
   - `FootballGameInfoScraper.py` (This may take a significant amount of time; proceed to the next steps while it runs.)
   - `GameUrlDateSeparator.py`
   - `DateToCSVFormat.py`
   - `TotalDataFormatting.py`
   - `SplitDataFormatting.py` (optional)
   
2. Specify the desired time period within the code.
3. Retrieve the generated CSV files from the output directory.

## Future Improvements

- Combine all scripts into a single execution flow for streamlined usability.
- Add support for real-time data updates.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
