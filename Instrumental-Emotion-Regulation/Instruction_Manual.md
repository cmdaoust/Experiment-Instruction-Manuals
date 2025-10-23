# **Instrumental Emotion Regulation Study: Step-by-Step Testing Manual**

---

## **Experimental Flow Overview**

**Order of Procedure:**
> Forms → Walk Through Experiment → Electrode Hook-Up → Questionnaires → Experiment → Debrief

---

## **Pre-Session Checklist**

### **Before the Participant Arrives**

#### **Room Setup**
- Ensure **thermostat** is **on** and set to **23°C**.  
- Dispose of any **rubbish** from previous sessions.
- Turn on all computers and the blue Biopac machine (on button is on the back at the bottom).  

#### **Documents**
Have the following ready:
- Consent form  
- Participant information sheet  
- Debrief document and **£1 payment**  
- Payment confirmation form  

#### **Equipment**
- **EL507A electrodes**  
- **EL503 electrodes** 
- **Spectra Electrode Gel**
- **BIOPAC isotonic GEL101a**
- **Medical Tape & Scissors**     

#### **Software**
1. **Open PsychoPy experiment in the Stimulus PC**
     ```
     This PC/Documents/Carmen_MD/Instrumental_emotion_reg/InstEmoReg/InstEmoRegCode.py
     ```
   - Set **condition order** and **stimuli groups** according to the [Participant Tracking File](https://sussex.box.com/s/s0kzan0eygbwbe86yhamu2iu2l0joptk)

| Participant | Researcher | First Condition | Stimuli Group | Second Condition | Stimuli Group | Third Condition | Stimuli Group |
|--------------|-------------|------------------|----------------|------------------|----------------|------------------|----------------|
| 001 | Researcher&nbsp;Name | Control | group1 | Up | group2 | Down | group3 |
| 006 | Researcher&nbsp;Name | Control | group2 | Up | group3 | Down | group1 |
| 003 | Researcher&nbsp;Name | Control | group3 | Up | group1 | Down | group2 |
| 007 | Researcher&nbsp;Name | Up | group1 | Down | group2 | Control | group3 |
| 004 | Researcher&nbsp;Name | Up | group2 | Down | group3 | Control | group1 |
| 008 | Researcher&nbsp;Name | Up | group3 | Down | group1 | Control | group2 |

For example, if running participant 001, update code segment in LoopOrderCode to reflect that the first condition should be **Control**, second **Up** and third **Down**. Do this by inserting a # in front of all redundant orders and removing the preceeding # from the desired order.

<p align="center">
  <img src="/images/UpdateLoopOrder.png" alt="How to update loop order code" width="100%">
  <br>
  <em>Update Loop Order by clicking onf LoopOrderCode -> Code -> Unhash correct order and hash out old order.</em>
</p>

Then, click into control_trials and change groupx.xls file to reflet correct grouping. In thise case, Control should be group 1. Scroll to the right and do the same for up_trials (group2) and down_trials (group3).

   <p align="center">
  <img src="/images/ConditionsUpdate.png" alt="How to update condition stimuli" width="100%">
  <br>
  <em>Update Update the stimuli shown in each conditions by clicking condition_trials -> groupx.xls </em>
</p>

2. **Open questionnaire link** -> Chrome -> Bookmarks -> Qualtrics
   - Input participant ID from [Participant Tracking File](https://sussex.box.com/s/s0kzan0eygbwbe86yhamu2iu2l0joptk)

4. **Open Biopac application** on the **recording PC**:
   - Open File from Disk -> 
     ```
     Documents/My Documents/Carmen MD/Data/instrumental_emotion_reg_template_01.acq
     ```

5. **Set up Avica Screen Mirroring*** by opening the application on the recording PC and on the PC in room S5. Type the code from the recording PC into the one in room S5 and press connect. You should be able to remotely access the recording PC from the S5 cubicle. 
---

## **Participant Arrival**

1. Ask the participant to **store belongings in S5**.
2. Ask if participant needs to **use the bathroom** (it’s difficult to disconnect/reconnect electrtodes after setup).  
3. Ask the participant to sit in A5, have them **read and sign** the **information sheet** and **consent form**.  
4. Check that the **consent form is signed on the back**.  

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
- Peel 3 ECG electrodes from the backing and inspect. Add a small amount of additional Spectra 360 gel if necessary.
- Instruct participant to attch 3 electrodes according to the diagram on the wall.

#### **Attaching Electrode Leads**
1. **VIN- (white):** under right clavicle, midclavicular line.  
2. **GND (black):** lower right abdomen.  
3. **VIN+ (red):** lower left abdomen.  
4. Secure leads and route through clothing.

- Once electrodes are wired up, ask the participant to clip the leads to the top of their trousers using the crocodile clip.

- Carry out signal check on Biopac
  
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
   - **Inhale fully** → ensure ** resistance** at full inhalation.  
5. Participant **sits down** in the testing chair.
6. Carry out signal check on Biopac

---

### **Electrodermal Activity (EDA)**

> [See detailed SOP here](https://github.com/cmdaoust/Experimental-SOPs/blob/main/EDA/EDA_SOP.md)

#### **Explanation**
> “Electrodermal Activity (EDA) is a non-invasive measure of physiological arousal via skin sweat.”

#### **Procedure**
1. Show **diagram** of electrode placement.
2. Peel 2 EDA electrodes from the backing and inspect. Add a small amount of additional Isotonic gel if necessary.  
3. Attach electrodes to first and index finger of left hand.  
4. Secure with tape
5. Carry out signal check on Biopac

---

## **6. Final Pre-Experiment Checks**
- **Press Start** on Biopac → confirm data is recording.
- Perform signal quality checks according to SOP guidelines [EDA](https://github.com/cmdaoust/Experimental-SOPs/blob/main/EDA/EDA_SOP.md)  [ECG](https://github.com/cmdaoust/Experimental-SOPs/blob/main/ECG/ECG_SOP.md) > [Respiration](https://github.com/cmdaoust/Experimental-SOPs/blob/main/Respiration/RespiratoryEffort_SOP.md)   
- Show how **movement affects data quality**.  
- Instruct participant to **stay still** during videos.
- Instruct participant to complete questionnaires and knock on the table when they are complete.
- Turn off Biopac monitor screen.

## **7. Post-questionnaire"
-  **Start PsychoPy experiment**, when participant ID box appers, insert participant ID from [Participant Tracking File](https://sussex.box.com/s/s0kzan0eygbwbe86yhamu2iu2l0joptk)

---

## **8. After the Experiment**

### **Removing Equipment**
1. **Stop Biopac recording.**  
2. Ask participant to:
   - Remove headphones.  
   - Unclip leads and electrodes.  
   - Unvelcro **respiration belt** and remove it.
3. Hang leads back on hooks.
---

### **Paperwork**
- Provide **debrief document** and **£1 payment** in an envelope.  
- Have participant **sign payment confirmation form**.

---

### **Saving Biopac Data**
1. **Save raw datafile** as participantnumber_raw.acq

2. Filter channels
   - EDA -> Transform -> Digital Filter -> IIR -> Low Pass -> 10hz
      - Edit -> Remove Waveform (of origional unfiltered data)
   - ECG -> Transform -> Digital Filter -> IIR -> Band Pass Low + High  -> 0.5 - 35hz
      - Edit -> Remove Waveform (of origional unfiltered data)
   - Respiration -> Transform -> Digital Filter -> IIR -> Low Pass -> 1hz
      - Edit -> Remove Waveform (of origional unfiltered data)
3. **Save filtered data file** as participantnumber_filtered.acq
4. Trim data from start and end of session
   - Use cursor icon to select relevant section -> Edit -> Clear all
5. **Save filtered and trimmed datafile** as participantnumber_filtered_chopped.acq
6. **Close Biopac** and **turn off Biopac machine.**
7. Upload both files to Box:
   > [Instrumental Emotion Regulation Physiology Box Folder](https://sussex.app.box.com/folder/303306815832)

---

### **Saving PsychoPy Data**
- Upload PsychoPy data to:
  > [Instrumental Emotion Regulation Psychopy Box Folder](https://sussex.app.box.com/folder/306319842633)
  > Data files can be found in
     ```
     This PC/Documents/Carmen_MD/Instrumental_emotion_reg/InstEmoReg/data/
     ```

---

## **8. After Session Administration**

### **File Storage**
Store these forms in the relevant folder in the S5 room:
- Signed consent form  
- Payment confirmation form  

### **Tracking**
Update the **Participant Tracking document**:  
> [Participant Tracking File](https://sussex.box.com/s/s0kzan0eygbwbe86yhamu2iu2l0joptk)
