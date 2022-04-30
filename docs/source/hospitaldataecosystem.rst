Hospital Data Ecosystem
===================================

A hospital is a complex multi-disciplinary institution with a wide variety of business and supporting processes resulting in a large data ecosystem. The scope of the Clinical Data Bible is limited to clinical data. Financial data or other data categories are out of scope.

The following figure illustrates an abstraction of a sample pathway in a hospital with associated data, processes and systems:

.. figure:: resources/hospital_pathway.png
    :alt: Sample hospital pathway
    :class: with-shadow

Systems
------------
Primary/secondary systems, registries, etc.

**Hospital Information System (HIS)**
    | The hospital information system is the main system for the clinical data in a hospital and serves as the "source-of-truth" for the longitudinal patient record with clinical routine data gathered either directly in the hospital information system or in department/clinic specific solutions. A set of interfaces ensures that the data gathered in other systems is feeded into the hospital information system. 
    | Typically the policy in a hospital is that each data set potentially relevant for the treatment of the patient must be fed into the system. Other data that is not directly relevant for the treatment process might also reside outside the hospital information system (refer to e.g. registries, studies, etc.). 
    | The following non-exhaustive list gives an overview over the data normally included in the HIS:

    * **Patient Demographics**
        * Name, Birthdate, Gender
        * Social Security Number
        * ...
    * **Appointments**
    * **Orders and Events / Interventions**
        * Medication
        * Installation (e.g. Catheter)
        * ...
    * **Vital Signs & Scores**
        * Blood Pressure
        * Temperature
        * ...
    * **Lab Results**
        * Chlinical Chemistry
        * Hematology
        * Virology
        * Microbiology
        * ...
    * **Assessments**
    * **Diagnoses & Procedures**
    * **Reports**
        * Admission / Discharge Reports
        * Clinical Notes
        * Prescriptions
        * Pathology Reports
        * ...
    * **Images**
        * Conventional X-Ray
        * CT / MRI
        * Ultrasound
        * Wound Documentation
        * ...

**Administrative System**
    | The administrative system (often an Enterprise Resource Planning System) holds the financial/billing information and typically also is the master system for the patient demographics.

**Laboratory Information System (LIS)**
    | The LIS (sometimes also "LIMS" for Laboratory Information and Management System) records, manages, and stores data for clinical laboratories. It accepts/processes lab orders to lab instruments, and records the results in a database.

**Radiology Information System (RIS)**
    | The RIS is the information system of the radiology department and serves to manage patient appointments, orders and results. The images are normally stored in an associated Picture Archiving and Communication System (PACS).

**Picture Archiving and Communication System (PACS)**
    | The Picture Archiving and Communication System stored medical images. Typically these images are stored in the DICOM standard, however it may also contain scanned PDF documents and other file formats. A PACS consists of four major components: The imaging modalities (CT / MRI / CR), a secured network for the transmission of patient information, workstations for interpreting and reviewing images, and archives for the storage and retrieval of images and reports.

**Patient Data Management System (PDMS)**
    | The Patient Data Management Systems (PDMS) supports the clinical documentation at intensive care units (ICUs). Compared to standard hospital information systems the data volume in PDMS systems is much higher because the data mostly comes from machines/devices. An ICU patient is monitored with many devices that record high-resolution data (one signal per parameter per second or even higher resolutions). 

**Long-Term Archiving System**
    | The long-term archiving system fullfills the regulatory requirements regarding the archiving of clinical routine data from patient treatment. After the deadline has expired, data is either anonymized, deleted or moved to the state archive.


Data Types
------------

There is no standard on how to describe the different data types and the categorization also depends on the implementation and the systems in the hospital but the following table summarizes the key ones.

.. csv-table:: Hospital Data Types
   :header: "Type", "Structure", "Description", "File Formats"
   :widths: auto

   "Demographics", "structured", "Name, Gender, Birthday, Social Security, Address etc.", "CSV / XML"
   "Clinical Routine Data", "structured", "Vital Signs, Scores, Orders, Events / Interventions, Diagnoses, Procedures, Lab etc.", "CSV / HL7"
   "Reports", "semi-structured or unstructured", "Admission / Discharge Reports, Clinical Notes, etc.", "TXT / JSON"
   "Imaging", "structured metadata and media files", "MRI, CT, Conventional X-Rays, Ultrasound, Capillary Microscopies, etc.", "CSV (Metadata) / DICOM / JPG / PNG"
   "Waveforms", "structured", "ECGs, high-resolution data (sensors, IoT), etc.", "CSV / XML / JSON"
   "-OMICS", "structured or semi-structured", "Genomics, Transcriptomics, Proteomics, Metabolomics, etc.", "TSV, VCF, BAM, FASTQ"
