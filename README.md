# Cosmic Data Visualizer (3D Interactive)

##LINK:https://abdallla142.github.io/Cosmic-Data-Visualizer/


## Overview

The **Cosmic Data Visualizer** is an immersive and interactive web application designed to bring the wonders of space directly to your browser. It transforms real-time and simulated astronomical data into a dynamic 3D environment, allowing users to explore a vibrant Earth, track orbiting objects, and interact with an AI assistant to learn more about the cosmos.

This project aims to provide an engaging and educational experience, blending scientific data with captivating visual art.

## Features

* **Interactive 3D Earth:** A detailed 3D model of Earth with a realistic texture and atmospheric glow. Users can rotate and zoom the scene using mouse controls.

* **Live ISS Tracking:** The International Space Station is accurately represented as a detailed 3D model, continuously orbiting Earth based on live data (latitude and longitude). Its recent trajectory is visualized with a dynamic, fading trail.

* **Dynamic Orbiting Satellites:** Multiple generic 3D satellite models, designed with more realistic bodies and solar panels, orbit Earth, adding to the visual depth of low Earth orbit. These satellites have varied orbital speeds and inclinations.

* **Astronaut Markers:** Small glowing spheres represent astronauts currently in space, positioned near the ISS, reflecting live crew count data.

* **Interactive Object Information:**

    * **Clickable Objects:** Users can click on the ISS, generic satellites, and astronaut markers to reveal a pop-up modal with specific information about that object.

    * **Contextual Actions:** The info modal includes "Focus Camera" to smoothly zoom in on the clicked object and "Ask AI Assistant" to send a pre-formatted question about the object to the integrated AI chat.

* **Interactive AI Assistant:** A chat interface powered by the Google Gemini API allows users to ask questions about space, astronomy, or any displayed celestial object. The AI provides concise and helpful answers.

* **Customizable View:**

    * **Toggle Auto-Rotate:** Turn the scene's automatic rotation on or off.

    * **Recenter Camera:** Instantly reset the camera's view to focus on Earth.

    * **Toggle Satellites:** Show or hide the generic orbiting satellites to adjust visual clutter.

* **Dynamic Starfield:** A colorful and dense 3D starfield surrounds the scene, enhancing the immersive cosmic environment.

* **Responsive Design:** The application adapts its layout and 3D rendering to various screen sizes, ensuring a consistent experience across desktop and mobile devices.

* **Robust Error Handling:** Gracefully handles API failures, network issues, and data loading errors, providing informative messages without disrupting the overall experience.

## Technologies Used

* **HTML5:** Structure of the web application.

* **CSS3:** Styling and visual presentation.

* **JavaScript (ES6+):** Core application logic, API integration, and interactive elements.

* **Three.js:** A powerful JavaScript 3D library for rendering the interactive celestial scene using WebGL.

* **OrbitControls.js:** A Three.js addon for intuitive camera controls (orbiting, zooming).

* **TWEEN.js:** A JavaScript animation engine for smooth transitions and visual effects (e.g., camera focus, click animations).

* **NASA APIs:**

    * Astronomy Picture of the Day (APOD): For daily background context (though the Earth texture is a standard one for realism).

* **Open-Notify APIs:**

    * ISS Current Location: For real-time International Space Station coordinates.

    * People In Space: For live astronaut count and names.

* **Google Gemini API (`gemini-2.0-flash`):** Powers the interactive AI Assistant, providing real-time responses to user queries about cosmic objects.

* **`corsproxy.io`:** Used to bypass Cross-Origin Resource Sharing (CORS) restrictions for certain external API calls, ensuring data can be fetched reliably.

## How to Run Locally

1.  **Clone the Repository:**
    ```bash
    git clone [https://github.com/abdallla142/Cosmic-Data-Visualizer.git](https://github.com/abdallla142/Cosmic-Data-Visualizer.git)
    cd Cosmic-Data-Visualizer
    ```

2.  **Open in Browser:**
    Simply open the `index.html` file in your web browser. You can do this by dragging the `index.html` file into your browser, or by right-clicking it and choosing "Open with" -> "Your Web Browser".

    *Note: For some browsers (especially Chrome), direct file access might have limited capabilities. For best results, it's recommended to serve the file through a local web server (e.g., using VS Code's Live Server extension, or a simple Python HTTP server: `python -m http.server` in the directory).*

## Important Note on API Keys

* **NASA API Key:** The application uses a NASA API key. While a `DEMO_KEY` is typically functional for basic testing, for sustained use or higher rate limits, you might want to obtain your own free API key from [api.nasa.gov](https://api.nasa.gov/).

* **Google Gemini API:** The application is configured to use the `gemini-2.0-flash` model. For this to work in certain environments (like Google's Canvas), the API key is **automatically provisioned** by the environment when the `apiKey` parameter is left as an empty string in the code.

    * **If you encounter `401 Unauthorized` or `400 Bad Request` errors from the Gemini API:** This typically indicates an issue with your development environment's configuration or API key setup (e.g., project not enabled for Gemini, incorrect billing, or incorrect environment setup for automatic key injection). This is usually an external setup issue and not a bug in the application's JavaScript code. Please ensure your environment is correctly configured for Gemini API access.

## Interaction Guide

* **Scene Rotation:** Click and drag your mouse on the 3D scene to rotate the camera around Earth.

* **Zoom:** Use your mouse scroll wheel to zoom in and out.

* **Object Information:** Click on the ISS, any generic satellite, or an astronaut marker to open a modal window with details about that object.

* **Modal Actions:**

    * **"Focus Camera" button:** Smoothly moves the camera to center on the selected 3D object.

    * **"Ask AI Assistant" button:** Sends a pre-defined question about the selected object to the AI chat.

* **AI Assistant:** Type questions in the chat box (top right) and press Enter or click "Send" to get AI-powered insights.

* **Control Panel (bottom right):**

    * \`Toggle Auto-Rotate\`: Turns the automatic scene rotation on/off.

    * \`Recenter Camera\`: Resets the camera to its default view of Earth.

    * \`Toggle Satellites\`: Hides or shows the generic satellites.

    * \`Focus ISS\`: Instantly centers the camera on the International Space Station.

## Credits

* Developed by Abdalla.

* Powered by NASA Open APIs, Open-Notify APIs, Google Gemini API.

* Built using Three.js, OrbitControls, and TWEEN.js.

* Read.me create by AI for transparency
