# AI Math Problem Solver

A professional web application that uses Llama Vision (via OpenRouter) to analyze images of math problems and provide detailed step-by-step solutions.

## Features

- **Drag & Drop Interface**: Modern, professional UI with drag-and-drop functionality
- **Image Upload**: Support for various image formats (PNG, JPG, JPEG, etc.)
- **AI-Powered Analysis**: Uses Meta's Llama 3.2 90B Vision model via OpenRouter
- **Detailed Solutions**: Step-by-step explanations with reasoning
- **Error Detection**: Identifies and corrects mistakes in shown work
- **Smart Validation**: Detects if uploaded image contains math problems
- **Responsive Design**: Works on desktop and mobile devices

## Quick Start

### 1. Prerequisites
- Node.js (v14 or higher)
- OpenRouter API key

### 2. Installation

```bash
# Clone the repository
git clone https://github.com/AwsmAsim/llama_maths_solver.git
cd llama_maths_solver

# Install dependencies
npm install
```

### 3. Get OpenRouter API Key

1. Visit [OpenRouter.ai](https://openrouter.ai)
2. Sign up for an account
3. Go to Keys section and create a new API key
4. Copy your API key

### 4. Configure Environment Variables

**Option 1: Create .env file (Recommended):**
```bash
# Create .env file from template
cp .env.template .env

# Edit the .env file and add your API key
OPENROUTER_API_KEY=your_api_key_here
PORT=3000
```

**Option 2: Set environment variables manually:**

**On Windows:**
```bash
set OPENROUTER_API_KEY=your_api_key_here
```

**On Mac/Linux:**
```bash
export OPENROUTER_API_KEY=your_api_key_here
```

### 5. Run the Application

```bash
# Start the server
npm start

# For development with auto-restart
npm run dev
```

### 6. Access the App

Open your browser and go to: `http://localhost:3000`

## Project Structure

```
llama_maths_solver/
├── server.js           # Main backend server
├── package.json        # Dependencies and scripts
├── .env.template      # Environment variables template
├── .gitignore         # Git ignore file
├── public/
│   └── index.html     # Frontend interface
└── README.md          # This file
```

## How It Works

1. **Upload**: User drags/drops or selects an image containing a math problem
2. **Analysis**: Image is sent to Llama Vision model via OpenRouter API
3. **Processing**: AI analyzes the image and determines if it contains math problems
4. **Solution**: If math problem detected, provides detailed step-by-step solution
5. **Display**: Results are shown in a clean, readable format

## API Endpoints

- `GET /` - Serves the main HTML interface
- `POST /analyze-image` - Accepts image upload and returns AI analysis

## Supported Image Types

- PNG, JPG, JPEG, WebP, GIF
- Maximum file size: 10MB
- Optimal resolution: 800x600 to 2000x2000 pixels

## Error Handling

- Invalid file types
- File size limits
- Network connectivity issues
- API rate limits
- Non-math image detection

## Customization

You can modify the AI prompt in `server.js` to:
- Focus on specific math topics (algebra, calculus, etc.)
- Change explanation style (beginner, advanced)
- Add different languages
- Include teaching tips

## Troubleshooting

**Common Issues:**

1. **"OPENROUTER_API_KEY environment variable is required"**
   - Make sure you've set the API key as an environment variable

2. **"Network error: Unable to reach OpenRouter API"**
   - Check your internet connection
   - Verify your API key is valid

3. **"File too large"**
   - Resize your image to under 10MB
   - Use image compression tools

4. **Poor recognition results**
   - Ensure good image quality and lighting
   - Make sure text/equations are clearly visible
   - Avoid blurry or tilted images

## Cost Considerations

- OpenRouter charges per token used
- Llama 3.2 90B Vision is approximately $0.50-$1.00 per image analysis
- Consider implementing usage limits for production

## Next Steps

Potential enhancements:
- User authentication
- Solution history
- Multiple image upload
- LaTeX output formatting
- Integration with educational platforms
- Batch processing
- Mobile app version

## License

MIT License - feel free to modify and distribute!