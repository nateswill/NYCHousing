# NYC Housing Data Chatbot

## Project Overview

This project aims to build an intelligent chatbot that can answer questions about New York City housing data by querying official NYC Open Data tables. The system combines natural language processing with structured database queries to make complex housing information accessible through conversational interfaces.

## Current Status: Proof of Concept (Phase 1)

The initial phase establishes the foundational infrastructure for the complete chatbot system, including:

### Core Components

**1. Data Extraction Pipeline**
- Connects to NYC Open Data's Socrata API
- Retrieves housing data from the PLUTO dataset (Primary Land Use Tax Lot Output)
- Handles large-scale data extraction with pagination and type conversion

**2. Database Storage Layer**
- Stores extracted data in a PostgreSQL database
- Creates optimized table structures for efficient querying
- Maintains data integrity during load operations

**3. AI-Powered Query Interface**
- Implements an LLM-based chatbot using local models (Ollama)
- Translates natural language questions into database queries
- Provides conversational access to housing information

## Data Source: PLUTO Dataset

The system uses NYC's PLUTO dataset, which contains comprehensive property-level information including:

- Property identifiers and locations
- Building characteristics and dimensions
- Zoning classifications
- Ownership details
- Assessment values
- Geographic district assignments

## Workflow Architecture

```
NYC Open Data API → ETL Pipeline → PostgreSQL Database → LLM Chatbot → User Interface
     (Extract)          (Transform        (Store)           (Query &         (Response)
                       & Load)                        Answer)
```

### Process Flow

1. **Data Ingestion**: Automated extraction of housing records from NYC's official data portal
2. **Transformation**: Data cleaning, type conversion, and schema optimization
3. **Storage**: Loading processed data into a structured database for fast retrieval
4. **Query Processing**: Natural language questions converted to database queries via AI
5. **Response Generation**: Query results formatted as conversational answers

## Future Development Roadmap

### Phase 2: Enhanced Capabilities
- Multi-dataset integration (building permits, sales records, zoning changes)
- Advanced query understanding and context awareness
- Historical data analysis capabilities

### Phase 3: Production Features
- User authentication and personalized experiences
- Real-time data synchronization with NYC Open Data
- Performance optimization for large-scale deployments
- Web interface and API endpoints

### Phase 4: Advanced Analytics
- Predictive modeling and trend analysis
- Geographic visualizations and mapping integration
- Comparative analysis tools
- Automated insights generation

## Technical Approach (High-Level)

The system leverages modern AI technologies to bridge the gap between complex municipal data structures and everyday language. By combining reliable database infrastructure with cutting-edge natural language processing, users can explore NYC housing information without needing technical expertise in SQL or data systems.

## Getting Started

This repository contains:
- **ETL Scripts**: Data extraction and loading pipelines
- **Database Configuration**: PostgreSQL setup and schema definitions  
- **Chatbot POC**: Initial LLM integration for query translation

See individual notebook files for detailed implementation examples.

---

*Note: This is an open-source project focused on making NYC housing data more accessible to researchers, developers, and the general public.*
