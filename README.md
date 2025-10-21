# 🔍 Deep Research AI Agent

An intelligent research assistant that performs comprehensive web research and delivers results via email, powered by OpenAI Agents SDK.

## 🌟 Features

- **Multi-Agent Architecture**: Orchestrates specialized agents for planning, searching, writing, and email delivery
- **Automated Research**: Generates and executes 5 strategic web searches based on your query
- **Comprehensive Reports**: Produces detailed 1000+ word markdown reports with follow-up questions
- **Email Delivery**: Automatically sends formatted HTML reports to your inbox
- **Interactive UI**: Built with Gradio for easy deployment and usage

## 🏗️ Architecture

The system employs four specialized agents:

1. **Planner Agent**: Strategizes search queries to comprehensively answer your research question
2. **Search Agent**: Executes web searches and produces concise summaries
3. **Writer Agent**: Synthesizes findings into a cohesive, detailed report
4. **Email Agent**: Formats and delivers the final report via SendGrid

## 🚀 Live Demo

Try it out: [Deep Research AI on HuggingFace](https://huggingface.co/spaces/SkepticML/smart_deep_research)

## 📋 Prerequisites

- Python 3.8+
- OpenAI API key
- SendGrid API key
- Verified sender email address in SendGrid

## ⚙️ Setup

1. **Clone the repository**
```bash
   git clone https://github.com/sohrabsarabian/deep-research-agentic-ai.git
   cd deep-research-ai
```

2. **Install dependencies**
```bash
   pip install -r requirements.txt
```

3. **Configure environment variables**
   
   Create a `.env` file in the root directory:
```env
   OPENAI_API_KEY=your_openai_api_key_here
   SENDGRID_API_KEY=your_sendgrid_api_key_here
```

4. **Update email addresses**
   
   Edit `email_agent.py` and replace the email addresses with your verified SendGrid sender and recipient:
```python
   from_email = Email("your-verified-sender@example.com")
   to_email = To("recipient@example.com")
```

5. **Run the application**
```bash
   python deep_research.py
```

## 📁 Project Structure
```
.
├── deep_research.py      # Main Gradio interface
├── research_manager.py   # Orchestrates the research workflow
├── planner_agent.py      # Plans search strategies
├── search_agent.py       # Executes web searches
├── writer_agent.py       # Generates comprehensive reports
├── email_agent.py        # Handles email delivery
└── requirements.txt      # Python dependencies
```

## 🔧 Usage

1. Launch the application
2. Enter your research query in the text box
3. Click "Run" or press Enter
4. Monitor the research progress
5. Receive the detailed report in your email

## 📝 Notes

- Search results are summarized to 2-3 paragraphs each
- Final reports aim for 5-10 pages (1000+ words)
- Tracing is enabled via OpenAI platform for debugging

## 🤝 Contributing

Contributions are welcome! Feel free to open issues or submit pull requests.

## 📄 License

MIT License - feel free to use this project for your own purposes.

---

Built with ❤️ using OpenAI Agents SDK and Gradio
