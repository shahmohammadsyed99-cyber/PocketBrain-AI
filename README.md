# PocketBrain AI — repaired starter project

This is a repaired **starter project**, not yet a complete offline AI app.

## Repairs made
- Added the missing Gradle version catalog used by the root build file.
- Added a basic Android memory manager required by the Kotlin code.
- Added missing app-name and theme resources; removed references to absent launcher icons.
- Updated GitHub Actions to install Gradle, because the original ZIP does not include the Gradle wrapper JAR.

## Important offline-AI limitation
The project calls native methods in `LlamaCppEngine` and attempts to load `pocketbrain_engine`, but this ZIP does **not** include the llama.cpp native implementation or its Android build configuration. Therefore, a successful APK build does not mean model inference works. The app still needs a real, compatible inference engine and model-loading integration before it can answer questions offline. Do not advertise or distribute it as a working offline chatbot yet.

## Build using an Android phone
1. Extract this ZIP using an Android archive/file-manager app.
2. Upload the contents of the `PocketBrainAI` folder to a new GitHub repository (the `.github` folder must be included).
3. Open the repository's **Actions** tab and enable workflows if GitHub asks.
4. Choose **Build PocketBrain AI Android APK** → **Run workflow**.
5. When the run finishes successfully, open it and download the `PocketBrain-AI-Release-APK` artifact.
6. Extract the artifact ZIP and install the APK. Only install builds you trust.

The first build may fail for additional source/dependency issues; review the Actions log if it does.
