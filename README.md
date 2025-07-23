# Indian Healthcare Supply Chain Management Assistant

A Streamlit-based chatbot that provides insights and recommendations for Indian healthcare supply chain management using Google's Gemini AI model.

## Features

- State-wise budget allocation recommendations
- Population-based resource distribution
- Supply chain optimization suggestions
- Healthcare infrastructure planning
- Interactive chat interface

## Prerequisites

- Python 3.8 or higher
- pip (Python package installer)
- Google API key for Gemini AI

## Installation Steps

1. Clone the repository:
```bash
git clone <repository-url>
cd Chatbot_scm
```

2. Create a virtual environment (recommended):
```bash
python -m venv venv
source venv/bin/activate  # On Windows, use: venv\Scripts\activate
```

3. Install required dependencies:
```bash
pip install -r requirements.txt
```

4. Set up your environment variables:
   - Create a `.env` file in the project root directory
   - Add your Google API key:
   ```
   GOOGLE_API_KEY=your_api_key_here
   ```

## Running the Application

1. Make sure you're in the project directory:
```bash
cd Chatbot_scm
```

2. Start the Streamlit application:
```bash
streamlit run qachat.py
```

3. The application will open in your default web browser at:
   - Local URL: http://localhost:8501
   - Network URL: http://<your-ip>:8501

## Usage

1. Select an analysis type from the sidebar:
   - Budget Allocation
   - Supply Chain Optimization
   - Infrastructure Planning
   - Resource Distribution

2. Choose a state/UT from the dropdown menu

3. Type your question in the chat interface and click "Submit Question"

4. The AI assistant will provide detailed responses based on:
   - Population-based resource allocation
   - Geographic distribution
   - Healthcare infrastructure needs
   - Supply chain optimization
   - Budget allocation metrics

## Note

Make sure you have a valid Google API key with access to the Gemini AI model. The application requires an active internet connection to function properly.

## Deployment

### Streamlit Cloud (Recommended)

1. Push your code to GitHub
2. Go to [Streamlit Cloud](https://share.streamlit.io/)
3. Connect your GitHub repository
4. Set the main file path to `Chatbot_Scm/qachat.py`
5. Add your GOOGLE_API_KEY as a secret in the Streamlit Cloud dashboard
6. Deploy

### Heroku

1. Make sure you have the Heroku CLI installed
2. Login to Heroku: `heroku login`
3. Create a new Heroku app: `heroku create your-app-name`
4. Set the API key: `heroku config:set GOOGLE_API_KEY=your_api_key_here`
5. Push to Heroku: `git push heroku main`

### Railway or Render

Both platforms offer simple deployment from GitHub repositories:

1. Connect your GitHub repository
2. Set the build command: `pip install -r requirements.txt`
3. Set the start command: `streamlit run Chatbot_Scm/qachat.py`
4. Add the GOOGLE_API_KEY as an environment variable
5. Deploy

## Error Handling

The application includes robust error handling for API overload situations:
- Automatic retries with exponential backoff (up to 5 attempts)
- Rate limiting to prevent excessive API calls (10 requests per minute)
- Clear user feedback during retries and errors
- Preservation of partial responses in case of streaming errors
"# Chatbot_Scm" 
"# Chatbot_Scm" 
