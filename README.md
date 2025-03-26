# Backend-Home-Project-Task

## Project Overview

Backend-Home-Project-Task is a Python-based command-line program that fetches and filters research papers from the PubMed API. The program identifies papers with at least one author affiliated with a pharmaceutical or biotech company and exports the results in a CSV file.

### Key Features
- Fetch research papers using the PubMed API with full query syntax support.
- Identify authors affiliated with non-academic institutions.
- Output results to a CSV file containing:
  - PubmedID
  - Title
  - Publication date
  - Non-academic author names
  - Company affiliations
  - Corresponding author email
- Command-line options for usability:
  - `-h` or `--help`: Display usage instructions.
  - `-d` or `--debug`: Print debug information.
  - `-f` or `--file`: Specify the output filename.

## Tools and Technologies Used
- **Programming Language**: Python (with typing)
- **API**: PubMed API
- **Dependency Management**: Poetry
- **Version Control**: Git (GitHub)
- **Output Format**: CSV
- **Documentation**: README.md with detailed instructions

## Project Structure
The project is modularized as follows:
```
/myproject
 ├── main.py                 # Entry point for command-line execution
 ├── pubmed_utils.py         # Module handling PubMed API interactions and filtering
 ├── pyproject.toml          # Poetry dependencies and project configuration
 ├── poetry.lock             # Poetry lock file
 ├── results.csv             # Output CSV file with query results
 ├── README.md               # Installation and usage instructions
 ├── .gitignore              # Git ignore file
```

## Installation

1. Clone the repository:
   ```sh
   git clone <repo_url>
   cd <repo_folder>
   ```
2. Install dependencies using Poetry:
   ```sh
   poetry install
   ```

## Running the Program

Execute the program with a research query:
```sh
poetry run python myproject/main.py "cancer"
```

### Store Results in a CSV File:
```sh
poetry run python myproject/main.py "cancer" -f results.csv
```

### Help and Debugging:
Display usage instructions:
```sh
poetry run python myproject/main.py -h
```
Print debug information:
```sh
poetry run python myproject/main.py -d
```

## Error Handling and Edge Cases
- **Invalid Queries**: Handles malformed PubMed queries gracefully with appropriate error messages.
- **API Failures**: Implements a retry mechanism and logs errors for failed API requests.
- **Missing Data**: Provides default values for missing author affiliations or emails to prevent crashes.
- **Performance Optimization**: Uses batch processing of API calls to reduce timeouts and latency.

## Additional Considerations
- **Typing**: Uses Python's type hints for improved code readability and robustness.
- **Documentation**: Includes project overview, installation guide, usage examples, and dependency details.
- **Version Control**: Managed using Git with a GitHub repository.
- **Modularization**: Separates core logic into a reusable module and a CLI program for better maintainability.

## Bonus Features
- **Modularization**: Separates functionality into core modules and a CLI program.
- **Test-PyPI Publishing**: The module can be published to Test-PyPI for package testing (if applicable).

## Conclusion
This project successfully implements:
- PubMed API integration for fetching research papers.
- CSV export with structured output fields.
- A flexible and user-friendly command-line interface.
- A modular, maintainable, and optimized architecture.

## License
This project is licensed under the MIT License.

---

For any questions or contributions, feel free to open an issue or submit a pull request!

