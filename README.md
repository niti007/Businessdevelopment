# Product Analysis Dashboard

A comprehensive product analysis tool powered by AI agents that provides detailed market research, technology assessment, and business development insights for any product.

## Overview

This application leverages **CrewAI** with **Groq's LLM** to orchestrate specialized AI agents that analyze products from multiple perspectives:

- **Market Research Analyst** - Analyzes market demand and marketing strategies
- **Technology Expert** - Assesses technological feasibility and manufacturing requirements
- **Business Consultant** - Evaluates business models, scalability, and revenue streams

The results are presented through an interactive **Streamlit** dashboard for easy visualization and exploration.

## Features

✨ **Multi-Agent Analysis** - Three specialized AI agents working together to provide comprehensive product insights

📊 **Market Research** - Detailed analysis of market demand, customer profiles, and marketing strategies

🔧 **Technology Assessment** - Comprehensive evaluation of technological requirements and manufacturing approaches

💼 **Business Development** - Scalability analysis, revenue stream identification, and launch timeline planning

🎯 **Interactive Dashboard** - Clean, user-friendly Streamlit interface for viewing detailed reports

## Tech Stack

- **Python 3.x** - Core language
- **Streamlit** - Web UI framework
- **CrewAI** - Multi-agent orchestration framework
- **Groq API** - LLM provider (using Gemini 2.5 Flash)
- **Langchain** - LLM integration and tools
- **SerperDev Tool** - Web search capabilities for research

## Project Structure

```
Businessdevelopment/
├── backend/
│   ├── agents.py          # ProductAnalysisAgents class with specialized agents
│   └── tasks.py           # Productanalysistask class with task definitions
├── main.py                # Streamlit application entry point
├── .env                   # Environment variables (not in repo)
├── requirements.txt       # Python dependencies
└── README.md             # This file
```

## Installation

### Prerequisites

- Python 3.8 or higher
- Groq API Key
- SerperDev API Key (for web search)

### Setup Steps

1. **Clone the repository**
   ```bash
   git clone https://github.com/niti007/Businessdevelopment.git
   cd Businessdevelopment
   ```

2. **Create a virtual environment**
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

4. **Configure environment variables**
   
   Create a `.env` file in the root directory:
   ```
   GEMINI_API_KEY=your_groq_api_key
   SERPER_API_KEY=your_serper_api_key
   ```

## Usage

1. **Start the application**
   ```bash
   streamlit run main.py
   ```

2. **Access the dashboard**
   - Open your browser and navigate to `http://localhost:8501`

3. **Enter a product name**
   - Type the name of any product you want to analyze
   - Click "Analyze Product" button

4. **Review the reports**
   - The analysis generates three detailed reports:
     - Market Research Analysis
     - Technology Assessment
     - Business Development Plan

## How It Works

### Architecture Flow

```
User Input (Product Name)
        ↓
ProductAnalysisAgents (Creates 3 agents)
        ↓
Productanalysistask (Defines analysis tasks)
        ↓
CrewAI Crew (Orchestrates agents and tasks)
        ↓
Groq LLM (Generates insights using Gemini 2.5 Flash)
        ↓
Streamlit Dashboard (Displays formatted reports)
```

### Analysis Process

1. **Market Research Task**
   - Analyzes current market demand
   - Identifies ideal customer profiles
   - Suggests marketing strategies
   - Minimum 5 key marketing areas covered

2. **Technology Expert Task**
   - Assesses manufacturing technologies
   - Evaluates production feasibility
   - Recommends technological approaches
   - Minimum 5 key technological areas covered

3. **Business Consultant Task**
   - Synthesizes market and tech reports
   - Evaluates business model scalability
   - Identifies revenue streams
   - Provides business plan and launch timeline
   - Minimum 5 key business areas with explanations

## Configuration

### Agent Settings

Modify `backend/agents.py` to adjust:
- LLM model selection
- Agent roles and goals
- Verbose output level
- Tool availability
- Maximum iterations

### Task Settings

Modify `backend/tasks.py` to adjust:
- Task descriptions and requirements
- Expected output format
- Execution mode (async/sync)
- Analysis focus areas

### Crew Settings

Modify `main.py` to adjust:
- Maximum RPM (requests per minute) limit
- Agent ordering and priority
- Task execution order

## API Keys Required

### Groq API Key
- Sign up at [Groq Console](https://console.groq.com)
- Create an API key for Gemini model access
- Add to `.env` as `GEMINI_API_KEY`

### SerperDev API Key
- Sign up at [Serper.dev](https://serper.dev)
- Create an API key for web search capabilities
- Add to `.env` as `SERPER_API_KEY`

## Output Examples

Each analysis generates comprehensive reports including:

- Executive summaries
- Detailed market analysis
- Customer profile segments
- Competitive landscape
- Technology requirements
- Revenue stream models
- Scalability roadmap
- Launch timeline and milestones

## Limitations

- Analysis quality depends on LLM model capabilities
- Web search results are based on current Serper.dev data
- Analysis may take several minutes depending on product complexity
- Requires valid API keys for both Groq and Serper.dev

## Future Enhancements

- [ ] Multi-language support
- [ ] Custom agent creation
- [ ] Export reports to PDF/Word formats
- [ ] Historical analysis comparison
- [ ] Cost estimation features
- [ ] Competitor analysis dashboard
- [ ] Risk assessment module
- [ ] Database integration for report storage

## Contributing

Contributions are welcome! Please feel free to:
- Submit issues and feature requests
- Create pull requests for improvements
- Suggest enhancements to analysis quality

## License

This project is open source and available under the MIT License.

## Contact & Support

For questions or support, please reach out via GitHub issues.

## Disclaimer

This tool provides AI-generated insights for informational purposes. Users should conduct their own due diligence and consult with domain experts before making business decisions based on these analyses.

---

**Built with ❤️ using CrewAI and Streamlit**
