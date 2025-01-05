# NFL Point Kicker Data Scraper

A Python-based web scraping toolkit that extracts and processes NFL kicking statistics from Pro-Football-Reference. This project automates the collection of comprehensive game data, with a particular focus on field goal attempts and environmental conditions.

## Overview

The NFL Point Kicker Data Scraper systematically collects and processes data through a pipeline of specialized Python scripts, each handling a specific aspect of the data collection and formatting process. The result is a series of well-structured CSV files ready for analysis.

## Key Features

- **Comprehensive Data Collection**
  - Stadium information
  - Roof type and playing surface
  - Weather conditions (temperature, humidity, wind speed)
  - Field goal attempts and success rates

- **Intelligent Data Processing**
  - Automatic rate limiting to prevent IP bans
  - Incremental data saving
  - Error handling and recovery
  - Multiple output formats for different analysis needs

- **Specialized Output Files**
  - Complete dataset (NFLKicksInfo2000-2022.csv)
  - Weather-specific analysis (NFLKicksInfo2000-2022WeatherSplit.csv)
  - Dome-specific analysis (NFLKicksInfo2000-2022NonSplitClosedDome.csv)
  - Wind chill analysis (NFLKicksInfo2000-2022WeatherSplitWindChill.csv)

## Technical Architecture

The system operates through a series of specialized scripts:

1. `FootballInfoScraper.py` - Initializes the scraping pipeline and collects game URLs
2. `FootballGameInfoScraper.py` - Extracts detailed game data
3. `GameUrlDateSeparator.py` - Processes game dates
4. `DateToCSVFormat.py` - Standardizes date formats
5. `TotalDataFormatting.py` - Creates the master dataset
6. `SplitDataFormatting.py` - Generates specialized analysis files

## Installation

```bash
# Clone the repository
git clone https://github.com/Code-JL/NFL-Point-Kicker-Data-Scraper.git

# Navigate to project directory
cd NFL-Point-Kicker-Data-Scraper

# Install required packages
pip install -r requirements.txt
```

## Usage

Execute the scripts in the following order:

```bash
python FootballInfoScraper.py
python FootballGameInfoScraper.py
python GameUrlDateSeparator.py
python DateToCSVFormat.py
python TotalDataFormatting.py
python SplitDataFormatting.py
```

Note: `FootballGameInfoScraper.py` may take significant time to complete due to rate limiting.

## Output Files

The scraper generates several CSV files optimized for different analysis scenarios:

- `NFLKicksInfo2000-2022.csv` - Complete dataset
- `NFLKicksInfo2000-2022WeatherSplit.csv` - Weather-specific analysis
- `NFLKicksInfo2000-2022NonSplit.csv` - General analysis
- `NFLKicksInfo2000-2022NonSplitClosedDome.csv` - Indoor game analysis
- `NFLKicksInfo2000-2022WeatherSplitWindChill.csv` - Wind chill impact analysis

## Data Fields

Each record includes:
- Game date and location
- Stadium characteristics
- Environmental conditions
- Kicking performance metrics

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments

- Data sourced from [Pro-Football-Reference](https://www.pro-football-reference.com/)
- Built with Python and BeautifulSoup4
