# siim-dataset
Collection of FHIR JSON objects representing fictious patient vignettes for use in our hackathon environment.

# What?
The [Society for Imaging Informatics in Medicine (SIIM)](http://www.siim.org/) is supporting the new DICOMWEB and FHIR standards by creating opportunities for it's members to interact with these systems at the annual meeting, and throughout the year through it's Hackathon/HackPack projects.

We're using images from [The Cancer Imaging Archive (TCIA)](http://www.cancerimagingarchive.net) and creating fictious but believable narratives that illustrate concepts common in imaging.

This project will contain FHIR JSON objects surrounding these patient narratives.

# Why?
During our first hackathon, we realized that in order to have a successful hackathon across multiple platforms, we need to have a cohesive, rich dataset that will allow people to build interesting applications. 

# Organization
In the top level directory there are directories for resources that cross patients (Medications, Practitioner, Organizations)

Also within the top level directory are a set of sub-folders for each patient.  This skeleton contains a set of top-level directories that correspond with the FHIR Resources: http://www.hl7.org/implement/standards/fhir/resourcelist.html.  Within these sub-folders are json FHIR documents.

Each FHIR document should have a commented header that looks like this:
    // filename
    // id: random

If set to something other than random, this will be used to create the FHIR resource.

This is not meant to be an exhaustive collection, the types are chosen based on relevance to imaging patients.

# Conventions
- Original TCIA IDs are retained as MRN
- Accession numbers are used as FHIR IDs for DiagnosticReports

# Uploading to a FHIR server
    cp fhir_server.yml.dist fhir_server.yml

Edit fhir_server.yml to fit your needs.

Install dependencies: ruby, bundler

Run Bundler to install needed gems
    bundle install

Run the script to upload all of the resources in the folders
    ruby update.rb

# Process to contribute
- Fork this repo
- Make your changes/improvements
- Send a pull request


# Patient Narratives
###Sally SIIM (mrn: BreastDx-01-0003)
58 yo female DOB: 04/12/1950

HPI: Had a palpable left breast mass discovered on self-breast exam.  Patient was initially seen for diagnostic mammogram on 4/12/2008.  Patient had a lumpectomy on 5/24/2008.

PMHx: Hypothyroidism

Allergies: NKDA

Medications: levothyroxine sodium 50mcg once daily 

Lab/Radiology

---------------------------------------
#####Diagnostic Bilateral Mammogram 4/12/2008 (FHIR ID/Accession Number: 2278028270041068)

DIAGNOSTIC BILATERAL 4/12/2008

Clinical History:  59 year-old female with history of left invasive ductal carcinoma (age 55) status post lumpectomy.

Technique: Bilateral CC and MLO, Left spot compression LMLO views were obtained

Findings:

LEFT BREAST: There are scattered fibroglandular densities. There are expected lumpectomy changes in the upper outer quadrant with surgical clips in place.  Skin thickening is consistent with post radiation changes. No concerning masses, architectural distortions, or suspicious calcifications are identified.

RIGHT BREAST: There are scattered fibroglandular densities. No concerning masses, architectural distortions, or suspicious calcifications are identified.

Impression:

LEFT BREAST: Expected lumpectomy changes. Benign. BI-RADS 2 - Recommend routine screening in 1 year.

RIGHT BREAST: Negative. BI-RADS 1 - Recommend routine screening in 1 year.

OVERALL BI-RADS 2 (Benign)

---------------------------------------
#####Bilateral Breast MRI 4/29/2008 (FHIR ID/Accession Number: 1085557173658239)
Bilateral Breast MRI 04/19/2008

Clinical History:  59 year-old female with history of left invasive ductal carcinoma (age 55) status post lumpectomy. High-risk screening MRI exam.

Technique: Bilateral axial imaging of the breasts was obtained including T1, STIR, T1FS, and sequential T1FS+C. Digital subtraction and dynamic contrast curve analysis was performed on a separate workstation.

Findings:

LEFT BREAST: There is minimal benign background enhancement. There are expected post surgical changes in the upper outer breast. Multiple signal voids represent surgical clips in place.  Skin thickening is consistent with post radiation change. There is no abnormal enhancement to indicate residual or recurrent disease.  There are no morphologically abnormal axillary lymph nodes.

RIGHT BREAST: There is minimal benign background enhancement. There is no abnormal enhancement or lymphadenopathy.

Impression:

LEFT BREAST: Expected post treatment changes. Benign. BI-RADS 2. Recommend routine screening mammography in 1 year.

RIGHT BREAST: Negative. BI-RADS 1. Recommend routine screening mammography in 1 year.

OVERALL BI-RADS 2 (Benign)

---------------------------------------
#####Full Field Digital Left Diagnostic Mammogram 4/19/2008 (FHIR ID/Accession No: 4361814883895900)


Full Field Digital Left Diagnostic Mammogram 4/19/2008 

Clinical History:  59 year-old female with history of left invasive ductal carcinoma (age 55) status post lumpectomy.

Technique: LML, L XCCL

Findings:

LEFT BREAST: There are scattered fibroglandular densities. There are expected lumpectomy changes in the upper outer quadrant with surgical clips in place.  Skin thickening is consistent with post radiation changes. No concerning masses, architectural distortions, or suspicious calcifications are identified.

Impression:

LEFT BREAST: Expected changes status post lumpectomy and radiation. Benign. BI-RADS 2 - Recommend routine screening in 1 year.

---------------------------------------
#####Surgical Specimen Radiograph 5/24/2008 (FHIR ID/Accession No 2889127246021897)
05/24/2008
Surgical Specimen Radiograph

Clinical History:  Unknown

Technique: Single surgical specimen radiograph

Findings: The surgical specimen contains an intact wire and surgical clip.  No masses or calcifications are identified.

Impression:

Specimen radiograph with intact wire and surgical clip.


###Ravi SIIM (mrn: LIDC-IDRI-0132)

HPI: 60 yo male with chronic lung disease.

####Imaging Exams

#####CT Chest with IV Contrast 1/1/2000 10:04 AM (FHIR ID/Accession Number: 2819497684894126)
CT Chest with Contrast 1/1/00 at 10:04 AM

Clinical History: Abnormal chest x-ray

Comparison: Chest XR 1/1/00

Technique: Contiguous axial CT images of the chest were obtained after the administration of IV contrast material.

Findings:

The heart is normal in size. There is no pericardial effusion.

The thoracic aorta is normal in size and caliber. There is a bovine configuration of the aortic arch, a normal variant. Mild atherosclerotic changes are present in the upper abdominal aorta.

There is a 2.2 x 1.4 cm cavitary lesion in the left upper lobe (Image 30/116). Linear bandlike areas of scarring/atelectasis are present in the right upper lobe with associated bronchiectasis. Bronchiectasis is also seen in the left upper lobe. The central airways are clear. Pleural-parenchymal scarring is present at the lung apices. There is no pleural effusion.

There is no axillary, mediastinal, or hilar adenopathy. The thyroid gland is within normal limits.

The visualized portions of the upper abdomen are unremarkable. No suspicious osseous lesion is seen. There is evidence of prior trauma/deformity of the right 5th rib.

Impression:

1. Cavitary lesion in the left upper lobe. Differential diagnosis infectious and neoplastic disease.

2. Bandlike areas of atelectasis/scarring and bronchiectasis in the right upper lobe likely related to prior infection/insult.

#####AP Chest Radiograph 1/1/2000 11:22 AM (FHIR ID/Accession Number: 2819497684894127)

Chest: AP View

Clinical History: Cough

Comparison: None

Findings:

The cardiomediastinal silhouette and pulmonary vasculature are within normal limits.

Linear scarring and pleural thickening are present in the right upper lobe. There is thickening of the right paratracheal stripe as well as questionable righit hillier adenopathy. A 1.6 cm nodule projects in the left upper lobe. The right costophrenic angle is effaced.

No free air beneath the hemidiaphragms. The osseous structures are grossly unremarkable.

Impression:

1. 1.6 cm left upper lobe nodule.

2. Right upper lobe scarring and pleural thickening along with right pleural effusion versus scarring.

Recommendations:

CT Chest is recommended to further evaluate the above findings and impression.

#####CT Chest with IV Contrast 1/1/2000 12:00 PM (FHIR ID/Accession Number: 2819497684894128)

CT Chest with Contrast

Clinical History: Abnormal chest x-ray

Comparison: Chest XR 1/1/00, Chest CT 10:04 AM 1/1/00

Technique: Contiguous axial CT images of the chest were obtained after the administration of IV contrast material.

Findings:

The heart is normal in size. There is no pericardial effusion.

The thoracic aorta is normal in size and calibur. There is a bovine configuration of the aortic arch, a normal variant. Mild atherosclerotic changes are present in the upper abdominal aorta.

There is a 2.1 x 1.4 cm cavitary lesion in the left upper lobe (Image 28/116). A smaller cavitary lesion is seen in the right lower lobe measuring 9 mm (Image 40/116). Linear bandlike areas of scarring/atelectasis are present in the right upper lobe with associated bronchiectasis. The central airways are clear.

There is no axillary, mediastinal, or hilar adenopathy. The thyroid gland is within normal limits.

The visualized portions of the upper abdomen are unremarkable. No suspicious osseous lesion is seen. There is evidence of prior trauma/deformity of the right 5th rib.

Impression:

1. Interval evolution of left upper lobe cavitary lesion in the left upper and new right lower lobe nodule. Given the rapid evolution of these cavitary lesions an infectious etiology is favored.

2. Unchanged bandlike areas of atelectasis/scarring and bronchiectasis in the right upper lobe likely related to prior infection/insult.

###Joe SIIM (mrn: TCGA-17-Z058)
HPI: 60 yo male with history of lung adenocarcinoma. 

####Imaging Exams

#####CT Chest 3/30/1986 (FHIR ID/Accession No: 2257132503242682)

CT Onco Lung Mass 3/30/1986

Clinical information
60 yo male with left hilar mass.

Comparison
None.

Findings
Lung mass
Size: 5.3 x 4.0 x 4.0 cm

Location: left hilar region

Shape: Smoothly marginated

Internal consistency: homogenous, hypodense to surrounding muscle.

Local extent
Pleural surface: Left lower lobe metastasis

Chest wall: No involvement.

Airway: Compression of the lingula

Vessels: Mass surrounds and nearly occludes the left inferior pulmonary artery.

Nerves: No involvement.

Regional extent
Lymph nodes: AP window, and right hilar adenopathy.

Distant metastases (chest and upper abdomen): None.

Other findings
Other findings: None.

Impression
Left hilar mass concerning for malignancy.

---------------------------------------

#####PET Oncologic Study 4/22/1986 (FHIR ID/Accession No: 2819497684894126)

Duration of fast prior to injection: 6 hours

Blood glucose prior to injection: 85 mg/dl

Scan region: Brain, Neck, Chest, Abdomen

Radiopharmaceutical: F-18 FDG 10 mCi IV

Calibration time: 4/22/1986 10:30 AM

Administration time: 4/22/1986 10:32 AM

Injection site: left antecubital fossa

Post-injection imaging delay: 60 minutes

Attenuation correction: Rod source transmission scan.

Clinical information
60 yo male with left hilar mass, evaluate for metastatic disease

Comparison
Chest CT scan 3/30/1986

Findings
Hypermetabolic foci:
5.0 cm hypermetabolic left hilar mass on image 162 with a maximum SUV of 3.2.
1.8 x 1.2 cm hypermetabolic AP window lymph node on image 132 maximum SUV of 2.7
There is spurious activity in the neck musculature.  No contralateral hypermetabolic lesions are appreciated.

The right hilar adenopathy suspected on the prior CT scan is not seen.

Other findings:
The visualized brain parenchyma is unremarkable.  The soft tissues of the neck are unremarkable. The thyroid gland is unremarkable.  No axillary adenopathy.  No focal infiltrate.  No pneumothorax.  There a tiny left pleural effusion vs. pleural thickening.  This is not FDG avid.  The heart size is normal.  No pericardial effusion.

Lack of IV contrast mildly limits evaluation of the organs in the abdomen and pelvis. The liver is unremarkable without focal lesion.  The adrenals are normal.  The pancreas, spleen, and kidneys are unreamarkable.

Atherosclerotic calcification is seen throughout the aorta.  No abnormally dilated bowel.  No suspicious retroperitoneal or mesenteric adenopathy.

There are no suspicious bony lesions.

Impression
1. Findings again compatible with left hilar malignancy with a left AP window lymph node. There is no evidence of contralateral disease.

EORTC Response Criteria: N/A - Baseline

---------------------------------------
#####Surgical Pathology Report 4/25/1986 (FHIR ID/Accession No: z058path)

SIIM Diagnostic Lab
Leesburg, VA
Tel: (555) 555-5555 Fax: (812) 353-5445

Surgical Pathology Report

Patient Name: TCGA-17-Z058. Accession #: z058path Med. Rec. #: TCGA-17-Z058
Taken: 4/25/1986 Encounter #: 000111111111 Received: 4/25/1986 Gender: M
Reported: 4/26/1986 16:50 DOB: (Age: 60) Submitting Physician: REFERRING, MD
Additional Physician(s):
Location: ENDOSCOPY BL 

Pre-Operative Diagnosis:
Lingular lung mass

Post-Operative Diagnosis:
Same

Specimen Received:
Lingular lung bxs

Final Pathologic Diagnosis:
Lingula, lung, transbronchial biopsies:
Adenocarcinoma (see note)

The examination of this case material and the preparation of this report were
performed by the staff pathologist.
Electronically Signed by Joe Pathologist, M.D. 

Signing Location:
SIIM Laboratory Services,
Leesburg, VA

Gross Description:
Submitted in formalin as "left upper lobe-lung biopsies" are multiple fragments of light tan tissue each measuring up to 0.5 cm in greatest dimension. The entire specimen is submitted in a single cassette.

Microscopic Description:
Sections of bronchial mucosa demonstrate infiltration by poorly differentiated malignant cells which form cords and some, and somewhat pale cytoplasm. Some cells have a suggestion of signet ring cell morphology. No keratinization is evident. 

NOTE: This is a fictious report that was created to match the TCIA images.  This is NOT the actual report for this patient.

END OF REPORT

---------------------------------------

#####CTA Chest 5/5/1986 (FHIR ID/Accession Number: 1857795211017352)

Clinical Indication:
Acute shortness of breath, elevated D-dimer. History of lung cancer. Concern for PE.

Comparison: PET/CT from 4/22/1986

Technique: Multidetector axial CT of the chest was performed after the administration of intravenous contrast in the arterial phase using a pulmonary embolus protocol.

Findings:
Enteric drainage catheter courses into the stomach. Endotracheal tube terminates in the mid-thoracic trachea.

There is adequate opacification of the pulmonary vasculature to the subsegmental level without significant motion artifact. No evidence of pulmonary embolism. The main pulmonary artery and right heart are normal in size. A small pericardial effusion is present.

The thyroid and thoracic inlet are normal. No axillary lymphadenopathy. There is stable right hilar lymphadenopathy, slightly enlarged compared to the prior exam.

Emphysema again noted. Post surgical changes from interval left lower lobectomy. A large left hydropneumothorax is noted. There is diffuse bilateral septal thickening compatible with pulmonary edema. The major airways are patent.

Stable indeterminate subcentimeter enhancing lesion in the hepatic dome. Stable mildly enlarged gastrosplenic lymph node. Upper abdomen otherwise unremarkable.

Surgical defect noted in the posterior 6th rib. Osseous structures otherwise unremarkable.

Impression:
1. No evidence of pulmonary embolism.
2. Interval left lower lobectomy with large left hydropneumothorax.
3. Development of severe pulmonary edema.
4. Slight interval enlargement of right hilar lymph node and stable mild enlargement of a gastrosplenic node.

---------------------------------------

#####CT Chest 5/31/1986 (FHIR ID/Accession Number: 1654061970756517)

Clinical indication: Followup lung mass.

Comparison: Chest CTA from 5/5/1986

Technique: Multidetector axial CT of the chest was performed without the administration of intravenous contrast.

Findings:

Interval placement of a tracheostomy tube. 

The thyroid and thoracic inlet are normal. There are no grossly enlarged axillary or mediastinal lymph nodes, however the hila are difficult to assess without the use of contrast. There is relative hyperdensity of the intraventricular septum suggestive of anemia. The heart is normal in size without significant pericardial effusion. A small hiatal hernia is present.

Stable emphysema. Post-surgical changes from left lower lobectomy again seen with persistent moderate to large subpulmonic loculated hydropneumothorax. Interval decrease in septal thickening with mild persistent septal prominence within the right lung.

Upper abdomen unremarkable given lack of IV contrast.

Stable surgical defect in the posterior left 6th rib. No suspicious osseous lesions.

Impression:
1. Stable findings of left lower lobectomy with persistent subpulmonic hydropneumothorax.
2. Interval decrease in pulmonary edema with mild residual right sided septal prominence.


---------------------------------------

#####CT Chest, abdomen and pelvis 9/28/1986 (FHIR ID/Accession Number: 3173095681219824)

Clinical indication:
History of lung adenocarcinoma, followup.

Comparison:
Multiple prior CTs, the most recent from 5/31/1986

Technique:
Multidetector axial CT of the chest, abdomen and pelvis was performed after the administration of intravenous contrast in the portal venous phase.

Findings:

Thorax:
The thyroid and thoracic inlet are normal. There are no enlarged axillary lymph nodes. There has been interval development of an enlarged lymph node conglomerate mass within the posterior mediastinum just anterior to the descending aorta, measuring 2.8 x 4.2 cm in axial dimension (series 5, image 36). This mass anteriorly displaces and mildly narrows the left main pulmonary artery. There is no clear evidence of vascular invasion. There is stable right hilar adenopathy. A new markedly enlarged precardial lymph node is also now seen, measuring 3.3 x 1.7 cm (series 5, image 42).

There is stable severe emphysema. A 4 mm left apical nodule (series 5, image 6) appears stable. Surgical changes from prior left lower lobectomy are evident with associated pleural thickening. Interval resolution of the previously noted left hydropneumothorax. A small left lateral rim enhancing pleural collection is suspicious for infection.

No suspicious osseous lesions. The visualized soft tissues are unremarkable.

Abdomen:
Punctate calcifications noted in the right hepatic lobe. Liver otherwise unremarkable. Gallbladder, pancrease, speen, and adrenal glands are normal. Bilateral renal cysts are noted. The kidneys are otherwise unremarkable with normal enhancement.

An enlarged gastrosplenic node is noted, measuring 1.3 cm in short axis dimension (series 6, image 13). The visualized bowel is within normal limits.

Impression:
1. Post surgical changes from left lower lobectomy.

2. Development of posterior mediastinal and precardial lymphadenopathy concerning for disease progression. An enlarged gastrosplenic node is nonspecific and appears grossly stable compared to CT from 4/22/1986 given differences in technique.

3. Small rim enhancing left pleural fluid collection concerning for infection.

---------------------------------------


###Neela SIIM (mrn: TCGA-BA-4077)

HPI: 65 yo Female with recurrent right base of tongue cancer after chemotherapy and radiotherapy

####Imaging Exams

#####CT Head and Neck 4/28/1986 (FHIR ID/Accession No: 2605867053656544)

CT Head and Neck with contrast
 4/28/1986     

Clinical information
65 yo Female with recurrent right base of tongue cancer after chemotherapy and radiotherapy     

Comparison
None. 

TECHNIQUE: Sequential axial CT images were obtained from the base of the brain to the thoracic inlet following the uneventful administration of intravenous contrast.

Findings
Orbits, paranasal sinuses, and skull base: Normal skull base and orbits. Mucosal thickening in both maxillary sinuses. 

Nasopharynx: Normal. 

Suprahyoid neck: There is a nectrotic heterogenously enhancing mass in the base of the right tongue that measures 
3.0 cm x 3.7 cm (Ap versus transverse) with gas identified in the mass. No bulky local lymph nodes. No extension of the mass 
into the mandible, retropharyngeal or parapharyngeal space. Mild mass effect into the oropharynx.

Infrahyoid neck: Normal larynx, hypopharynx, and supraglottis. 

Thyroid: Normal. 

Thoracic inlet: Normal lung apices and brachial plexus.

Lymph nodes Normal. No lymphadenopathy. 

Vascular structures: Normal. 

Other findings: None. 

Impression
1. 3.0 cm x 3.7 cm mass in the base of the right tongue as detailed above consistent with known malignancy


##### WHole Body PET/CT Restaging 5/14/1996 (FHIR ID/Accession No: 2142485449496602)

PET Oncologic Study

Duration of fast prior to injection: 12 hours

Blood glucose prior to injection:  100  mg/dl

Scan region: Whole body scan

Radiopharmaceutical: [F-18 FDG] 4.8   mCi IV

Administration time: 11:35

Post-injection imaging delay: 60 minutes

Attenuation correction: Rod source transmission scan. 

Clinical information
65 yo Female with recurrent right base of tongue cancer after chemotherapy and radiotherapy     

Comparison
CT Head and Neck 4/28/1986  . No prior comparison PET scan 

Findings
Hypermetabolic foci: Increased FDG uptake in the base of the tongue with max SUV of 67918. 

Physiologic uptake identified. No other areas of increased uptake.

Other findings: [CT Chest, Abdomen and Pelvis without contrast.]

The lungs are clear bilaterally. No pulmonary nodules, consolidations, or pleural effusions.
No axillary, hilar, mediastinal, or paratracheal lymphadenopathy.

Heart size is normal. No pericardial effusion.  Calcific coronary atherosclerosis of the aorta

The visualized osseous structures are unremarkable. No suspicious sclerotic or lytic lesions observed.

Chest wall is unremarkable.

The liver, gallbladder, pancreas, spleen and adrenal glands are within normal limits. There is no retroperitoneal or mesenteric lymphadenopathy. 
The visualized loops of small bowel and large bowel are within normal limits. No free fluid or free air within the visualized abdomen.


Impression

1. FDG hypermetabolic lesion in the base of the right tongue suggests recurrent disease. No areas of increased peripheral uptake 
suggestive of distant metastatic disease

---------------------------------------

###Andy SIIM (mrn: TCGA-50-5072)




