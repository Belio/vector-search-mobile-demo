# vector-search-mobile-demo

Kotlin demo for vector search on Android with Couchbase Lite for images classification

The demo consists of two different projects:
- Python project consisting in an API based on Alexnet to generate embeddings on images
- Android Application leveraging Couchbase Lite (https://docs.couchbase.com/couchbase-lite/current/android) and vector search extension on Mobile (https://docs.couchbase.com/couchbase-lite/current/android/working-with-vector-search.html)

Environment Setup:

1) Install the latest version of Android Studio from the official website.
Ensure you have the Java Development Kit (JDK) installed on your system.

2) Clone the Repository:

git clone [https://github.com/your-username/quiz-app-couchbase-lite.git
cd quiz-app-couchbase-lite

3) Open the Project:

Launch Android Studio.
Select "Open an Existing Project" and navigate to the cloned repository.
Configure Gradle:

Once the project is opened, Android Studio will automatically sync the Gradle files.
If prompted, update to the latest Gradle version.

4) Check Dependencies:

Open the app/build.gradle file.

Ensure the following dependencies are included:
```json
dependencies {
    implementation "org.jetbrains.kotlin:kotlin-stdlib:$kotlin_version"
    implementation "androidx.core:core-ktx:$core_ktx_version"
    implementation "androidx.appcompat:appcompat:$appcompat_version"
    implementation "com.couchbase.lite:couchbase-lite-android:$couchbase_lite_version"
    // Add other necessary dependencies
}
```

5) Prepare the Questions:

Verify that the questions.json file in the assets folder contains the quiz questions.
Make sure the JSON structure matches the expected format in the app.
6) Configure the Android Emulator:

In Android Studio, go to Tools > AVD Manager.
Create a new virtual device or use an existing one (preferably with API level 29 or higher).

7) Build the Project:

Click on Build > Make Project to compile the code.
Resolve any build errors that may occur.
Run the Application:

8) Before running the Android application, run the Python server separately.

Open another terminal window, and navigate to the python-server directory

cd python-server
The requirements.txt file in the python-server directory lists the necessary dependencies. Install them using pip:
pip install -r requirements.txt
The app.py file has the logic for the AlexNet model to generate embeddings for an image passed by the Kotlin app. Now run the app.
python app.py


Now let's head back to our Android app
Select the emulator or connect a physical Android device.
Click on the "Run" button (green play icon) in Android Studio.
Wait for the app to install and launch on the device.

9) Using the App:

When the app launches, you'll see the main screen.
Enter your username when prompted.
The app will likely ask for camera permissions for image recognition.
Take a photo or select an image to determine the quiz category.
Answer the quiz questions as they appear.
After completing the quiz, view your score and check the leaderboard.

10) Debugging:

If you encounter any issues, check the Logcat in Android Studio for error messages.

