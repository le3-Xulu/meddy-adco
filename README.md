# Meddy AI – Digital Health Companion

## 1. Overview

**Meddy** is a digital medicine education companion developed as a prototype under Adcock Ingram. Its purpose is to make medicine information more accessible, understandable, and convenient for users.

Users can select a medicine, explore information about it, access educational videos, and use text-to-speech functionality to listen to information. The prototype is designed to complement approved Patient Information Leaflets (PILs), particularly when users have difficulty accessing or understanding the information provided with their medication.

Meddy is an educational tool and is **not intended to diagnose medical conditions, prescribe medication, or replace professional medical advice**.

## 2. The Problem

Patient Information Leaflets contain important information about medicines, including dosage instructions, ingredients, warnings, and storage requirements. However, users may struggle to locate, access, or understand this information when they need it.

Meddy explores how digital technology can help make medicine information easier to access and understand through a simple, interactive interface.

## 3. Our Approach

Meddy provides a digital interface where users can explore medicine-specific information and educational resources. The prototype combines medicine information, interactive features, video content, and audio assistance to support a more accessible medicine education experience.

The current prototype focuses on two products:

* **Panado® Paediatric Syrup Strawberry** – Paracetamol 120 mg/5 mL.
* **Allergex® Non Drowsy Syrup** – Loratadine 5 mg/5 mL.

## 4. Features

### 4.1 Medicine Information

Users can select a supported medicine and explore information presented through the Caregiver View, including available dosage information, safety information, ingredients, and storage guidance.

The prototype also provides access to the relevant Patient Information Leaflet PDFs.

### 4.2 Information Zone

The Information Zone provides educational video content associated with the selected medicine. This feature aims to make medicine-related information easier to understand through additional educational resources.

### 4.3 Multilingual Interface

The prototype includes language selection for:

* English
* isiZulu
* Afrikaans

Language and content coverage may vary across the prototype's features.

### 4.4 Text-to-Speech

Meddy includes browser-based text-to-speech functionality, allowing supported information to be read aloud. Availability depends on the browser and its installed speech voices.

### 4.5 Interactive Medicine Questions

Users can enter questions about the selected medicine through the question interface. The current prototype uses predefined questions, keyword matching, and programmed responses.

**Note:** The current question feature is a rule-based prototype and is not connected to a live AI model.

### 4.6 QR Code Demonstration

The prototype includes a packaging simulator that generates QR codes for supported medicines. These QR codes demonstrate how users could access the digital companion through a link associated with a medicine product.

The QR code image is generated using an external QR code service.

### 4.7 Healthcare Resources

The interface includes links to RecoMed to help users access external healthcare-related resources.

## 5. Technology Stack

The current prototype uses:

* **HTML5** – Structure and content.
* **CSS3** – Styling, layout, and responsive interface design.
* **JavaScript** – Interactive functionality, medicine selection, question matching, and QR code generation.
* **Web Speech API** – Browser-based text-to-speech functionality.
* **YouTube embeds** – Educational video content.
* **QuickChart QR Code API** – QR code image generation.
* **PDF documents** – Access to medicine-specific Patient Information Leaflets.
* **RecoMed** – External healthcare resource links.

## 6. Project Structure

The prototype is currently implemented as a single HTML file containing the page structure, styling, and JavaScript functionality.

A simplified project structure could look like this:

```text
Meddy/
├── index.html
├── README.md
├── PIL-2025739-Panado-Strawberry_TG (1).pdf
└── ALLERGEX-NON-DROWSY-SYRUP-360008-0008-1.3.2-PIL-Approved.pdf
```

The PDF filenames above reflect the documents referenced by the current prototype. Ensure that the actual files are present in the project directory and that their filenames match the references in the code.

## 7. Getting Started

### Prerequisites

To run the prototype locally, you need:

* A modern web browser, such as Google Chrome, Microsoft Edge, or Firefox.
* The project HTML file.
* The referenced Patient Information Leaflet PDFs, if you want to access them locally.
* An internet connection for external resources such as embedded videos and QR code generation.

### Option 1: Open the HTML File

1. Download or clone the project repository.
2. Locate the `index.html` file.
3. Open it in a modern web browser.
4. Select a supported medicine and explore the available features.

Some features that depend on external resources may require an internet connection.

### Option 2: Run a Local Development Server

If Python is installed on your computer:

1. Open a terminal or command prompt.
2. Navigate to the project folder.
3. Run the following command:

```bash
python -m http.server 8000
```

4. Open the following address in your browser:

```text
http://localhost:8000
```

This starts a basic local development server for testing the prototype.

## 8. How to Use Meddy

1. Open the Meddy prototype.
2. Select a supported medicine.
3. Choose the available language option.
4. Explore the Caregiver View for the information provided about the selected medicine.
5. Access the relevant Patient Information Leaflet where required.
6. Open the Information Zone to explore educational videos.
7. Use the text-to-speech feature to listen to supported information.
8. Try the question interface to explore its predefined responses.
9. Use the packaging simulator to demonstrate how a medicine-related QR code could connect users to the digital companion.

## 9. QR Code Functionality

The packaging simulator demonstrates a possible connection between medicine packaging and digital medicine education.

The prototype creates product-specific URLs using query parameters, such as:

* `?product=PANADO`
* `?product=ALLERGEX`

These parameters identify the selected product within the demonstration. For the QR code to work outside the local environment, the generated URL must point to a publicly accessible deployment of the application.

## 10. Current Limitations

Meddy is a prototype, and its current implementation has several limitations:

* The question interface uses predefined, keyword-based responses rather than a live AI model.
* The prototype does not include a backend server or database.
* User accounts and personalised user profiles are not implemented.
* The available medicines are limited to the products included in the prototype.
* Language coverage and translations may be incomplete.
* Text-to-speech functionality depends on browser support and available voices.
* Educational videos, QR code generation, and other external resources depend on third-party services and internet connectivity.
* The accuracy and suitability of medicine information must be checked against the latest approved product documentation.

## 11. Safety and Regulatory Considerations

Meddy is intended to support access to medicine education and is not a substitute for a healthcare professional.

Medicine-related information must be reviewed against the current, approved Patient Information Leaflet and applicable South African regulatory requirements before the application is used in a live environment.

The prototype should not be relied upon to independently determine diagnoses, recommend treatment, or make clinical decisions.

Any future implementation involving AI-generated medicine information would require appropriate safeguards, reliable approved source material, validation, and professional review.

Privacy and data protection requirements, including applicable obligations under South Africa's Protection of Personal Information Act (POPIA), should be assessed before introducing user accounts, personal information collection, or additional integrations.

## 12. Future Improvements

Potential future enhancements include:

* Integrating a carefully controlled AI question-answering system grounded in approved Patient Information Leaflets.
* Expanding the medicine catalogue.
* Improving multilingual content and accessibility.
* Adding more educational videos and accessible learning resources.
* Developing a backend to manage approved medicine information.
* Improving QR code deployment and product-specific routing.
* Introducing content version control and review workflows.
* Conducting user testing to evaluate usability, accessibility, and comprehension.
* Completing appropriate legal, regulatory, privacy, and clinical reviews before any real-world deployment.

## 13. Contributors

Meddy was developed as a collaborative project involving Information Technology, Legal, Finance, and Pharmacy team members.

Contributors and responsibilities can be added here as appropriate.

## 14. Disclaimer

Meddy is a prototype developed for medicine education and accessibility purposes. It is intended to complement, not replace, approved Patient Information Leaflets or advice from qualified healthcare professionals.

Always consult the approved product information and a qualified healthcare professional when you need guidance about a medicine.
