# Face Recognition-Based Attendance System This project implements a face recognition-based attendance system using Python, OpenCV, Flask, and scikit-learn. It allows for registering new users, taking attendance, and managing user data.  
## Technologies Used 

* **Python:** Programming language 
* **Flask:** Web framework 
* **OpenCV:** Computer vision library (face detection, image processing) 
* **Scikit-learn:** Machine learning library (K-Nearest Neighbors for face recognition) 
* **Pandas:** Data manipulation and analysis 
* **Joblib:** Serialization for saving/loading the trained model 
* **HTML, CSS, JavaScript (implied):** Front-end technologies for the web interface 

## Project Structure 

``` FaceTrack-Attendance/ ├── app.py  # Main Flask application file ├── templates/ # HTML templates for the web interface │ ├── home.html │ └── listusers.html ├── static/ # Static files (CSS, JS, images, etc.) │ ├── faces/ # Folder to store user face images │ └── face_recognition_model.pkl # Trained model file └── Attendance/ # Folder to store attendance CSV files └── Attendance-{date}.csv ``` 

## Installation 
1. **Clone the repository:** `git clone ` 
2. **Create a virtual environment (recommended):** `python3 -m venv venv` 
3. **Activate the virtual environment:** `source venv/bin/activate` (Linux/macOS) or `venv\Scripts\activate` (Windows) 
4. **Install dependencies:** `pip install -r requirements.txt` (Create `requirements.txt` with the following: `opencv-python`, `flask`, `scikit-learn`, `pandas`, `joblib`) 
5. **Download Haar Cascade Classifier:** Download `haarcascade_frontalface_default.xml` from the OpenCV repository ([link to haarcascade download](https://github.com/opencv/opencv/blob/master/data/haarcascades/haarcascade_frontalface_default.xml)) and place it in the project's root directory. 

## Usage 
1. **Run the app:** `flask run` (or `python app.py` if you don't have the Flask CLI installed) 
2. **Access the web interface:** Open your browser and navigate to `http://127.0.0.1:5000/` (or the port specified by Flask). 
3. **Add Users:** Register new users via the web interface, providing their name and ID. The system will capture images from your webcam to train the model. 
4. **Take Attendance:** Use the attendance feature to capture and process images from your webcam, identifying registered users and recording their attendance in a CSV file. 
5. **Manage Users:** List and delete registered users. The model will automatically retrain after user deletion. ## Contributing Contributions are welcome! Please feel free to open an issue or submit a pull request. 
