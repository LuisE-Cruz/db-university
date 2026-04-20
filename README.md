<!-- 
Esercizio di oggi:
nome repo: db-university

Modellizzare la struttura di un database per memorizzare tutti i dati riguardanti una università:
sono presenti diversi Dipartimenti (es.: Lettere e Filosofia, Matematica, Ingegneria ecc.);
ogni Dipartimento offre più Corsi di Laurea (es.: Civiltà e Letterature Classiche, Informatica, Ingegneria Elettronica ecc..)
ogni Corso di Laurea prevede diversi Corsi (es.: Letteratura Latina, Sistemi Operativi 1, Analisi Matematica 2 ecc.);
ogni Corso può essere tenuto da diversi Insegnanti;
ogni Corso prevede più appelli d'Esame;
ogni Studente è iscritto ad un solo Corso di Laurea;
ogni Studente può iscriversi a più appelli di Esame;
per ogni appello d'Esame a cui lo Studente ha partecipato, è necessario memorizzare il voto ottenuto, anche se non sufficiente.
Pensiamo a quali entità (tabelle) creare per il nostro database e cerchiamo poi di stabilirne le relazioni. Infine, andiamo a definire le colonne e i tipi di dato di ogni tabella.

Utilizzare https://www.drawio.com/ per la creazione dello schema.
Esportare quindi il diagramma in png, caricarlo in un file html e pushare tutto nella repo.
 -->



## departments

- id INT PK AI       
- name VARCHAR(50) NN


## courses_degree

-id INT PK AI
-name VARCHAR(50) NN
-department_id INT NN


## course_subjects

-id INT PK AI
-name VARCHAR(50) NN
-courses_degree_id INT NN
-teachers_id INT NN


## teachers

-id INT PK AI
-name VARCHAR(50) NN
-surname VARCHAR(50) NN
-dob DATE NULL
-contract_date DATE NULL
-phone VARCHAR(20) NULL
-email VARCHAR(50) NULL
-course_subject_id INT NULL

## students

-id INT PK AI
-name VARCHAR(50) NN
-surname VARCHAR(50) NN
-course_degree_id INT NULL
-dob DATE NULL
-email VARCHAR(50) NN
-phone VARCHAR(20) NULL


## exam_appeal

-id INT PK AI
-students_id INT NN
-course_subject_id INT NN
-teachers_id INT NULL
-date DATE NULL

## exam_votes

-id INT PK AI 
-students_id INT NN
-exam_appeal_id INT NN
-outcome FLOAT(2,1) NN






  
 