# Agentic App Manager

**Target Platforms:** iOS, Android, Web  
**Tech Stack:** Flutter (Frontend), Firebase AI Logic & Vertex AI (Backend), Gemini API  

Agentic App Manager demonstrates how to build **agentic, multimodal apps** using Flutter and Firebase AI Logic with Gemini. The app integrates **voice, image, and text interactions**, enabling intelligent agents to interpret user feedback and act on it or generate detailed feedback reports.  

---

## Key Features  

- **Multimodal Feedback Handling:** Users can annotate screenshots, provide text feedback, or speak, and the agent interprets their input.  
- **Actionable Agents:** The agent can take actions like changing app colors, fonts, or suggesting confirmations based on available tools.  
- **Automated Feedback Reports:** Generates reports including device info, action history, and priority tags.  
- **Generative AI Integration:** Uses Gemini 2.0/2.5 for reasoning, function calling, and multimodal interactions.  
- **Cross-platform:** Runs on iOS, Android, and Web from a single Flutter codebase.  

---

## Architecture & Models  

| Model | Input | Output / Functionality |
|-------|-------|----------------------|
| **GenerativeModel** | Text + Images | Executes tool-based actions and responds to feedback |
| **ImagenModel** | Text | Generates images (e.g., profile pictures) |
| **LiveGenerativeModel** | Live Audio | Handles real-time audio input/output with tool actions |

- Flutter frontend communicates with Gemini via Vertex AI SDK.  
- Agents analyze feedback, decide actions, and interact with the app accordingly.  

---

## Screenshots  

See a visual overview of the app here: [Screenshots](./screenshots)

---

## Getting Started (Local Setup)  

**Prerequisites:**  
- Flutter SDK installed  
- Firebase account & project set up  
- Gemini API key from Vertex AI  

**Steps:**  

1. **Clone the repo:**  
```bash
git clone https://github.com/harini08k/multimodal_agentic_app.git
cd multimodal_agentic_app
````

2. **Configure Firebase:**

```bash
flutterfire configure
```

* Connect your project to Firebase for iOS, Android, and Web.

3. **Install dependencies:**

```bash
flutter pub get
```

4. **Run the app:**

```bash
flutter run -d <device-id>
```

* Replace `<device-id>` with your target device (`flutter devices` to list available devices).

**Tip:**

* `main.dart` → Feedback UI for user annotations and text.
* `main_audio_streaming.dart` → Real-time audio streaming version.

---

## How it Works

1. User provides feedback via text, screenshots, or voice.
2. Agent processes input using Gemini + Firebase AI Logic.
3. Agent decides if an action can be taken:

   * If yes → executes action (e.g., change color/font)
   * If confirmation is needed → asks user
   * If no tools are available → generates detailed feedback report

---

## Resources & References

* [Firebase AI Logic Docs](https://firebase.google.com/docs)
* [Vertex AI & Gemini Docs](https://cloud.google.com/vertex-ai)
* [Flutter Documentation](https://flutter.dev/docs)

---

## Contributing

Contributions are welcome! Please see [CONTRIBUTING.md](./CONTRIBUTING.md) for guidelines on how to contribute to this project.

---

## Notes

This project is a **demonstration of agentic app principles** using Flutter and Firebase AI Logic. It’s designed to be a starting point for exploring intelligent, multimodal interactions in cross-platform apps.
