# 🎵 Spotify Top Tracks Analysis

## Project Overview

This project presents a comprehensive analysis of Spotify's top 50 tracks, exploring musical characteristics, artist popularity, and genre distributions. Through statistical analysis, we uncover patterns and relationships that help understand what makes songs popular on Spotify.

📓 **[View Full Analysis](spotify_analysis.ipynb)**

---

## Dataset

The dataset is publicly available on Kaggle: [Top 50 Spotify Tracks 2020](https://www.kaggle.com/atillacolak/top-50-spotify-tracks-2020)

It covers 50 tracks with 17 features each, including audio characteristics (energy, danceability, loudness, etc.), track metadata (artist, album, name), genre classifications, and duration.

---

## Data Preparation

- Verified no missing values or duplicates
- Converted duration from milliseconds to minutes for readability
- Applied Standard Deviation Method for outlier detection — outliers were **retained** as they represent meaningful artistic choices in music production

---

## Key Findings

**Artists**
- Billie Eilish and Travis Scott lead with 3 tracks each across 3 albums
- 40 unique artists represented in the top 50

**Genres**
- Hip-Hop and Pop dominate with 15 tracks each
- 22 unique genres represented, including niche genres like Chamber Pop and Nu-disco

**Audio Features**
- Strong positive correlation: Energy & Loudness (0.79)
- Strong negative correlation: Energy & Acousticness (-0.68)
- Hip-Hop/Rap favors louder, more danceable, less acoustic tracks
- Pop benefits from quieter, acoustic, danceable characteristics

---

## Data Structure

| Feature | Type | Description |
|---|---|---|
| artist, album, track_name, track_id, genre | Categorical | Track metadata |
| energy | Numerical | Intensity and activity level |
| danceability | Numerical | Suitability for dancing |
| loudness | Numerical | Overall loudness in dB |
| acousticness | Numerical | Measure of acoustic sound |
| speechiness | Numerical | Presence of spoken words |
| instrumentalness | Numerical | Predicts absence of vocals |
| liveness | Numerical | Presence of live performance elements |
| valence | Numerical | Musical positiveness |
| tempo | Numerical | Track tempo in BPM |
| duration_min | Numerical | Track length in minutes |

---

## Getting Started

1. Clone this repository
2. Install dependencies:
```bash
pip install pandas numpy
```
3. Download the dataset from [Kaggle](https://www.kaggle.com/atillacolak/top-50-spotify-tracks-2020) and place `spotifytoptracks.csv` in the project folder
4. Open `spotify_analysis.ipynb` in Jupyter Notebook
