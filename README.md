# 🚀 Smart MarketPlace - AI Job Mission Generator

> **Create professional freelance missions in seconds with artificial intelligence**

A cutting-edge web application powered by AI that intelligently generates detailed freelance job missions from minimal client input using advanced language models.

## ✨ Features

- 🤖 **AI-Powered Generation** - Leverages Qwen2.5 model via OpenRouter API
- 🌍 **Multi-Language Support** - Automatic language detection and generation
- 🎨 **Modern UI/UX** - Clean, professional interface with responsive design
- ⚡ **Real-time Processing** - Instant mission generation and display
- 📋 **Structured Output** - Comprehensive mission details with JSON export
- 🔧 **RESTful API** - Well-documented endpoints for integration

## 🏗️ Architecture

```
┌─────────────────┐    ┌─────────────────┐    ┌─────────────────┐
│   Frontend      │    │   Backend API   │    │   AI Service    │
│  (Razor Pages)  │◄──►│  (ASP.NET Core) │◄──►│  (Python/AI)    │
└─────────────────┘    └─────────────────┘    └─────────────────┘
```

### 🧩 Components

| Component | Technology | Description |
|-----------|------------|-------------|
| **Frontend** | ASP.NET Core Razor Pages | Modern, responsive user interface |
| **Backend API** | ASP.NET Core Web API | RESTful API with comprehensive endpoints |
| **AI Integration** | Python + OpenRouter API | Advanced language model processing |
| **Shared Models** | .NET Class Library | Common data models and DTOs |

## 🚀 Quick Start

### Prerequisites

- **.NET 8.0 SDK** or later
- **Python 3.8+** with pip
- **Git** (optional)

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/badrbenabdellah/Smart_MarKetPlace.NET.git
   cd Smart-marketplace
   ```

2. **Install Python dependencies**
   ```bash
   cd PythonScripts
   pip install -r requirements.txt
   cd ..
   ```

3. **Build the .NET solution**
   ```bash
   dotnet build
   ```

4. **Run the API project**
   ```bash
   cd SmartMarketPlace.API
   dotnet run
   ```

5. **Run the Web project** (in a new terminal)
   ```bash
   cd SmartMarketPlace.Web
   dotnet run
   ```

6. **Access the application**
   - 🌐 **Web Interface**: http://localhost:8001
   - 📚 **API Documentation**: http://localhost:7001/swagger

## 📖 Usage

### Web Interface

1. **Enter a description** like "Java developer web application"
2. **Select language** or use automatic detection
3. **Click "Generate My Mission"**
4. **Review** the generated mission details
5. **Copy JSON** output if needed

### API Endpoint

```http
POST /api/JobMission/generate
Content-Type: application/json

{
  "prompt": "Java developer web application",
  "language": "english"
}
```

## 📊 Example Output

```json
{
  "title": "Java Web Developer Needed",
  "description": "## Responsibilities\n- Develop and maintain Java web applications\n- Collaborate with design and backend teams\n- Implement robust and scalable solutions\n- Participate in code reviews and testing\n\n## Requirements\n- Strong experience with Java and web technologies\n- Knowledge of Spring Framework, Hibernate\n- Understanding of RESTful APIs\n- Experience with front-end technologies (HTML, CSS, JavaScript)",
  "country": "United States",
  "city": "New York",
  "workMode": "REMOTE",
  "duration": 3,
  "durationType": "MONTH",
  "startImmediately": true,
  "experienceYear": "3-7",
  "contractType": "FIXED_PRICE",
  "estimatedDailyRate": 400,
  "domain": "Technology",
  "position": "Java Web Developer",
  "requiredExpertises": ["Java", "Spring", "Hibernate", "REST API", "HTML/CSS", "JavaScript"]
}
```

## 🎯 Supported Languages

- 🇺🇸 **English** - Full support
- 🇫🇷 **French** - Full support  
- 🇸🇦 **Arabic** - Full support
- 🇪🇸 **Spanish** - Full support
- 🌐 **Auto-detection** - Intelligent language recognition

## 🛠️ API Reference

### Generate Mission

**Endpoint:** `POST /api/JobMission/generate`

**Request Body:**
```json
{
  "prompt": "string",
  "language": "auto|english|french|arabic|spanish"
}
```

**Response:**
```json
{
  "title": "string",
  "description": "string (markdown)",
  "position": "string",
  "location": "string",
  "workMode": "string",
  "duration": "number",
  "durationType": "string",
  "experienceYear": "string",
  "contractType": "string",
  "estimatedDailyRate": "number",
  "domain": "string",
  "requiredExpertises": ["string"],
  "detectedLanguage": "string",
  "uiLabels": "object"
}
```

## 🎨 Screenshots

### Main Interface
![Main Interface](Images/mission1.png)

### Language Selection
![Language Selection](Images/MISSION2.png)

### Generated Mission
![Generated Mission](Images/MISSION3.png)

### Arabic Support
![Arabic Support](Images/mission4.png)

### Arabic Output
![Arabic Output](Images/mission5.png)

## 🔧 Development

### Project Structure

```
Smart-marketplace/
├── SmartMarketPlace.Web/          # Frontend application
├── SmartMarketPlace.API/          # Backend API
├── SmartMarketPlace.Models/       # Shared models
├── PythonScripts/                 # AI integration scripts
└── README.md                      # This file
```

### Technologies Used

- **Frontend**: ASP.NET Core Razor Pages, Bootstrap, Modern CSS
- **Backend**: ASP.NET Core Web API, Entity Framework
- **AI**: Python, OpenRouter API, Qwen2.5 Model
- **Styling**: Custom CSS with professional design system

## 🤝 Contributing

We welcome contributions! Please feel free to submit a Pull Request.

## 📄 License

This project is developed by **Safae Hammouch** and **Oumaima Boughdad**.

## 🆘 Support

If you encounter any issues or have questions, please open an issue on GitHub.

---

<div align="center">
  <strong>Made with ❤️ by the Smart MarketPlace Team</strong>
</div>
