KING METROPOLITAN PORTAL — ANDROID APK BUILDER

THE EASIEST METHOD (NO ANDROID STUDIO ON YOUR PC)
This package uses GitHub Actions to build the APK online. You need a GitHub account and internet.

ONE-TIME SETUP
1. Extract this ZIP.
2. Open the extracted Android-APK folder.
3. Before uploading, you may change the portal URL in:
   app/src/main/java/com/kingmetropolitan/portal/MainActivity.java
   Find PORTAL_URL and replace the URL inside quotes. Keep https:// and the trailing slash.
4. Create a NEW PRIVATE GitHub repository.
5. Upload the CONTENTS of the extracted Android-APK folder into the repository root, including the .github folder. If .github is hidden, enable hidden files in File Explorer or upload the workflow file through GitHub's web interface.
6. Open the repository's Actions tab and enable Actions if asked.
7. Select “Build Android APK” on the left, click “Run workflow”, then click the green Run workflow button.
8. Wait for the workflow to finish successfully.
9. Open the completed workflow run, scroll to Artifacts, and download “king-metropolitan-portal-apk”.
10. Extract the downloaded artifact ZIP on your PC. Copy app-debug.apk to your Android phone and open it. If Android asks, allow installation from that file manager/browser.

CHANGE THE PORTAL ADDRESS LATER
Edit only the PORTAL_URL line in app/src/main/java/com/kingmetropolitan/portal/MainActivity.java, commit the change to GitHub, and run the workflow again.

IMPORTANT
- This ZIP builds an APK; it does not already contain a compiled APK.
- It is a debug APK for direct testing/install, not a Play Store release. Play Store publishing needs a signed release build and a protected signing key.
- The app needs internet and opens the live secure portal. Firebase authentication and server permissions still apply.
- Do not put private Firebase service-account keys or Cloudinary API secrets in the Android app.
