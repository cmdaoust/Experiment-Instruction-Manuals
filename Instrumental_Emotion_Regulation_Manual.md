# **Instrumental Emotion Regulation Study: Step-by-Step Testing Manual**

---

## **1. Access and Setup**

### **Keys and Passwords**
- Keys are in the leftmost drawer in the wet lab at the end of the hallway (marked **S5** and **A5**).  

### **Power On**
Turn on all computers and the Biopac machine.
---

## **2. Experimental Flow Overview**

**Order of Procedure:**
> Forms → Walk Through Experiment → Electrode Hook-Up → Questionnaires → Experiment → Debrief

---

## **3. Pre-Session Checklist**

### **Before the Participant Arrives**

#### **Room Setup**
- Ensure **thermostat** is **on** and set to **23°C**.  
- Dispose of any **rubbish** from previous sessions.  

#### **Documents**
Have the following ready:
- Consent form  
- Participant information sheet  
- Debrief document and **£1 payment**  
- Payment confirmation form  

#### **Equipment**
- **EL507A electrodes**  
- **EL503 electrodes** 
- **Spectra Electrode Gel** – confirm it’s available in the room
- **BIOPAC isotonic GEL101a** – confirm it’s available in the room    

#### **Software**
1. **Open PsychoPy experiment in the Stimulus PC**
   - Set **condition order** and **stimuli groups** according to the **project tracking sheet**.
2. **Open Biopac application** on the **recording computer**:
   - Open File from Disk -> 
     ```
     Documents/My Documents/Carmen MD Instrumental Ereg/
     instrumental_emotion_reg_template_01.gtl
     ```
3. **Open questionnaire link** -> Chrome -> Bookmarks -> Qualtrics
---

## **4. Participant Arrival**

### **Before Entering the Testing Cubicle**
1. Ask the participant to **store belongings in S5**.  
2. Ask the participant to sit in A5, have them **read and sign** the **information sheet** and **consent form**.  
3. Check that the **consent form is signed on the back**.  
4. Ask if participant needs to **use the bathroom** (it’s difficult to disconnect/reconnect after setup).

---

## **5. Hook-Up Procedure**

### **Electrocardiogram (ECG)**

> [See detailed SOP here](https://github.com/cmdaoust/Experimental-SOPs/blob/main/ECG/ECG_SOP.md)

#### **Explanation**
> “A 3-lead electrocardiogram (ECG) is a non-invasive procedure that measures the electrical activity of the heart muscle.”

#### **Preparation**
- Show **diagram** of electrode placement and explain connections.  
- If needed, provide **razor** for shaving small areas around electrode sites.  
- Wrap used razors in **paper and tape** before discarding in **general waste**.

#### **Electrode Placement**
- Peel 3 ECG electrodes from the backing and inspect. Add a small amount of additional get if necessary
- Instruct participant to attch 3 electrodes according to the diagram on the wall

#### **Attaching Electrode Leads**
1. **VIN- (white):** under right clavicle, midclavicular line.  
2. **GND (black):** lower right abdomen.  
3. **VIN+ (red):** lower left abdomen.  
4. Secure leads and route through clothing.

---

### **Respiration Belt**

> [See detailed SOP here](https://github.com/cmdaoust/Experimental-SOPs/blob/main/Respiration/RespiratoryEffort_SOP.md)

#### **Explanation**
> “The respiration belt records respiratory effort - in other words, your breathing.”

#### **Procedure**
1. Show **diagram** of placement.  
2. Have participant **stand**, face away, and raise arms.  
3. Strap belt **around chest**, above clothing.  
4. Instruct participant to:
   - **Exhale completely** → tighten belt (no looseness).  
   - **Inhale fully** → ensure **slight resistance** at full inhalation.  
5. Participant **sits down** in the testing chair.

---

### **Electrodermal Activity (EDA)**

> [See detailed SOP here](https://github.com/cmdaoust/Experimental-SOPs/blob/main/EDA/EDA_SOP.md)

#### **Explanation**
> “Electrodermal Activity (EDA) is a non-invasive measure of physiological arousal via skin sweat.”

#### **Procedure**
1. Show **diagram** of electrode placement.    
2. Attach electrodes to first and index finger of left hand.  
3. Secure with tape

---

## **6. Final Pre-Experiment Checks**
- **Press Play** on Biopac → confirm data is recording.
- Perform signal quality checks according to SOP guidelines (insert link)  
- Show how **movement affects data quality**.  
- Instruct participant to **stay still** during videos.
- Instruct participant to complete questionnaires and knock on the table when they are complete  
- **Turn off Biopac monitor screen.**  
- When questionnaires are complete **Start PsychoPy experiment.** 

---

## **7. After the Experiment**

### **Removing Equipment**
1. **Stop Biopac recording.**  
2. Ask participant to:
   - Remove **headphones**.  
   - Unclip **EDA electrodes** and remove pads.  
3. Researcher:
   - Unvelcro **respiration belt** and remove it.  
4. Participant removes **ECG electrodes** and pads.

---

### **Paperwork**
- Provide **debrief document** and **£1 payment** in an envelope.  
- Have participant **sign payment confirmation form**.

---

### **Saving Biopac Data**
1. **Save raw datafile** as participantnumber_raw.acq

2. Filter channels
   - EDA -> Transform -> IIR -> Low Pass -> 10hz
      - Edit -> Remove Waveform (of origional unfiltered data)
   - ECG -> Transform -> IIR -> Low + High Pass -> 0.5 - 35hz
      - Edit -> Remove Waveform (of origional unfiltered data)
   - Respiration -> Transform -> IIR -> Low Pass -> 1hz
      - Edit -> Remove Waveform (of origional unfiltered data)
3. **Save filtered datafile** as participantnumber_filtered.acq
4. Trim data from start and end of session
   - Use cursor icon to select relevant section -> Edit -> Clear all
5. **Save filtered and trimmed datafile** as participantnumber_filtered_chopped.acq
6. **Close Biopac** and **turn off Biopac machine.**
7. Upload both files to Box:
   > [Instrumental Emotion Regulation Physiology Box Folder](https://sussex.app.box.com/folder/303306815832)

---

### **Saving PsychoPy Data**
- Upload PsychoPy data to:
  > [Instrumental Emotion Regulation Physiology Box Folder](https://sussex.app.box.com/folder/306319842633)

---

## **8. After Session Administration**

### **File Storage**
Store these forms in the relevant folder in the S5 room:
- Signed consent form  
- Payment confirmation form  

### **Tracking**
Update the **Participant Tracking document**:  
> [Participant Tracking File](https://sussex.box.com/s/s0kzan0eygbwbe86yhamu2iu2l0joptk)
