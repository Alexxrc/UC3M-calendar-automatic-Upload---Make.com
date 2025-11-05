# Calendar Sync Automation

This open-source automation connects **MOODLE calendar of AULAGLOBAL** with your **Google/APPLE Calendar** of your personal device, automatically reading events and uploading them in a structured format.

---

## 🚀 Features
- Fetches events from AULAGLOBAL Calendar uploaded events
- Compares and uploads only new or updated ones
- Supports duplicate prevention and date synchronization
- Compatible with Make (formerly Integromat)

---

## 🧠 How It Works
1. The scenario reads all events from AULAGLOBAL dynamic Calendar
2. It checks the alredy uploaded ones on your device.
3. If an event is new or updated, it pushes the data to your API or system.

---

## 🧰 Setup Instructions
1. Import the `make_scenario.json` file in Make.

2. Get your dynamic link of your Aulaglobal calendar, located in the calendar section, below the calendar, import or export calendars,
export a calendar, then select the filters you want to apply to the events that will upload to your device and finally copy that link.

3. Now, select the first module in the scenario in make, htttp one, in the URL section you will have to paste the link you alredy got in the previous section.

**If you want to implement custom names for the subjects to be followed by the event created follow step 4, if not, jump to step 5**

4. After that, you will have to select the purple module called Tools located before the first blue Data Store module(If you counted the existed ones, is the fourth one). Opening that module will show you a switch function, in each section separated by ";", you can find a separation of codes of the class and the class name, this is an example: 
{{switch(28.`$6`; "[2025/26] C2.381.19100-250"; "Actuadores y sensores para robótica"; "[2025/26] C2.381.19101-250"; "Aprendizaje Automático")}} , for "C2.381.191.100-250, the subject name will be "Actuadores y sensores para robótica", then changing those codes and names will lead you to the implementation of subjects names in your automation.

**----**

5. Finally you will have to accomplish the following mandatory connections
**-> Data Store and its structure, that is explained by photos in the word/pdf document of instructions**

**-> Apple/Google Calendar modules to the likely of the user. In the case of apple the modules of calendar are alredy in the automation sequence you will only have to connect your own device following the steps. For google or Android users just delete those modules copying its structure and add your ANDROID/google specific ones on make**

**NOTION MODULES ARE OPTIONAL, YOU CAN DELETE THEM**



6. **NOTE THAT YOU WILL HAVE TO SELECT TO EXECUTE THAT ENVIRONMENT ONCE A DAY IN MAKE.COM TO UPDATE TO YOUR DEVICE THE NEW EVENTS OF AULAGLOBAL CALENDAR** 


Optional step: There are also some notion modules that are include for storing the events as task in notion to keep track easily of them

---

## 📄 License
This project is licensed under the **MIT License** — free to use, modify, and distribute.

---