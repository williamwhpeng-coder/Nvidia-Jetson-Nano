# American Sign Language Alphabet Translator

This is a computer vision project that uses the Jetson Orin Nano and a connected webcam that allows detects the different letters that the users hand shapes and translates them back. This project works better in a light colored, solid background. I picked this project because I thought that communication with deaf people is hard without learning sign language, so this bot could help people understand without needing to learn it.

<img width="484" height="375" alt="Screenshot 2026-07-29 165158" src="https://github.com/user-attachments/assets/64eee718-7e9a-424f-905b-28ef714157cb" />
<img width="484" height="375" alt="Screenshot 2026-07-29 165227" src="https://github.com/user-attachments/assets/df0cb495-2248-4bae-a893-5dad5ff4b44a" />
<img width="484" height="375" alt="Screenshot 2026-07-29 165251" src="https://github.com/user-attachments/assets/e2ba9dcb-150a-46ae-8897-24cb3f47b0b3" />

## Running this project

1. Ssh into Orin
2. Download{https://www.kaggle.com/datasets/danrasband/asl-alphabet-test?select=D}this dataset off of Kaggle using this command
path = kagglehub.dataset_download("grassknoted/asl-alphabet")
print("Path to dataset files:", path)
3. File must be converted to from Pytoarch to Onnex 
4. This dataset has around 3000 photos per letter of the alphabet in the train folder, but does not come with a val folder so create a val folder and start moving roughly 300 photos from train to val
5. Unzip the file from Kaggle to get all the context and then let the model train, this may take a long time.
6. After training open RuskDesk and start livestreaming with a webcam to use model

https://drive.google.com/file/d/1DPad9PopqV-tNpXnpcIRJlF_O3aGxJqG/view?usp=sharing
