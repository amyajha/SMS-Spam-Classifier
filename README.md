# SMS-Spam-Classifier

<h2>Introduction:</h2><br>
<p>This project implements an SMS spam classifier using Natural Language Processing (NLP) and Machine Learning. It aims to accurately distinguish between spam and ham (non-spam) messages by analyzing patterns in SMS text data.</p><br>

<h2>Methodology:</h2><br>

<p><h3>1.	Data Collection and cleaning:</h3><br>
  
•	Dataset: SMS Spam Collection Dataset from Kaggle.<br>
•	Total Messages: 5,572 SMS entries with 5 columns.<br>
•	Cleaning Steps:  Removed irrelevant columns: Unnamed: 2, Unnamed: 3, Unnamed: 4<br>
•	Dropped 403 duplicate messages to ensure data quality.</p><br>


<p><h3>2. Data Exploration and Analysis:</h3><br>
  
• The dataset contained no null values, ensuring data integrity.<br>
•	Value counts of the target labels:<br>
&nbsp;&nbsp;&nbsp;&nbsp;  •	Ham: 87.37%<br>
&nbsp;&nbsp;&nbsp;&nbsp;  •	Spam: 12.63%<br>
•	This indicates a class imbalance, common in spam detection tasks.<br>
•	Histograms and box plots of message lengths revealed that:<br>
&nbsp;&nbsp;&nbsp;&nbsp;  •	Ham messages are generally shorter and less variable.<br>
&nbsp;&nbsp;&nbsp;&nbsp;  •	Spam messages tend to be longer and more skewed in length distribution.</p><br>


<p><h3>3. Data Preprocessing:</h3><br>
•	Lowercasing – Converted all text to lowercase to maintain consistency.<br>
•	Tokenization – Split messages into individual words (tokens).<br>
•	Removing Special Characters – Stripped out symbols, numbers, and unnecessary characters.<br>
•	Removing Stop Words and Punctuation – Eliminated common words (e.g., "the", "is") and punctuation that add little semantic value.<br>
•	Stemming – Reduced words to their root forms (e.g., "running" → "run") using a stemming algorithm.</p><br>


<p><h3>4.	Model Building:</h3><br>
•	TF-IDF (Term Frequency–Inverse Document Frequency) vectorization was applied to convert the cleaned text messages into numerical form.<br>
•	The dataset was split into training (80%) and testing (20%) sets.<br>
•	Different classifiers were trained and evaluated using various performance metrics.</p><br>

<p><h3>5. Conclusion:</h3><br>
Among all the models tested, Multinomial Naive Bayes achieved the best balance of performance metrics, with particularly high precision—a key requirement for spam detection to reduce false positives. Given its reliability and efficiency, Multinomial Naive Bayes was chosen as the final model for deployment.</p><br>
