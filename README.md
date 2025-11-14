# UAV Multi-Modal Control Prototype – Milestone #2  
**Multi-Modal Intention Integration Method for Uncrewed Aerial Vehicles (UAVs)**  

## Progress Update (Since Milestone #1)

Since Milestone #1, a **fully functional low-fidelity web prototype** has been implemented using **HTML, CSS, and vanilla JavaScript**. The system simulates **voice and gesture inputs** via interactive buttons, applies **user-adjustable modality weights** through sliders, performs **rule-based fusion** with confidence scoring, and displays **transparent reasoning** (e.g., “Gesture prioritized due to higher weighted score”). The fused intention drives a **2D canvas-based UAV simulation**, where a drone icon moves in response to commands such as “Ascend,” “Turn Left,” or “Takeoff.” All core HCI features from the design—**transparency, personalization, and real-time feedback**—are now fully interactive and demonstrable in a browser.

## Implementation Artifacts

`Link to the web based prototype`: https://maninder99.github.io/Multi-Modal-Intention-Integration-Method-for-Uncrewed-Aerial-Vehicles-UAVs-/
`Full dashboard layout.png`: **Full dashboard layout** showing input panel (voice/gesture buttons), sliders for modality priority, fusion log, and simulation canvas with UAV at starting position.
`Fusion conflict resolution.png`: **Fusion conflict resolution** example: Voice: "Takeoff" (Confidence: 70%); Gesture: "Descend" (Confidence: 91%); Gesture: "Ascend" (Confidence: 94%); Gesture: "Turn Left" (Confidence: 89%); Gesture: "Turn Right" (Confidence: 95%); FUSED: "Takeoff" with log message: *"Voice prioritized (score: 61.9 > 10.4)"*.
`UAV simulation in action.png`: **UAV simulation in action**: Drone has moved upward after fused “Takeoff” command, showing real-time canvas update and trajectory.

## Next Steps & Testing Plan

I will be conduct **internal testing** with **10–15 simulated scenarios** (such as low-confidence voice + high-confidence gesture) to validate **≥80% fusion accuracy** and **<2s latency**, iterating based on **Nielsen’s usability heuristics**. 
**Comparative evaluation** will be performed against **baselines**:  
- **Single-modal voice-only** (modified prototype)  
- **Single-modal gesture-only** (OpenCV-style simulation)  

**Quantitative metrics**: task completion time, error rate, fusion accuracy.  
**Qualitative metrics**: **NASA-TLX** (cognitive load), **SUS** (usability >70), and **trust/intuitiveness** via post-task interviews.  

The **formal user study** with **5-7 novice participants** will follow a **within-subject design**, using the final prototype and surveys. All testing will be conducted by me under the approved REB protocol (25-08-071). Data will be anonymized and stored on **McGill-approved OneDrive for Business**.