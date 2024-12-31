### True\_live.ai

True\_live.ai is an innovative project designed to bring real-time analytics, machine learning insights, and advanced AI-driven functionalities into a unified platform. This repository provides a robust foundation for live data processing and AI-based decision-making across various applications.


<p align="center">
  <img src="images/Landing_page.jpg" alt="Landing Page" title="Landing Page Screenshot" width="750">
</p>



### Table of Contents

- [Features](#features)
- [Usage](#usage)
- [AI Pipeline for News Verfication](#AI Pipeline for News Verfication)
- [Installation](#installation)
- [Screenshots](#screenshots)
- [Contributing](#contributing)
- [License](#license)

---

### Features

- Verify Multimedia Content: Authenticate the credibility of video and audio files.
- Article Verification: Analyze and verify the authenticity of written articles.
- News Summarization: Generate concise summaries of news articles for quick insights.
- 
<p align="center">
  <img src="images/get_started.jpg" alt= "get_started" width="90%" />
</p>

### Usage
1. Select a video from your local device and upload it.
2. The model starts processing the video.
3. The results are provided with a claim status: verified or unverified.
4. The system provides a transcription of the news using ASR (Automatic Speech Recognition).

   ![Results](images/result.jpg "Results")
   
### AI Pipeline for News Verfication

1. **Extract Audio from Video**:
   The pipeline begins by extracting the audio track from the uploaded video file.

2. **Audio Sampling with Vosk ASR**:
   The extracted audio is then sampled according to the configuration of the Vosk Automatic Speech Recognition (ASR) system. Vosk processes the audio to convert speech into text.

   #### Vosk Model for ASR (Automatic Speech Recognition)
   - Model: [vosk-model-en-in-0.5](https://alphacephei.com/vosk/models/vosk-model-en-in-0.5.zip))

3. **Transcription for Claim Detection**:
   The transcribed text from Vosk ASR is passed to the claim detection model. This model analyzes the text to determine whether the news claim is **verified** or **unverified**.

   #### News Detection Model (BA-Claim/DistilBERT)
   - Model: [ba-claim/distilbert](https://huggingface.co/ba-claim/distilbert)

4. **Verification and Confidence Score**:
   Based on the claim detection model's analysis, the output is either **verified** or **unverified**, accompanied by a confidence score. The confidence score indicates how strongly the model believes in the accuracy of its prediction, helping assess the reliability of the news claim.





### Installation

Follow these steps to set up the project locally:

#### Clone the Repository

```bash
git clone https://github.com/svsaurav95/True_live.ai.git
cd True_live.ai
```

#### Set Up Virtual Environment

```bash
python -m venv env
source env/bin/activate   # On Windows, use `env\Scripts\activate`
```

#### Install Dependencies

```bash
pip install -r requirements.txt
```

#### Configure Environment Variables

Create a `.env` file and add necessary configurations:

```env
FLASK_APP=app.py
DATABASE_URL=<your_database_url>
SECRET_KEY=<your_secret_key>
```

#### Run the Application

```bash
flask run
```

#### Access the Application

Open your browser and navigate to `http://localhost:5000`.

### Usage
1. Select a video from your local device and upload it.
2. The model starts processing the video.
3. The results are provided with a claim status: verified or unverified.
4. The system provides a transcription of the news using ASR (Automatic Speech Recognition).

   ![Results](images/result.jpg "Results")


#### Uploading Data

- Navigate to the dashboard and upload your dataset.
- Supported formats: CSV, JSON.

#### Running AI Models

- Select a pre-trained model or upload your own.
- Configure model parameters and run predictions.

#### Live Analytics

- Visualize real-time data insights on the dashboard.
- Customize charts and reports.

#### Extending Pipelines

- Use the `pipelines/` directory to add new workflows.

### Screenshots

Add screenshots of your application below to showcase its features and user interface:

#### Dashboard Overview

```markdown
![Dashboard Overview](path/to/screenshot1.png)
```

#### Data Upload Interface

```markdown
![Data Upload Interface](path/to/screenshot2.png)
```

#### Analytics Visualization

```markdown
![Analytics Visualization](path/to/screenshot3.png)
```

### Contributing

Contributions are welcome! Follow these steps to contribute:

#### Fork the Repository

```bash
git clone https://github.com/svsaurav95/True_live.ai.git
```

#### Create a New Branch

```bash
git checkout -b feature-name
```

#### Commit Your Changes

```bash
git commit -m "Add new feature"
```

#### Push to Your Branch

```bash
git push origin feature-name
```

#### Open a Pull Request

Submit your pull request to the main repository.

### License

This project is licensed under the [MIT License](LICENSE).

---

### Author

Developed by **Team Digi Dynamos**. For inquiries, please contact [svsaurav95@gmail.com](mailto\:svsaurav95@gmail.com).

---

Happy coding!

### Script

#### Clone the Repository

```bash
git clone https://github.com/svsaurav95/True_live.ai.git
cd True_live.ai
```

#### Set Up Virtual Environment

```bash
python -m venv env
source env/bin/activate   # On Windows, use `env\Scripts\activate`
```

#### Install Dependencies

```bash
pip install -r requirements.txt
```

#### Configure Environment Variables

```bash
cat <<EOL > .env
FLASK_APP=app.py
DATABASE_URL=<your_database_url>
SECRET_KEY=<your_secret_key>
EOL
```

#### Run the Application

```bash
flask run
```

#### Access the Application

```markdown
Open your browser and navigate to:
[http://localhost:5000](http://localhost:5000)
```

