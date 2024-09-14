# News Aggregator Application

This is a news aggregator application that fetches and displays the latest news articles from various categories and countries, allowing users to search and filter results dynamically.

## Project Overview

This project integrates with the **GNews API** to retrieve news articles. Users can search for specific news, filter by category and country, and navigate through multiple pages of results using pagination.

### Key Features:
- Search news by keywords.
- Filter by categories (e.g., Business, Sports, Technology).
- Filter by country (e.g., USA, UK, India).
- Pagination to browse through multiple pages of results.

## Project Setup Instructions

### 1. Backend Setup

The backend is built using **Node.js** and **Express**, and it fetches data from the GNews API.

 
### Approach
**Backend:**
The backend serves as an API to fetch news data from the GNews API. It processes parameters like search queries, categories, and countries, and returns the filtered results to the frontend.
Axios is used to make HTTP requests to the GNews API, and the API key is securely stored in an environment variable.
**Frontend:**
The frontend provides a user interface where users can search for news, filter by category and country, and browse through results using pagination.
It uses Axios to call the backend API and display the results in a grid layout.
The UI includes filters for selecting news categories (e.g., business, sports) and country-specific news.


#### Challenges Faced and Solutions
**1. Handling GNews API Rate Limits**
*Challenge:* While testing, the GNews API would occasionally return a 403 Forbidden error, indicating rate limits or API key issues.
*Solution:* Added error handling for the API responses and made sure the API key was correctly configured in the environment variables. If the API request fails, the user sees an error message on the frontend, informing them of the issue.

**2. Pagination Handling**
*Challenge:* The API initially returned large sets of data, and paginating through these results while maintaining the search and filter states was tricky.
*Solution:* Implemented pagination on both the backend and frontend, ensuring that the current page, search query, and filters were sent to the backend API correctly, and only the relevant data was returned.

**3. Maintaining Search and Filter State Across Pages**
*Challenge:*  Ensuring that user-selected filters (category, country) and search queries persisted across page navigations.
*Solution:* Used React state to manage the search and filter inputs, and passed them as query parameters to the backend. This ensured the data remained consistent across paginated pages.

### Links
**Firebase Hosted Project:** https://acowale-1d56b.web.app/
**GitHub Repository:**  https://github.com/Prajjwalajit15/accowale