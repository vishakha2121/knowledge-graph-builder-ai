# 🚀 AI Knowledge Graph Generator

> Transform unstructured enterprise documents into intelligent, queryable knowledge graphs using AI and GraphRAG

[![Python Version](https://img.shields.io/badge/python-3.9+-blue.svg)](https://www.python.org/downloads/)
[![Node Version](https://img.shields.io/badge/node-16+-green.svg)](https://nodejs.org/)
[![FastAPI](https://img.shields.io/badge/FastAPI-0.100+-teal.svg)](https://fastapi.tiangolo.com/)
[![React](https://img.shields.io/badge/React-18+-blue.svg)](https://reactjs.org/)
[![Neo4j](https://img.shields.io/badge/Neo4j-4.4+-yellow.svg)](https://neo4j.com/)
[![License](https://img.shields.io/badge/license-MIT-red.svg)](LICENSE)

---

## 📖 Table of Contents
- [Overview](#-overview)
- [Key Features](#-key-features)
- [Tech Stack](#-tech-stack)
- [Architecture](#-architecture)
- [Quick Start](#-quick-start)
- [Installation](#-installation)
- [Usage Guide](#-usage-guide)
- [API Documentation](#-api-documentation)
- [Project Structure](#-project-structure)
- [Contributing](#-contributing)
- [License](#-license)
- [Contact](#-contact)

---

## 🎯 Overview

The **AI Knowledge Graph Generator** is an intelligent document processing system that automatically converts unstructured enterprise documents into structured, evolving knowledge graphs. By combining the power of Google's Gemini AI, spaCy NLP, and Neo4j graph database, this system extracts meaningful entities, discovers hidden relationships, and enables powerful semantic querying.

### 🎨 What Makes This Special?
- **🧠 AI-Powered**: Uses Gemini API for intelligent entity extraction
- **🔗 GraphRAG Ready**: Built for Retrieval-Augmented Generation
- **💻 CPU Optimized**: No GPU required - runs on any laptop
- **📊 Beautiful UI**: Modern, responsive React interface
- **🗄️ Graph Database**: Neo4j for efficient relationship storage
- **🔍 Semantic Search**: Query in natural language

---

## ✨ Key Features

### 📄 Document Processing
- **Multi-format Support**: PDF, DOCX, TXT, and more
- **Smart Text Extraction**: Automatic content parsing
- **Batch Processing**: Handle multiple documents simultaneously
- **Progress Tracking**: Real-time processing status

### 🧠 Entity Extraction
- **AI-Powered Extraction**: Gemini API for high accuracy
- **NLP Integration**: spaCy for entity recognition
- **Entity Types**: People, Organizations, Locations, Concepts
- **Confidence Scoring**: Quality measurement for each entity

### 🔗 Relationship Discovery
- **Automated Detection**: Find connections between entities
- **Relationship Types**: Works for, Located in, Partnered with, etc.
- **Pattern Recognition**: Identify common relationship patterns
- **Confidence Metrics**: Score relationship accuracy

### 🌐 Graph Visualization
- **Interactive Graph**: Click, zoom, and explore
- **Node Details**: View entity information on click
- **Relationship Highlighting**: Visual connection paths
- **Export Options**: Download graph as JSON or image

### 💬 Semantic Querying
- **Natural Language**: Ask questions in plain English
- **Contextual Answers**: Response with graph context
- **Query History**: Save and reuse queries
- **Smart Suggestions**: Recommended queries based on graph

### 📊 Dashboard Analytics
- **Statistics**: Document count, entity count, relationship count
- **Recent Activity**: Latest processed documents
- **Graph Insights**: Key nodes and connections
- **Performance Metrics**: Processing time and accu


### Data Flow
1. **Upload** → Document uploaded via frontend
2. **Process** → Text extraction and preprocessing
3. **Extract** → Entity and relationship extraction using AI
4. **Build** → Graph construction in Neo4j
5. **Query** → Natural language query processing
6. **Visualize** → Interactive graph display

---

## 🚀 Quick Start

### Prerequisites
```bash
# Required Software
- Python 3.9+
- Node.js 16+
- Docker & Docker Compose (optional)
- Git

# Required Accounts
- Google Gemini API Key (free tier available)
- GitHub Account (for repository)

# Clone the repository
git clone https://github.com/vishakha2121/knowledge-graph-builder-ai.git
cd knowledge-graph-builder-ai

# Run with Docker Compose
docker-compose up -d

# Access the application
http://localhost:3000

# Backend Setup
cd backend
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
pip install -r requirements.txt

# Frontend Setup
cd ../frontend
npm install

# Environment Configuration
cp .env.example .env
# Edit .env with your API keys and database credentials

# Start Backend
cd ../backend
uvicorn main:app --reload --host 0.0.0.0 --port 8000

# Start Frontend (in new terminal)
cd frontend
npm run dev


git clone https://github.com/vishakha2121/knowledge-graph-builder-ai.git
cd knowledge-graph-builder-ai

cd backend
python -m venv venv

# Activate virtual environment
# On Windows:
venv\Scripts\activate
# On Mac/Linux:
source venv/bin/activate

# Install dependencies
pip install -r requirements.txt

# Download spaCy model
python -m spacy download en_core_web_sm

# Setup environment variables
cp .env.example .env
# Edit .env file with your credentials

# Install Neo4j Desktop or run via Docker
docker run -d --name neo4j -p 7474:7474 -p 7687:7687 \
  -e NEO4J_AUTH=neo4j/password123 neo4j:latest

# Install PostgreSQL (or via Docker)
docker run -d --name postgres -p 5432:5432 \
  -e POSTGRES_PASSWORD=postgres \
  -e POSTGRES_DB=knowledge_graph postgres:13

# Initialize databases
python scripts/init_db.py

cd ../frontend
npm install

# Setup environment
cp .env .env.example
# Edit .env file with API URL

# Start development server
npm run dev