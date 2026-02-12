![2ff5499e-0bf8-4ffc-b205-e496aca01204-5fe397b4e68ca](https://github.com/user-attachments/assets/cd7083a7-3c72-4a09-af5b-c2a33ce17ef2)

YouTube Trends: Project of Foundations Of Computer Science

The repository contains an analysis of YouTube Trends of 10 countries conducted through the use of Python.

For more details, the pojects consisted in:
1. Creating a single dataframe with the concatenation of all input csv files, adding a column called country
2. Extracingt all videos that have no tag.
3. For each channel, determining the total number of views
4. Saving all rows with disabled comments and disabled ratings, or that have video_error_or_removed in a new dataframe called excluded, and remove those rows from the original dataframe.
5. Adding a like_ratio column storing the ratio between the number of likes and of dislikes
6. Clustering the publish time into 10-minute intervals (e.g. from 02:20 to 02:30)
7. For each interval, determining the number of videos, average number of likes and of dislikes.
8. For each tag, determining the number of videos
9. Finding the tags with the largest number of videos
10. For each (tag, country) pair, computing average ratio likes/dislikes
11. For each (trending_date, country) pair, the video with the largest number of views
12. Dividing trending_date into three columns: year, month, day
13. For each (month, country) pair, finding the video with the largest number of views
14. Reading all json files with the video categories
15. For each country, determining how many videos have a category that is not assignable.
