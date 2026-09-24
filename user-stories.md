# User Stories - Healthcare Management System

# Domain context mapping

•	Patient Management:
Handles patient information, appointments, medical records, treatment and care plan.

•	Billing & Insurance Claims:
Handles payments, invoices, insurance policies and claims.

•	Lab Test Diagnostics:
 Handles laboratory test requests, samples, test processing, and results.



## Story 1
Story 1: Tracking Medical History
As a patient,
I want to access and view my historical medical reports and visit summaries online
So that I can easily keep track of my medical history without needing to call the desk

```gherkin
Scenario: Patient successfully views past medical reports and summaries
  Given an authenticated patient with ID "P-88421" is logged into the Patient Portal
  When the patient navigates to the "Medical History" section
  Then the system should retrieve and display a list of all past medical records, lab summaries, and care plans ordered by date
  And each record should display the date of visit, attending doctor, and an option to download the report PDF
```

## Story 2
 “Self-Service Appointment Rescheduling”
 As a patient
 I want to reschedule my upcoming medical appointment through the portal
 So that I can adjust my booking to a convenient time without needing to call the clinic
As a registered patient
I want to update my emergency contact details or phone number,
So that the medical staff always has my accurate information in case of an emergency


```gherkin
Scenario: Patient successfully reschedules an appointment outside the 24-hour window
  Given a patient has an active appointment scheduled for "2026-10-20T10:00:00Z"
  When the patient requests to reschedule the appointment to "2026-10-22T14:00:00Z" more than 24 hours prior
  Then the system should update the appointment time to "2026-10-22T14:00:00Z"
  And emit an "Appointment Rescheduled" event to the Notification Service
  And display a confirmation message with the updated schedule details to the patient
```
