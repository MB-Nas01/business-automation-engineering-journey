Trigger1: A patient pays for a hospital card at the OPD front desk (for a new patient). To be digitized and Automated. with Nurse to access the severity at front desk for both new and returning patient so as treatment can start from the front desk. 
Trigger2: A returning patient is manually verified at the front desk and sent to Step 2. to be Automated, retuning patient with existing folder will have there folders manually updated and linked to their existing hospital number that can be used to print their new hospital card at front desk to avoid having double hospital number for a single patient. these will be done during first visit of the patient after the system is introduced. the reason for these approach is to avoid redundant data on the server for patients that do not return again. 
Step 1: The cashier input new patient information on the digital form and printout the Hospital card with an auto generated hospital number, this should only happen when there is no existing record with the same name and phone number or the existing is actually not the patient being registered.
Step 2: The cashier then refers the patient to the records department for file opening. To be eliminated, with records going automatically to a database controlled by records department that is accessible based on permission (Role base access control) by doctors and patients go straight to the consultation room.
Step 3: The records department then rewrites the patient's name on a flat folder. In case of a returning patient, the records clerk searches for the folder in a pile of other folders. Eliminate. 
Step 4: The records clerk takes the folder to the doctor in the consulting room. Eliminated, with doctors having direct access through to the patient record through their hospital number that was generated at step 1. 
Step 5: The patient waits outside the consultation room for their name to be called. maintained, with queue board and special update for emergency cases. Have a human attendant that ensures the queue is being abide by.

   constraints: no internet, power cuts, security
  Solution: The service will be hosted entirely on a local network without involving internet for normal operation, but will have a dedicated server system for schedule reminder which will be cost effective because it does not require heavy networking equipment no resource intensive server setting, simple laptop with a router and modem. The laptop should not communicate back to the internal system, it only receives a reminder message, phone number or email of the patient and the date of the schedule such that it can forward the reminder as desired. with bulk SMS bundles as low as 6 naira, we see an estimated budget of 6000 naira monthly for 1000 SMS which is generous enough. 
 In case of power-cut, the system will be hosted on a two way power system, Solar/battery (backup power plan) and National grid with a low latency fall over ensuring a very negligible downtime. 

## TO_BE FLOW:
step 1: Patient get checked at front desk (New patient taking around 10 minutes for payment and record input and hospital number generation and printing of card, while returning get verified and forwarded to consultation in about 5 minutes) and for severity of case. 
step 2. doctor queue list update as patient are cleared. 
step 3. Doctor can update record and also be able to assign a revisit booking schedule that automatically send a reminder to the patient 24 hours before the due date (using either mail or SMS). 

For security purpose, all login and operations will be recorded, filtered and passed to a dashboard that can be easily read by security and audit team. Any administrative operation must be recorded. Initial Backup be made and subsequent backup will be made daily at midnights, with only the changes being recorded. 

## Audit log protection
Logs are copied live to a separate machine that hospital administrators cannot edit. Any change to the main log would show up as a mismatch between the two copies, so tampering is detectable.

## Queue board
The board shows queue numbers, not patient names, so people in the waiting area cannot see who is being treated.

## To-be flow
1. Front desk (cashier): search by name and phone for an existing record. If a match is genuine, link to it. If not, create a new record, take payment, generate the hospital number and print the card. New patient about 10 minutes, returning patient about 5.
2. Front desk (nurse): check severity during the same visit. when there is emergency, emergencies go straight to treatment, and registration is completed afterwards for unconscious patients.
3. System: the patient joins the doctor's queue automatically, and an attendant keeps the order fair.
4. Consulting room (doctor): opens the record using the hospital number, consults, and updates the record.
5. Doctor books a revisit. The reminder laptop sends an SMS 24 hours before.
6. System: every login and administrative action goes into the audit log.

## Time saved before reaching the doctor's queue
New patient: about 35 minutes before, about 10 now, saving about 25 minutes.
Returning patient: about 55 minutes before, about 5 now, saving about 50 minutes.