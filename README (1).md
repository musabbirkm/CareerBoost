---
license: other
title: CareerBoost
sdk: streamlit
emoji: 📈
colorFrom: blue
colorTo: purple
pinned: true
short_description: AI-powered, futuristic, and career-accelerating
---
# CareerBoost: Your Job Search & Prep Companion

**Empowering Your Career Journey with AI-Driven Tools**

**Creator**: Musabbir KM

---

## Overview

CareerBoost is an AI-powered web application designed to assist job seekers in finding job opportunities, preparing for interviews, and creating professional CVs. Built with a focus on usability and efficiency, it leverages advanced AI agents to deliver tailored results for users worldwide, with a special emphasis on the Indian job market.

---

## Features

CareerBoost offers four core functionalities, each powered by specialized AI agents:

1. **Job Finding Agent**:
   - Scrapes job listings from major job boards like Naukri.com, Shine.com, LinkedIn, and Indeed.
   - Supports location-based searches (e.g., "data science in Kochi").
   - Displays detailed job information: title, company, location, link, and source.
   - Falls back to web search for additional links if scraping fails.

2. **RapidAPI Job Search**:
   - Fetches structured job listings using the RapidAPI JSearch endpoint.
   - Allows filtering by job title, location, and country code (default: India).
   - Provides clean, reliable job data with minimal latency.

3. **Interview Preparation**:
   - Generates 10 tailored interview questions and answers for a specified job field (4 technical, 3 behavioral, 3 situational).
   - Incorporates trends from 2022–2025, covering skills like machine learning, data visualization, and ethical AI.
   - Delivers plain-text output for easy review.

4. **CV Creator**:
   - Builds ATS-friendly CVs based on user-provided job field and experience.
   - Includes sections for Summary, Skills, Experience, and Education.
   - Uses a standardized format optimized for job applications.

---

## Technologies Used

CareerBoost is built with a robust tech stack to ensure performance and scalability:

- **Frontend**:
  - [Streamlit](https://streamlit.io/) (v1.29.0): For the interactive web interface.
  - Custom CSS: For enhanced UI styling (tabs, cards, logo display).

- **Backend & AI**:
  - [LangChain](https://python.langchain.com/) (v0.2.16): For agent orchestration and tool integration.
  - [Google Gemini LLM](https://cloud.google.com/vertex-ai/docs/generative-ai/model-reference/gemini) (via langchain-google-genai v1.0.8): Powers natural language processing and generation.
  - [DuckDuckGo Search](https://github.com/deedy5/duckduckgo_search) (v6.2.11): For fallback web searches.
  - [RapidAPI JSearch](https://rapidapi.com/letscrape-6bRBaM6guO5/api/jsearch): For structured job data.
  - [aiohttp](https://docs.aiohttp.org/) (v3.10.5): For asynchronous web scraping.
  - [Selectolax](https://github.com/rushter/selectolax) (v0.3.21): For efficient HTML parsing.
  - [Tenacity](https://github.com/jd/tenacity) (v8.5.0): For retry logic in scraping.
  - [python-dotenv](https://github.com/theskumar/python-dotenv) (v1.0.1): For environment variable management.

---

## Agent Info

CareerBoost leverages four specialized AI agents, each designed for a specific task:

- **Job Finding Agent**:
  - Uses a ReAct (Reasoning + Acting) framework to scrape job boards asynchronously.
  - Handles errors like rate limits and timeouts with retries and randomized delays.
  - Formats output as a numbered list for clarity.

- **RapidAPI Job Search Agent**:
  - Queries the JSearch API for structured job data.
  - Processes results into a consistent format (title, company, location, link, source).

- **Interview Preparation Agent**:
  - Generates 10 questions and answers using the Google Gemini LLM.
  - Integrates web search insights to reflect recent trends (e.g., cloud computing, ethical AI).
  - Fixed to prevent iteration limit errors by enforcing strict tool usage.

- **CV Creator Agent**:
  - Generates ATS-friendly CVs with a single LLM call.
  - Customizes content based on user input, ensuring relevance to the job field.

---

## Installation and Setup

To run CareerBoost locally or deploy it to Hugging Face Spaces, follow these steps:

### Prerequisites
- Python 3.9+
- Git
- Hugging Face account (for deployment)
- API keys:
  - [Google API Key](https://cloud.google.com/docs/authentication/api-keys) for Gemini LLM
  - [RapidAPI Key](https://rapidapi.com/letscrape-6bRBaM6guO5/api/jsearch) for JSearch

