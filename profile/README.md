
<p align="center">
  <img width="600" height="250" src="https://github.com/eNutri/.github/blob/main/enutri_logo.png">
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

**Academic publications**

Selected publications directly related to eNutri:

- [Effectiveness of Web-Based Personalized Nutrition Advice for Adults Using the eNutri Web App: Evidence From the EatWellUK Randomized Controlled Trial](https://scholar.google.com/scholar?q=Effectiveness+of+Web-Based+Personalized+Nutrition+Advice+for+Adults+Using+the+eNutri+Web+App) — R Zenun Franco, R Fallaize, M Weech, F Hwang, JA Lovegrove; Journal of Medical Internet Research 24 (4), e29088 (2022). Cited by 44.
- [Online Recommender System for Personalized Nutrition Advice](https://scholar.google.com/scholar?q=Online+Recommender+System+for+Personalized+Nutrition+Advice) — R Zenun Franco; Proceedings of the Eleventh ACM Conference on Recommender Systems, 411-415 (2017). Cited by 59.
- [Insights into the delivery of personalized nutrition: evidence from face-to-face and web-based dietary interventions](https://scholar.google.com/scholar?q=Insights+into+the+delivery+of+personalized+nutrition%3A+evidence+from+face-to-face+and+web-based+dietary+interventions) — B Al-Awadhi, R Fallaize, R Zenun Franco, F Hwang, JA Lovegrove; Frontiers in Nutrition 7, 570531 (2021). Cited by 43.
- [Evaluation of the eNutri automated personalised nutrition advice by users and nutrition professionals in the UK](https://scholar.google.com/scholar?q=Evaluation+of+the+eNutri+automated+personalised+nutrition+advice+by+users+and+nutrition+professionals+in+the+UK) — R Fallaize, RZ Franco, F Hwang, JA Lovegrove; PloS one 14 (4), e0214931 (2019). Cited by 30.
- [Dietary Quality in Vegetarian and Omnivorous Female Students in Germany: A Retrospective Study](https://scholar.google.com/scholar?q=Dietary+Quality+in+Vegetarian+and+Omnivorous+Female+Students+in+Germany%3A+A+Retrospective+Study) — J Blaurock, B Kaiser, T Stelzl, M Weech, R Fallaize, RZ Franco, F Hwang, ...; International Journal of Environmental Research and Public Health 18 (4), 1888 (2021). Cited by 29.
- [Online dietary intake assessment using a graphical food frequency app (eNutri): Usability metrics from the EatWellUK study](https://scholar.google.com/scholar?q=Online+dietary+intake+assessment+using+a+graphical+food+frequency+app+%28eNutri%29%3A+Usability+metrics+from+the+EatWellUK+study) — R Zenun Franco, R Fallaize, JA Lovegrove, F Hwang; PLoS One 13 (8), e0202006 (2018). Cited by 24.
- [A Web-Based Graphical Food Frequency Assessment System: Design, Development and Usability Metrics](https://scholar.google.com/scholar?q=A+Web-Based+Graphical+Food+Frequency+Assessment+System%3A+Design%2C+Development+and+Usability+Metrics) — RZ Franco, B Alawadhi, R Fallaize, JA Lovegrove, F Hwang; JMIR Human Factors 4 (2) (2017). Cited by 23.
- [Web-Based Dietary Intake Estimation to Assess the Reproducibility and Relative Validity of the EatWellQ8 Food Frequency Questionnaire: Validation Study](https://scholar.google.com/scholar?q=Web-Based+Dietary+Intake+Estimation+to+Assess+the+Reproducibility+and+Relative+Validity+of+the+EatWellQ8+Food+Frequency+Questionnaire%3A+Validation+Study) — B Alawadhi, R Fallaize, RZ Franco, F Hwang, J Lovegrove; JMIR Formative Research 5 (3), e13591 (2021). Cited by 17.
- [Strategies for online personalised nutrition advice employed in the development of the eNutri web app](https://scholar.google.com/scholar?q=Strategies+for+online+personalised+nutrition+advice+employed+in+the+development+of+the+eNutri+web+app) — RZ Franco, R Fallaize, F Hwang, JA Lovegrove; Proceedings of the Nutrition Society 78 (3), 407-417 (2019). Cited by 16.
- [The eNutri app: using diet quality indices to deliver automated personalised nutrition advice](https://scholar.google.com/scholar?q=The+eNutri+app%3A+using+diet+quality+indices+to+deliver+automated+personalised+nutrition+advice) — R Fallaize, M Weech, R Zenun Franco, A Kehlbacher, F Hwang, ...; Agro Food Industry Hi-Tech 31 (2) (2020). Cited by 8.
- [Designing Apps to Support Engagement by Older Adults: A think-aloud study of the eNutri dietary-intake assessment web app](https://scholar.google.com/scholar?q=Designing+Apps+to+Support+Engagement+by+Older+Adults%3A+A+think-aloud+study+of+the+eNutRi+dietary-intake+assessment+web+app) — E Kelly, M Weech, R Fallaize, R Zenun Franco, F Hwang, J Lovegrove; Proceedings of the 23rd International ACM SIGACCESS Conference on Computers … (2021). Cited by 2.
- [Usability of a web-based food frequency questionnaire app (eNutri) and a 24-hour dietary recall system (Intake24) in adults aged 65+ years](https://scholar.google.com/scholar?q=Usability+of+a+web-based+food+frequency+questionnaire+app+%28eNutRi%29+and+a+24-hour+dietary+recall+system+%28Intake24%29+in+adults+aged+65%2B+years) — E Kelly, M Weech, R Fallaize, RZ Franco, F Hwang, JA Lovegrove; Proceedings of the Nutrition Society 81 (OCE5), E213 (2022). Cited by 1.
- [Validity of the EatWellQ8 online food frequency questionnaire against a 4-day weighed food record](https://scholar.google.com/scholar?q=Validity+of+the+EatWellQ8+online+food+frequency+questionnaire+against+a+4-day+weighed+food+record) — B Al-Awadhi, R Fallaize, RZ Franco, F Hwang, JA Lovegrove; Proceedings of the Nutrition Society 78 (OCE1), E13 (2019). Cited by 1.
- [Importance, motivation and confidence of eating healthily whilst at university and barriers UK students face to eating well at university](https://scholar.google.com/scholar?q=Importance%2C+motivation+and+confidence+of+eating+healthily+whilst+at+university+and+barriers+UK+students+face+to+eating+well+at+university) — E Kelly, M Weech, R Fallaize, RZ Franco, F Hwang, JA Lovegrove; Proceedings of the Nutrition Society 82 (OCE5), E347 (2023).
- [Co-designing personalised nutrition advice with adults aged 65+ years: a user study of the eNutri web app](https://scholar.google.com/scholar?q=Co-designing+personalised+nutrition+advice+with+adults+aged+65%2B+years%3A+a+user+study+of+the+eNutri+web+app) — E Kelly, M Weech, R Fallaize, RZ Franco, F Hwang, JA Lovegrove; Proceedings of the Nutrition Society 80 (OCE5), E187 (2021).

