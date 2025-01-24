Here’s a detailed README file you can use for your project on GitHub:  

---

# **Subtitle Generation, Translation, and PDF Creation App**  

This project is an interactive web application built with **Streamlit** that transcribes audio from videos or MP3 files, generates subtitles, translates them into multiple languages, and allows users to download the results as PDF files. It leverages powerful libraries and tools such as **OpenAI's Whisper**, **MoviePy**, **FPDF**, and **Google Translate API** to deliver a seamless user experience.

---

## **Features**  

### 🔊 **Input Options**  
- Supports **MP4 video** and **MP3 audio** file formats.  
- Extracts audio from video files and processes it for transcription.  

### ✍️ **Subtitle Generation**  
- Utilizes **OpenAI's Whisper** model for accurate speech-to-text transcription.  
- Generates **time-aligned subtitles** with start and end timestamps for each segment.  

### 🌍 **Language Translation**  
- Allows users to translate subtitles into a wide range of languages, including:  
  - **English (en)**  
  - **Hindi (hi)**  
  - **Bengali (bn)**  
  - **Telugu (te)**  
  - **Tamil (ta)**  
  - **Malayalam (ml)**  
  - **Kannada (kn)**  
  - **Punjabi (pa)**  
  - **Marathi (mr)**  

### 📄 **PDF Export**  
- Saves subtitles in **two formats**:  
  1. **With Timestamps**: Each subtitle is displayed with its respective start and end time.  
  2. **Without Timestamps**: Subtitles are combined into a single paragraph.  
- Provides downloadable **PDFs** for both formats.  

### 📽️ **Interactive Interface**  
- Allows users to:  
  - Upload files directly through a drag-and-drop interface.  
  - Preview videos and audio files within the app.  
  - Select a preferred language for translation.  
  - Download generated subtitle files as PDFs.  

### 🛠️ **Error Handling & Optimization**  
- Ensures smooth handling of file uploads and temporary storage using **Python's `tempfile`**.  
- Optimized for performance by processing only when required (e.g., button clicks).  

---

## **Libraries and Technologies Used**  

### 1. **Streamlit**  
Streamlit is an open-source Python framework for creating interactive web applications. Key features used:  
- **`st.file_uploader`**: Enables users to upload MP4 or MP3 files.  
- **`st.video` and `st.audio`**: Previews uploaded media files.  
- **`st.download_button`**: Provides download options for generated PDFs.  

### 2. **OpenAI's Whisper**  
The **Whisper** speech-to-text model is used for transcribing audio files. Key methods:  
- **`whisper.load_model`**: Loads the Whisper model for transcription.  
- **`model.transcribe`**: Performs transcription and provides time-aligned segments.  

### 3. **MoviePy**  
The **MoviePy** library is used for audio extraction from video files.  
- **`VideoFileClip`**: Handles video files.  
- **`video.audio.write_audiofile`**: Converts the audio from videos into WAV files.  

### 4. **FPDF**  
The **FPDF** library is used for creating PDF files from generated subtitles.  
- **`pdf.add_page()`**: Adds new pages to the PDF.  
- **`pdf.cell()` and `pdf.multi_cell()`**: Handles text formatting within the PDF.  

### 5. **Google Translate API (`googletrans`)**  
The **`googletrans`** library is used for translating subtitles into multiple languages.  
- **`Translator`**: Translates text to a target language.  

### 6. **Tempfile**  
Python's **`tempfile`** module is used for managing temporary files during processing.  

---

## **How It Works**  

1. **File Upload**  
   - The user uploads an MP4 or MP3 file through the app's interface.  

2. **Audio Extraction** (for videos)  
   - If an MP4 video file is uploaded, the app extracts the audio and saves it as a WAV file for processing.  

3. **Subtitle Generation**  
   - The Whisper model transcribes the audio, generating time-aligned subtitles.  

4. **Translation**  
   - Users select a target language, and the subtitles are translated using Google Translate.  

5. **PDF Export**  
   - Users can download subtitles as PDFs in two formats: with or without timestamps.  

6. **Interactive Display**  
   - The app displays the video/audio, generated subtitles, and translation options in a user-friendly interface.  

---

## **Installation and Setup**  

### 1. **Prerequisites**  
Ensure you have the following installed:  
- **Python 3.8+**  
- **Pip**  

### 2. **Clone the Repository**  
```bash  
git clone https://github.com/your-username/subtitle-generator  
cd subtitle-generator  
```  

### 3. **Install Dependencies**  
```bash  
pip install -r requirements.txt  
```  

### 4. **Run the App**  
```bash  
streamlit run app.py  
```  

---

## **Project Structure**  

```plaintext  
subtitle-generator/  
├── app.py                 # Main Streamlit application  
├── requirements.txt       # List of dependencies  
├── README.md              # Project documentation  
```  

---

## **Screenshots**  

### 1. **Home Page**  
Provides an overview of the app's functionality.  

### 2. **File Upload Page**  
- Allows users to upload MP4 or MP3 files.  
- Displays the uploaded file (video or audio).  

### 3. **Subtitles and Translation**  
- Displays generated subtitles (with timestamps).  
- Shows translated subtitles in the selected language.  

### 4. **PDF Downloads**  
- Options to download subtitles in two formats (with or without timestamps).  

---

## **Future Enhancements**  

- **Additional Formats**: Support for more file types like AVI, MKV, etc.  
- **Custom Translations**: Allow users to manually edit translations before exporting.  
- **Improved Models**: Integration of more accurate transcription and translation models.  
- **Cloud Deployment**: Host the app on platforms like AWS, Heroku, or Streamlit Cloud.  

---

## **Contributing**  

Contributions are welcome!  
1. Fork the repository.  
2. Create a new branch: `git checkout -b feature-name`.  
3. Commit your changes: `git commit -m "Add feature"`.  
4. Push to the branch: `git push origin feature-name`.  
5. Submit a pull request.  


---

## **Contact**  

For any queries or suggestions, feel free to contact:  
**Jagadabi Yaswanth Abhishek Varma**  
- **GitHub**: [GitHub Profile]((https://github.com/AbhiVarma77))  
- **Email**: jagadabiabhivarma@gmai.com  

--- 

You can adjust the contact information, screenshots, or links to match your actual repository. Let me know if you'd like help with hosting the app or adding further enhancements!
