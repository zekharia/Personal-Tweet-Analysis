# zekharia-Personal-Tweet-Analysis

Personal Tweet Analysis
In this project, we explore a personal Twitter archive with a focus on meaningful insights drawn from years of tweet history. This analysis provides a way to look back on your own social media habits, revealing patterns in emoji use, tweet frequency over time, and more subtle trends in how and when you’ve engaged with Twitter. By digging into tweet content, we can see how online behavior evolves over time and understand our own digital footprints better.

Table of Contents
Why Analyze Tweets?
How This Analysis Works
Key Insights Uncovered
Setup
License
Why Analyze Tweets?
Social media platforms capture bits of our thoughts, habits, and interactions over time. By analyzing these digital records, we can see when we were most active, how our tone and topics changed, and how emojis add personality to our online voice. This analysis provides insights into:

Activity Patterns: When you were most engaged on Twitter.
Emoji Trends: Which emojis you’ve used most often and how that changed over time.
Content Frequency: Peaks and lulls in tweeting activity, giving a visual reflection of engagement levels.
How This Analysis Works
The notebook guides you through loading, cleaning, and analyzing your Twitter archive data. Here’s a closer look at each step:

Loading and Preparing Data:

Using Twitter's .js export files, this analysis loads tweets, extracts the JSON data, and organizes it in a DataFrame.
Any excess formatting from Twitter's export is cleaned away, leaving just the tweet data.
We convert timestamps into readable dates and prepare text and emoji content for analysis.
Breaking Down the Content:

Emoji Extraction: Emojis are treated as an integral part of the analysis, offering insight into the tone and emotional coloring of tweets.
Text Patterns: The content is stripped of unnecessary symbols and structured to better understand recurring themes.
Visualizing Patterns Over Time:

A timeline visualization is created to show tweet frequency, revealing the highs and lows in engagement.
Separate visualizations highlight trends in emoji use, letting you see how your style of expression changed over time.
Key Insights Uncovered
With the data prepared and organized, the following analyses bring the archive to life:

Timeline Analysis:

Plotting tweet activity over time reveals trends such as periods of high engagement or lulls in activity. This can correlate with real-life events, busy periods, or changes in personal interest in the platform.
Emoji Trends:

By breaking down emojis used in tweets, this analysis finds which emojis you favored most and whether new emojis entered your rotation over the years. This adds a layer of personality to the analysis, showing how your mood or communication style has evolved.
Activity Patterns and Insights:

Interactive plots show tweet frequencies by month or year, allowing for a more granular look at your engagement patterns. Peaks might reflect periods when you were particularly active or inspired, while quieter periods could indicate shifts in focus or lifestyle changes.
Example Visualization
Below is an example of how a timeline visualization of tweet activity can look:

python
Copy code
import plotly.express as px

fig = px.histogram(df, x='created_at', title="Tweet Activity Over Time")
fig.show()
Setup
To recreate this analysis, the following packages are needed:

pandas: For handling and organizing data.
emoji: To support emoji extraction.
plotly: To visualize tweet activity interactively.
Install required packages with:

python
Copy code
!pip install emoji plotly
Place your Twitter .js files (e.g., tweets.js, tweets-part1.js) in the same directory as the notebook or specify their paths to load the data.

License
This project is open-source and available under the MIT License.

