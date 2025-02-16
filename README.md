# Patient Management System

## Overview

This program is a patient management system that allows users to add, display, search, and categorize patients based on their nutritional status (BMI). The system supports the creation of an unhealthy patient list for patients categorized as obese.

### Features
- **Add new patient**: Add a patient to the list with name, surname, birth date, height, and weight.
- **Display all patients**: View the list of all patients with their details and BMI.
- **Search for a patient**: Search for a patient by their first name.
- **Categorize unhealthy patients**: Move patients categorized as obese (Class 1, 2, or 3) into a new list of unhealthy patients.
- **Display unhealthy patients**: View a list of unhealthy patients (obese classes).

## Files

- `main.c`: The main program file containing the logic for patient management.
- `patients.txt`: Input file containing patient data (name, surname, birth date, height, weight, BMI).

## Data Structure

The program uses a **singly linked list** to store patient data. Each patient is represented by a `Node` containing:
- **name**: The first name of the patient.
- **surname**: The last name of the patient.
- **birth**: The birth date of the patient.
- **height**: The height of the patient (in meters).
- **weight**: The weight of the patient (in kilograms).
- **BMI**: The BMI classification (e.g., Underweight, Normal Weight, Obese Class 1).
- **next**: A pointer to the next patient node.

The list is maintained with a dummy head node for easier management of the list operations.

## Functions

### 1. `InitialisePatients(fileName[])`
Initializes the patient list by reading data from a file and inserting patients into the list alphabetically.

### 2. `InsertNewPatient(List list)`
Prompts the user to enter a new patient's information and inserts it alphabetically into the list.

### 3. `UpdateNutritionalStatus(List list)`
Calculates and updates the BMI for each patient in the list based on their height and weight.

### 4. `SearchPatient(List list, char name[])`
Searches for a patient by their first name and displays their details if found.

### 5. `InitialiseUnhealthyPatientList(List list, List unhealthy)`
Moves patients categorized as "Obese Class 1", "Obese Class 2", or "Obese Class 3" to a new list of unhealthy patients.

### 6. `PrintPatients(List list)`
Prints the list of all patients, displaying their name, surname, birth date, height, weight, and BMI.

### 7. `CreateList()`
Creates a new list with a dummy head node.

### 8. `MakeEmpty(List list)`
Initializes an empty list with a dummy head node.

### 9. `InsertAlphabetically(List list, char name[], char surname[], char birth[], float height, int weight, char BMI[])`
Inserts a new patient into the list in alphabetical order by their first name.

## Compilation and Execution

To compile the program, run the following command in the terminal:

```bash
gcc main.c -o patient_manager -lm
