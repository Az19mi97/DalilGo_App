# Project - DalilGo App

DalilGo is a mobile application developed with Flutter to provide fast and accurate identification of E-numbers in food products. The app enables users to search, scan, and analyze products with advanced image processing techniques, offering a seamless and informative experience for understanding ingredient data.

With DalilGo, users can not only identify E-numbers but also see whether each E-number is suitable for vegans or vegetarians. The app provides a detailed overview of each searched or detected E-number and offers a complete summary when multiple E-numbers are detected from a single image or via live scanning with the Smart Camera Overlay feature. This makes it easy to assess the overall suitability of a product at a glance.

- DalilGo is planned to be available only on Android devices.
  
---

## Note on Code Privacy

The source code for DalilGo is **private and not publicly accessible**. This repository/file is intended to provide information about the app, its features, and functionality only. The implementation details are not shared publicly to protect the integrity and security of the application.

---

## Technical Overview

DalilGo is structured with a modular architecture to ensure maintainability, scalability, and efficient asynchronous processing. The app leverages modern mobile technologies, including:

- **Flutter & Dart:** For cross-platform mobile development with high-performance UI rendering.
- **Firebase Firestore:** For cloud data storage and real-time timestamping of user messages.
- **Camera & Image Processing:** Integrates `camera` and `image_picker` packages for capturing product images.
- **OCR and Text Recognition:** For live text detection in the Smart Camera Overlay.
- **Custom UI:** Implements Google Fonts for consistent and appealing typography and Material design for intuitive user experience.

---

## Features

- **E-number Search:** Users can search the entire database of E-numbers with normalized results.
- **Image-Based Scanning:** Supports scanning of products via photos from the gallery or live camera feed.
- **Smart Camera Overlay (live):** Detects and highlights E-numbers in real-time while scanning products.
- **Detailed Results:** Displays each detected E-number with its origin, dietary suitability (vegan, vegetarian), and halal status.
- **Contact Form:** Sends structured messages through Firestore with proper validation, enabling secure user feedback collection.

---

## Software Architecture

The application is designed with a focus on modularity and performance:

- **State Management:** Managed with `StatefulWidgets` and local state for form handling, camera processing, and OCR results.
- **Asynchronous Processing:** Utilizes Dart `async/await` and `compute` for parallel image preprocessing and OCR analysis to ensure smooth UI performance.
- **Image Preprocessing Pipeline:** Implements grayscale conversion, contrast adjustment, resizing, and binarization for accurate text recognition.
- **OCR Post-Processing:** Normalizes scanned text to correct common OCR errors (e.g., misinterpreted characters like O → 0 or I → 1) for reliable E-number extraction.
- **Real-Time Detection:** Smart Camera Overlay polls frames every 500ms, performing lightweight text recognition and updating detected E-numbers dynamically.
- **Data Handling:** Maintains unique E-number detection sets to avoid duplicates and provides detailed structured objects (`ECode`) for each detected code.

---

## Technical Highlights

- **Flutter-Based UI:** Fully responsive and adaptive layout using `SingleChildScrollView`, `DropdownButtonFormField`, and `ElevatedButton` widgets.
- **OCR Optimization:** Generates multiple image variants for each scan to improve recognition accuracy.
- **Firebase Integration:** Firestore is used to persist contact messages, including email, category, title, description, and server-side timestamping.
- **Real-Time Updates:** Detected E-numbers are displayed in an overlay with clear visual cues and color-coded dietary/halal status.
- **Reusable Modules:** Core components like `ECode`, `ECodeLoader`, and image analysis functions are encapsulated for maintainability and potential future expansion.

---

## Development Notes

- Designed with a **focus on performance**: asynchronous processing ensures smooth UI during OCR scanning.
- Will be compatible with **Android devices**.
- Assets and configuration.

---

## Skills Demonstrated

This project showcases expertise in:

- Mobile application development with Flutter & Dart.
- Asynchronous and parallel processing for performance-sensitive tasks.
- Real-time camera integration and live image analysis.
- OCR preprocessing and post-processing for robust text recognition.
- Firebase Firestore integration for structured data storage.
- Modular code organization and maintainable software design.
- UI/UX implementation with custom fonts, overlays, and responsive design.

---

## Conclusion

DalilGo is a technically robust, user-friendly application designed to make food ingredient analysis accessible and reliable. The project demonstrates advanced skills in mobile development, image processing, OCR, and cloud integration, providing a clear example of professional software development practices and attention to performance, scalability, and usability.
