Spotify Data Cleaning and Analysis Project
Project Overview
This project entails the cleaning, preparation, and merging of two Spotify datasets to facilitate meaningful analysis of artist and song streaming performance. The primary objective is to structure and organize the data to enable accurate exploration, visualization, and potential predictive modeling. The process demonstrates practical proficiency in data handling using Python and pandas within a Jupyter Notebook environment.

Project Objectives
To clean and prepare two distinct Spotify datasets for analysis.

To extract and separate combined columns for clarity and consistency.

To standardize naming conventions and numerical formats across datasets.

To merge the datasets to allow both artist-level and song-level analysis.

To prepare the final dataset for visualization and potential machine learning applications.

Datasets Description
1. Spotify Artists Dataset
This dataset contains artist-level streaming statistics.

Key Features:

Artist: Name of the artist.

Total Streams: Total cumulative streams of the artist’s songs on Spotify. (Assumed to be expressed in millions of streams based on dataset scale.)

Daily: Average daily streams across all songs by the artist.

As lead: Streams where the artist is the primary performer.

Solo: Streams from the artist's solo tracks.

As feature: Streams from collaborations where the artist is featured.

2. Spotify Most Streamed Songs Dataset
This dataset provides information on individual songs and their streaming performance.

Key Features:

Artist and Title: A combined column listing both artist and song title, which was separated during the cleaning process.

Streams: Total streams for each individual song.

Daily: Average daily streams for each song.

Data Preparation Process
The following key steps were undertaken to prepare the datasets:

Data Loading:
Both datasets were successfully loaded into pandas DataFrames.

Data Cleaning:

Removed leading and trailing spaces from text fields.

Applied consistent casing for artist names to ensure accurate merging.

Separated the combined Artist and Title column using a safe splitting strategy (rsplit) to handle potential hyphens in artist names.

Column Renaming:
Renamed ambiguous columns to reflect their true meaning:

Total Streams → Total Artist Streams

Daily_x → Artist Daily Average Streams

Streams → Song Total Streams

Daily_y → Song Daily Average Streams

Data Type Standardization:

Converted string-formatted numerical columns to appropriate float types.

Adjusted stream figures, assuming that values were expressed in millions.

Dataset Merging:

Merged the datasets using the Artist column to integrate artist-level and song-level data.

Maintained the one-to-many relationship, allowing for artists with multiple songs to appear correctly.

Data Export:
The final, cleaned dataset was exported as final_spotify_dataset.csv.

Final Dataset Structure
The final dataset contains the following columns:

Column	Description
Artist	Name of the artist
Total Artist Streams	Total cumulative streams of all the artist’s songs
Artist Daily Average Streams	Average daily streams across all artist’s songs
As lead	Streams where the artist is the primary performer
Solo	Streams from the artist's solo tracks
As feature	Streams from collaborations where the artist is featured
Song Total Streams	Total streams of a specific song
Song Daily Average Streams	Average daily streams of the specific song
Title	Song title

Technologies Utilized
Python

pandas

Jupyter Notebook

Potential Future Work
Visualizing trends in artist and song streaming performance.

Predictive modeling to estimate future streaming growth.

Deeper analysis of collaborations and genre influence.

Interactive dashboards for real-time Spotify data tracking.

Author
Peter Waweru
Spotify Data Analysis Project
June 2025

