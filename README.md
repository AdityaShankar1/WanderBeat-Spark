# 🚀 Vibe Voyage: Music-Based Travel Recommendation System:
This project is classifies the emotional "vibe" of a song using Machine Learning and recommends matching travel destinations. 

## 🗺️ Real-world use:

1. Deep Personalization Through Implicit Signals: Uses music preferences to infer emotional state and deliver personalized travel recommendations without forcing users through complex preference selections.
   This reduces choice fatigue while creating stronger emotional engagement and higher conversion rates.

2. Scalable Integration Model: Provides a modular framework for connecting with streaming platforms (Spotify, Gaana, JioSaavn) to build recommendation engines.
   This approach creates a competitive advantage through creative data integration without requiring complex API infrastructures.

3. Cross-Domain Application: Demonstrates how implicit behavioral data can drive personalization across industries—from travel and e-commerce to content platforms and lifestyle services.
   The core methodology transfers to any product requiring intelligent, user-centric recommendations.

## ✨ Project Features:
Vibe Classification: Uses a K-Nearest Neighbors (KNN) model, trained on 114,000 tracks, to classify music into Introspective, Mellow, Intense, or Jubilant.

Spotify Integration: The system architecture relies on the Spotify Web API to retrieve song audio features (e.g., valence, energy).

Note: Due to runtime restrictions, the final execution utilized a robust Fallback Mode relying on the local backup dataset.

Recommendation Engine: Queries a local SQLite database to find destinations pre-labeled with the predicted song Vibe.

Visualization: A scatter plot shows the 114k Vibe distribution, highlighting the user's predicted track within the Vibe space.

## 🗺️ Data Sources:

### Initially worked with Spotify API however due to API issues resorted to SQLite data

ML Training Data: Sourced from a large local CSV file (dataset.csv) containing 114,000 Spotify tracks and their audio features.

Travel Destinations: Sourced from a local CSV file (travel\_data.csv). This static file was loaded into the SQLite database.

Destinations like Rio and Ibiza, used in early tests, were hardcoded placeholders.

## ⚙️ Execution Flow:
Dependencies are installed (spotipy, scikit-learn, etc.).

KNN Model is trained on the 114k tracks and features are Scaled.

User Input (Song Title/Artist) is processed.

Fallback Mode activates, fetching the track's features from the local backup data.

Vibe is Predicted by the trained ML model.

SQLite Database is queried to match the predicted Vibe to a destination.

Final Recommendation and Visualization are displayed.

## 🎯 Example Results:
Input Song: "Malang (Title Track)" by Ved Sharma

Predicted Vibe: Jubiliant

Recommended Destinations: Rio, Ibiza
