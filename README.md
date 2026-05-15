# Mickey AI Clone 🤖

## NOW MIGRATED TO LANGGRAPH AND LANGCHAIN BASED AGENTIC FLOW.
## REFER TO THIS REPO FOR THE WORKFLOW. THE MIGRATION IS NOT OPEN-SOURCE.

> **An intelligent AI assistant that serves as Aman's digital clone, capable of answering queries about his portfolio, projects, and professional profile### 📅 **NEW: Calendar & - **🗞️ Professional Boundaries &### 📊 *### 🔒 **Professional Boundaries & Data Management**
- **Scope Enforcement**: Strict adherence to professional query handling with enhanced capabilities
- **Contact Requirements**: Mandatory name and email verification for communication features
- **Working Hours Validation**: Business hours enforcement (8AM-8PM PT) with appropriate messaging
- **Lead Privacy**: Transparent lead tracking without user disclosure while maintaining professional standards
- **Data Freshness**: Automated monthly GitHub updates, weekly portfolio updates
- **Lead Tracking**: Automatic lead capture and Google Sheets integration with intelligent contact validation
- **Notification System**: Comprehensive email alerts for updates, errors, interactions, and new leads
- **Meeting Data Security**: Secure handling of meeting details and attendee informationIntelligent Lead Management System**
- **Automated Lead Detection**: AI-powered identification of business opportunities and potential collaborations
- **Smart Contact Capture**: Intelligent extraction of contact details (name, email, phone, organization, designation)
- **Intent Analysis**: Automatic categorization of opportunity types (hiring, collaboration, partnership, client inquiry)
- **HTTP Webhook Architecture**: Streamlined lead processing through dedicated webhook endpoints
- **Google Sheets Integration**: Real-time lead tracking with automated data organization and duplicate prevention
- **Professional Notifications**: Email alerts for new leads, duplicate detection, and API errors with comprehensive contact information
- **Privacy-First Approach**: Operates transparently without disclosing lead tracking to users
- **Contact Validation**: Ensures minimum contact information before lead capture to maintain data qualityData Management**
- **Scope Enforcement**: Strict adherence to professional query handling with enhanced capabilities
- **Contact Requirements**: Mandatory name and email verification for communication features
- **Working Hours Validation**: Business hours enforcement (8AM-8PM PT) with appropriate messaging
- **Data Freshness**: Automated monthly GitHub updates, weekly portfolio updates
- **Lead Tracking**: Automatic lead capture and Google Sheets integration
- **Notification System**: Comprehensive email alerts for updates, errors, and interactions
- **Meeting Data Security**: Secure handling of meeting details and attendee informationg Management**
- **Real-time Availability**: Direct Google Calendar integration for live availability checking
- **Smart Scheduling**: Automated meeting coordination with professional communication
- **Timezone Awareness**: America/Los_Angeles timezone with proper time formatting
- **Meeting Lifecycle**: Complete meeting invitation, acceptance, and decline workflow
- **Professional Communication**: Automated email responses for meeting requests
- **Working Hours Compliance**: 8AM-8PM Pacific Time business hours enforcement
- **Meeting Data Handling**: Comprehensive support for meeting name, agenda, location, and attendee management
- **HTTP Webhook Integration**: Streamlined meeting request processing through webhook endpoints advanced RAG (Retrieval Augmented Generation) technology with enhanced calendar and communication capabilities.**

## 🎯 Overview

Mickey AI Clone is a sophisticated AI-powered assistant designed to represent Aman Jain professionally. The system uses a **supervisor-agent architecture** with intelligent query classification and routing, powered by vector databases containing Aman's complete GitHub repositories, portfolio data, and professional information. Mickey provides accurate, contextual responses while also managing calendar availability, scheduling meetings, facilitating professional communication through automated email systems, and intelligently filtering traffic with a specialized agent for handling unrelated queries and potential trolling attempts.

## 🏗️ Architecture

The Mickey AI Clone follows a **supervisor-agent architecture** with intelligent query classification and **webhook-based service integration**:

```
User Query → Mickey (Supervisor) → Query Classification → Specialized Agent/Service → Contextual Response
                ↓                                           ↓
    Webhook-Based Services ←─────────→ Multi-Model AI Fallbacks
                ↓                                           ↓
      Lead Detection System ←────────→ Google Sheets Integration
                ↓                                           ↓
         Error Handling ←─────────→ Comprehensive Notifications
```

### Core Components

1. **Supervisor Agent (Mickey)** - Main orchestrator using GPT-4 Mini with enhanced capabilities for calendar, communication, and intelligent lead management, featuring public webhook access and 7-tool integration
2. **Recruiter Agent** - Handles HR/recruitment-focused queries using Portfolio Vector Storage
3. **Developer Agent** - Manages technical queries using GitHub Vector Storage with complete codebase access
4. **Stalker Agent** - Intelligent traffic filter for unrelated queries and trolling attempts using xAI Grok with frank, assertive responses
5. **Webhook-Based Email System** - HTTP webhook email creation and sending with multi-model fallbacks
6. **Webhook-Based Calendar Service** - HTTP webhook meeting scheduling with complete lifecycle management
7. **Webhook-Based Lead Management** - HTTP webhook lead detection, capture, and Google Sheets integration with duplicate prevention
8. **Enhanced Error Handling** - Comprehensive error management with detailed email notifications across all services
9. **RAG (Retrieval Augmented Generation) System** - Dual vector storage with automatic updates via webhook triggers
10. **MCP (Model Context Protocol) Servers** - Streamlined data access for vector databases

## 🚀 Key Features

### 🧠 **7-Tool Intelligent Architecture**
Mickey operates as a sophisticated supervisor agent with **7 specialized tools**:

1. **🤝 Recruiter Agent** - Professional portfolio discussions, hiring conversations
2. **💻 Developer Agent** - Technical project details, code-related queries  
3. **� Email Creation Server** - Multi-model email drafting with fallback architecture
4. **� Gmail Server** - Webhook-based email sending with comprehensive delivery tracking
5. **📅 Google Calendar Server** - Meeting coordination with real-time availability validation
6. **📊 Google Sheets Server** - Lead management with advanced duplicate prevention and multi-model processing
7. **🛡️ Stalker Agent** - Traffic filtering and boundary enforcement with xAI Grok

### 🎯 **Enhanced Query Classification System**
Mickey intelligently routes conversations using **7-tier classification**:

- **Asked By A Recruiter** → Routes to Recruiter Agent (GPT-4 Mini)
- **Asked By A Developer** → Routes to Developer Agent (GPT-4 Mini)  
- **Calendar Request** → Routes to Google Calendar Server with webhook processing
- **Email Communication** → Routes to Email Creation + Gmail Server with multi-model fallbacks
- **Lead Detection** → Routes to Google Sheets Server (background operation with duplicate prevention)
- **Asked By A Stalker** → Routes to Stalker Agent (xAI Grok)
- **Unrelated Query** → Polite deflection with role reminder

### 🔄 **Multi-Model Fallback Architecture**
- **Primary Models**: Google Gemini 2.5 Flash, Gemini 2.0 Flash Lite (cost-free operation)
- **Fallback Models**: OpenAI GPT-4 Mini for reliability when rate limits are hit
- **Specialized Models**: xAI Grok for traffic filtering with high creativity
- **Auto-Recovery**: Automatic model switching ensures 99.9% uptime
- **Cost Optimization**: Prioritizes free models while maintaining quality

### 📧 **Enhanced Email Communication System**
- **Multi-Model Email Creation**: Primary Gemini models with GPT-4 Mini fallback
- **Webhook-Based Processing**: Real-time email generation and sending
- **Enhanced Error Handling**: Comprehensive failure notifications and recovery
- **Professional Templates**: Time-based greetings and structured communication
- **Contact Verification**: Email format validation and requestor information requirements

### 📊 **Advanced Lead Management System**  
- **Multi-Model Lead Processing**: Gemini 2.0 Flash with GPT-4 Mini fallback for reliability
- **Enhanced Duplicate Prevention**: Advanced contact validation using email and phone matching
- **Real-Time Google Sheets Integration**: Webhook-based lead capture with comprehensive error handling
- **Intelligent Contact Extraction**: AI-powered analysis of name, email, phone, organization, designation, and intent
- **Privacy-First Operations**: Transparent lead tracking without user disclosure
- **Comprehensive Notifications**: Success/failure alerts with detailed contact information

### 🔧 **Webhook-Based Service Architecture**
- **Real-Time Processing**: HTTP webhook endpoints for all major services
- **Enhanced Error Recovery**: Comprehensive error handling with detailed notifications
- **Service Independence**: Each service operates independently with fallback capabilities
- **Scalable Integration**: Easy addition of new services through webhook architecture
- **Monitoring & Alerts**: Detailed success/failure notifications across all operations

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
  - "Can we meet at 10 PM tonight?" (Working hours validation)
- **Handler**: Google Calendar integration with real-time availability checking
- **Features**: 1-hour availability windows, America/Los_Angeles timezone, meeting coordination, business hours enforcement (8AM-8PM PT)

#### � **NEW: Intelligent Lead Management**
- **NEW FEATURE**: Automatic lead detection and professional opportunity tracking
- **Examples**:
  - "I'm from Microsoft, we have an opening for a software engineer"
  - "Our startup is looking for a technical co-founder"
  - "We'd like to collaborate on a project"
  - "I represent a client interested in your expertise"
- **Handler**: Google Sheets Server with intelligent lead analysis and automated capture
- **Features**: Contact extraction (name, email, phone, organization, designation), intent analysis, smart prompting for missing information
- **Privacy**: Operates as private tool - users unaware of lead tracking functionality
- **Requirements**: Minimum contact information (email or phone) before lead capture
#### 📧 **Communication & Notification Requests**
- **NEW FEATURE**: Requests to send messages, notifications, or meeting invites to Aman
- **Examples**:
  - "Can you let Aman know about this opportunity?"
  - "Please send him my contact information"
  - "Schedule a meeting about the project discussion"
  - "Set up a call for tomorrow at 3 PM"
- **Handler**: Gmail Server with automated professional communication and HTTP webhook meeting scheduling
- **Requirements**: Requestor name and email verification before sending
- **Features**: Structured email generation, meeting invites, professional formatting, working hours validation

#### ❌ **Asked By A Stalker (Unrelated/Trolling)**
- **Triggers**: Questions outside Aman's professional scope, trolling attempts, idle or intrusive behavior
- **Handler**: Stalker Agent with xAI Grok using frank, assertive, and sarcastic responses
- **Response Style**: Blunt, direct, short punchy sentences designed to deter inappropriate usage
- **Features**: High creativity temperature (1.2), safety-constrained frankness, traffic filtering

## 🛠️ Technology Stack

### AI & Language Models
- **OpenAI GPT-4 Mini** - Primary language model for supervisor and professional agents with fallback support
- **Google Gemini 2.5 Flash** - High-performance language model for email creation and communication tasks
- **Google Gemini 2.0 Flash Lite** - Lightweight model for structured output parsing and lead generation
- **xAI Grok** - High-creativity language model for Stalker Agent with frank response capabilities
- **LangChain** - Framework for building AI applications and agent workflows with multi-model support

### Multi-Model Fallback Architecture
- **Primary Models**: Google Gemini 2.5 Flash (250 RPD), Gemini 2.0 Flash Lite (200 RPD) - Cost-free operation
- **Fallback Models**: OpenAI GPT-4 Mini ($0.40 input, $1.60 output) - No daily limits for reliability
- **Specialized Models**: xAI Grok for traffic filtering with high creativity settings
- **Auto-Fallback System**: Automatic model switching on rate limits or failures

### Vector Database & Embeddings
- **Pinecone** - Cloud-native vector database for RAG implementation with dual-index strategy
- **OpenAI text-embedding-3-small** - Cost-optimized embeddings ($0.02/1M tokens) for semantic search
- **Dual Index Strategy**: 
  - `github` index with Repository Metadata & Repository Data namespaces
  - `portfolio` index with 9 specialized namespaces

### Workflow Automation & Integration
- **n8n** - Self-hosted workflow automation platform with webhook-based architecture
- **HTTP Webhooks** - Real-time conversation handling and service integration
- **Memory Buffer** - 20-message conversation context window
- **Scheduled Updates** - Webhook-triggered GitHub updates, portfolio updates

### External Services & APIs
- **GitHub API** - Repository data and codebase access with automated updates
- **Gmail API** - Professional email communication with enhanced error handling
- **Google Calendar API** - Real-time availability checking and meeting scheduling
- **Google Sheets API** - Intelligent lead tracking with duplicate prevention and contact validation
- **Pinecone API** - Vector database operations and semantic search with auto-scaling

## 📁 Project Structure

```
Mickey-AI-Clone/
├── Mickey AI Clone.json                              # Enhanced supervisor workflow with 7-tool system and intelligent lead management
├── README.md                                         # Project documentation
├── Agents/
│   ├── Developer Agent.json                         # Technical query handler with GitHub integration
│   ├── Recruiter Agent.json                         # HR/recruitment query handler with portfolio access
│   └── Stalker Agent.json                           # Traffic filtering and trolling prevention handler
├── RAG Servers/
│   ├── GitHub Vector Storage MCP Server.json        # MCP server for GitHub data (2 namespaces)
│   └── Portfolio Vector Storage MCP Server.json     # MCP server for portfolio data (9 namespaces)
├── RAG Updaters/
│   ├── GitHub Vector Store Updater.json             # Webhook-triggered GitHub data refresh
│   └── Portfolio Data Vector Store Updater.json     # Webhook-triggered portfolio data refresh
├── Servers/
│   ├── Gmail Server.json                            # Webhook-based email sending with enhanced error handling
│   ├── Google Calendar Server.json                  # Webhook-based meeting scheduling and calendar management
│   └── Google Sheets Server.json                    # Webhook-based intelligent lead management with multi-model fallbacks
└── Tools/
    └── Email Creation Server.json                   # Multi-model email generation with fallback architecture
```

## 🚀 Key Features

### 🎭 **Intelligent Persona Management**
- **Consistent Personality**: Acts as Aman's digital clone with professional, convincing tone
- **Context-Aware Responses**: Maintains conversation history with 20-message buffer
- **Public Accessibility**: Available through public webhook for real-time interactions
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
- **Intelligent Email Creation**: AI-powered email generation with proper formatting and meeting context
- **Professional Templates**: Time-based greetings and structured professional communication
- **Third-party Communication**: Emails sent as Mickey on behalf of requestors
- **Meeting Integration**: Complete meeting information inclusion in email communications
- **Contact Verification**: Email format validation and required requestor information
- **Error Handling**: Automated failure notifications and retry mechanisms
- **Meeting Coordination**: Calendar invite generation and meeting-specific communications
- **Business Hours Awareness**: Working hours validation and appropriate messaging

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
- **Meeting Coordination**: **Enhanced** - Real-time availability checking with business hours enforcement
- **Professional Communication**: **Enhanced** - HTTP webhook-based messaging and notifications
- **Lead Generation**: **Enhanced** - Intelligent lead detection with automated Google Sheets tracking
- **Calendar Integration**: **Enhanced** - Complete meeting scheduling lifecycle with professional communications
- **Working Hours Intelligence**: **NEW** - Business hours validation and appropriate messaging
- **Opportunity Tracking**: **NEW** - Transparent lead identification and professional contact management

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
- **Enhanced System Prompt**: Now includes 7 available tools with complete communication, lead management, and traffic filtering suite
  1. Call 'Recruiter Agent'
  2. Call 'Developer Agent'  
  3. **Call 'Stalker Agent'** - Traffic filtering and trolling prevention
  4. **Get availability in Google Calendar** - Real-time calendar checking
  5. **Call 'Gmail Server'** - Professional email communication
  6. **Call 'Google Calendar Server'** - Meeting scheduling and coordination
  7. **Call 'Google Sheets Server'** - Intelligent lead management (private tool operation)
- **Temperature Setting**: 0.6 for balanced creativity and accuracy
- **Calendar Integration**: Real-time availability checking with 1-hour duration windows
- **Meeting Scheduling**: Complete meeting invite and scheduling workflow
- **Lead Management**: Intelligent lead detection with automated Google Sheets integration
- **Email Requirements**: Mandatory requestor name and email verification
- **Timezone Awareness**: America/Los_Angeles timezone for all calendar operations
- **Working Hours**: 8AM to 8PM Pacific Time enforcement
- **Private Operations**: Background lead tracking without user disclosure

#### Agent Configurations
- **Recruiter Agent**: GPT-4 Mini optimized for professional, convincing responses
- **Developer Agent**: GPT-4 Mini configured for technical depth and accuracy
- **Stalker Agent**: xAI Grok with high creativity (temperature 1.2) for frank, assertive traffic filtering
- **Memory Management**: 20-message conversation window for context retention

#### Communication & Calendar Services
- **Email Creation Server**: AI-powered email generation with professional templates and meeting support
- **Gmail Server**: Automated email sending with error handling and notifications
- **Google Calendar Server**: HTTP webhook-based meeting scheduling with complete lifecycle management
- **Google Sheets Server**: HTTP webhook-based intelligent lead management with automated contact capture and duplicate prevention
- **Calendar Integration**: Direct Google Calendar API integration with real-time data
- **Meeting Workflow**: Complete meeting lifecycle from invitation to acceptance/decline with automated communications
- **Lead Management**: Intelligent opportunity detection with structured data extraction, duplicate prevention, and privacy-first operations
- **Working Hours Enforcement**: Business hours validation (8AM-8PM Pacific Time)
- **Meeting Data Management**: Comprehensive handling of meeting details (name, agenda, time, location, attendees)

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
   # Import Recruiter Agent.json, Developer Agent.json, and Stalker Agent.json
   # Link agents to supervisor workflow
   # Configure agent-specific prompts and settings
   # Set up xAI Grok credentials for Stalker Agent
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
- **Stalker Agent Tone**: Frank, assertive, sarcastic for traffic filtering
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
