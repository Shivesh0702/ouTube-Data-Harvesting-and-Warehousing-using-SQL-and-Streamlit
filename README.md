1. Set Up the Streamlit App:

Create a basic Streamlit app structure.
Add input fields to collect the YouTube channel ID.
Add buttons for retrieving data and saving it to the database.
Display areas for output and data visualization.
2. Connect to the YouTube API:

Use the Google API client library for Python to authenticate and make requests to the YouTube Data API.
Implement functions to retrieve channel details (name, subscribers, total video count, etc.), playlists, and video information (likes, dislikes, comments).
3. Store and Clean Data:

Store the retrieved data temporarily using pandas DataFrames.
Clean and format the data as needed for consistency.
Ensure all relevant data (channel ID, channel name, video details) is captured.
4. Migrate Data to SQL Database:

Set up a MySQL or PostgreSQL database to act as a data warehouse.
Use SQLAlchemy or another ORM to connect to the database.
Create tables for channels, videos, and comments.
Implement a function that saves the cleaned DataFrames to the database.
5. Query the SQL Database:

Implement SQL queries that answer the required questions:
Video names and corresponding channels.
Channels with the most videos.
Top 10 most viewed videos and their channels.
Comments count per video.
Videos with the highest likes and their channels.
Total likes and dislikes per video.
Total views per channel.
Channels that published videos in 2022.
Average video duration per channel.
Videos with the highest comments and their channels.
6. Display Data in Streamlit:

Display the results of the SQL queries in tables.
Use Streamlit's data visualization features (e.g., st.bar_chart, st.line_chart) to create interactive charts and graphs based on the data.
Key Considerations:
Google API Quotas: Be aware of API call limits.
Data Storage: Consider normalization for database schema.
Error Handling: Implement error checks for invalid YouTube channel IDs and database connectivity issues.
Scalability: For larger datasets, consider batch processing or pagination for API requests.
