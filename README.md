<p align="center">
  <img src="https://www.especial.gr/wp-content/uploads/2019/03/panepisthmio-dut-attikhs.png" alt="UNIWA" width="150"/>
</p>

<p align="center">
  <strong>UNIVERSITY OF WEST ATTICA</strong><br>
  SCHOOL OF ENGINEERING<br>
  DEPARTMENT OF COMPUTER ENGINEERING AND INFORMATICS
</p>

</p>

---

<p align="center">
  <strong>Software Engineering</strong>
</p>

<h1 align="center">
  Preze Cinemas Desktop – Phase 3<br>
  Robustness Diagram Design
</h1>

<p align="center">
  <strong>Vasileios Evangelos Athanasiou</strong><br>
  Student ID: 19390005
</p>

<p align="center">
  <a href="https://github.com/Ath21" target="_blank">GitHub</a> ·
  <a href="https://www.linkedin.com/in/vasilis-athanasiou-7036b53a4/" target="_blank">LinkedIn</a>
</p>

<hr/>

<p align="center">
  <strong>Supervision</strong>
</p>

<p align="center">
  Supervisor: Georgios Prezerakos, Professor
</p>
<p align="center">
  <a href="https://ice.uniwa.gr/en/emd_person/george-prezerakos/" target="_blank">UNIWA Profile</a> ·
  <a href="https://www.linkedin.com/in/georgenprezerakos/" target="_blank">LinkedIn</a>
</p>

</hr>

---

<p align="center">
  Athens, August 2023
</p>

---

# Preze Cinemas Desktop - Phase 3: Robustness Diagrams

This README documents **Phase 3** of the *Preze Cinemas Desktop* project.  
This phase focuses on the **structural and behavioral system design** using **Robustness Diagrams**, bridging requirements analysis and detailed system design.

---

## Table of Contents

| Section | Folder/File | Description |
|------:|-------------|-------------|
| 1 | `assign/` | Assignment instructions and supporting material |
| 1.1 | `assign/seng_instructions_2022_23_v2.pdf` | Assignment instructions (English) |
| 1.2 | `assign/λμηχ_οδηγίες_2022_23_β2.pdf` | Assignment instructions (Greek) |
| 2 | `diagrams/` | Robustness diagrams for cinema system use cases |
| 2.1 | `diagrams/EN/` | Robustness diagrams in English |
| 2.1.1 | `diagrams/EN/1. Register.png` | Robustness diagram — User registration |
| 2.1.2 | `diagrams/EN/2. Login.png` | Robustness diagram — User login |
| 2.1.3 | `diagrams/EN/3. Check Availability.png` | Robustness diagram — Availability checking |
| 2.1.4 | `diagrams/EN/4. Ticket Selection.png` | Robustness diagram — Ticket selection |
| 2.1.5 | `diagrams/EN/5. Movie Selection.png` | Robustness diagram — Movie selection |
| 2.1.6 | `diagrams/EN/6. Time View selection.png` | Robustness diagram — Show time selection |
| 2.1.7 | `diagrams/EN/7. Download transaction receipt.png` | Robustness diagram — Receipt download |
| 2.1.8 | `diagrams/EN/8. tickets download.png` | Robustness diagram — Ticket download |
| 2.1.9 | `diagrams/EN/9. Payment.png` | Robustness diagram — Payment process |
| 2.2 | `diagrams/GR/` | Robustness diagrams in Greek |
| 2.2.1 | `diagrams/GR/1. Εγγραφή.png` | Διάγραμμα robustness — Εγγραφή χρήστη |
| 2.2.2 | `diagrams/GR/2. ΕίσοδοςΧρήστη.png` | Διάγραμμα robustness — Είσοδος χρήστη |
| 2.2.3 | `diagrams/GR/3. Έλεγχος διαθεσιμότητας.png` | Διάγραμμα robustness — Έλεγχος διαθεσιμότητας |
| 2.2.4 | `diagrams/GR/4. Επιλογή Εισιτηρίων.png` | Διάγραμμα robustness — Επιλογή εισιτηρίων |
| 2.2.5 | `diagrams/GR/5. Επιλογή Ταινίας.png` | Διάγραμμα robustness — Επιλογή ταινίας |
| 2.2.6 | `diagrams/GR/6. Επιλογή ώρας προβολής.png` | Διάγραμμα robustness — Επιλογή ώρας προβολής |
| 2.2.7 | `diagrams/GR/7. Λήψη Αποδεικτικού Συναλλαγής.png` | Διάγραμμα robustness — Λήψη αποδεικτικού συναλλαγής |
| 2.2.8 | `diagrams/GR/8. Λήψη Εισιτηρίων.png` | Διάγραμμα robustness — Λήψη εισιτηρίων |
| 2.2.9 | `diagrams/GR/9. Πληρωμή.png` | Διάγραμμα robustness — Πληρωμή |
| 3 | `docs/` | Compiled robustness diagram documentation |
| 3.1 | `docs/Robustness-Diagrams.pdf` | Robustness diagrams document (English) |
| 3.2 | `docs/Διαγράμματα-Robustness.pdf` | Robustness diagrams document (Greek) |
| 4 | `README.md` | Repository overview and usage instructions |

---

## Project Overview 

Phase 3 transforms previously defined **use cases** into **robustness diagrams**, helping identify:

- Boundary objects (user interface interaction)
- Control objects (system logic)
- Entity objects (data and persistent information)

The diagrams were produced using **Visual Paradigm** and represent internal system behavior during major operations.

---

## Deliverables – Robustness Diagrams

### 1. User Access & Security

#### Registration
Handles creation of new user accounts including:

- Customer information input
- Password validation rules
- Creation of records in the cinema database

Password rules require at least:
- One uppercase letter
- One numeric character

#### User Login
Responsible for:

- Credential validation
- Database verification
- Success or error feedback handling

---

### 2. Selection & Scheduling

#### Movie Selection
Allows users to:

- Browse available movies
- Select viewing formats such as:
  - Standard projection
  - Dolby Atmos
  - 3D screenings

#### Viewing Time Selection
Displays available screening times retrieved from the database.

#### Ticket Selection
Manages ticket selection for chosen screenings, including seat selection logic.

---

### 3. Inventory & Transaction Management

#### Availability Check
A core logical process that:

- Verifies seat availability
- Allows reservation continuation with fewer seats if necessary
- Supports waiting list functionality to notify users when seats become available

#### Payment Processing
Handles interaction with an external banking system to:

- Validate payment details
- Verify account balance
- Confirm or reject transactions

#### Transaction Receipt
After successful payment:

- Reservation completion is verified
- A downloadable proof of transaction is generated
- Digital receipt becomes available to the customer

---

## Summary Table of Use Cases

| Use Case ID | Name | Key Interaction |
|-------------|------|----------------|
| 5.1.1 | Registration | Account creation & password validation |
| 5.1.2 | User Login | Credential verification |
| 5.1.3 | Movie Selection | Film and format selection |
| 5.1.4 | Viewing Time Selection | Screening schedule retrieval |
| 5.1.6 | Availability Check | Seat allocation & waiting list |
| 5.1.7 | Payment | Banking system interaction |
| 5.1.8 | Receipt Generation | Transaction proof generation |

---

## Phase 3 Objective

This phase serves as the **transition point from requirements analysis to system design**, ensuring all major user interactions are translated into structured internal system behavior.

---

## Conclusion

Phase 3 refines system functionality by modeling how internal components collaborate during user operations. These robustness diagrams provide a solid foundation for the next development stage, enabling smoother implementation and clearer system architecture decisions.