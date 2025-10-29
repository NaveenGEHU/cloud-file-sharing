# 🤖 AI FileShare

An intelligent file sharing application powered by AI that provides automatic file analysis, content summarization, security scanning, and smart search capabilities.

## Features

### 🧠 AI-Powered Analysis
- **Content Type Detection**: Automatically identifies document types, code files, data files, etc.
- **Language Detection**: Recognizes programming languages in code files
- **Content Summarization**: Generates intelligent summaries for text-based files
- **Security Risk Assessment**: Analyzes files for potential security risks
- **Smart Tagging**: Automatically tags files based on content analysis

### 🔍 Intelligent Search
- **Semantic Search**: Search files by content, type, or AI-generated tags
- **Real-time Results**: Instant search results as you type
- **Smart Filtering**: Filter by content type, security risk, or language

### 📁 File Management
- **Secure Upload**: Files are securely stored with SHA-256 hashing
- **Temporary Links**: Shareable links that expire in 15 minutes
- **Automatic Cleanup**: Background process removes expired files
- **File Metadata**: Comprehensive file information and analysis

## Setup Instructions

### 1. Install Dependencies
```bash
pip install -r requirements.txt
```

### 2. Set OpenAI API Key
You need an OpenAI API key for AI analysis features:

**Option A: Environment Variable (Recommended)**
```bash
export OPENAI_API_KEY="your-openai-api-key-here"
```

**Option B: Direct Configuration**
Edit `app.py` and replace `'your-openai-api-key-here'` with your actual API key.

### 3. Run the Application
```bash
python app.py
```

The application will be available at `http://localhost:5000`

## Usage

1. **Upload Files**: Drag and drop or select files to upload
2. **View AI Analysis**: Get instant AI-powered analysis of your files
3. **Share Links**: Copy the generated link to share files
4. **Search Files**: Use the search box to find files by content or tags
5. **Download Files**: Click on search results to download files

## Supported File Types

The AI analysis works with:
- **Text Files**: `.txt`, `.md`, `.doc`, `.docx`
- **Code Files**: `.py`, `.js`, `.html`, `.css`, `.java`, `.cpp`
- **Data Files**: `.json`, `.xml`, `.csv`
- **Configuration Files**: Various config formats

## API Endpoints

- `GET /` - Main upload interface
- `POST /` - Upload files
- `GET /<file_id>` - Download file
- `GET /analyze/<file_id>` - Get AI analysis for a file
- `POST /search` - Search files using AI

## Security Features

- **File Hashing**: SHA-256 hash generation for file integrity
- **Secure Filenames**: Automatic filename sanitization
- **Risk Assessment**: AI-powered security risk evaluation
- **Temporary Storage**: Files automatically deleted after 15 minutes

## Configuration

- **File Size Limit**: 25 MB maximum
- **Link Expiry**: 15 minutes
- **Cleanup Interval**: 60 seconds
- **AI Model**: GPT-3.5-turbo (configurable)

## Troubleshooting

### OpenAI API Issues
- Ensure your API key is valid and has sufficient credits
- Check your internet connection
- Verify the API key is set correctly

### File Upload Issues
- Check file size (max 25 MB)
- Ensure file type is supported
- Verify uploads directory permissions

## License

This project is open source and available under the MIT License.


