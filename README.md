# AI Resume Checker

An innovative web app that analyzes resumes for Applicant Tracking System (ATS) compatibility and extracts key candidate information. Built with Streamlit, the app is aimed at both recruiters and job seekers.

## Features

- **Resume Analysis for Recruiters:** Upload multiple PDF resumes, extract valuable candidate data, and compare resumes.
- **ATS Evaluation for Job Seekers:** Get detailed feedback on resume ATS compatibility including keyword analysis, formatting, structure, and content.
- **Dynamic Data Extraction:** Configure custom extraction settings and prompt generation.
- **Rate Limiting:** Safeguards to prevent API overload during resume processing.

## Technologies Used

- **Streamlit:** Interactive web app interface.
- **Python-dotenv:** Environment variable management.
- **Pandas:** Data manipulation and analysis.
- **pdfplumber:** PDF parsing.
- **Google Generative AI:** API for advanced content generation.
- **openpyxl:** Excel file handling.

## Installation

1. **Clone the Repository:**

    ```
    git clone https://your-repo-url.git
    cd AI-Resume-Checker
    ```

2. **Set Up Environment Variables:**

    Create a `.env` file in the project root with the following variables:

    ```
    GOOGLE_API_KEY=your_google_api_key
    USERNAME=your_username   # Optional: defaults to "admin"
    PASSWORD=your_password   # Optional: defaults to "password123"
    ```

3. **Install Dependencies:**

    Install the required dependencies using pip:

    ```
    pip install -r requirements.txt
    ```

## Usage

1. **Run Locally:**

    Execute the app using Streamlit:

    ```
    streamlit run app.py
    ```

    Access the app in your web browser at `http://localhost:8501`.

2. **Authentication:**

    Log in using the credentials specified in your `.env` file or the Streamlit secrets.

3. **Resume Processing:**

    - Recruiters: Upload one or more PDF resumes via the sidebar.
    - Job Seekers: Follow the guided instructions for resume ATS evaluation.

## Docker Deployment

A Dockerfile is provided for containerized deployment.

1. **Build the Docker Image:**

    ```
    docker build -t ai-resume-checker .
    ```

2. **Run the Docker Container:**

    ```
    docker run -p 8501:8501 ai-resume-checker
    ```

    The app will be available on `http://localhost:8501`.

## Project Structure

```
AI-Resume-Checker/
│
├── app.py            # Main application code
├── requirements.txt  # Python dependencies
├── Dockerfile        # Docker configuration
├── .env              # Environment variables (not included in repo)
└── README.md         # Project documentation
```

## Contributing

Contributions are welcome. Please open issues or submit pull requests for improvements or bug fixes.

## License

This project is licensed under the MIT License.
