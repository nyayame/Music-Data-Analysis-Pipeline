# Music Data Analysis Pipeline
### Disclaimer: This README/Documentation was made with the assistance of AI

## Overview
This project analyzes the evolution of music listening trends over time using Billboard Top 100 chart data. It focuses on how genre popularity and song tempo (BPM) have changed across multiple decades.

The system is designed as a data pipeline that ingests chart data, enriches it using external APIs, and processes it for analysis and visualization.

## Objectives
- Analyze how music genres have evolved over time
- Track changes in average song tempo (BPM) across decades
- Explore relationships between genre trends and listening behavior

## Data Sources
- Billboard Top 100 chart data (selected years and days across decades)
- MusicBrainz API (genre classification)
- AcousticBrainz API (tempo/BPM data)

## Pipeline Architecture

1. **Data Ingestion**
   - Extract artist and track data from Billboard charts
   - Fetch additional metadata using external APIs (MusicBrainz, AcousticBrainz)

2. **Data Processing**
   - Normalize genre labels (e.g., "Pop Rock" vs "Pop-Rock") using regex
   - Structure raw API responses into usable formats
   - Aggregate data by year and genre

3. **Analysis**
   - Identify top genres per decade
   - Compute average BPM trends over time
   - Compare genre evolution alongside tempo changes

4. **Visualization**
   - Heatmaps showing genre popularity over time
   - Line charts tracking BPM trends
   - Combined analysis of genre vs tempo evolution

## Key Findings
- Rock music peaked around the 1980s and declined in later decades
- Hip-hop, electronic, and country genres increased in popularity over time
- The 2010s featured higher average BPM, indicating faster-paced music trends
- Emergence and decline of genres can be observed clearly across decades

## Technical Implementation
- **Language:** Python  
- **Libraries:** Pandas, Regex, Requests (APIs), Matplotlib  
- **Design:** Object-Oriented Programming (Track and Processor classes)  
- **Data Types:** Structured and unstructured (API responses)  

## Challenges
- API calls introduced significant runtime (~80+ minutes for full dataset)
- Tradeoff between dataset size and processing time
- Required normalization of inconsistent genre labels
