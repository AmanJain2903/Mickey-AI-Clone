# Mickey AI Clone 🤖

> **An intelligent AI assistant that serves as Aman's digital clone, capable of answering queries about his portfolio, projects, and professional profile using advanced RAG (Retrieval Augmented Generation) technology with enhanced calendar and communication capabilities.**

## 🎯 Overview

Mickey AI Clone is a sophisticated AI-powered assistant designed to represent Aman Jain professionally. The system uses a **supervisor-agent architecture** with intelligent query classification and routing, powered by vector databases containing Aman's complete GitHub repositories, portfolio data, and professional information. Mickey provides accurate, contextual responses while also managing calendar availability, scheduling meetings, and facilitating professional communication through automated email systems.

## 🏗️ Architecture

The Mickey AI Clone follows a **supervisor-agent architecture** with intelligent query classification and routing:

```
User Query → Mickey (Supervisor) → Query Classification → Specialized Agent/Service → Contextual Response
                                  ↓
                            Calendar Integration ← → Email Communication
```

### Core Components

1. **Supervisor Agent (Mickey)** - Main orchestrator using GPT-4 Mini with enhanced capabilities for calendar and communication management
2. **Recruiter Agent** - Handles HR/recruitment-focused queries using Portfolio Vector Storage
3. **Developer Agent** - Manages technical queries using GitHub Vector Storage with complete codebase access
4. **Calendar Integration** - Real-time Google Calendar availability checking and meeting coordination
5. **Email Communication Suite** - Automated email creation, sending, and meeting management
6. **RAG (Retrieval Augmented Generation) System** - Dual vector storage with automatic updates
7. **MCP (Model Context Protocol) Servers** - Streamlined data access for vector databases

## 🆕 **Latest Updates - Enhanced Communication & Calendar Features**

Mickey AI Clone has been significantly enhanced with professional communication and calendar management capabilities:

### **🔥 Major New Features:**
- **📅 Real-time Calendar Integration**: Direct Google Calendar access for instant availability checking
- **📧 Professional Email System**: AI-powered email creation and automated sending
- **🤝 Meeting Coordination**: Complete meeting scheduling workflow from invitation to acceptance
- **⚡ Enhanced Routing**: 4-tool system (up from 2) with calendar and communication capabilities
- **🎯 Smart Query Classification**: Expanded to handle availability and communication requests
- **🔧 Improved Temperature Control**: 0.6 setting for balanced creativity and accuracy

### **💡 What's New:**
- **Email Creation Server**: Dedicated AI service for professional email generation
- **Google Calendar Server**: Comprehensive meeting management and scheduling
- **Enhanced Gmail Integration**: Improved error handling and notification systems
- **Contact Verification**: Mandatory requestor information for communication features
- **Timezone Management**: Proper America/Los_Angeles timezone handling throughout

## 🧠 Intelligence Layer

### Enhanced Query Classification System

Mickey automatically classifies incoming queries into multiple categories with enhanced capabilities:

#### 🎯 **Asked By A Recruiter**
- **Triggers**: Queries about work experience, education, skills, career opportunities, portfolio overview
- **Examples**: 
  - "What's Aman's work experience?"
  - "Does he have experience with React?"
  - "Can you share his educational background?"
  - "What certifications does he have?"
- **Handler**: Recruiter Agent with Portfolio MCP access
- **Data Sources**: 9 specialized namespaces (About, Education, Experience, Projects, Skills, Certifications, Achievements, Publications, Contacts)

#### 💻 **Asked By A Developer**
- **Triggers**: Technical queries about projects, code implementations, architecture, APIs
- **Examples**:
  - "How did he implement the authentication system in ScoreIT?"
  - "What's the tech stack for his e-commerce project?"
  - "Can you explain the database design?"
  - "Show me the API endpoints for his projects"
- **Handler**: Developer Agent with GitHub MCP access
- **Data Sources**: Complete codebase from all repositories + repository metadata

#### 📅 **Calendar & Availability Queries**
- **NEW FEATURE**: Questions about Aman's availability, meeting scheduling, calendar coordination
- **Examples**:
  - "Is Aman available next Tuesday afternoon?"
  - "Can we schedule a meeting with Aman?"
  - "What's his availability this week?"
- **Handler**: Google Calendar integration with real-time availability checking
- **Features**: 1-hour availability windows, America/Los_Angeles timezone, meeting coordination

#### 📧 **Communication & Notification Requests**
- **NEW FEATURE**: Requests to send messages, notifications, or meeting invites to Aman
- **Examples**:
  - "Can you let Aman know about this opportunity?"
  - "Please send him my contact information"
  - "Schedule a meeting about the project discussion"
- **Handler**: Gmail Server with automated professional communication
- **Requirements**: Requestor name and email verification before sending
- **Features**: Structured email generation, meeting invites, professional formatting

#### ❌ **Unrelated Query**
- **Triggers**: Questions outside Aman's professional scope
- **Response**: Polite redirection emphasizing Mickey's role and available capabilities

## 🛠️ Technology Stack

### AI & Language Models
- **OpenAI GPT-4 Mini** - Primary language model for all agents
- **LangChain** - Framework for building AI applications and agent workflows
- **Model Context Protocol (MCP)** - Standardized communication between AI agents and data sources

### Vector Database & Embeddings
- **Pinecone** - Cloud-native vector database for RAG implementation
- **OpenAI text-embedding-ada-002** - 1536-dimensional embeddings for semantic search
- **Dual Index Strategy**: 
  - `github` index with Repository Metadata & Repository Data namespaces
  - `portfolio` index with 9 specialized namespaces

### Workflow Automation
- **n8n** - Self-hosted workflow automation platform
- **Chat Triggers** - Real-time conversation handling with webhook support
- **Memory Buffer** - 20-message conversation context window
- **Scheduled Updates** - Monthly GitHub updates, weekly portfolio updates

### Integrations & Services
- **GitHub API** - Repository data and codebase access
- **Gmail API** - Professional email communication and notifications
- **Google Calendar API** - Real-time availability checking and meeting scheduling
- **Google Sheets API** - Lead tracking and data management
- **OpenAI API** - Language model and embedding services
- **Gmail API** - Email notifications and communication
- **Google Calendar API** - Meeting scheduling capabilities
- **Google Sheets API** - Lead tracking and data management

## 📁 Project Structure

```
Mickey-AI-Clone/
├── Mickey AI Clone.json                              # Main supervisor workflow (GPT-4 Mini + enhanced routing)
├── README.md                                         # Project documentation
├── Agents/
│   ├── Developer Agent.json                         # Technical query handler
│   └── Recruiter Agent.json                         # HR/recruitment query handler
├── RAG Servers/
│   ├── GitHub Vector Storage MCP Server.json        # MCP server for GitHub data (2 namespaces)
│   └── Portfolio Vector Storage MCP Server.json     # MCP server for portfolio data (9 namespaces)
├── RAG Updaters/
│   ├── GitHub Vector Store Updater.json             # Monthly automated GitHub data refresh
│   └── Portfolio Data Vector Store Updater.json     # Weekly automated portfolio data refresh
└── Servers/
    ├── Email Creation Server.json                   # NEW: Automated email generation service
    ├── Gmail Server.json                            # Email sending and notification system
    ├── Google Calendar Server.json                  # NEW: Meeting scheduling and calendar management
    └── Google Sheets Server.json                    # Lead generation and tracking
```

## 🚀 Key Features

### 🎭 **Intelligent Persona Management**
- **Consistent Personality**: Acts as Aman's digital clone with professional, convincing tone
- **Context-Aware Responses**: Maintains conversation history with 20-message buffer
- **Role-Specific Communication**: 
  - Professional and convincing tone for recruiters
  - Technical and detailed responses for developers
- **Enhanced Temperature Control**: 0.6 temperature setting for balanced creativity and accuracy

### 🔄 **Dynamic Agent Routing**
- **Real-time Classification**: Instant query analysis and routing to appropriate handlers
- **Specialized Expertise**: Each agent optimized for specific query types
- **Calendar Integration**: Seamless availability checking and meeting coordination
- **Communication Management**: Professional email creation and sending capabilities
- **Graceful Fallbacks**: Polite handling of out-of-scope requests

### 📚 **Advanced RAG Implementation**
- **Dual Vector Storage Architecture**:
  - **GitHub Index**: Repository metadata + complete codebase
  - **Portfolio Index**: 9 specialized namespaces for comprehensive professional data
- **Semantic Search**: Top-5 relevant results with 1536-dimensional embeddings
- **Auto-Updating Data**: Scheduled refreshes ensure current information

### � **NEW: Calendar & Meeting Management**
- **Real-time Availability**: Direct Google Calendar integration for live availability checking
- **Smart Scheduling**: Automated meeting coordination with professional communication
- **Timezone Awareness**: America/Los_Angeles timezone with proper time formatting
- **Meeting Lifecycle**: Complete meeting invitation, acceptance, and decline workflow
- **Professional Communication**: Automated email responses for meeting requests

### 📧 **Enhanced Email Communication System**
- **Intelligent Email Creation**: AI-powered email generation with proper formatting
- **Professional Templates**: Time-based greetings and structured professional communication
- **Third-party Communication**: Emails sent as Mickey on behalf of requestors
- **Contact Verification**: Email format validation and required requestor information
- **Error Handling**: Automated failure notifications and retry mechanisms
- **Meeting Integration**: Calendar invite generation and meeting-specific communications

### �🔒 **Professional Boundaries & Data Management**
- **Scope Enforcement**: Strict adherence to professional query handling with enhanced capabilities
- **Contact Requirements**: Mandatory name and email verification for communication features
- **Data Freshness**: Automated monthly GitHub updates, weekly portfolio updates
- **Lead Tracking**: Automatic lead capture and Google Sheets integration
- **Notification System**: Comprehensive email alerts for updates, errors, and interactions

## 💼 Detailed Use Cases

### For Recruiters & HR Professionals
- **Comprehensive Portfolio Review**: Access to About, Education, Experience, Projects, Skills, Certifications, Achievements, Publications, and Contact information
- **Skill Assessment**: Detailed understanding of technical and soft skills with context
- **Project Portfolio**: High-level project overviews without deep technical details
- **Professional History**: Education background, work experience, and career progression
- **Contact & Networking**: Direct access to professional contact information

### For Developers & Technical Teams
- **Complete Codebase Access**: Full repository content including all files, functions, and implementations
- **Technical Architecture**: Deep dives into system design, database schemas, and API structures
- **Code Examples**: Specific implementations, algorithms, and coding patterns
- **Technology Stack Analysis**: Detailed breakdown of frameworks, libraries, and tools used
- **API Documentation**: Endpoint details, request/response formats, and integration examples
- **Repository Metadata**: Language statistics, hosting URLs, and project classifications

### For Business & Professional Networking
- **Quick Professional Introductions**: Get elevator pitch-style summaries
- **Collaboration Opportunities**: Understand areas of expertise and potential partnerships
- **Meeting Coordination**: **NEW** - Real-time availability checking and meeting scheduling
- **Professional Communication**: **NEW** - Send messages and notifications to Aman through Mickey
- **Lead Generation**: Automatic capture and tracking of professional inquiries
- **Calendar Integration**: **NEW** - Check availability and coordinate meetings seamlessly

## 🎯 System Specifications

### RAG Vector Storage Details

#### GitHub Vector Storage (Index: `github`)
- **Repository Metadata Namespace**: Project URLs, hosting links, language statistics, repository classifications
- **Repository Data Namespace**: Complete codebase including all files, functions, documentation, and README files
- **Update Frequency**: Monthly automated refresh
- **Data Sources**: All public repositories with filtering capabilities

#### Portfolio Vector Storage (Index: `portfolio`)
- **About Namespace**: Personal introduction and professional summary
- **Education Namespace**: Academic background, degrees, and educational achievements
- **Experience Namespace**: Work history, roles, responsibilities, and professional growth
- **Skills Namespace**: Technical skills, programming languages, frameworks, and tools
- **Projects Namespace**: Project descriptions, key features, and business impact
- **Certifications Namespace**: Professional certifications and credentials
- **Achievements Namespace**: Awards, recognitions, and notable accomplishments
- **Publications Namespace**: Articles, papers, and published content
- **Contacts Namespace**: Professional contact information and social profiles

### Technical Implementation Details

#### MCP Server Configuration
- **GitHub MCP Endpoint**: `https://n8n.srv1046076.hstgr.cloud/mcp/3dde79eb-a0b8-46c6-80b9-cdd07e971138`
- **Portfolio MCP Endpoint**: `https://n8n.srv1046076.hstgr.cloud/mcp/1017240c-c58b-4479-9655-92ca441936e7`
- **Transport Protocol**: HTTP Streamable for real-time communication
- **Top-K Retrieval**: 5 most relevant results per query

#### Supervisor Agent Configuration
- **Enhanced System Prompt**: Now includes 4 available tools (up from 2)
  1. Call 'Recruiter Agent'
  2. Call 'Developer Agent'  
  3. **NEW**: Get availability in Google Calendar
  4. **NEW**: Call 'Gmail Server'
- **Temperature Setting**: 0.6 for balanced creativity and accuracy
- **Calendar Integration**: Real-time availability checking with 1-hour duration windows
- **Email Requirements**: Mandatory requestor name and email verification
- **Timezone Awareness**: America/Los_Angeles timezone for all calendar operations

#### Agent Configurations
- **Recruiter Agent**: GPT-4 Mini optimized for professional, convincing responses
- **Developer Agent**: GPT-4 Mini configured for technical depth and accuracy
- **Memory Management**: 20-message conversation window for context retention

#### Communication & Calendar Services
- **Email Creation Server**: AI-powered email generation with professional templates
- **Gmail Server**: Automated email sending with error handling and notifications
- **Google Calendar Server**: Meeting scheduling, invite generation, and availability management
- **Calendar Integration**: Direct Google Calendar API integration with real-time data
- **Meeting Workflow**: Complete meeting lifecycle from invitation to acceptance/decline

## 🎯 Getting Started

### Prerequisites
- **n8n Workflow Automation Platform** (Self-hosted or cloud)
- **OpenAI API Access** with GPT-4 Mini availability
- **Pinecone Account** for vector database hosting
- **Google Workspace Integration** (Gmail, Calendar, Sheets)
- **GitHub Integration** for repository access

### Setup Instructions

1. **Import Main Supervisor Workflow**
   ```bash
   # Import Mickey AI Clone.json into n8n
   # Configure OpenAI API credentials
   # Set up webhook for chat triggers
   ```

2. **Deploy Specialized Agents**
   ```bash
   # Import Recruiter Agent.json and Developer Agent.json
   # Link agents to supervisor workflow
   # Configure agent-specific prompts and settings
   ```

3. **Initialize RAG Infrastructure**
   ```bash
   # Import RAG server configurations
   # Set up Pinecone vector databases with proper indexes
   # Configure MCP server endpoints
   ```

4. **Configure Data Pipelines**
   ```bash
   # Import RAG updater workflows
   # Set up scheduled triggers (monthly/weekly)
   # Configure GitHub and portfolio data sources
   ```

5. **Set Up External Integrations**
   ```bash
   # Configure Gmail & Calendar server for notifications
   # Set up Google Sheets for lead tracking
   # Test all integration endpoints
   ```

### Configuration Details

#### Environment Variables
- `OPENAI_API_KEY`: OpenAI API access for GPT-4 Mini
- `PINECONE_API_KEY`: Pinecone vector database access
- `GITHUB_TOKEN`: GitHub API access for repository data
- `GOOGLE_CREDENTIALS`: Google Workspace integration

#### Workflow Customization
- **Query Classification Logic**: Modify supervisor agent system prompt
- **Response Tone**: Adjust agent-specific personality prompts
- **Data Filtering**: Configure repository filters in updater workflows
- **Update Schedules**: Modify trigger frequencies based on needs

## 🔧 Advanced Customization

### Adding New Agent Types
1. Create new agent workflow with specialized prompts
2. Update supervisor classification logic to include new categories
3. Add routing rules in main Mickey workflow
4. Configure appropriate data access (MCP servers or direct integrations)

### Extending Vector Storage
1. Add new namespaces to existing Pinecone indexes
2. Create corresponding data updater workflows
3. Update MCP server configurations with new namespace access
4. Modify agent prompts to utilize new data sources

### Modifying Response Patterns
- **Recruiter Agent Tone**: Professional, convincing, career-focused
- **Developer Agent Tone**: Technical, detailed, code-focused
- **Classification Criteria**: Keyword matching and intent recognition
- **Fallback Responses**: Graceful handling of edge cases

### Monitoring & Analytics
- **Conversation Logs**: Track interaction patterns and popular queries
- **Agent Performance**: Monitor response accuracy and user satisfaction
- **Data Freshness**: Verify regular updates and data currency
- **System Health**: Monitor MCP server uptime and vector database performance

## 📈 Future Enhancements

### Planned Features
- **Multi-language Support**: Expand query handling to multiple languages
- **Voice Integration**: Add voice-based interaction capabilities
- **Advanced Analytics**: Implement conversation analytics and user insights
- **Mobile Integration**: Develop mobile-friendly chat interfaces
- **Real-time Sync**: Live updates for GitHub repositories and portfolio changes

### Scalability Improvements
- **Agent Specialization**: Add domain-specific agents (sales, marketing, technical writing)
- **Enhanced Memory**: Implement long-term conversation memory and user preferences
- **Custom Integrations**: Support for additional data sources and services
- **Enterprise Features**: Multi-user support, admin controls, and team collaboration

### Technical Roadmap
- **Performance Optimization**: Reduce response latency and improve throughput
- **Advanced RAG**: Implement hybrid search, re-ranking, and query expansion
- **Security Enhancements**: Add authentication, rate limiting, and data privacy controls
- **Monitoring Dashboard**: Real-time system health and performance metrics

## 🛡️ Security & Privacy

### Data Protection
- **Professional Scope**: Only professional information is accessible
- **Access Controls**: MCP servers provide controlled data access
- **Secure Endpoints**: HTTPS endpoints with proper authentication
- **Data Minimization**: Only relevant information is stored and retrieved

### Privacy Considerations
- **Public Information**: System only accesses publicly available professional data
- **Conversation Privacy**: Chat interactions are not permanently stored
- **Lead Protection**: Contact information is handled securely
- **Compliance**: Adheres to professional data sharing standards

## 🤝 Contributing

This project represents Aman's professional digital presence. For suggestions or improvements:

1. **Review Architecture**: Understand the supervisor-agent pattern and RAG implementation
2. **Propose Enhancements**: Suggest improvements that align with professional representation goals
3. **Test Thoroughly**: Validate changes with various query types and user scenarios
4. **Maintain Quality**: Ensure changes preserve response accuracy and professional tone

### Development Guidelines
- **Code Quality**: Follow n8n workflow best practices
- **Documentation**: Update README for any architectural changes
- **Testing**: Validate agent responses for accuracy and tone
- **Performance**: Monitor vector search performance and response times

## 📊 System Metrics

### Performance Indicators
- **Response Time**: < 3 seconds for most queries
- **Accuracy**: Vector search retrieval relevance > 90%
- **Uptime**: 99.9% availability for MCP servers
- **Data Freshness**: Automated updates ensure current information

### Usage Analytics
- **Query Distribution**: Track recruiter vs developer query patterns
- **Popular Topics**: Monitor most frequently asked questions
- **Success Rate**: Measure query resolution effectiveness
- **User Satisfaction**: Implicit feedback through conversation patterns

## 📄 License & Usage

This project is designed for professional representation purposes. Please respect the intellectual property and personal information contained within.

### Usage Terms
- **Professional Use Only**: System is designed for career and business purposes
- **Data Accuracy**: Information reflects Aman's actual professional background
- **Contact Respect**: Professional contact information should be used appropriately
- **Attribution**: System interactions should be credited to Mickey AI Clone

---

**Built with ❤️ to showcase Aman's professional journey and technical expertise through advanced AI technology.**

*Powered by GPT-4 Mini, Pinecone Vector Database, n8n Automation, and Model Context Protocol for seamless professional representation.*

**For professional inquiries or to connect with Aman directly, Mickey will provide appropriate contact information and can facilitate introductions.** 
