LANES AND HANDOFF

#Your handoff counts in the new-patient path

1. Process start in Front Desk. No handoff.
2. pay for hospital card: Front Desk to Patient. Handoff 1.
3. After payment, Write patient details: Patient to Front Desk. Handoff 2.
4. Write and then refer, after checking if Patient have a folder: all in Front Desk. None.
5. No, then create new folder: Front Desk to Records. Handoff 3.
6. After creating a folder then Carry folder to consultation room: both by Records. None.
7. Patient is then sent to Wait in queue: Records to Patient. Handoff 4.
8. Doctor then consult patient: Patient to Doctor. Handoff 5.
9. Consult to the end event with patient leavin with prescription: Doctor to Patient. Handoff 6.


#Your handoff counts in the returning-patient path
1. Start, then check if it is a new patient?: both in Front Desk. No handoff.
2. Not a new patient, then verify returning patient: No handoff.
3. After verified, refer patient to record: No handoff.
4. search for patient folder: front desk to record. Handoff 1.
5. After folder found, patient is sent to queue: Record to patient. Handoff 2.
6. Patient is then consulted by a doctor: Patient to doctor. Handoff 3
7. After consultation, Patient leaves with prescription: Doctor to patient. Handoff 4.

## Handoff counts
New patient: 6. Returning patient: 4.


#DANGEROUS HANDOFF
For both returning and new patients, the dangerous handoff is handoff2 and 4 respectively, having folders move from record to consultation room, because that create posibilities for folder lost, damage and data privacy issues.  


## Why a handoff adds time even when nobody is slow
The reason why handoff adds time is because, regrdless of the speed of that person, if a folder arrived to their table, or a request, it has to wait its turn. 

## Why the handoff count can mislead
Handoff may add time, but not all the time added is the same. Take, for example, it is easier to just pick a new folder and fill it than to search for an existing folder in a very large pile. Based on the stated reason, returning patients tend to waste more time than new patients. 

