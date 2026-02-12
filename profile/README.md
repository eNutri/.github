<p align="center">
  <img width="600" height="250" src="https://github.com/eNutri/.github/blob/main/enutri_logo.png">
</p>

<p align="center">
  <img width="600" height="250" src="https://github.com/eNutRi/.github/blob/main/enutri_logo.png">
</p>

# eNutri — Overview

eNutri is a web app designed to (1) make dietary intake assessment easier (eNutri-FFQ), and (2) help people eat more healthily by providing personalised nutrition advice (eNutri-PN).

For dietary intake assessment, the eNutri-FFQ is an online graphical food frequency questionnaire (FFQ), with an extensive and up-to-date list of foods, drinks and supplements consumed in the UK. Food group and nutrient intakes are automatically calculated. The data are immediately available for download by the researcher, making dietary intake analysis faster and easier.

eNutri-PN combines the eNutri-FFQ with a personalised nutrition feature. Based on a user’s questionnaire responses, the app automatically provides recommendations to the individual on what specific foods and drinks in their diet they should have more, or less, of to get closer to meeting healthy eating recommendations. The app also includes tips from qualified nutritionists and dietitians to help people make healthy dietary choices, explained in a way that is easy to understand and practical. The personalised healthy eating food-based advice is instantly available, helping to keep people engaged.

**Main features:**
- User management (participants, researchers, administrators).
- User journey: account creation → consent → screening → FFQ → feedback and reports.
- Automated FFQ processing (composition calculations, DQS, Excel export generation).
- Research dashboard for eligibility checks, monitoring and data export.
- Online personalised nutrition reports.
- Daily backups fully public cloud based.

**High-level architecture:**
- Frontend: Single Page Application implemented with AngularJS, served from Firebase Hosting
- Authentication: Firebase Authentication (email/password).
- Database: Firebase Realtime Database for profiles, FFQs and application state.
- Storage: Firebase Storage for Excel files and food images.
- Backend: Google Cloud Functions (Gen2 / Cloud Run) written in Python
- Supporting tools: Jupyter notebooks and Python scripts to generate/import database JSON from Excel.

**Technologies used:**
- Frontend: AngularJS, HTML, CSS, JavaScript.
- Cloud platform: Google Firebase (Hosting, Realtime DB, Auth, Storage).
- Serverless backend: Google Cloud Functions (Python 3.12 / Cloud Run).
- Deployment tools: `firebase` CLI and `gcloud`.

**Security and privacy:**
- Communications use HTTPS. Realtime Database security rules control access levels via the `profiles` node (participant vs researcher vs admin).
- Daily database backups can be configured.

