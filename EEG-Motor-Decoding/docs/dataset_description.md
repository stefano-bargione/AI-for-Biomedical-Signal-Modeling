# EEGMMIDB Curated (.mat) — Dataset Structure

This repository uses a curated MATLAB export of the EEGMMIDB dataset (**EGMMIDB_Curated.mat**), loaded via mat73.

At the top level, the `.mat` file contains a dictionary with a **single key**:

- **EEGMMIDB**

Inside EEGMMIDB, the relevant fields are:

- **Signal**
- **Annotations**
- **Frequency**
- **Subjects**

---

## Signal

**Signal** is a list of **runs**:

- Signal → **list** of length **12**
- Each element Signal[run_idx] is a **dict** containing all subjects for that run

To access a specific subject in a given run:

- The subject key is: Subject_<ID>_Signal
- Example: Signal[0]["Subject_100_Signal"]

Each subject entry is a list with a single element:

- Signal[0]["Subject_100_Signal"] → list of length **1**
- The actual EEG array is at index [0]:

Example Python:
Signal[0]["Subject_100_Signal"][0].shape  # (19680, 64)

So the final structure is:

Signal[run_idx] → dict
Signal[run_idx]["Subject_<ID>_Signal"] → list (len=1)
Signal[run_idx]["Subject_<ID>_Signal"][0] → np.ndarray (time_samples, channels)

## Annotations

**Annotations** (Labels) mirrors the structure of Signal:

- Annotations → list of length 12
- Each element Annotations[run_idx] is a dict containing all subjects for that run
  - Subject key: Subject_<ID>_Annotations

Example:
Annotations[0]["Subject_100_Annotations"]

Again, each subject entry is a list with a single element:

Annotations[0]["Subject_100_Annotations"] → list (len=1)

The [0] element contains a list of trials. Each trial is a list of 5 fields.

Typical output:

Annotations[0]["Subject_100_Annotations"][0]  # list of trials
Annotations[0]["Subject_100_Annotations"][0][0]  # first trial: [..5 fields..]
