# UAV Multi-Modal Control Prototype – Milestone #2  
**Multi-Modal Intention Integration Method for Uncrewed Aerial Vehicles (UAVs)**  

## 1. Progress Update

A fully functional web prototype has been developed and deployed on GitHub Pages. 
`Link to the web based prototype`: https://maninder99.github.io/Multi-Modal-Intention-Integration-Method-for-Uncrewed-Aerial-Vehicles-UAVs-/
The system integrates three input modalities:
- Voice: Real-time speech recognition + simulated commands
- Hand Gestures: Real-time detection via camera
- Fallback Buttons: For low-light or camera-denied environments

A weighted fusion engine combines inputs using:
1. Score = Confidence × Priority Weight
2. Final Command = Highest scoring input

Priority weights are adjustable via sliders (Voice: 0–100%, Gesture: 100–0%).
Pilot study (n=3) has been completed with sufficiently good task accuracy, SUS = 87.5, and NASA-TLX = 30 (low workload).  
Participants reported high trust due to transparent feedback (large arrows, labels, fusion log).

## 2. Prototype Design Explanation

|---------------------|--------------------|------------------------------------------------------------------|
| Feature             | Purpose            |                            Implementation                        |
|---------------------|--------------------|------------------------------------------------------------------|
| Big Central Canvas  | Clear UAV feedback | 500×400px canvas with RED drone dot                              |
| Live Camera Overlay | Show hand + drone  | MediaPipe draws skeleton + bounding box                          |
| Fusion Log          | Transparency       | Timestamped decisions (e.g., “Gesture prioritized: 92.0 > 75.0”) |
| Sliders             | Dynamic priority   | Real-time weight update, tooltips                                |
| Fallback Buttons    | Robustness         | Works without camera/microphone                                  |
|---------------------|--------------------|------------------------------------------------------------------|

Hand Gesture Mapping:
- Open Palm     → Takeoff  
- Thumbs Up     → Ascend  
- Point Left    → Turn Left  
- Point Right   → Turn Right  
- Fist          → Land  

## 3. Pilot Study Artifacts

Proof of preliminary evaluation provided via:
|---------------------------|--------------------------------------------------------------------|
| Artifact                  |                                   Description                      |
|---------------------------|--------------------------------------------------------------------|
| `Report_Milestone_3.docx` | Full pilot protocol, task logs, interview quotes, SUS/TLX raw data |
| `photos/p1-gesture.jpg`   | Participant performing Open Palm → Takeoff                         |
| `photos/p2-sus.jpg`       | P2 filling SUS form                                                |
| `photos/p3-tlx.jpg`       | P3 completing NASA-TLX                                             |
|---------------------------|--------------------------------------------------------------------|

Results Summary:
- Participants: 3 graduate students (McGill ECE, KTH, McGill Biotechnology)
- Tasks: 5 per user (Takeoff, Ascend, Turn Left, Turn Left, Land, Hover)
- Avg Task Time: 1.4 seconds
- SUS: 87.5 (P1=82.5, P2=85, P3=95)
- NASA-TLX: 30 (low cognitive load)

> Quote: _“Very cool, the big arrow made it 100% clear what the system saw.”_ – P1

## 5. Future Evaluation Steps

|-----------|-----------------------------------------------------------------------|
| Date      |                                       Task                            |
|-----------|-----------------------------------------------------------------------|
| Nov 19–22 | Recruit 7 additional participants (n=10 total) |
| Nov 23–26 | Run full within-subjects study (3 conditions × 10 tasks)              |
| Nov 27–29 | Analyze data: paired t-tests (accuracy, time), thematic coding (trust)|
| Dec 1     | Submit final report + benchmark comparison                    |
|-----------|-----------------------------------------------------------------------|